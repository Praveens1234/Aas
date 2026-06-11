───────────────────────────────────────────────────────────────────────────────
  FINTRACE — ANDROID APPLICATION BLUEPRINT
  Personal-Grade Real-Time Financial Price Monitor & Alert System
───────────────────────────────────────────────────────────────────────────────
  Version   : 4.0 — Final Production Release
  Author    : Praveen Kumar
  Date      : June 2026
  Stack     : Flutter 3.22+ · Kotlin · Material You 3 · Android API 26–35
  Data      : Twelve Data WebSocket API
  Scope     : Local / Individual Use — Not for Google Play publication
  Tool      : Antigravity  ·  Model: Claude (Anthropic)
  Contact   : praveens12346@gmail.com
───────────────────────────────────────────────────────────────────────────────

  COMPLETE AUDIT & VERSION LOG

  v1.0  Initial draft
  v2.0  Removed: charts (Symbol Detail), spread monitor, session OHLC,
        P&L helper, alert templates, notification log, multi-timezone clock,
        CSV export, OTA update, alternative data sources (Polygon, Finnhub,
        Alpha Vantage, MT5 Bridge), exotic symbols (USDINR, USDCNH).
        Added: DND Respect Policy, 3-mode theme system, API key management.
  v2.1  Fixed: 6 architectural vulnerabilities — isolate termination on
        swipe-to-dismiss, widget binder saturation (TransactionTooLargeException),
        storage contention between concurrent isolates, Android 14
        USE_FULL_SCREEN_INTENT silent downgrade, Virtual Call overlay failure
        on active (unlocked) screen, Doze Mode network shutdown vs wake lock.
  v3.0  Removed: Price chart (Symbol Detail screen), fl_chart package,
        sqflite package, all chart-related screens and navigation tab.
        Added: Permanent Live Ticker Notification — a persistent, updateable
        notification showing 1–5 user-selected symbol prices in real time.
        Fixed: All internal section number mismatches. Navigation 4→3 tabs.
        Removed fl_chart and sqflite from package list.
  v4.0  ── PRODUCTION RELEASE ──
        AUDIT FINDINGS RESOLVED:
          · Virtual Call / Alarm: fully hardened to fire even when screen off,
            even when WhatsApp/Instagram occupy foreground — dual-path overlay
            spec extended with CALL_PRIORITY escalation channel and
            Telecom-style InCallService shim for maximum system priority.
          · Added §08.4-EXT: System-Level Call Simulation (WhatsApp/Instagram
            override strategy) with full technical implementation.
          · Alert Delivery Channel escalated: 5th channel added —
            "call_simulation" — TYPE_CALL intent category for OS-level priority.
          · Wake-from-any-state specification formalised: covers screen off,
            Instagram fullscreen, WhatsApp call active, gaming foreground.
        NEW FEATURES ADDED:
          · Settings § Data Source: "Price Update Interval (ms)" — free-entry
            numeric field, default 500ms, user-configurable, min 100ms, no max.
          · Settings § About: full "About This App" and "About the Developer"
            panels with production metadata.
        UI/UX DESIGN:
          · Complete redesign of design system: §10 rewritten as full
            production-grade UI/UX specification.
          · New: Gesture control map, micro-interaction catalogue, haptic
            feedback matrix, accessibility audit, fast-path control spec.
          · New: Bottom Sheet Quick Panel for one-thumb control.
          · New: Live Price Ticker — swipeable mini-ticker strip on dashboard.
          · New: Quick Alert FAB — long-press for instant alert from any screen.
          · New: Alert Preview Toast — non-blocking confirmation of alert fire.
          · Updated screen inventory (S14 added: About Screen).
          · Updated file structure to reflect new screens and settings.
        DND POLICY: unchanged — no override, no bypass, ever.

───────────────────────────────────────────────────────────────────────────────

TABLE OF CONTENTS

  §01  Product Vision & Identity
  §02  Data Architecture — Twelve Data WebSocket
  §03  Android OS Barriers & Solutions
  §04  Critical Architecture (v2.1 Fixes)
  §05  DND Respect Policy
  §06  Theme System
  §07  Feature Specification
       07.1  Live Price Dashboard
       07.2  Symbol Detail Screen
       07.3  Symbol Management
       07.4  Permanent Live Ticker Notification
       07.5  Settings Screen  ← UPDATED (Price Update ms + About sections)
       07.6  API Key Management
  §08  Alert System
       08.1  Alert Creation — Field Specification
       08.2  Trigger Condition Logic
       08.3  Delivery Methods
       08.3-EXT  System-Level Call Simulation (WhatsApp/Instagram Override)
       08.4  Alert List Screen
       08.5  Batch Actions
       08.6  Search & Filter
       08.7  Trigger History
       08.8  Statistics Summary
  §09  Home Screen Widget System
       09.1  Widget Types
       09.2  Widget Configuration
       09.3  Widget Update Mechanism
  §10  UI/UX Design System  ← FULL REDESIGN
       10.1  Design Language & Principles
       10.2  Typography
       10.3  Colour System
       10.4  Component Reference
       10.5  Navigation Architecture
       10.6  Animations & Motion
       10.7  Gesture Control Map
       10.8  Micro-Interaction Catalogue
       10.9  Haptic Feedback Matrix
       10.10 Fast-Path Controls (One-Thumb Operation)
       10.11 Accessibility Specification
       10.12 Responsive Behaviour
  §11  Application Architecture
       11.1  Pattern
       11.2  Flutter Package Registry
       11.3  Native Android Components
       11.4  Production Data Flow
  §12  Screen Inventory  ← UPDATED
  §13  Permissions Registry  ← UPDATED
  §14  Project File Structure  ← UPDATED
  §15  Build & Sideload Guide
  §16  Roadmap
  §A   Appendix A — WebSocket Protocol Reference
  §B   Appendix B — Alert Evaluation Pseudocode
  §C   Appendix C — Notification Channel Registry  ← UPDATED (5 channels)
  §D   Appendix D — About This App & Developer Information  ← NEW

───────────────────────────────────────────────────────────────────────────────


═══════════════════════════════════════════════════════════════════════════════
§01  PRODUCT VISION & IDENTITY
═══════════════════════════════════════════════════════════════════════════════

WHAT IS FINTRACE?
  FinTrace is a personal-grade, real-time financial price monitoring and alert
  system for Android. It is built for individual traders who need sub-second
  price updates across XAUUSD, XAGUSD, and the top major forex pairs, with
  price alerts that reliably fire under ALL device states — screen off, phone
  locked, WhatsApp in foreground, Instagram fullscreen, gaming active — with
  live prices always visible from the home screen and notification panel.

DESIGN PRINCIPLES

  ① Data-first        Price numbers own the visual hierarchy. Every other
                      element exists to support the data, not compete with it.

  ② Focused           No feature is included unless it directly serves the
                      trader's core loop: monitor → alert → act.

  ③ Persistent        The user should never have to open the app to see the
                      current price. It is always visible — in the notification
                      panel, on the home screen widget, at a glance.

  ④ Reliable          Alerts fire regardless of whether the UI is open, whether
                      the app was swiped away, whether the screen is off, or
                      whether WhatsApp / Instagram occupy the foreground.
                      Reliability is non-negotiable and unconditional.

  ⑤ Respectful        The app never overrides the user's system settings.
                      Do Not Disturb means exactly that. Always.

  ⑥ Honest            The app clearly communicates its connection state. A
                      stale price is labelled stale. An offline state is shown
                      explicitly. No false confidence is displayed.

  ⑦ Fast              Every primary action — view price, create alert, change
                      setting — must be reachable within 2 taps or 1 long press.
                      Speed of interaction matches speed of markets.

  ⑧ Intelligent       The app anticipates the user's intent. Smart defaults.
                      Pre-filled alert targets. Context-aware menus. Adaptive
                      UI that puts the right controls in reach without searching.

CORE USER
  Individual trader operating a prop account (e.g. FundedNext Stellar).
  Monitors XAUUSD primarily, alongside XAGUSD and major forex pairs.
  Needs background price tracking and reliable alert delivery at all times —
  including when the phone is idle, screen is off, or other apps are active.
  Wants live prices visible on home screen and in the notification shade.


═══════════════════════════════════════════════════════════════════════════════
§02  DATA ARCHITECTURE — TWELVE DATA WEBSOCKET
═══════════════════════════════════════════════════════════════════════════════

DATA SOURCE
  Provider   : Twelve Data
  Protocol   : WebSocket (native push — not polling)
  Endpoint   : wss://ws.twelvedata.com/v1/quotes/price
  Free Tier  : 8 symbols, ~1 update/second
  Paid Tier  : $29/month — 14+ symbols, 500ms updates
  Fallback   : Twelve Data REST API (polling at 5s when WebSocket is down)
               Endpoint: GET https://api.twelvedata.com/price?symbol=XAU/USD
               Auto-switches back to WebSocket on recovery.

SUPPORTED SYMBOLS — 14 TOTAL

  Group      Symbols (Twelve Data wire format)
  ─────────  ──────────────────────────────────────────────────
  Metals     XAU/USD  XAG/USD
  Majors     EUR/USD  GBP/USD  USD/JPY  USD/CHF  AUD/USD  USD/CAD  NZD/USD
  Crosses    EUR/GBP  EUR/JPY  GBP/JPY  EUR/AUD  GBP/AUD

  User can activate or deactivate any symbol. Only active symbols are
  subscribed to the WebSocket, conserving API quota. Subscribing and
  unsubscribing are sent as live WebSocket messages without reconnecting.

API KEY MANAGEMENT
  Key stored in Android Keystore (AES-256). Never logged, never exported
  in plain text, never stored in SharedPreferences. Managed entirely via
  the dedicated API Key screen (see §07.6).

CONNECTION LIFECYCLE

  ┌─────────────────────────────────────────────────────────┐
  │  CONNECTION MANAGER (inside PriceTrackerService)        │
  ├─────────────────────────────────────────────────────────┤
  │  WebSocket State Machine:                               │
  │    DISCONNECTED → CONNECTING → CONNECTED → SUBSCRIBED   │
  │    Any failure → RECONNECTING (exponential backoff)     │
  │                                                         │
  │  Reconnect backoff: 1s → 2s → 4s → 8s → 16s → 60s max │
  │  Heartbeat:  {"action":"heartbeat"} every 25 seconds    │
  │  Reconnect trigger: on CONNECTIVITY_CHANGE broadcast    │
  │  On reconnect: re-subscribe active symbols immediately  │
  │                                                         │
  │  Price cache: last known price per symbol               │
  │  Served to UI when connection is temporarily lost       │
  │  Labelled "stale" in UI until live feed resumes         │
  └─────────────────────────────────────────────────────────┘

SUBSCRIPTION MANAGEMENT
  Symbol activated   →  send: {"action":"subscribe","params":{"symbols":"XAU/USD"}}
  Symbol deactivated →  send: {"action":"unsubscribe","params":{"symbols":"XAU/USD"}}
  Service stops      →  unsubscribe all active symbols gracefully
  Reconnect          →  re-subscribe only currently active symbols

PRICE UPDATE INTERVAL (UI RENDER RATE)
  The WebSocket delivers ticks at its own rate (up to 500ms on paid tier).
  The UI render rate is user-configurable in Settings → Data Source →
  "Price Update Interval (ms)". Default: 500ms. Minimum: 100ms. No maximum.
  This controls how frequently the Flutter UI redraws price values.
  Alert evaluation always runs on every raw WebSocket tick regardless of
  the UI interval — the UI interval affects display only, never alert firing.


═══════════════════════════════════════════════════════════════════════════════
§03  ANDROID OS BARRIERS & SOLUTIONS
═══════════════════════════════════════════════════════════════════════════════

Android aggressively restricts background execution to preserve battery.
Every known barrier relevant to FinTrace is documented and solved below.

───────────────────────────────────────────────────────────────────────────────
BARRIER 01 — Process Killed by Battery Optimizer / Doze Mode
───────────────────────────────────────────────────────────────────────────────

Problem:
  Android Doze Mode, App Standby Buckets, and OEM power managers (MIUI,
  OneUI, OxygenOS, ColorOS) terminate background processes within 5–30
  minutes when the screen is off, regardless of active threads.

Solutions:

  [A] Foreground Service — PRIMARY
      A Foreground Service holds a permanent system-level notification. Android
      cannot kill a running Foreground Service without user action. This is the
      same mechanism used by Google Maps navigation, Spotify, and trading apps.

      Manifest declaration:
        <service
            android:name=".PriceTrackerService"
            android:foregroundServiceType="dataSync"
            android:exported="false"/>
        <uses-permission android:name="android.permission.FOREGROUND_SERVICE"/>
        <uses-permission android:name="android.permission.FOREGROUND_SERVICE_DATA_SYNC"/>

  [B] Battery Optimization Exemption — HARD PREREQUISITE
      WAKE_LOCK keeps the CPU awake but does NOT exempt the app from Doze
      Mode network interface shutdowns. After the screen has been off for
      a sustained period, Android completely halts internet access for
      apps not on the battery exemption whitelist — the WebSocket drops
      regardless of any wake lock.

      Battery exemption is mandatory. The tracker service cannot be started
      until the system confirms isIgnoringBatteryOptimizations() == true.
      This is enforced in the Setup Wizard — the Start button is disabled
      until the exemption is granted.

      Permission: android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS
      Deep link:  Settings → Battery → Special App Access → Unrestricted

  [C] WorkManager Watchdog — SAFETY NET
      In the rare event the Foreground Service is killed by the OS (e.g.
      extreme memory pressure), a WorkManager periodic task re-spawns it:
        frequency: Duration(minutes: 15)
        constraints: networkType == NetworkType.connected

  [D] Manufacturer-Specific Guidance
      Device info is read via device_info_plus on first launch. If the
      device manufacturer matches a known OEM with additional restrictions,
      the Permission Helper screen surfaces device-specific instructions.

      Manufacturer       Additional Required Step
      ─────────────────  ──────────────────────────────────────────────
      Xiaomi / MIUI      Autostart permission + "No restrictions" battery
      Samsung / OneUI    "Allow background activity" in app battery settings
      OnePlus / OOS      "Auto launch" enabled in battery settings
      Realme / ColorOS   "Auto-start" enabled, Freeze OFF
      Stock Android      Battery exemption only (step B above)

───────────────────────────────────────────────────────────────────────────────
BARRIER 02 — WebSocket Drops After Screen Off
───────────────────────────────────────────────────────────────────────────────

Problem:
  Even with a Foreground Service running, Doze Mode throttles network
  I/O for apps not on the battery exemption list. The WebSocket connection
  silently dies. The service appears alive but receives no data.

Solutions:
  · Battery exemption (Barrier 01-B) is the root fix.
  · Partial CPU Wake Lock prevents the CPU from deep-sleeping mid-connection.
    Permission: android.permission.WAKE_LOCK
    Held by: PriceTrackerService only, for its lifetime.
  · WebSocket heartbeat {"action":"heartbeat"} every 25 seconds detects
    a dead connection immediately rather than waiting for a timeout.
  · ConnectivityManager broadcast listener triggers immediate reconnect
    when network is restored after any interruption.

───────────────────────────────────────────────────────────────────────────────
BARRIER 03 — Notifications Blocked or Not Delivered
───────────────────────────────────────────────────────────────────────────────

Problem:
  Android 13+ requires runtime POST_NOTIFICATIONS permission. Android 8+
  requires notification channels with appropriate importance levels.
  OEM notification managers (MIUI, OneUI) may additionally block channels
  unless the user explicitly allows them.

Solutions:
  · Runtime permission requested at first launch with plain-language
    explanation before the system dialog is shown.
  · Five distinct notification channels (see Appendix C for full registry).
  · OEM-specific guidance surfaced in the Permission Helper screen.

───────────────────────────────────────────────────────────────────────────────
BARRIER 04 — USE_FULL_SCREEN_INTENT Silently Revoked on Android 14+
───────────────────────────────────────────────────────────────────────────────

Problem:
  On Android 14 (API 34+), USE_FULL_SCREEN_INTENT is no longer auto-granted
  for sideloaded apps. It is restricted to alarm and dialer applications.
  If the permission is absent, Android silently downgrades a full-screen
  notification to a standard heads-up banner — no error, no log.
  Both the Alarming Notification and Virtual Call features break invisibly.

Solution — Runtime Policy Check (Kotlin, required on API 34+):

  fun checkAndRequestFullScreenIntentPermission(context: Context) {
      if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.UPSIDE_DOWN_CAKE) {
          val nm = context.getSystemService(NOTIFICATION_SERVICE) as NotificationManager
          if (!nm.canUseFullScreenIntent()) {
              val intent = Intent(Settings.ACTION_MANAGE_APP_USE_FULL_SCREEN_INTENT)
                  .addFlags(Intent.FLAG_ACTIVITY_NEW_TASK)
                  .putExtra(Settings.EXTRA_APP_PACKAGE, context.packageName)
              context.startActivity(intent)
          }
      }
  }

  Called at three points:
    1. Setup Wizard Step 4 — for Android 14+ devices only
    2. When user selects Alarm or Virtual Call as the alert method
    3. Permission Helper screen — live status display

───────────────────────────────────────────────────────────────────────────────
BARRIER 05 — Virtual Call Overlay Fails When Screen Is Unlocked
───────────────────────────────────────────────────────────────────────────────

Problem:
  Android 10+ prevents apps from launching Activities from the background
  when the screen is on and unlocked. A full-screen intent only works as
  designed when the device is locked. On an active, unlocked screen, Android
  silently downgrades it to a heads-up banner — the overlay never appears.

Solution — Dual-Path Overlay Strategy:

  Path A — Screen locked:
    Full-screen intent fires, VirtualCallActivity renders over the lock screen.
    Standard USE_FULL_SCREEN_INTENT mechanism.

  Path B — Screen unlocked / active (including WhatsApp/Instagram in foreground):
    SYSTEM_ALERT_WINDOW permission is used to add the overlay directly via
    WindowManager, bypassing Activity launch restrictions entirely.
    This overlay appears ABOVE WhatsApp, Instagram, and all other apps.

  fun configureOverlayWindowFlags(activity: Activity) {
      if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
          activity.window.setType(WindowManager.LayoutParams.TYPE_APPLICATION_OVERLAY)
      } else {
          @Suppress("DEPRECATION")
          activity.window.setType(WindowManager.LayoutParams.TYPE_SYSTEM_ALERT)
      }
      activity.window.addFlags(
          WindowManager.LayoutParams.FLAG_SHOW_WHEN_LOCKED or
          WindowManager.LayoutParams.FLAG_TURN_SCREEN_ON  or
          WindowManager.LayoutParams.FLAG_KEEP_SCREEN_ON  or
          WindowManager.LayoutParams.FLAG_NOT_TOUCH_MODAL
      )
  }

  IMPORTANT — WhatsApp/Instagram foreground handling:
  TYPE_APPLICATION_OVERLAY windows have system-level z-order and render
  above all regular app windows including messaging and social apps.
  See §08.3-EXT for the complete System-Level Call Simulation specification
  that covers all foreground app override scenarios.

  DND note: Both paths are initiated via the notification system. DND suppresses
  the notification before either path is reached. See §05.

───────────────────────────────────────────────────────────────────────────────
BARRIER 06 — App Does Not Resume After Phone Reboot
───────────────────────────────────────────────────────────────────────────────

Problem:
  After the device restarts, FinTrace does not auto-start. Active alerts
  are silently inactive until the user manually opens the app.

Solution:
  BOOT_COMPLETED and MY_PACKAGE_REPLACED broadcasts are received by
  BootReceiver, which re-starts the Foreground Service if the tracker
  was active before the reboot. This behaviour is opt-in (default ON),
  configurable in Settings → App Behaviour → Auto-start on boot.

  On Xiaomi MIUI: additional "Autostart" permission must be granted
  via the MIUI Security app — surfaced in the Permission Helper screen.

───────────────────────────────────────────────────────────────────────────────
BARRIER 07 — Alert Fails When WhatsApp Is Receiving a Call (NEW — v4.0)
───────────────────────────────────────────────────────────────────────────────

Problem:
  When WhatsApp or Instagram are receiving or active on a call, their
  Telecom-registered foreground priority causes Android to suppress
  TYPE_APPLICATION_OVERLAY windows from third-party apps in some OEM
  implementations. Similarly, Instagram fullscreen video suppresses
  overlay windows below a certain z-order on some devices.

Solution:
  See §08.3-EXT — System-Level Call Simulation specification.
  The call_simulation notification channel (Appendix C) uses CATEGORY_CALL
  and AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE to interrupt audio
  focus from WhatsApp/Instagram and assert the alert delivery at the
  OS telephony priority level. The overlay uses LAYOUT_IN_DISPLAY_CUTOUT_MODE
  and maximum z-order elevation to defeat fullscreen suppression.


═══════════════════════════════════════════════════════════════════════════════
§04  CRITICAL ARCHITECTURE (v2.1 FIXES — RETAINED & EXTENDED)
═══════════════════════════════════════════════════════════════════════════════

All three original architectural fixes are retained and unchanged. Extended
for v4.0 with the production data flow diagram and architecture decision matrix.

───────────────────────────────────────────────────────────────────────────────
FIX 01 — Background Isolate Termination on Swipe-to-Dismiss
───────────────────────────────────────────────────────────────────────────────

Flaw:
  The original design routed WebSocket ticks from the native
  PriceTrackerService to Dart via an EventChannel. The EventChannel's
  consumer (PriceRepository) lives in the main Flutter UI Isolate. When
  the user swipes the app from Recents, Android destroys the main Activity
  and terminates the UI Isolate. The native service survives, but is now
  pushing ticks down a destroyed channel. Result: MissingPluginException,
  broken binary messenger, alert evaluation stops entirely. The app appears
  alive (persistent notification visible) but is functionally dead.

Fix:
  Decouple alert evaluation from the UI Isolate. The native
  PriceTrackerService spawns a Headless Background Flutter Engine (via
  FlutterEngineGroup) that hosts the Dart AlertEngine in its own isolated
  execution context with no UI dependency.

  // PriceTrackerService.kt
  class PriceTrackerService : Service() {
      private lateinit var backgroundEngine: FlutterEngine

      override fun onCreate() {
          super.onCreate()
          val engineGroup = FlutterEngineGroup(applicationContext)
          backgroundEngine = engineGroup.createAndRunEngine(
              applicationContext,
              DartExecutor.DartEntrypoint.createDefault()
          )
          // Register storage IPC MethodChannel on this engine
      }
  }

  // main.dart — headless entry point
  @pragma('vm:entry-point')
  void backgroundAlertEntry() {
      // No runApp() — headless only
      WidgetsFlutterBinding.ensureInitialized();
      AlertEngine().initialize();
  }

  Result: Swipe-to-dismiss has zero effect on alert evaluation. The
  Background Isolate continues independently of all UI lifecycle events.

───────────────────────────────────────────────────────────────────────────────
FIX 02 — Widget RemoteViews Binder Saturation
───────────────────────────────────────────────────────────────────────────────

Flaw:
  The original design pushed widget RemoteViews updates on every WebSocket
  tick. Android widget updates operate over IPC via the system Binder to
  the Launcher process. At 500ms–1s per tick with multiple widget instances,
  this saturates the system Binder transaction buffer. Consequences:
  TransactionTooLargeException crash, OS-wide UI stutter, severe battery
  drain, potential service termination by Android's Binder watchdog.

Fix:
  A strict native-side throttle in PriceTrackerService decouples widget
  updates completely from the WebSocket tick rate.

  private val WIDGET_UPDATE_INTERVAL_MS = 5_000L  // Max 0.2Hz
  private var lastWidgetUpdate = 0L

  private fun onPriceTick(symbol: String, price: Double) {
      // Always: send to Background Isolate for alert evaluation
      backgroundChannel.invokeMethod("onTick",
          mapOf("symbol" to symbol, "price" to price))

      // Always: update in-memory price cache (for UI EventChannel if open)
      priceCache[symbol] = price

      // Also: update permanent ticker notification (throttled to 2s)
      updateTickerNotificationIfDue()

      // Throttled: widget RemoteViews update (max 0.2Hz)
      val now = System.currentTimeMillis()
      if (now - lastWidgetUpdate >= WIDGET_UPDATE_INTERVAL_MS) {
          lastWidgetUpdate = now
          updateAllWidgets()
      }
  }

  Result: Widget RemoteViews updates are limited to once per 5 seconds.
  Binder saturation is structurally impossible. The price ticker in the
  UI and alerts both continue at full tick rate unaffected.

───────────────────────────────────────────────────────────────────────────────
FIX 03 — Storage File Contention Between Concurrent Isolates
───────────────────────────────────────────────────────────────────────────────

Flaw:
  The original design allowed both the UI Isolate and the Background Alert
  Isolate to open and write to Hive and SQLite directly. With both executing
  simultaneously, SQLite file locks cause transaction deadlocks and Hive
  block corruption occurs on concurrent writes. Alert history records can
  be silently dropped or corrupted without any exception thrown.

Fix — Single Writer Principle:
  The Background Isolate (inside PriceTrackerService) is the sole owner of
  all storage. It is the only execution context that opens Hive boxes in
  write mode. The UI Isolate performs all storage operations by sending
  IPC requests via MethodChannel("fintrace/storage") to the Background
  Isolate, which executes the operation and returns the result.

  Storage Access Architecture:

  ┌──────────────────────────────────────────────────────┐
  │  UI Isolate                                          │
  │    invokeMethod("getAlerts")   ──►  Background reads │
  │    invokeMethod("saveAlert")   ──►  Background writes│
  │    invokeMethod("setStatus")   ──►  Background writes│
  └──────────────────────────────────────────────────────┘
                          │
              MethodChannel: "fintrace/storage"
                          │
  ┌──────────────────────────────────────────────────────┐
  │  Background Isolate (single writer)                  │
  │    Hive  — alerts, settings, symbol state            │
  │    (sole open instance; no other write paths)        │
  └──────────────────────────────────────────────────────┘

  Result: Zero file contention. One writer, one database lifecycle.
  All writes are serialised through a single controlled path.

───────────────────────────────────────────────────────────────────────────────
ARCHITECTURE DECISION MATRIX
───────────────────────────────────────────────────────────────────────────────

  Component              Original Design                Final Design (v4.0)
  ─────────────────────  ─────────────────────────────  ──────────────────────────────
  Alert evaluation       UI Isolate via EventChannel    Headless Background Engine
  Widget updates         Every WebSocket tick           Native 5-second throttle
  Storage access         Both Isolates directly         Background Isolate only
  Android 14 FSI         Assumed auto-granted           canUseFullScreenIntent() guard
  Virtual Call overlay   Full-screen intent only        Dual-path: FSI + TYPE_APP_OVERLAY
  Battery exemption      Recommended                    Hard prerequisite to start
  WA/IG foreground       Not addressed                  CATEGORY_CALL + AudioFocus shim
  Price update rate      Fixed 500ms UI interval        User-configurable (default 500ms)

───────────────────────────────────────────────────────────────────────────────
PRODUCTION DATA FLOW (CANONICAL v4.0)
───────────────────────────────────────────────────────────────────────────────

  [Boot / App Launch]
        │
        ▼
  PriceTrackerService  (Android Foreground Service — always running)
        │
        ├─► Spawns Headless Background Flutter Engine (Alert Engine Isolate)
        │       │
        │       ├── Single writer: Hive storage (alerts, settings, state)
        │       ├── Alert condition evaluator (every tick, all active alerts)
        │       └── Notification fire path (all 3 methods + call_simulation)
        │
        ├─► Native WebSocket Manager (Twelve Data WS / REST fallback)
        │       │
        │       └─► onTick(symbol, price) ─► Background Engine via MethodChannel
        │                                ─► in-memory priceCache update
        │
        ├─► UI Render Throttle (user-configured interval, default 500ms)
        │       └── Gates EventChannel tick delivery to PriceBloc (UI only)
        │
        ├─► Live Ticker Notification Updater (throttled: 2-second interval)
        │       └── Updates notification content with latest priceCache values
        │
        ├─► Widget Throttle Manager (throttled: 5-second interval)
        │       └── AppWidgetManager.updateAppWidget() — single batched IPC
        │
        └─► EventChannel ──► [If UI Isolate is alive]
                                └── PriceBloc → Dashboard UI (price animation)
                                    (UI death does not affect any path above)


═══════════════════════════════════════════════════════════════════════════════
§05  DND RESPECT POLICY
═══════════════════════════════════════════════════════════════════════════════

PRINCIPLE
  FinTrace never overrides Do Not Disturb under any condition.
  This is a firm design constraint, not a preference. If the user has
  DND active, FinTrace produces zero sound, zero vibration, and zero
  visual interruption. The user's system intent is absolute.

TECHNICAL ENFORCEMENT

  ①  ACCESS_NOTIFICATION_POLICY not requested
     This permission enables DND override. FinTrace does not request it.
     It does not appear in AndroidManifest.xml.

  ②  STREAM_NOTIFICATION used exclusively
     AudioAttributesUsage.notification is used for all alert audio.
     STREAM_ALARM, which bypasses silent mode and DND, is never used.

  ③  canBypassDnd never set on any channel
     No notification channel in FinTrace has setBypassDnd(true) set.
     See Appendix C for full channel specification.

  ④  Full-screen intents are suppressed by DND automatically
     Android suppresses full-screen intents when DND is active.
     FinTrace does not attempt to circumvent this.

  ⑤  Virtual Call overlay is downstream of notification
     The TYPE_APPLICATION_OVERLAY overlay is launched from the
     notification's full-screen intent. If DND suppresses the notification,
     neither path (locked screen nor unlocked screen) reaches the overlay.

  ⑥  Call Simulation channel respects DND
     The call_simulation channel (§08.3-EXT) also has canBypassDnd = false.
     When DND is active, audio focus is not requested and no overlay fires.

BEHAVIOUR TABLE

  Alert Method            DND OFF                         DND ON
  ──────────────────────  ──────────────────────────────  ────────────────────
  Default Notification    Heads-up + sound + vibration    Per user DND rules
  Alarming Notification   Full-screen + sound + wake      Suppressed entirely
  Virtual Call            Call overlay on screen          Suppressed entirely
  Call Simulation         OS-priority overlay + sound     Suppressed entirely
  Ticker Notification     Updated silently in panel       Not suppressed (LOW
                          (no sound, no heads-up)         importance — always
                                                          visible in shade)

  Note: The Permanent Live Ticker Notification (LOW importance, no sound)
  remains visible in the notification shade during DND because it produces
  no interruption and LOW importance channels are not subject to DND rules.

USER COMMUNICATION
  The alert creation screen displays a static info chip:

    ℹ  Alerts respect Do Not Disturb. If DND is active when this alert
       triggers, it will be silenced and shown when DND ends.

  No workarounds. No exceptions. No "Critical" override category.


═══════════════════════════════════════════════════════════════════════════════
§06  THEME SYSTEM
═══════════════════════════════════════════════════════════════════════════════

THREE MODES

  Mode 1 — Light
    Clean white surfaces. Accessible colour contrast on all text.
    Material You accent from wallpaper (Android 12+).

    Background:       #FFFFFF
    Surface:          #F5F5F5
    Card Surface:     #EFEFEF
    Primary Text:     #0D0D0D
    Secondary Text:   #555555
    Price Up:         #00897B    (teal-green — passes WCAG AA on white)
    Price Down:       #E53935    (red — passes WCAG AA on white)
    Neutral Price:    #607D8B

  Mode 2 — Dark AMOLED
    Pure black backgrounds for OLED panels. Lit pixels = battery consumed.
    True black background conserves maximum battery on OLED/AMOLED screens.
    (Redmi Note 10 Pro has an AMOLED display — this mode is optimal for it.)

    Background:       #000000
    Surface:          #0D0D0D
    Card Surface:     #141414
    Primary Text:     #F0F0F0
    Secondary Text:   #888888
    Price Up:         #00E676    (bright green — high contrast on black)
    Price Down:       #FF5252    (bright red — high contrast on black)
    Neutral Price:    #78909C

  Mode 3 — System Adaptive
    Follows Android system light/dark toggle automatically.
    On Android 12+: Material You dynamic colour seeds from user wallpaper.
    On Android 11 and below: fixed deep teal seed colour used.

THEME SWITCHER
  Location: Settings → Appearance → Theme
  Control: Three-segment chip selector — ☀ Light / ◗ AMOLED / ⟳ System
  Behaviour: Live, no restart required. Persisted in Hive settings box.

SEMANTIC COLOURS (FIXED ACROSS ALL THEMES)
  These values do not change. They override Material You for safety-critical
  data representations.

  Price Up (light theme):    #00897B   Price Up (dark theme):    #00E676
  Price Down (light theme):  #E53935   Price Down (dark theme):  #FF5252
  Alert Active:              #FFB300   (amber)
  Alert Triggered:           #29B6F6   (light blue)
  Alert Expired:             #78909C   (grey)
  Alert Critical:            #FF1744   (deep red)
  Connection Live:           #69F0AE   (teal green)
  Connection Reconnecting:   #FFD740   (yellow)
  Connection Offline:        #FF6D00   (orange)

MATERIAL YOU IMPLEMENTATION

  // main.dart
  DynamicColorBuilder(
    builder: (lightScheme, darkScheme) => MaterialApp(
      theme:     AppTheme.buildLight(lightScheme),
      darkTheme: AppTheme.buildDark(darkScheme),
      themeMode: settingsBox.read('themeMode'), // light / dark / system
    ),
  )


═══════════════════════════════════════════════════════════════════════════════
§07  FEATURE SPECIFICATION
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
§07.1  LIVE PRICE DASHBOARD (HOME)
───────────────────────────────────────────────────────────────────────────────

LAYOUT (top to bottom)
  1. Connection Status Bar — full-width, colour-coded
  2. Mini Ticker Strip — swipeable horizontal strip of pinned symbols (NEW)
  3. Symbol Price Cards — scrollable grid

CONNECTION STATUS BAR
  ● LIVE  ·  XAU EUR GBP JPY USD  ·  last: 320ms          [❚❚ pause]

  · Green dot = WebSocket connected and receiving ticks
  · Amber dot = reconnecting (shows countdown / attempt number)
  · Red dot   = offline (shows "OFFLINE" label + last update age)
  · Active symbol abbreviations shown
  · Last tick latency shown (ms)
  · Pause button: suspends all subscriptions (useful on limited data plans)

MINI TICKER STRIP (NEW — v4.0)
  Horizontal scrollable strip pinned between the status bar and the card grid.
  Shows all active symbols in compact inline format: XAU 2318.45 ▲
  User can pin this strip as their at-a-glance price reference.
  Tapping any symbol in the strip jumps to that symbol's card.
  Hidden by default; enabled via Settings → Appearance → Show Ticker Strip.

SYMBOL PRICE CARD

  ┌────────────────────────────────────────┐
  │  XAU/USD                       ⚡ 2   │  ← symbol + active alert badge
  │                                        │
  │          2,318.45                      │  ← 42sp JetBrains Mono Bold
  │          ▲ +12.30   +0.53%            │  ← direction + points + percent
  │                                        │
  │   Bid  2,318.10    Ask  2,318.80       │  ← bid/ask strip
  │   ▓▓▓▓▓▓▓▓▓▓░░   (sparkline)         │  ← last 20 ticks (custom canvas)
  │                             3s ago     │  ← last update age
  └────────────────────────────────────────┘

  Card states:
    Live     — price flashes green/red on each tick change
    Stale    — price dimmed, timestamp shows "⚠ stale Xm ago"
    Offline  — price dimmed, "● OFFLINE" chip, last known price shown
    Alerted  — card border glows in the alert's priority colour

CARD INTERACTIONS
  Tap              → open Symbol Detail screen
  Long press       → open Quick Alert creation sheet (symbol pre-filled,
                     current price pre-filled as target)
  Swipe left       → deactivate symbol (unsubscribe, remove from dashboard)
  Swipe right      → re-activate symbol (if deactivated)
  Double tap       → toggle card expanded/collapsed (compact mode)

DASHBOARD CONTROLS (top-right overflow menu)
  Sort by:   Name (A–Z) / Price Change % / Current Price (asc or desc)
  View mode: Grid 2-column (default) / List 1-column / Compact (dense)
  Pause all: toggle to suspend all subscriptions simultaneously
  Pin to top: any symbol card can be pinned to top of list

QUICK ALERT FAB (NEW — v4.0)
  The FAB on the Prices tab is now a Speed Dial FAB with two options:
    ➕ Add Symbol  — standard symbol management
    ⚡ Quick Alert — opens a streamlined 2-field alert sheet (symbol + price)
                    For users who want to set an alert in under 5 seconds.
  Speed dial expands on tap, collapses on outside touch or after selection.

───────────────────────────────────────────────────────────────────────────────
§07.2  SYMBOL DETAIL SCREEN
───────────────────────────────────────────────────────────────────────────────

  No chart. The symbol detail screen provides price data and alert access.

  · Full-width large price (JetBrains Mono Bold, 42sp)
  · Bid / Ask / Spread (spread = ask − bid, shown in pips)
  · 24h High / Low bar (horizontal range indicator)
  · Last update timestamp
  · Price direction indicator (▲ / ▼ / — with colour)
  · Active Alerts section: inline list of alerts configured for this symbol
    — shows target price, condition, method icon, status chip per row
    — "Add Alert" action button inline
  · FAB: + Add Alert (pre-fills symbol and current price as suggested target)

───────────────────────────────────────────────────────────────────────────────
§07.3  SYMBOL MANAGEMENT
───────────────────────────────────────────────────────────────────────────────

  · All 14 symbols available. User activates/deactivates each individually.
  · Active = subscribed to WebSocket = visible on dashboard.
  · Inactive = unsubscribed = hidden from dashboard (API quota preserved).
  · Drag-and-drop reorder of active symbols on the dashboard.
  · Symbol search within the 14 supported symbols (for quick activation).

───────────────────────────────────────────────────────────────────────────────
§07.4  PERMANENT LIVE TICKER NOTIFICATION
───────────────────────────────────────────────────────────────────────────────

OVERVIEW
  This is a dedicated, persistent notification that lives permanently in the
  Android notification panel (shade). It shows live prices for 1–5
  user-selected symbols, updating in near-real-time. It is separate from
  the Foreground Service ticker notification.

  Feature                Foreground Service Ticker    Live Ticker Notification
  ─────────────────────  ───────────────────────────  ─────────────────────────
  Purpose                Keep service alive           Dedicated price display
  Managed by system      Yes (cannot be dismissed)    Yes (cannot be dismissed
                                                       while enabled)
  User can disable       No (FGS is mandatory)        Yes — from within app
  Symbol count           Shows service status         1–5 user-selected
  Update rate            On every tick (text only)    Throttled: every 2 seconds

USER CONTROLS
  Enable / disable: Settings → Notifications → Live Ticker Notification (toggle)
  When enabled:  notification appears in panel immediately
  When disabled: notification is cancelled; does not reappear until re-enabled
  Symbol selection: Settings → Notifications → Live Ticker Symbols
    — checklist of all 14 supported symbols
    — select 1 to 5 (minimum 1 if enabled, maximum 5)
    — order matches display order in notification
  Preference persisted in Hive settings. Restored on service restart and boot.

DISPLAY FORMAT
  Single symbol (1 selected):
  ┌────────────────────────────────────────────┐
  │  FinTrace  ●  LIVE                         │
  │  XAU/USD    2,318.45   ▲ +0.53%           │
  └────────────────────────────────────────────┘

  Multi-symbol (up to 5 selected):
  ┌────────────────────────────────────────────┐
  │  FinTrace  ●  LIVE                     ... │
  │  XAU  2,318.45 ▲   EUR  1.0823 ▲          │
  │  GBP  1.2741 ▼     JPY  156.34 ▲          │
  │  AUD  0.6521 ▼                             │
  └────────────────────────────────────────────┘

  Offline state:
  ┌────────────────────────────────────────────┐
  │  FinTrace  ●  OFFLINE                      │
  │  XAU  2,318.45 (last known)                │
  └────────────────────────────────────────────┘

NOTIFICATION CHANNEL
  Channel ID:    price_ticker_live
  Importance:    LOW
  Sound:         None
  Vibration:     None
  Heads-up:      No
  DND effect:    Not suppressed (LOW importance — passive, no interruption)
  Dismissable:   No (while feature is enabled, it is re-posted if dismissed)

TECHNICAL IMPLEMENTATION
  The PriceTrackerService (already running) maintains this notification.
  On each onPriceTick() call, it updates an in-memory liveTickerLastUpdate
  timestamp and only rebuilds the notification if ≥ 2 seconds have passed
  since the last rebuild. This avoids excessive notification rebuilds while
  still providing near-live updates.

  val TICKER_NOTIFICATION_ID = 1002
  val TICKER_UPDATE_INTERVAL_MS = 2_000L
  private var lastTickerUpdate = 0L

  private fun updateTickerNotificationIfDue() {
      if (!tickerNotificationEnabled) return
      val now = System.currentTimeMillis()
      if (now - lastTickerUpdate < TICKER_UPDATE_INTERVAL_MS) return
      lastTickerUpdate = now
      val content = buildTickerContent(tickerSymbols, priceCache)
      val notification = buildTickerNotification(content, isConnected)
      notificationManager.notify(TICKER_NOTIFICATION_ID, notification)
  }

  On connection state change: update immediately regardless of throttle interval.
  On feature disabled: notificationManager.cancel(TICKER_NOTIFICATION_ID)
  On feature enabled: rebuild notification immediately from priceCache
  Tap action: opens FinTrace home.

───────────────────────────────────────────────────────────────────────────────
§07.5  SETTINGS SCREEN  ← UPDATED v4.0
───────────────────────────────────────────────────────────────────────────────

  Grouped Material You 3 settings list. Tap any group header to expand.
  All groups use smooth expand/collapse animation (300ms easing).

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: Data Source                                                  │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · Manage API Key                 → links to §07.6 API Key screen    │
  │                                                                      │
  │  · Price Update Interval (ms)     [  500  ]  ← numeric input field  │
  │    Controls how often the UI redraws prices.                         │
  │    Default: 500ms (= 0.5 seconds).                                   │
  │    Minimum: 100ms. No maximum enforced.                              │
  │    Hint text: "e.g. 500 = half second, 1000 = 1 second"             │
  │    Alert evaluation is NOT affected by this setting.                 │
  │    Input validation: must be a positive integer ≥ 100.               │
  │    Saved on blur / keyboard dismiss. Live-applied without restart.   │
  │    Reset button: "↺ Reset to 500ms" appears if value ≠ 500.         │
  │                                                                      │
  │  · Connection Diagnostics         → links to diagnostics screen      │
  └──────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: Notifications                                                │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · Live Ticker Notification       ON / OFF toggle                    │
  │  · Live Ticker Symbols            → symbol selector (1–5 symbols)    │
  │  · Foreground service style       Compact / Detailed                 │
  └──────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: Appearance                                                   │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · Theme                          ☀ Light / ◗ AMOLED / ⟳ System     │
  │  · Dynamic colour (Material You)  ON / OFF                           │
  │  · Price animation                Flash / Digit roll / None          │
  │  · Show Ticker Strip              ON / OFF (mini ticker on dashboard) │
  └──────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: Alerts                                                       │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · Default alert method           Notification / Alarm / Virtual Call│
  │  · Default priority               Low / Medium / High / Critical     │
  │  · Vibration patterns             per priority level (4 rows)        │
  └──────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: App Behaviour                                                │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · Auto-start on boot             ON / OFF                           │
  │  · Start minimised                ON / OFF                           │
  │  · Keep screen on while open      ON / OFF                           │
  └──────────────────────────────────────────────────────────────────────┘

  ┌──────────────────────────────────────────────────────────────────────┐
  │  GROUP: About                                                        │
  ├──────────────────────────────────────────────────────────────────────┤
  │  · App version                    v4.0 (build 40)                    │
  │  · Permissions status             → links to Permission Helper       │
  │  · Twelve Data API docs           → opens browser                    │
  │  · About This App                 → opens About screen (S14)         │
  │  · About the Developer            → opens Developer panel (S14-B)    │
  └──────────────────────────────────────────────────────────────────────┘

PRICE UPDATE INTERVAL — DETAILED SPECIFICATION

  Storage key:    "price_update_interval_ms"       (Hive settings box)
  Type:           int
  Default:        500
  Minimum:        100
  Maximum:        none (user may enter any positive integer ≥ 100)
  Validation:     Live — red border + error text if value < 100
                  "Minimum interval is 100ms"
  Apply:          Applied immediately to the UI render throttle timer.
                  Does NOT require service restart.
  Scope:          Controls only the Flutter UI EventChannel delivery rate.
                  WebSocket tick rate and alert evaluation are unaffected.

  UI component:   TextField with numeric keyboard, suffix "ms",
                  leading icon: ⏱, Material You outlined style.
                  InputFormatters: digits only, max 6 characters.
                  On "Reset" tap: animates to "500", saves, applies.

───────────────────────────────────────────────────────────────────────────────
§07.6  API KEY MANAGEMENT SCREEN
───────────────────────────────────────────────────────────────────────────────

  Accessible via: Settings → Data Source → Manage API Key

  ┌──────────────────────────────────────────────┐
  │  Twelve Data API Key                         │
  │                                              │
  │  ●●●●●●●●●●●●●●●●●●●●●●●●●●●●      👁      │
  │                                              │
  │  Status:  ✓  Valid & Connected               │
  │                                              │
  │  [ Update Key ]        [ Validate ]          │
  │                                              │
  │  ─────────────────────────────────────────   │
  │  No key yet?                                 │
  │  Get a free API key at twelvedata.com  →     │
  └──────────────────────────────────────────────┘

  Behaviour:
  · Key masked by default. Eye icon toggles plain text display.
  · Validate: sends test subscribe → awaits server response →
    shows ✓ Valid (green) or ✗ Invalid (red) with specific error.
  · Update Key: user enters new key → Validate auto-runs →
    on success, old WebSocket connection is cleanly closed,
    new connection opened with new key, subscriptions restored.
  · Key stored in Android Keystore (AES-256 encrypted).
    No plain text anywhere — not in logs, not in exports.
  · Key deletion: all subscriptions cancelled, app enters
    "No API Key" state with setup prompt on the home screen.


═══════════════════════════════════════════════════════════════════════════════
§08  ALERT SYSTEM
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
§08.1  ALERT CREATION — FIELD SPECIFICATION
───────────────────────────────────────────────────────────────────────────────

  Field            Type              Detail
  ───────────────  ────────────────  ────────────────────────────────────────
  Symbol           Dropdown          Any of 14 supported symbols
  Condition        3-chip selector   Crossing / Crossing Up / Crossing Down
  Target Price     Numeric field     Formatted per symbol decimal convention;
                                     if opened via long-press on a card, the
                                     current live price is pre-filled.
  Title            Text field        Default: "XAU/USD crossed 2,320.00"
  Message          Text field        Optional body text for notification
  Alert Method     3-chip selector   Default Notification / Alarm / Virtual Call
  Priority         4-chip selector   Low / Medium / High / Critical
  Expiration       Date-time picker  Never (default) / Specific datetime
  Repeat           Toggle            One-time (default) / Repeating
  Cooldown         Duration picker   If Repeat ON: 5m / 15m / 30m / 1h / Custom
  Sound            Dropdown          System default / Custom / Silent
  Vibration        Dropdown          None / Short / Long / Pattern (SOS)
  Colour Tag       Colour picker     6 colours for visual identification

  Screen layout: three steps, each a scrollable section within a single screen.
    Step 1  Symbol + Condition + Price
    Step 2  Method + Priority + Sound + Vibration
    Step 3  Title + Message + Expiration + Repeat + Colour
  Preview panel at bottom: live preview of the notification as configured.

QUICK ALERT SHEET (NEW — v4.0)
  Accessible from: long-press on any price card, or Speed Dial FAB (⚡).
  A bottom sheet with just 3 fields:
    Symbol    — pre-filled from the card tapped
    Price     — pre-filled with current live price (user adjusts)
    Method    — 3-chip selector with last-used method pre-selected
  "Create Alert" button creates immediately with all other fields set to
  their defaults from Settings → Alerts → Default values.
  Designed to complete in under 5 seconds.

───────────────────────────────────────────────────────────────────────────────
§08.2  TRIGGER CONDITION LOGIC
───────────────────────────────────────────────────────────────────────────────

  Evaluated on every received WebSocket tick.
  prev_price = last received price for this symbol (from priceCache).
  current_price = this tick's price.

  CROSSING (either direction):
    (prev_price < target AND current_price >= target)   ← upward cross
    OR
    (prev_price > target AND current_price <= target)   ← downward cross

  CROSSING UP:
    prev_price < target AND current_price >= target

  CROSSING DOWN:
    prev_price > target AND current_price <= target

  Gap handling:
    If the WebSocket drops and reconnects with the price already past the
    target, the crossing is detected on the first tick after reconnect,
    using the last pre-disconnect cached price as prev_price.
    No crossing is silently missed due to a connectivity gap.

  Cooldown handling:
    If an alert has a cooldown active, the evaluator skips it entirely
    until cooldown expires. Cooldown is stored as an absolute datetime
    (cooldownUntil). Comparison: tickTime < alert.cooldownUntil → skip.

───────────────────────────────────────────────────────────────────────────────
§08.3  DELIVERY METHODS
───────────────────────────────────────────────────────────────────────────────

  METHOD 1 — DEFAULT NOTIFICATION
    Channel:      price_alert_default (Importance: HIGH)
    Behaviour:    Heads-up notification, slides in from top of screen
    Audio:        User-selected (STREAM_NOTIFICATION)
    Vibration:    As configured in alert
    Persistence:  Auto-dismissed after user interacts
    Actions:      [Dismiss]  [View Alert]
    DND:          Fully suppressed when DND is ON

  METHOD 2 — ALARMING NOTIFICATION
    Channel:      price_alert_alarm (Importance: MAX)
    Behaviour:    Full-screen intent — wakes screen when locked,
                  persistent until explicitly dismissed by user
    Audio:        User-selected (STREAM_NOTIFICATION — NOT alarm stream)
    Vibration:    Urgent pattern
    Screen wake:  FLAG_TURN_SCREEN_ON — only fires when DND is OFF
    Android 14:   canUseFullScreenIntent() checked before delivery
    Actions:      [Dismiss]  [View Alert]
    DND:          Fully suppressed when DND is ON

  METHOD 3 — VIRTUAL CALL
    Channel:      price_alert_alarm (same channel as Method 2)
    Behaviour:    Call-style full-screen overlay with pulsing animation
    Screen locked:     VirtualCallActivity via full-screen intent
    Screen unlocked:   WindowManager overlay via TYPE_APPLICATION_OVERLAY
    Permissions:  USE_FULL_SCREEN_INTENT + SYSTEM_ALERT_WINDOW both required
    Actions:      [✖ Dismiss]  [✔ View in App]
    Audio:        Same as Alarming Notification
    DND:          Fully suppressed when DND is ON (notification suppressed
                  before either overlay path is reached)

  IMPORTANT — All three methods fire correctly when the device is:
    · Screen off and locked (standard path)
    · Screen on, app in background (overlay path)
    · WhatsApp or Instagram in foreground (overlay path — see §08.3-EXT)
    · Gaming app in foreground (overlay path — TYPE_APPLICATION_OVERLAY
      renders above all regular app windows)
    · Device rebooted (BootReceiver re-starts service; alerts resume)

───────────────────────────────────────────────────────────────────────────────
§08.3-EXT  SYSTEM-LEVEL CALL SIMULATION  ← NEW v4.0
           (WhatsApp / Instagram Override Strategy)
───────────────────────────────────────────────────────────────────────────────

PROBLEM STATEMENT
  The user requires that price alerts fire visually and audibly even when:
    (a) WhatsApp is actively receiving or on a call
    (b) Instagram is playing a fullscreen Reel/video with audio focus
    (c) Any other foreground app holds exclusive audio focus
    (d) The phone screen appears to be "off" but is actually in an app

  Standard TYPE_APPLICATION_OVERLAY windows can be suppressed on certain
  OEM firmware (MIUI, OneUI) when a Telecom-registered call is active or
  when the foreground app holds FLAG_FULLSCREEN with FLAG_LAYOUT_NO_LIMITS.

SOLUTION — CALL SIMULATION CHANNEL + AUDIO FOCUS ESCALATION

  This is a FOURTH alert delivery method, available in the alert creation
  screen as an advanced option. It is designed specifically for situations
  where the trader knows they will likely be in WhatsApp or Instagram when
  the alert fires.

  Implementation:

  STEP 1 — Notification with CATEGORY_CALL
    Post a notification on the call_simulation channel (Appendix C).
    NotificationCompat.Builder:
      .setCategory(NotificationCompat.CATEGORY_CALL)
      .setPriority(NotificationCompat.PRIORITY_MAX)
      .setFullScreenIntent(callIntent, true)
    CATEGORY_CALL grants this notification the same system priority as
    incoming phone calls, putting it above WhatsApp and social media apps
    in the Android notification dispatch pipeline.

  STEP 2 — AudioFocus Escalation
    Request AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE from AudioManager.
    This tells the OS to duck/pause all other audio — including WhatsApp
    call audio and Instagram video playback — and deliver our alert sound.

    val audioManager = context.getSystemService(AudioManager::class.java)
    val focusRequest = AudioFocusRequest.Builder(
        AudioManager.AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE
    )
        .setAudioAttributes(AudioAttributes.Builder()
            .setUsage(AudioAttributes.USAGE_NOTIFICATION_COMMUNICATION_INSTANT)
            .setContentType(AudioAttributes.CONTENT_TYPE_SONIFICATION)
            .build())
        .setOnAudioFocusChangeListener { /* release on dismiss */ }
        .build()
    audioManager.requestAudioFocus(focusRequest)

    NOTE: STREAM_NOTIFICATION is still used for the actual playback. This
    does NOT use STREAM_ALARM. DND remains fully respected (§05).

  STEP 3 — Maximum Z-Order Overlay Window
    If the screen is unlocked (Path B — §03 Barrier 05):
    The WindowManager overlay uses these additional flags to defeat
    fullscreen suppression:

    val params = WindowManager.LayoutParams(
        WindowManager.LayoutParams.TYPE_APPLICATION_OVERLAY,
        WindowManager.LayoutParams.FLAG_SHOW_WHEN_LOCKED or
        WindowManager.LayoutParams.FLAG_TURN_SCREEN_ON or
        WindowManager.LayoutParams.FLAG_KEEP_SCREEN_ON or
        WindowManager.LayoutParams.FLAG_NOT_TOUCH_MODAL or
        WindowManager.LayoutParams.FLAG_LAYOUT_IN_SCREEN or
        WindowManager.LayoutParams.FLAG_LAYOUT_NO_LIMITS,
        PixelFormat.TRANSLUCENT
    ).also {
        it.gravity = Gravity.TOP or Gravity.START
        it.x = 0; it.y = 0
        it.width = WindowManager.LayoutParams.MATCH_PARENT
        it.height = WindowManager.LayoutParams.MATCH_PARENT
        // Android 9+: cutout mode extends into display cutout area
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.P) {
            it.layoutInDisplayCutoutMode =
                WindowManager.LayoutParams.LAYOUT_IN_DISPLAY_CUTOUT_MODE_SHORT_EDGES
        }
    }

    This window renders at the absolute top z-order, above Instagram
    fullscreen videos and above WhatsApp's in-call UI.

  STEP 4 — Vibration with VibrationEffect (API 26+)
    Use VibrationEffect.createWaveform with a strong pattern to ensure
    physical notification even if the user misses the visual overlay.
    val effect = VibrationEffect.createWaveform(
        longArrayOf(0, 500, 200, 500, 200, 800), -1
    )
    vibrator.vibrate(effect)

  PHONE-OFF SCENARIO
    "Phone off" is interpreted as screen off + device locked.
    When the screen is off:
      · The CATEGORY_CALL notification fires the full-screen intent.
      · FLAG_TURN_SCREEN_ON wakes the screen.
      · The lock screen alert overlay renders on top of the lock screen.
    This works correctly regardless of WhatsApp or Instagram state because
    those apps are not in a running foreground state when the screen is off.

  OEM CAVEAT — MIUI (Xiaomi)
    MIUI has a "Focus Mode" that can suppress all overlays including
    TYPE_APPLICATION_OVERLAY. FinTrace detects MIUI (device_info_plus)
    and shows a warning in the Permission Helper:
      "⚠ MIUI Focus Mode may suppress price alerts. Please add FinTrace
       to the MIUI Focus Mode exclusion list in Security → Focus Mode."

  DELIVERY METHOD NAME IN UI
    Displayed in alert creation as: "📞 Priority Call Alert"
    Tooltip: "Maximum urgency. Appears above WhatsApp and Instagram."
    Requires: SYSTEM_ALERT_WINDOW + USE_FULL_SCREEN_INTENT

  DND COMPLIANCE
    All four steps respect DND. If DND is active:
      · CATEGORY_CALL notification is still subject to DND (canBypassDnd = false)
      · AudioFocus is not requested
      · No overlay is created
    DND is always fully respected. See §05.

───────────────────────────────────────────────────────────────────────────────
§08.4  ALERT LIST SCREEN
───────────────────────────────────────────────────────────────────────────────

  Header: "Alerts" + count chip + search icon + filter icon + select icon

  Filter chips row (below search bar, scrollable):
    [All]  [Active]  [Triggered]  [Expired]  [Deactivated]

  Alert row layout:
    ● [colour dot]  XAU/USD   ↗ Cross Up  2,320.00   🔊  CRITICAL
      "FundedNext entry signal"
      Active · One-time · Expires 30 Jun 2026                        [ ⋮ ]

  Status chips:
    Active (green) / Triggered (blue) / Deactivated (grey) / Expired (red)

  Method icons:
    🔔 Default Notification  /  🔊 Alarm  /  📞 Virtual Call  /  ⚡ Priority Call

  Per-row swipe actions:
    Swipe right → toggle Active/Deactivated
    Swipe left  → Delete (requires confirmation: "Delete this alert?")

  Row tap → open Alert Detail screen
  Long press → enter multi-select mode (checkboxes appear on all rows)

───────────────────────────────────────────────────────────────────────────────
§08.5  BATCH ACTIONS
───────────────────────────────────────────────────────────────────────────────

  Activated by long-pressing any alert row or tapping the select icon.
  Action bar slides up from bottom with the following actions:

  Action                   Detail
  ───────────────────────  ──────────────────────────────────────────────────
  Select All               Select all alerts in current filtered view
  Deselect All             Clear selection
  Activate Selected        Set status = Active for all selected
  Deactivate Selected      Set status = Deactivated for all selected
  Delete Selected          Permanently delete — confirmation: "Delete N alerts?"
  Activate All             Activate all alerts (ignores current filter)
  Deactivate All           Deactivate all alerts (ignores current filter)
  Delete All               Delete entire list — strong confirmation required

───────────────────────────────────────────────────────────────────────────────
§08.6  SEARCH & FILTER
───────────────────────────────────────────────────────────────────────────────

  Search: Full-text match on Title and Message fields.

  Filter panel (bottom sheet, opens on filter icon tap):

  Filter         Options
  ─────────────  ────────────────────────────────────────────────────────────
  Symbol         Multi-select from 14 symbols
  Status         All / Active / Deactivated / Triggered / Expired
  Method         All / Notification / Alarm / Virtual Call / Priority Call
  Priority       All / Low / Medium / High / Critical
  Condition      All / Crossing / Crossing Up / Crossing Down
  Has Expiry     All / Never expires / Has expiry date
  Colour Tag     Any of 6 colour chips
  Date Created   Date range picker (From → To)

  Sort by: Creation date · Target price · Priority · Symbol · Method

  Active filters are shown as dismissable chips below the search bar.
  Tapping × on a chip removes that filter. "Clear all" button clears all.

───────────────────────────────────────────────────────────────────────────────
§08.7  TRIGGER HISTORY (per alert)
───────────────────────────────────────────────────────────────────────────────

  Accessible from the Alert Detail screen.
  · Summary: "Triggered N times"
  · Timeline list: each row shows —
      timestamp  ·  price at trigger  ·  method used
  · One-time alerts show a single entry.
  · Repeating alerts show the full history chronologically.

───────────────────────────────────────────────────────────────────────────────
§08.8  ALERT STATISTICS SUMMARY
───────────────────────────────────────────────────────────────────────────────

  Accessible from: Alerts screen → overflow menu → Statistics

  · Total alerts created
  · Currently active
  · Triggered today
  · Triggered this week
  · Most alerted symbol
  · Most used delivery method


═══════════════════════════════════════════════════════════════════════════════
§09  HOME SCREEN WIDGET SYSTEM
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
§09.1  WIDGET TYPES
───────────────────────────────────────────────────────────────────────────────

  TYPE 1 — SINGLE SYMBOL (2×1 — Small)
    ┌────────────────────────────┐
    │  XAU/USD                  │
    │  2,318.45                 │
    │  ▲ +0.53%      3s ago     │
    └────────────────────────────┘
    Symbol name, price (large), change %, last update age.
    Tap → open FinTrace home or symbol detail (configurable).

  TYPE 2 — MULTI-SYMBOL (4×2 — Medium)
    ┌────────────────────────────────────────────┐
    │  FinTrace  ●                               │
    │  XAU/USD     2,318.45     ▲  +0.53%       │
    │  XAG/USD        27.82     ▼  -0.21%       │
    │  EUR/USD      1.0823      ▲  +0.12%       │
    │  GBP/USD      1.2741      ▼  -0.08%       │
    │  USD/JPY     156.34       ▲  +0.30%       │
    └────────────────────────────────────────────┘
    Up to 5 symbols (user-configured per slot).
    Connection dot: ● green (live) / ● red (offline).
    Tap any row → open that symbol's detail in app.

  TYPE 3 — COMPACT TICKER (4×1 — Thin)
    ┌────────────────────────────────────────────────────┐
    │  XAU  2318.45 ▲  │  EUR  1.0823 ▲  │  GBP  1.2741 ▼  │
    └────────────────────────────────────────────────────┘
    3 symbols side-by-side. Minimal, horizontal.
    Tap → open FinTrace home.

───────────────────────────────────────────────────────────────────────────────
§09.2  WIDGET CONFIGURATION
───────────────────────────────────────────────────────────────────────────────

  When user long-presses the launcher and adds a FinTrace widget:
    1. Type picker screen with live visual previews of all 3 types.
    2. Configuration screen:
         Symbol slots     Per-slot dropdown (Type 2: 5 slots; Type 3: 3 slots)
         Theme            Follow app theme / Force dark / Force light / Transparent
         Show/hide        Last update timestamp · Change percentage
         Tap action       Open app home / Open symbol detail / Open alerts

  Multiple widget instances are fully supported. Each instance is
  independently configured with its own symbol set and display options.

───────────────────────────────────────────────────────────────────────────────
§09.3  WIDGET UPDATE MECHANISM
───────────────────────────────────────────────────────────────────────────────

  Widgets are updated by the Foreground Service — not by AppWidgetProvider's
  AlarmManager interval (which is limited to 30 minutes by Android).

  The service calls AppWidgetManager.updateAppWidget() on a native 5-second
  throttle (Fix 02 from §04). This is the only way to achieve near-real-time
  widget updates without triggering Binder saturation.

  Update frequency: max 0.2Hz (once every 5 seconds)
  Connection loss: widget immediately shows "● OFFLINE" on next throttle tick


═══════════════════════════════════════════════════════════════════════════════
§10  UI/UX DESIGN SYSTEM  ← FULL PRODUCTION REDESIGN v4.0
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
§10.1  DESIGN LANGUAGE & PRINCIPLES
───────────────────────────────────────────────────────────────────────────────

  Material You 3 — "Trading Precision"

  CORE LAW:
  The price number is the most important element on every screen that shows one.
  It must be the largest, most visually dominant element. Everything else
  exists to label, contextualise, or act upon the price. Structure is created
  through space and typography, not decorative lines or boxes.

  DESIGN PILLARS:

  ① Data Dominance
    Price typography at 42sp Bold Mono is the visual anchor. Labels are
    supporting cast. No decorative chrome, no gradients that obscure data,
    no icons that compete with numbers.

  ② Instant Comprehension
    Colour carries meaning before text is read: green = up, red = down,
    amber = alert active, blue = triggered. A trader must understand the
    state of any card in 200ms or less.

  ③ One-Thumb Reachability
    All primary actions are reachable within the thumb zone on a standard
    phone held in portrait. FAB is bottom-right. Critical actions are in
    the bottom half of the screen. Overflow menus are a last resort.

  ④ Calm Intelligence
    The app does not fight for attention with the data. Status indicators
    are subtle when things are normal, prominent only when action is needed.
    No animated logos. No splash screens beyond minimum orientation.

  ⑤ Adaptive Density
    Three view modes let the user tune information density to their context:
    Grid (visual), List (balanced), Compact (dense / maximum symbols).

───────────────────────────────────────────────────────────────────────────────
§10.2  TYPOGRAPHY
───────────────────────────────────────────────────────────────────────────────

  All price numbers use JetBrains Mono (monospaced). This is critical:
  proportional fonts cause the layout to shift horizontally as digits
  change width (e.g. "1" vs "8"). Monospaced fonts prevent this entirely.

  All interface text uses Inter.

  Role                       Size   Weight   Font             Line Height
  ─────────────────────────  ─────  ───────  ───────────────  ───────────
  Price — primary display    42sp   Bold     JetBrains Mono   1.0
  Price — secondary          24sp   Medium   JetBrains Mono   1.1
  Price — widget / compact   18sp   Regular  JetBrains Mono   1.0
  Price — ticker strip       15sp   Medium   JetBrains Mono   1.0
  Symbol name                16sp   SemiBold Inter            1.2
  Screen / section title     20sp   Bold     Inter            1.2
  Labels / metadata          13sp   Regular  Inter            1.4
  Captions / timestamps      11sp   Regular  Inter 60% op.    1.3
  Alert condition text       14sp   Medium   Inter            1.3
  Button labels              14sp   Medium   Inter            1.0
  Settings group header      12sp   SemiBold Inter CAPS       1.4
  Settings item label        15sp   Regular  Inter            1.3
  Settings item subtitle     13sp   Regular  Inter 60% op.    1.3

  NUMBER FORMATTING
    XAU/USD, XAG/USD:     5 decimal places (e.g. 2,318.45000)
                           displayed at 2dp in compact, 5dp in detail view
    Forex majors:          4 decimal places (e.g. 1.0823)
    JPY pairs:             2 decimal places (e.g. 156.34)
    Thousands separator:   comma (,) — locale-aware override
    Decimal separator:     period (.) — always, for consistency with markets

───────────────────────────────────────────────────────────────────────────────
§10.3  COLOUR SYSTEM
───────────────────────────────────────────────────────────────────────────────

  See §06 for complete colour token values per theme.
  Semantic colours (price up/down, connection state, alert states) are
  fixed regardless of theme — see §06 Semantic Colours table.

  ELEVATION MODEL (Material You 3)
    Level 0: Background surface — base layer
    Level 1: Cards, list items — 1dp elevation tint
    Level 2: App bar, FAB — 3dp elevation tint
    Level 3: Navigation bar — 6dp elevation tint
    Level 4: Modals, bottom sheets — 8dp elevation tint
    Level 5: Dialogs, tooltips — 12dp elevation tint

  ALERT PRIORITY COLOUR CODING
    Low:      #4CAF50  (green)   — informational, minor threshold
    Medium:   #FFB300  (amber)   — watch level, noteworthy
    High:     #FF6D00  (orange)  — action recommended
    Critical: #FF1744  (red)     — immediate action required

───────────────────────────────────────────────────────────────────────────────
§10.4  COMPONENT REFERENCE
───────────────────────────────────────────────────────────────────────────────

  PRICE CARD — VISUAL STATES

    State: LIVE (receiving ticks)
    ┌─ Card surface (#141414 AMOLED / #EFEFEF Light) ──────────────────────┐
    │  XAU/USD                                                     ⚡ 2    │
    │                                                                       │
    │                      2,318.45                                         │
    │                      ▲ +12.30   +0.53%                               │
    │                                                                       │
    │   Bid  2,318.10          Ask  2,318.80                               │
    │   ████████████░░   (sparkline — last 20 ticks)                       │
    │                                                3s ago                 │
    └───────────────────────────────────────────────────────────────────────┘
    Price flashes green or red (120ms) on each tick change.

    State: STALE (no tick in > 30 seconds)
    Border: amber dashed 1px
    Price: 60% opacity
    Timestamp: "⚠ stale 2m ago" in amber

    State: OFFLINE
    Border: orange solid 1px
    Price: 50% opacity
    Overlay chip: "● OFFLINE" (orange)
    Timestamp: "last known price" label

    State: ALERTED (a configured alert is active)
    Border: continuous glow animation in alert's priority colour
    Glow: 2px border, 50% opacity, pulsing at 1Hz

  CONNECTION STATUS BAR

    LIVE:        ● green   "LIVE"   ·  XAU EUR GBP  ·  320ms      [❚❚]
    RECONNECTING:● amber   "RECONNECTING…"  attempt 2/5  15s       [❚❚]
    OFFLINE:     ● red     "OFFLINE"  ·  last data 4m ago          [▶]

  ALERT ROW (list item)
    ● [colour dot]  XAU/USD   ↗ Cross Up  2,320.00   📞  CRITICAL
      "FundedNext entry signal"
      Active · One-time · No expiry                              [ ⋮ ]

    Colour dot: 8px circle in the alert's assigned tag colour
    Arrow icon: ↗ (up) / ↘ (down) / ↕ (crossing either)
    Method icon: 🔔 / 🔊 / 📞 / ⚡

  SYMBOL DETAIL HEADER
    XAU/USD
    2,318.45
    ▲ +12.30  +0.53%
    Bid 2,318.10  Ask 2,318.80  Spread 70 pts
    24h: Low 2,301.20  ────────●────────  High 2,325.80

  QUICK ALERT BOTTOM SHEET
    ┌─ Bottom Sheet (rounded top, 24dp radius) ─────────────────────────────┐
    │  ⚡ Quick Alert                                          [ × ]         │
    │  ───────────────────────────────────────────────────────────────────   │
    │  Symbol       XAU/USD  ▼                                               │
    │  Target       [ 2,318.45 ]  (current price pre-filled)                 │
    │  Method       [🔔 Notify]  [🔊 Alarm]  [📞 Call]  [⚡ Priority]        │
    │                                                                        │
    │               [   ⚡  Create Alert   ]  ← primary CTA                 │
    │  "More options →" link opens full alert creation screen                │
    └────────────────────────────────────────────────────────────────────────┘

  VIRTUAL CALL OVERLAY SCREEN

    ┌─ Full screen — true black ─────────────────────────────────────────────┐
    │                                                                        │
    │                         FinTrace                                       │
    │                         Price Alert                                    │
    │                                                                        │
    │                  XAU/USD  ▲ CROSSING UP                               │
    │                                                                        │
    │                      2,320.15                                          │
    │                  Target was  2,320.00                                  │
    │                                                                        │
    │            "FundedNext entry signal"                                   │
    │                                                                        │
    │  ─────────────────────────────────────────────────────────────────     │
    │                                                                        │
    │         [  ✖  Dismiss  ]            [  ✔  View in App  ]              │
    │                                                                        │
    │  [pulsing green ring animation around FinTrace logo — 2 cycles]        │
    └────────────────────────────────────────────────────────────────────────┘

    Animation: sine-wave pulsing ring at 1Hz, 2–4 cycles, then steady.
    Background: #000000 (always, regardless of theme).
    Dismiss: sends user back to previous state (no app open).
    View in App: opens FinTrace to the alert's detail screen.

───────────────────────────────────────────────────────────────────────────────
§10.5  NAVIGATION ARCHITECTURE
───────────────────────────────────────────────────────────────────────────────

  BOTTOM NAVIGATION BAR — 3 tabs
    📈 Prices      Live price dashboard (home)
    🔔 Alerts      Alert list, create, manage
    ⚙  Settings   All configuration

  CONTEXT FAB (Speed Dial Floating Action Button)
    Prices tab   →  Speed Dial: [➕ Add Symbol]  [⚡ Quick Alert]
    Alerts tab   →  Single FAB: [+ New Alert]
    Settings tab →  (none)

  TOP APP BAR
    Screen title / context title
    Search icon (shown on Alerts screen)
    Overflow menu (3-dot, context-sensitive)

  NAVIGATION PATTERNS
    Screen → Screen  :  go_router named routes, type-safe
    Modal content    :  ModalBottomSheet for filter panels, quick actions
    Full-screen form :  pushed route (Alert creation, API key screen)
    Settings groups  :  in-place expansion (no navigation required)
    About screens    :  pushed route from Settings → About group

───────────────────────────────────────────────────────────────────────────────
§10.6  ANIMATIONS & MOTION
───────────────────────────────────────────────────────────────────────────────

  Event                        Animation                    Duration
  ───────────────────────────  ───────────────────────────  ────────
  Price tick — upward change   Green flash on price digit   120ms
  Price tick — downward        Red flash on price digit     120ms
  Alert fires (card)           Card border pulse: 2 cycles  400ms
  Virtual Call overlay         Ring pulse animation         2 cycles at 1Hz
  Connection restored          Status dot pulses green once 500ms
  Dashboard load               Cards stagger-fade in        40ms offset/card
  Alert created                Success snackbar slides up   300ms
  Swipe action reveal          Spring physics k=400 d=0.8   —
  Theme switch                 CrossFade                    300ms
  Bottom sheet open            Slide up + backdrop fade     250ms
  Settings group expand        Height animation             200ms
  Speed Dial FAB expand        Stagger scale up             150ms/item
  Tab switch                   CrossFade + icon scale       200ms
  Quick Alert creation         Ripple + checkmark           300ms

  All animations respect the Android "Reduce Motion" accessibility setting.
  When enabled, all transitions are replaced with instant state changes.

───────────────────────────────────────────────────────────────────────────────
§10.7  GESTURE CONTROL MAP
───────────────────────────────────────────────────────────────────────────────

  DASHBOARD SCREEN

  Gesture                Target           Action
  ─────────────────────  ───────────────  ──────────────────────────────────
  Tap                    Price card       Open Symbol Detail screen
  Long press             Price card       Open Quick Alert sheet (pre-filled)
  Double tap             Price card       Toggle card expanded/compact
  Swipe left             Price card       Deactivate symbol (unsubscribe)
  Swipe right            Price card       Re-activate symbol
  Tap                    Status bar       Open Connection Diagnostics
  Long press             Status bar       Copy connection status text
  Swipe down (tab)       Any             Pull-to-refresh / reconnect
  Tap                    FAB             Speed Dial open/close
  Tap                    FAB → Add Sym   Open Symbol Management screen
  Tap                    FAB → Quick Al  Open Quick Alert sheet
  Long press             Any card        Enter drag-to-reorder mode

  ALERTS SCREEN

  Gesture                Target           Action
  ─────────────────────  ───────────────  ──────────────────────────────────
  Tap                    Alert row        Open Alert Detail screen
  Long press             Alert row        Enter multi-select mode
  Swipe right            Alert row        Toggle Active / Deactivated
  Swipe left             Alert row        Delete (with confirmation)
  Tap                    Search icon      Expand search bar
  Tap                    Filter icon      Open filter bottom sheet
  Tap                    FAB              Open full Alert Creation screen

  SETTINGS SCREEN

  Gesture                Target           Action
  ─────────────────────  ───────────────  ──────────────────────────────────
  Tap                    Group header     Expand / collapse group
  Tap                    Setting item     Activate (toggle / open sub-screen)
  Long press             Version number   Copy version string to clipboard

───────────────────────────────────────────────────────────────────────────────
§10.8  MICRO-INTERACTION CATALOGUE
───────────────────────────────────────────────────────────────────────────────

  Micro-interaction           Trigger              Feedback
  ──────────────────────────  ───────────────────  ────────────────────────────
  Price digit roll            Tick change          Digits scroll up/down (opt.)
  Alert badge appear          New alert fires      Badge scales in (bounce)
  Alert badge clear           Alert dismissed      Badge fades out
  Quick Alert sheet open      Long press card      Sheet rises + haptic tick
  Quick Alert create success  Button tap           ✓ checkmark + snackbar
  Alert toggle (swipe right)  Swipe gesture        Colour transition Active→Grey
  Alert delete confirm        Swipe left + confirm Card animates out (slide)
  FAB speed dial              Tap FAB              Options fan out (stagger)
  Settings toggle ON          Switch tap           Switch slides → haptic click
  Settings toggle OFF         Switch tap           Switch slides → haptic click
  Price Update field change   Edit field           Live "Applying…" indicator
  Theme switch                Chip tap             Full-screen crossfade
  Pause subscription          Pause button tap     Status bar dims → "PAUSED"
  Connection restored         Auto-reconnect       Status bar pulses green once
  API key validated           Validate button      Green checkmark animates in
  API key invalid             Validate result      Red X + shake animation

───────────────────────────────────────────────────────────────────────────────
§10.9  HAPTIC FEEDBACK MATRIX
───────────────────────────────────────────────────────────────────────────────

  Event                            Haptic Pattern
  ───────────────────────────────  ──────────────────────────────────────────
  Long press on card               HapticFeedbackConstants.LONG_PRESS
  Quick Alert sheet opens          HapticFeedbackConstants.VIRTUAL_KEY
  Alert created successfully       VibrationEffect: short click (40ms, 200amp)
  Settings toggle                  HapticFeedbackConstants.CLOCK_TICK
  Swipe action reveal              HapticFeedbackConstants.TEXT_HANDLE_MOVE
  Delete confirmation gesture      VibrationEffect: double pulse
  Alert fires — Default            Per alert vibration config
  Alert fires — Alarm              Urgent: 0,500,200,500,200,800 (waveform)
  Alert fires — Virtual Call       Urgent: same as Alarm
  Alert fires — Priority Call      Urgent: same + AUDIOFOCUS escalation
  Error / invalid input            HapticFeedbackConstants.REJECT  (API 34+)

───────────────────────────────────────────────────────────────────────────────
§10.10  FAST-PATH CONTROLS (ONE-THUMB OPERATION)
───────────────────────────────────────────────────────────────────────────────

  PRINCIPLE: Every primary trader action must be reachable in ≤ 2 gestures
  from any screen, with the dominant thumb, in portrait orientation.

  ACTION PATH MAP

  "Set an alert at the current price"
    ① Long press any price card on dashboard      (1 gesture, thumb zone)
    ② Tap "Create Alert" in Quick Alert sheet     (2 gestures total)
    Total: 2 gestures, ≤ 5 seconds.

  "See XAU price"
    ① Glance at dashboard (0 gestures — price is always visible)
    OR ① Pull notification shade (0 gestures — ticker notification)
    Total: 0 gestures.

  "Pause tracking to save data"
    ① Tap [❚❚] pause button in connection status bar  (1 gesture, top area)
    Total: 1 gesture.

  "Change price update speed"
    ① Tap Settings tab
    ② Tap "Price Update Interval" field in Data Source group
    ③ Type new value + dismiss keyboard
    Total: 3 gestures. (Settings → Data Source group is first group, expanded
    by default, minimising scroll.)

  "Dismiss an alert"
    ① Swipe any alert row → right on the Alerts screen   (1 gesture)
    Total: 1 gesture.

  "View triggered alert detail"
    ① Pull notification shade
    ② Tap notification "View Alert"
    Total: 2 gestures.

  THUMB ZONE COMPLIANCE
    Bottom navigation bar: thumb-zone — always accessible.
    FAB: bottom-right — thumb-zone.
    Pause button: top-right status bar — stretch zone (acceptable; infrequent).
    Settings groups: Data Source is first — minimal scroll required.

───────────────────────────────────────────────────────────────────────────────
§10.11  ACCESSIBILITY SPECIFICATION
───────────────────────────────────────────────────────────────────────────────

  VISUAL
  · All text meets WCAG AA contrast ratio minimum (4.5:1 for normal text,
    3:1 for large text/bold ≥18sp).
  · Price Up / Down colours pass WCAG AA on both light and dark themes
    (verified above in §06 colour table).
  · No information conveyed by colour alone — direction indicator ▲ / ▼ /
    text labels always accompany colour coding.
  · Minimum touch target: 48×48dp for all interactive elements.

  SCREEN READER (TalkBack)
  · All price cards have content descriptions:
    "XAU/USD, 2318.45, up 12.30 points, 0.53 percent, 3 seconds ago"
  · Alert rows: "XAU/USD crossing up 2320.00, CRITICAL, active, one-time"
  · Status bar: "Connection live, last update 320 milliseconds ago"
  · FAB: "Speed dial menu, open to add symbol or create quick alert"
  · Animated elements: contentDescription updates on each tick.

  REDUCE MOTION
  · Detected via MediaQuery.disableAnimations in Flutter.
  · All duration-based animations replaced with instant state changes.
  · Exception: price flash (120ms) retained even with Reduce Motion ON
    because it communicates data state, not decoration.

  FONT SCALE
  · All text uses sp units (scale-independent pixels).
  · Tested at 200% font scale. Layouts use flexible containers.
  · Price numbers clip at maximum width before wrapping (monospaced
    allows predictable overflow calculation).

  COLOUR BLIND MODES
  · Price up/down rely on both colour AND symbol (▲ ▼) — accessible.
  · No design decision depends on red/green distinction alone.

───────────────────────────────────────────────────────────────────────────────
§10.12  RESPONSIVE BEHAVIOUR
───────────────────────────────────────────────────────────────────────────────

  Device / Orientation          Layout
  ────────────────────────────  ──────────────────────────────────────────────
  Phone portrait (primary)      Bottom nav bar, 2-column card grid
  Phone landscape               1-column list auto-activates, wider price view
  Tablet portrait               3-column card grid, side rail navigation
  Tablet landscape              Master-detail: symbol list left, detail right

  BREAKPOINTS (Flutter LayoutBuilder)
  · Compact:   width < 600dp   — phone portrait
  · Medium:    600–840dp        — phone landscape / small tablet
  · Expanded:  > 840dp          — tablet


═══════════════════════════════════════════════════════════════════════════════
§11  APPLICATION ARCHITECTURE
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
§11.1  PATTERN
───────────────────────────────────────────────────────────────────────────────

  Clean Architecture with BLoC state management.
  Three layers: Domain → Data → Presentation.
  Dependency direction: inward only (Presentation depends on Domain,
  Data implements Domain interfaces, Presentation depends on Domain only).
  No business logic in Widget classes. No direct storage access from UI.

───────────────────────────────────────────────────────────────────────────────
§11.2  FLUTTER PACKAGE REGISTRY
───────────────────────────────────────────────────────────────────────────────

  Package                     Purpose
  ──────────────────────────  ────────────────────────────────────────────────
  flutter_bloc                State management — BLoC and Cubit patterns
  hive_flutter                Local storage: alerts, settings, symbol state
                              (sole write access: Background Isolate only)
  web_socket_channel          WebSocket connection to Twelve Data
  flutter_local_notifications All notification delivery (all 4 alert methods,
                              FGS notification, live ticker notification)
  workmanager                 Background watchdog — re-spawns service if dead
  permission_handler          Runtime permission management + status queries
  home_widget                 Android widget bridge (Flutter → native widget)
  wakelock_plus               CPU partial wake lock (held by FGS only)
  auto_start_flutter          Xiaomi/MIUI autostart permission helper
  audioplayers                Custom alert sounds
  get_it                      Dependency injection container
  freezed + json_serializable Immutable model classes + JSON serialisation
  go_router                   Type-safe navigation / routing
  google_fonts                JetBrains Mono + Inter typefaces
  dynamic_color               Material You dynamic colour (Android 12+)
  device_info_plus            Manufacturer detection for setup guidance
  flutter_secure_storage      Android Keystore-backed encrypted API key storage
  battery_optimization        Battery exemption request + status check
  shared_preferences          Lightweight key-value (non-sensitive settings)

  INTENTIONALLY EXCLUDED
  fl_chart     — removed (no chart feature)
  sqflite      — removed (Hive is sufficient for all remaining storage)

───────────────────────────────────────────────────────────────────────────────
§11.3  NATIVE ANDROID COMPONENTS (KOTLIN)
───────────────────────────────────────────────────────────────────────────────

  Component                Type                  Purpose
  ───────────────────────  ────────────────────  ──────────────────────────────
  PriceTrackerService      ForegroundService     WebSocket, alert engine host,
                                                 widget throttle, ticker notif.
  BootReceiver             BroadcastReceiver     Auto-start on BOOT_COMPLETED
                                                 and MY_PACKAGE_REPLACED
  VirtualCallActivity      Activity              Full-screen call overlay
                                                 (both screen-on/off paths)
  CallSimulationService    Service               CATEGORY_CALL delivery +
                                                 AudioFocus escalation (v4.0)
  SinglePriceWidget        AppWidgetProvider     2×1 single symbol widget
  MultiPriceWidget         AppWidgetProvider     4×2 multi-symbol widget
  CompactTickerWidget      AppWidgetProvider     4×1 compact ticker widget
  PermissionHelper         Utility class         canUseFullScreenIntent() guard
                                                 + SYSTEM_ALERT_WINDOW check

  All Flutter ↔ Native communication uses:
    MethodChannel  — command/response (commands from Flutter, storage IPC,
                     widget update triggers)
    EventChannel   — streaming (price tick stream to UI Isolate when alive)

───────────────────────────────────────────────────────────────────────────────
§11.4  PRODUCTION DATA FLOW (CANONICAL v4.0)
───────────────────────────────────────────────────────────────────────────────

  ┌─────────────────────────────────────────────────────────────────┐
  │  PriceTrackerService  (Android Foreground Service)              │
  │  · Always running while tracker is active                       │
  │  · Holds: CPU partial wake lock, FGS notification (1001)        │
  └─────────────────────────────────────────────────────────────────┘
        │
        ├──────────────────────────────────────────────────────┐
        ▼                                                      ▼
  ┌────────────────────────────┐              ┌────────────────────────────┐
  │  Headless Background       │              │  Native WebSocket Manager  │
  │  Flutter Engine (Isolate)  │              │  · Twelve Data WS primary  │
  │  · Dart AlertEngine        │◄─ onTick() ──│  · REST fallback at 5s     │
  │  · Sole Hive write owner   │  MethodCh.   │  · Auto-reconnect backoff  │
  │  · Notification fire path  │              │  · Heartbeat every 25s     │
  │  · Storage IPC handler     │              │  · Connectivity listener   │
  └────────────────────────────┘              └────────────────────────────┘
        │                                              │
        │  For each tick:                              │  priceCache[symbol]
        │  ① Evaluate all active alerts for symbol    │  updated in memory
        │  ② If crossing detected:                    │
        │     → fire notification (method-dependent)  │
        │     → if Priority Call: CallSimulationSvc   │
        │  ③ Write trigger record to Hive             │
        │                                             ─┤
        │                                ┌────────────┘
        │                                │  every 2 seconds (throttled)
        │                                ▼
        │                   ┌──────────────────────────────┐
        │                   │  Live Ticker Notification    │
        │                   │  Notification ID: 1002       │
        │                   │  Channel: price_ticker_live  │
        │                   │  Updated from priceCache     │
        │                   └──────────────────────────────┘
        │
        │                   ┌──────────────────────────────┐
        │                   │  Widget Throttle Manager     │
        ├──────────────────►│  every 5 seconds max (0.2Hz) │
        │                   │  AppWidgetManager batched IPC│
        │                   └──────────────────────────────┘
        │
        │  UI Render Throttle (user-configured: default 500ms)
        │  Gates EventChannel delivery to PriceBloc.
        │  [If UI Isolate is alive — app is open]
        └──► EventChannel → PriceBloc → Dashboard (price animations)
             UI death does not affect any path above this line.


═══════════════════════════════════════════════════════════════════════════════
§12  SCREEN INVENTORY  ← UPDATED v4.0
═══════════════════════════════════════════════════════════════════════════════

  #    Screen Name                Route / Access
  ───  ─────────────────────────  ──────────────────────────────────────────

  S1   Splash Screen              App launch (brief, then Setup Wizard or Home)
  S2   Setup Wizard               First launch only; 5 linear steps:
         Step 1: Welcome          — App intro, feature summary
         Step 2: API Key          — Enter + validate Twelve Data key
         Step 3: Symbol Select    — Choose active symbols (min 1)
         Step 4: Permissions      — Guided permission grants, mfr-aware
         Step 5: Ready            — Summary, Start FinTrace button
  S3   Home Dashboard             Tab: 📈 Prices (primary home screen)
  S4   Symbol Detail              Tap any price card from S3
  S5   Alert List                 Tab: 🔔 Alerts
  S6   Create / Edit Alert        FAB on S5, or long-press card on S3
  S7   Alert Detail               Tap any alert row on S5
  S8   Settings                   Tab: ⚙ Settings
  S9   API Key Management         Settings → Data Source → Manage API Key
  S10  Live Ticker Symbols        Settings → Notifications → Live Ticker Symbols
  S11  Permission Helper          Settings → About → Permissions
  S12  Connection Diagnostics     Settings → Data Source → Diagnostics
  S13  Widget Configuration       Launcher widget long-press → configure
  S14  About This App             Settings → About → "About This App"       ← NEW
  S14B About the Developer        Settings → About → "About the Developer"  ← NEW


═══════════════════════════════════════════════════════════════════════════════
§13  PERMISSIONS REGISTRY  ← UPDATED v4.0
═══════════════════════════════════════════════════════════════════════════════

PHILOSOPHY
  · Never batch-request all permissions at once.
  · Every permission is explained in plain language before the system dialog.
  · Consequences of denying each permission are stated honestly.
  · Optional permissions: app functions without them (degraded mode described).
  · Battery exemption is a hard prerequisite. All others are either
    auto-granted (manifest) or contextually requested.

REQUIRED PERMISSIONS

  Permission                             Declared    Requested When
  ─────────────────────────────────────  ──────────  ──────────────────────────
  INTERNET                               Manifest    Auto (never shown to user)
  FOREGROUND_SERVICE                     Manifest    Auto
  FOREGROUND_SERVICE_DATA_SYNC           Manifest    Auto
  WAKE_LOCK                              Manifest    Auto
  VIBRATE                                Manifest    Auto
  RECEIVE_BOOT_COMPLETED                 Manifest    Setup Wizard Step 4
  POST_NOTIFICATIONS  (Android 13+)      Runtime     Setup Wizard Step 4
  REQUEST_IGNORE_BATTERY_OPTIMIZATIONS   Runtime     Setup Wizard Step 4
                                                     ← HARD PREREQUISITE:
                                                       service will not start
                                                       until granted

OPTIONAL PERMISSIONS

  Permission                             Purpose                When Requested
  ─────────────────────────────────────  ─────────────────────  ────────────────────────────────
  USE_FULL_SCREEN_INTENT                 Alarm & Virtual Call   When user first selects Alarm
                                         full-screen overlay    or Virtual Call as alert method
  SYSTEM_ALERT_WINDOW                    Virtual Call overlay   When user first selects Virtual
                                         on active screen       Call or Priority Call method

EXPLICITLY NOT REQUESTED

  Permission                             Reason
  ─────────────────────────────────────  ────────────────────────────────────────
  ACCESS_NOTIFICATION_POLICY             Enables DND override — never used
  READ_CONTACTS / CAMERA / LOCATION      Completely irrelevant to app function
  READ_PHONE_STATE                       Not needed
  Any SMS or telephony permissions       Virtual Call is a UI overlay, not a call
  STREAM_ALARM usage                     Would bypass DND — never used
  CALL_PHONE                             Not used — Priority Call is an overlay,
                                         not a real phone call


═══════════════════════════════════════════════════════════════════════════════
§14  PROJECT FILE STRUCTURE  ← UPDATED v4.0
═══════════════════════════════════════════════════════════════════════════════

  fintrace/
  ├── android/
  │   ├── app/
  │   │   └── src/main/
  │   │       ├── kotlin/com/fintrace/
  │   │       │   ├── MainActivity.kt
  │   │       │   ├── PriceTrackerService.kt        FGS: WS, alert host,
  │   │       │   │                                 widget throttle, ticker notif
  │   │       │   ├── BootReceiver.kt               BOOT_COMPLETED handler
  │   │       │   ├── VirtualCallActivity.kt        Full-screen call overlay
  │   │       │   ├── CallSimulationService.kt      Priority Call: CATEGORY_CALL
  │   │       │   │                                 + AudioFocus escalation (v4.0)
  │   │       │   ├── PermissionHelper.kt           FSI guard + SYSTEM_ALERT_WINDOW
  │   │       │   └── widget/
  │   │       │       ├── SinglePriceWidget.kt      2×1 widget provider
  │   │       │       ├── MultiPriceWidget.kt       4×2 widget provider
  │   │       │       └── CompactTickerWidget.kt    4×1 widget provider
  │   │       ├── res/
  │   │       │   ├── layout/
  │   │       │   │   ├── widget_single.xml
  │   │       │   │   ├── widget_multi.xml
  │   │       │   │   └── widget_ticker.xml
  │   │       │   └── xml/
  │   │       │       ├── widget_single_info.xml
  │   │       │       ├── widget_multi_info.xml
  │   │       │       └── widget_ticker_info.xml
  │   │       └── AndroidManifest.xml
  │   └── build.gradle
  │
  ├── lib/
  │   ├── core/
  │   │   ├── constants/
  │   │   │   ├── app_constants.dart               Intervals, IDs, limits
  │   │   │   │                                    PRICE_UPDATE_INTERVAL_DEFAULT = 500
  │   │   │   │                                    PRICE_UPDATE_INTERVAL_MIN = 100
  │   │   │   ├── symbols.dart                     14 supported symbols
  │   │   │   └── api_endpoints.dart               Twelve Data WS + REST URLs
  │   │   ├── errors/
  │   │   │   └── failures.dart                    Typed failure classes
  │   │   └── utils/
  │   │       ├── price_formatter.dart             Decimal places per symbol
  │   │       └── date_utils.dart                  Human-readable durations
  │   │
  │   ├── data/
  │   │   ├── datasources/
  │   │   │   ├── twelvedata_websocket.dart        WS: connect, subscribe, hb
  │   │   │   └── twelvedata_rest.dart             REST fallback polling
  │   │   ├── models/
  │   │   │   ├── price_model.dart
  │   │   │   ├── alert_model.dart
  │   │   │   └── symbol_model.dart
  │   │   └── repositories/
  │   │       ├── price_repository_impl.dart
  │   │       └── alert_repository_impl.dart       Write path: BG Isolate only
  │   │
  │   ├── domain/
  │   │   ├── entities/
  │   │   │   ├── price.dart
  │   │   │   ├── alert.dart
  │   │   │   └── symbol.dart
  │   │   ├── repositories/
  │   │   │   ├── i_price_repository.dart
  │   │   │   └── i_alert_repository.dart
  │   │   └── usecases/
  │   │       ├── watch_prices.dart
  │   │       ├── create_alert.dart
  │   │       ├── update_alert.dart
  │   │       ├── delete_alert.dart
  │   │       └── evaluate_alerts.dart
  │   │
  │   ├── presentation/
  │   │   ├── blocs/
  │   │   │   ├── price/
  │   │   │   │   ├── price_bloc.dart
  │   │   │   │   ├── price_event.dart
  │   │   │   │   └── price_state.dart
  │   │   │   ├── alert/
  │   │   │   │   ├── alert_bloc.dart
  │   │   │   │   ├── alert_event.dart
  │   │   │   │   └── alert_state.dart
  │   │   │   └── connection/
  │   │   │       └── connection_cubit.dart
  │   │   │
  │   │   ├── screens/
  │   │   │   ├── splash/
  │   │   │   │   └── splash_screen.dart
  │   │   │   ├── setup_wizard/
  │   │   │   │   ├── setup_wizard_screen.dart
  │   │   │   │   ├── step_welcome.dart
  │   │   │   │   ├── step_api_key.dart
  │   │   │   │   ├── step_symbols.dart
  │   │   │   │   ├── step_permissions.dart
  │   │   │   │   └── step_ready.dart
  │   │   │   ├── home/
  │   │   │   │   ├── home_screen.dart
  │   │   │   │   ├── price_card.dart
  │   │   │   │   ├── mini_ticker_strip.dart        Horizontal ticker strip (v4.0)
  │   │   │   │   └── connection_status_bar.dart
  │   │   │   ├── symbol_detail/
  │   │   │   │   └── symbol_detail_screen.dart    Price + alerts only; no chart
  │   │   │   ├── alerts/
  │   │   │   │   ├── alert_list_screen.dart
  │   │   │   │   ├── create_alert_screen.dart
  │   │   │   │   ├── quick_alert_sheet.dart        New: 3-field bottom sheet
  │   │   │   │   └── alert_detail_screen.dart
  │   │   │   ├── settings/
  │   │   │   │   ├── settings_screen.dart
  │   │   │   │   ├── api_key_screen.dart
  │   │   │   │   ├── ticker_symbols_screen.dart   Live Ticker Notification config
  │   │   │   │   ├── permission_helper_screen.dart
  │   │   │   │   ├── connection_diagnostics_screen.dart
  │   │   │   │   ├── about_app_screen.dart         New: About This App (v4.0)
  │   │   │   │   └── about_developer_screen.dart   New: About Developer (v4.0)
  │   │   │   └── virtual_call/
  │   │   │       └── virtual_call_screen.dart      Call overlay UI (Flutter side)
  │   │   │
  │   │   ├── widgets/
  │   │   │   ├── price_change_badge.dart
  │   │   │   ├── alert_row_tile.dart
  │   │   │   ├── sparkline_widget.dart            20-tick sparkline (custom canvas)
  │   │   │   ├── connection_chip.dart
  │   │   │   ├── permission_card.dart
  │   │   │   ├── speed_dial_fab.dart              New: Speed Dial FAB (v4.0)
  │   │   │   └── price_update_interval_field.dart New: Settings ms input (v4.0)
  │   │   │
  │   │   └── theme/
  │   │       ├── app_theme.dart                   buildLight() + buildDark()
  │   │       ├── color_tokens.dart                Semantic colour constants
  │   │       └── text_theme.dart                  Type scale
  │   │
  │   ├── services/
  │   │   ├── background_alert_entry.dart          @pragma vm:entry-point
  │   │   │                                        Headless engine entry point
  │   │   ├── alert_engine.dart                    Crossing evaluation logic
  │   │   │                                        Runs in Background Isolate
  │   │   ├── storage_ipc_channel.dart             MethodChannel handler:
  │   │   │                                        UI → BG Isolate storage IPC
  │   │   ├── notification_service.dart            All 5 notification channels
  │   │   ├── call_simulation_service.dart         New: Priority Call delivery
  │   │   ├── foreground_service_channel.dart      MethodChannel: Flutter → FGS
  │   │   └── widget_channel.dart                  MethodChannel: Flutter → widgets
  │   │
  │   └── main.dart
  │
  ├── test/
  │   ├── alert_engine_test.dart                   Crossing logic unit tests
  │   ├── alert_condition_edge_cases_test.dart     Gap / reconnect edge cases
  │   ├── price_formatter_test.dart
  │   ├── websocket_manager_test.dart
  │   ├── price_update_interval_test.dart          New: interval validation tests
  │   └── call_simulation_test.dart               New: audio focus + overlay tests
  │
  ├── pubspec.yaml
  └── README.md


═══════════════════════════════════════════════════════════════════════════════
§15  BUILD & SIDELOAD GUIDE
═══════════════════════════════════════════════════════════════════════════════

PREREQUISITES
  Flutter 3.22+    (check: flutter --version)
  Android SDK 34+
  Java 17+
  Android device with USB Debugging enabled, or use ADB over Wi-Fi

STEP 1 — Generate Signing Keystore (one-time only)

  keytool -genkey -v \
    -keystore fintrace_key.jks \
    -keyalg RSA -keysize 2048 -validity 10000 \
    -alias fintrace \
    -storepass YOUR_STORE_PASSWORD \
    -keypass YOUR_KEY_PASSWORD

  Store the .jks file securely. Do not commit it to version control.

STEP 2 — Configure android/key.properties

  storePassword=YOUR_STORE_PASSWORD
  keyPassword=YOUR_KEY_PASSWORD
  keyAlias=fintrace
  storeFile=../fintrace_key.jks

STEP 3 — Build Release APK

  flutter clean
  flutter pub get
  flutter build apk --release --split-per-abi

  Output location: build/app/outputs/flutter-apk/

    app-arm64-v8a-release.apk      ← Use for Redmi Note 10 Pro and all
                                      modern 64-bit Android phones
    app-armeabi-v7a-release.apk    ← Older 32-bit devices
    app-x86_64-release.apk         ← Android emulator only

STEP 4A — Install via ADB (USB or Wi-Fi)

  adb install -r build/app/outputs/flutter-apk/app-arm64-v8a-release.apk

STEP 4B — Sideload via File Transfer

  1. Copy app-arm64-v8a-release.apk to phone internal storage.
  2. On phone: Settings → Security → Install unknown apps.
  3. Allow your file manager app to install unknown apps.
  4. Open the APK from your file manager and tap Install.

  Redmi Note 10 Pro note: MIUI may show a "Verification required" dialog.
  Tap "Install anyway" or allow via "Package installer" permission.
  After install, open the MIUI Security app and grant FinTrace Autostart.


═══════════════════════════════════════════════════════════════════════════════
§16  ROADMAP
═══════════════════════════════════════════════════════════════════════════════

  v1.0 — Foundation
    · Live prices: 14 symbols via Twelve Data WebSocket
    · Foreground Service with FGS ticker notification (Notification ID 1001)
    · Permanent Live Ticker Notification (Notification ID 1002, 1–5 symbols)
    · API key management (enter, validate, update, Keystore storage)
    · 3 theme modes: Light / Dark AMOLED / System Adaptive
    · Symbol activate/deactivate with live subscription management
    · Basic alert creation — Default Notification method only
    · Single and Multi-symbol home screen widgets (Types 1 and 2)
    · Setup Wizard with manufacturer-specific permission guidance
    · Battery exemption enforcement (hard prerequisite)
    · Boot auto-start
    · Price Update Interval setting (user-configurable ms, default 500)
    · About This App screen and About Developer screen

  v1.1 — Full Alert System
    · Alert methods: Alarm + Virtual Call + Priority Call
    · Android 14 canUseFullScreenIntent() runtime guard
    · Dual-path Virtual Call overlay (TYPE_APPLICATION_OVERLAY)
    · Priority Call: CATEGORY_CALL + AudioFocus escalation
    · Alert list with swipe actions (activate/deactivate, delete)
    · Batch actions (activate/deactivate/delete all or selected)
    · Search and filter alerts
    · Alert trigger history per alert
    · Alert statistics summary
    · Speed Dial FAB with Quick Alert sheet

  v1.2 — Polish & Completion
    · Compact Ticker Widget (Type 3 — 4×1)
    · Symbol Detail screen — bid/ask/spread, 24h High/Low
    · Sparkline implementation (custom canvas — no fl_chart)
    · Mini Ticker Strip on dashboard
    · Connection Diagnostics screen
    · Alert import / export as JSON backup file
    · Reduce Motion accessibility support

  v1.3 — Refinement
    · Tablet layout (master-detail for landscape)
    · Full performance profiling pass
    · Dark/Light theme polish pass
    · Edge case hardening (network transition, rapid alert creation)


═══════════════════════════════════════════════════════════════════════════════
§A   APPENDIX A — WEBSOCKET PROTOCOL REFERENCE (TWELVE DATA)
═══════════════════════════════════════════════════════════════════════════════

CONNECT
  wss://ws.twelvedata.com/v1/quotes/price?apikey=YOUR_KEY

SUBSCRIBE (sent after connection, for all active symbols)
  {
    "action": "subscribe",
    "params": {
      "symbols": "XAU/USD,XAG/USD,EUR/USD,GBP/USD,USD/JPY,USD/CHF,
                  AUD/USD,USD/CAD,NZD/USD,EUR/GBP,EUR/JPY,GBP/JPY,
                  EUR/AUD,GBP/AUD"
    }
  }

UNSUBSCRIBE (sent when user deactivates a symbol — no reconnect needed)
  {
    "action": "unsubscribe",
    "params": { "symbols": "GBP/AUD" }
  }

INCOMING — PRICE TICK
  {
    "event": "price",
    "symbol": "XAU/USD",
    "price": "2318.4500",
    "day_volume": 142000,
    "timestamp": 1717000000,
    "type": "Precious Metal"
  }

OUTGOING — HEARTBEAT (every 25 seconds)
  { "action": "heartbeat" }

INCOMING — HEARTBEAT RESPONSE
  { "event": "heartbeat" }

INCOMING — SUBSCRIBE CONFIRMATION
  {
    "event": "subscribe-status",
    "status": "ok",
    "success": ["XAU/USD", "EUR/USD"],
    "fails": []
  }

INCOMING — ERROR
  {
    "event": "error",
    "message": "Invalid apikey",
    "status": "error",
    "code": 401
  }

  Code 401 → invalid or expired key → show API Key Management screen
  Code 429 → quota exceeded → show upgrade prompt + REST fallback
  Any other error → log, attempt reconnect after backoff


═══════════════════════════════════════════════════════════════════════════════
§B   APPENDIX B — ALERT EVALUATION PSEUDOCODE
═══════════════════════════════════════════════════════════════════════════════

  // Runs in the Background Isolate (headless engine)
  // Called on every WebSocket price tick delivered via MethodChannel
  // Complexity: O(n) where n = active alerts for this symbol
  // Storage access: Background Isolate is sole writer

  void evaluateAlerts(
    String symbol,
    double prevPrice,      // last cached price before this tick
    double currentPrice,   // this tick's price
    DateTime tickTime,
  ) {
    final alerts = alertRepository.getActive(symbol);

    for (final alert in alerts) {

      // Skip if currently in cooldown
      if (alert.cooldownUntil != null &&
          tickTime.isBefore(alert.cooldownUntil!)) continue;

      // Skip if expired
      if (alert.expiry != null && tickTime.isAfter(alert.expiry!)) {
        alertRepository.setStatus(alert.id, AlertStatus.expired);
        continue;
      }

      bool triggered = false;
      switch (alert.condition) {
        case AlertCondition.crossing:
          triggered =
            (prevPrice < alert.target && currentPrice >= alert.target) ||
            (prevPrice > alert.target && currentPrice <= alert.target);
        case AlertCondition.crossingUp:
          triggered =
            prevPrice < alert.target && currentPrice >= alert.target;
        case AlertCondition.crossingDown:
          triggered =
            prevPrice > alert.target && currentPrice <= alert.target;
      }

      if (!triggered) continue;

      // Fire the alert — method determines delivery path
      switch (alert.method) {
        case AlertMethod.defaultNotification:
        case AlertMethod.alarm:
        case AlertMethod.virtualCall:
          notificationService.fire(alert, currentPrice, tickTime);
        case AlertMethod.priorityCall:            // NEW v4.0
          callSimulationService.fire(alert, currentPrice, tickTime);
      }

      // Record trigger
      alertRepository.recordTrigger(alert.id, currentPrice, tickTime);

      // Lifecycle
      if (alert.isOneTime) {
        alertRepository.setStatus(alert.id, AlertStatus.triggered);
      } else if (alert.hasCooldown) {
        alertRepository.setCooldownUntil(
          alert.id, tickTime.add(alert.cooldownDuration));
      }
    }
  }

  NOTE ON GAP HANDLING:
  prevPrice is the last value stored in priceCache[symbol] before this tick.
  On reconnect after a connection gap, prevPrice = last price before
  disconnect. The first tick after reconnect evaluates against that price,
  meaning any crossing that occurred during the gap is detected on the
  first tick back. No crossing is silently missed due to connectivity loss.


═══════════════════════════════════════════════════════════════════════════════
§C   APPENDIX C — NOTIFICATION CHANNEL REGISTRY  ← UPDATED v4.0 (5 channels)
═══════════════════════════════════════════════════════════════════════════════

  Five channels. Each has a distinct role, importance level, and DND behaviour.

  ─────────────────────────────────────────────────────────────────────────────
  ID: price_ticker_fgs
  Name: FinTrace Service
  Importance: MIN (API 26+ minimum required for FGS visibility)
  Sound: None  ·  Vibration: None  ·  Heads-up: No
  Purpose: Mandatory Foreground Service notification (always present while
           tracker is active). Shows connection status + price summary.
  Dismissable: No (tied to FGS lifecycle)
  DND effect: Visible in shade (MIN importance — no interruption generated)
  ─────────────────────────────────────────────────────────────────────────────
  ID: price_ticker_live
  Name: Live Price Ticker
  Importance: LOW
  Sound: None  ·  Vibration: None  ·  Heads-up: No
  Purpose: Permanent Live Ticker Notification (user-controlled; shows 1–5
           symbols with live prices, updated every 2 seconds).
  Dismissable: No (re-posted if dismissed, while feature is enabled)
  DND effect: Visible in shade (LOW importance — no interruption generated)
  ─────────────────────────────────────────────────────────────────────────────
  ID: price_alert_default
  Name: Price Alerts
  Importance: HIGH
  Sound: Yes (STREAM_NOTIFICATION)  ·  Vibration: Yes  ·  Heads-up: Yes
  Purpose: Standard price alert notifications (Default Notification method).
  Dismissable: Yes
  DND effect: Fully suppressed when DND is ON
  canBypassDnd: false  (explicitly)
  ─────────────────────────────────────────────────────────────────────────────
  ID: price_alert_alarm
  Name: Priority Price Alerts
  Importance: MAX
  Sound: Yes (STREAM_NOTIFICATION — NOT STREAM_ALARM)
  Vibration: Yes (urgent pattern)  ·  Heads-up: Yes  ·  Full-screen: Yes
  Purpose: Alarming Notification and Virtual Call alert methods.
  Dismissable: No (persistent until explicit user dismissal)
  DND effect: Fully suppressed when DND is ON
  canBypassDnd: false  (explicitly)
  Note: MAX importance = highest visual priority when DND is OFF.
        It does not grant DND bypass rights. DND is always respected.
  ─────────────────────────────────────────────────────────────────────────────
  ID: price_alert_call_simulation                                       ← NEW
  Name: Price Alert — Priority Call
  Importance: MAX
  Sound: Yes (STREAM_NOTIFICATION — NOT STREAM_ALARM)
  Vibration: Yes (urgent waveform pattern)  ·  Heads-up: Yes
  Full-screen: Yes  ·  Category: CATEGORY_CALL
  AudioFocus: AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE (requested separately)
  Purpose: Priority Call alert method. CATEGORY_CALL gives this notification
           OS-level telephony priority, rendering above WhatsApp, Instagram,
           and social apps in the notification dispatch pipeline.
           AudioFocus escalation ducks other app audio (WA call, IG video).
  Dismissable: No (persistent until explicit user dismissal)
  DND effect: Fully suppressed when DND is ON
  canBypassDnd: false  (explicitly — DND is always fully respected)
  Requires permissions: USE_FULL_SCREEN_INTENT + SYSTEM_ALERT_WINDOW
  OEM caveat: MIUI Focus Mode may suppress this channel. User guidance
              shown in Permission Helper if Xiaomi device detected.
  ─────────────────────────────────────────────────────────────────────────────


═══════════════════════════════════════════════════════════════════════════════
§D   APPENDIX D — ABOUT THIS APP & DEVELOPER INFORMATION  ← NEW v4.0
═══════════════════════════════════════════════════════════════════════════════

───────────────────────────────────────────────────────────────────────────────
ABOUT THIS APP SCREEN  (S14)
───────────────────────────────────────────────────────────────────────────────

  Screen route: /settings/about-app
  Accessible from: Settings → About → About This App

  LAYOUT:

  ┌──────────────────────────────────────────────────────────────────────────┐
  │  ← About FinTrace                                                        │
  │                                                                          │
  │       ┌──────────────────────────────┐                                   │
  │       │        [FinTrace Logo]        │                                   │
  │       │      FinTrace  v4.0           │                                   │
  │       │   Real-Time Price Monitor     │                                   │
  │       └──────────────────────────────┘                                   │
  │                                                                          │
  │  ─── About ─────────────────────────────────────────────────────────    │
  │                                                                          │
  │  FinTrace is a personal-grade real-time financial price monitoring       │
  │  and alert system for Android. Built for individual traders who need     │
  │  sub-second price updates and reliable alerts under all device states.   │
  │                                                                          │
  │  ─── Technical Details ─────────────────────────────────────────────    │
  │                                                                          │
  │  Version          4.0 (build 40)                                         │
  │  Build date       June 2026                                              │
  │  Platform         Flutter 3.22+ · Android API 26–35                     │
  │  UI Framework     Material You 3                                         │
  │  Data Provider    Twelve Data WebSocket API                              │
  │  Architecture     Clean Architecture · BLoC · Headless Engine           │
  │  Storage          Hive (encrypted) · Android Keystore                   │
  │  Scope            Local / Individual Use                                 │
  │                   Not for Google Play publication                        │
  │                                                                          │
  │  ─── Supported Symbols ─────────────────────────────────────────────    │
  │                                                                          │
  │  XAU/USD  XAG/USD  EUR/USD  GBP/USD  USD/JPY  USD/CHF                  │
  │  AUD/USD  USD/CAD  NZD/USD  EUR/GBP  EUR/JPY  GBP/JPY                  │
  │  EUR/AUD  GBP/AUD                                                       │
  │                                                                          │
  │  ─── Open Source Acknowledgements ─────────────────────────────────    │
  │                                                                          │
  │  · Flutter — Google Inc. (BSD 3-Clause)                                 │
  │  · Material You Design — Google Inc.                                    │
  │  · flutter_bloc — Felix Angelov (MIT)                                   │
  │  · JetBrains Mono — JetBrains (OFL)                                    │
  │  · Inter — Rasmus Andersson (OFL)                                       │
  │                                                                          │
  │  [  Copy Version  ]        [  Open Twelve Data Docs  ]                  │
  │                                                                          │
  └──────────────────────────────────────────────────────────────────────────┘

───────────────────────────────────────────────────────────────────────────────
ABOUT THE DEVELOPER SCREEN  (S14B)
───────────────────────────────────────────────────────────────────────────────

  Screen route: /settings/about-developer
  Accessible from: Settings → About → About the Developer

  LAYOUT:

  ┌──────────────────────────────────────────────────────────────────────────┐
  │  ← About the Developer                                                   │
  │                                                                          │
  │       ┌──────────────────────────────┐                                   │
  │       │  ┌─────┐                     │                                   │
  │       │  │  PK │  Praveen Kumar      │                                   │
  │       │  └─────┘  Developer          │                                   │
  │       └──────────────────────────────┘                                   │
  │                                                                          │
  │  ─── Developer ────────────────────────────────────────────────────    │
  │                                                                          │
  │  Name               Praveen Kumar                                        │
  │  Contact            praveens12346@gmail.com                              │
  │                                                                          │
  │  ─── Project Credits ───────────────────────────────────────────────    │
  │                                                                          │
  │  Coding Tool        Antigravity                                          │
  │  AI Model           Claude (Anthropic)                                   │
  │  Blueprint Version  v4.0 — Production Release                           │
  │  Design System      Material You 3                                       │
  │  Primary Language   Dart (Flutter) + Kotlin                             │
  │                                                                          │
  │  ─── Message ────────────────────────────────────────────────────────   │
  │                                                                          │
  │  FinTrace was built to solve a real need: reliable, always-on price     │
  │  alerts for active traders. Every design decision prioritises the        │
  │  trader's workflow — data first, reliability always, never intrusive.    │
  │                                                                          │
  │  If you have questions or feedback:                                      │
  │                                                                          │
  │  [  ✉  Email Developer  ]  → opens mail client with pre-filled address  │
  │     praveens12346@gmail.com                                              │
  │                                                                          │
  └──────────────────────────────────────────────────────────────────────────┘

  BEHAVIOUR:
  · "Email Developer" tap: opens default email app with
      To: praveens12346@gmail.com
      Subject: "FinTrace v4.0 Feedback"
    Pre-fills device info and app version in the body automatically.

  · "PK" avatar: a simple circular monogram avatar, Material You themed.

  · All text is selectable and copyable (long press).

  · Long press on version string: copies full version info to clipboard,
    shows toast "Version info copied".


───────────────────────────────────────────────────────────────────────────────
  FinTrace Blueprint v4.0 — Final Production Release
  Praveen Kumar · June 2026
  Coding Tool: Antigravity · Model: Claude (Anthropic)
  Contact: praveens12346@gmail.com
  ─────────────────────────────────────────────────────────────────────
  Flutter 3.22+ · Material You 3 · Twelve Data WebSocket · API 26–35
  Local / Individual Use · Not for Google Play publication
  DND fully respected — no override, no bypass, no exceptions, ever
  Architecture: Headless BG Engine · 5s Widget Throttle · Single-Writer Hive
  Alert delivery: 4 methods incl. Priority Call (WhatsApp/Instagram override)
  Price Update Interval: user-configurable (default 500ms, min 100ms)
───────────────────────────────────────────────────────────────────────────────
