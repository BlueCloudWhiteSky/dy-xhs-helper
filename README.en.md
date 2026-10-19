# Yanghao Helper | AutoJs6 Android Automation

[简体中文](./README.md) | **English**

**An Android operations assistant for Xiaohongshu, Douyin and WeChat Channels.**

Configure keywords, browsing modes, interaction rules and schedules on your phone. Individuals can use device-local settings, while teams can manage devices and rules through a web dashboard.

The Android client is based on **AutoJs6** and uses **Auto.js**-style JavaScript scripts to organize task execution. End users can install the packaged APK and configure it through the app.

[Website](https://rpa.yangcongyingyang.com/) · [Download APK](https://download.yangcongyingyang.com/rpa/%E5%85%BB%E5%8F%B7%E5%8A%A9%E6%89%8B_v3.0.0.apk) · [Installation](#download-and-installation) · [Contact](#contact)

A first-time **24-hour free trial** is available when the service is enabled and the device is eligible. Availability, eligibility and remaining time are determined by the app's online verification.

This is the English documentation. The app uses Chinese interface labels; key labels are included below to help you follow the steps.

## Contents

- [Use cases](#use-cases)
- [Features](#features)
- [AutoJs6 and Auto.js](#autojs6-and-autojs)
- [Supported platforms](#supported-platforms)
- [Download and installation](#download-and-installation)
- [Usage guide](#usage-guide)
- [Trial and activation](#trial-and-activation)
- [Troubleshooting](#troubleshooting)
- [Permissions and data](#permissions-and-data)
- [Disclaimer](#disclaimer)
- [Contact](#contact)
- [Related keywords](#related-keywords)

## Use cases

Yanghao Helper supports repetitive browsing tasks, keyword-based content filtering and configuration of multiple Android devices.

- **Individual use**: Save separate settings for each platform, schedule tasks and check execution status on your phone.
- **Content browsing and filtering**: Browse supported home, recommendation or search views with keyword matching.
- **Team operations**: Use enterprise online mode to configure rules, assign them to devices, schedule tasks and review operation records.

Before use, confirm your right to use the account and device, as well as whether the platform permits the intended actions. See the [disclaimer](#disclaimer).

## Features

- **Three platform entries**: Select Xiaohongshu, Douyin or WeChat Channels in one app, with separate settings for each.
- **Keyword filtering**: Match content by keywords in supported home, recommendation and search views.
- **Configurable interactions**: Set probabilities for likes, comments and other supported actions. A value of `0` disables an action; favorites support varies by platform.
- **Scheduled execution**: Select running days and time windows for task execution.
- **Status and records**: Check execution status, logs and operation records to review task behavior.
- **Enterprise management**: Manage devices, rules and authorization through a web dashboard, depending on the activated service type.

## AutoJs6 and Auto.js

The Android client uses **AutoJs6** as its project runtime and development baseline. JavaScript scripts, accessibility services and UI layouts organize automation tasks. AutoJs6 is also commonly written as **Auto.js 6** or **autojs6**; related technology topics include **Auto.js**, **AutoJS**, **autojs** and **Android automation**.

- **APK users**: Install the packaged Android application, then configure permissions, rules and activation as described below. You do not need to set up a script development environment yourself.
- **Script development and integration**: The client is organized as an AutoJs6 project. Compatibility with other Auto.js versions or forks requires separate verification.
- **Execution**: Android accessibility services perform assisted operations. WeChat Channels also requires system screen-capture permission. Enterprise online mode adds web-based device and task management.

## Supported platforms

| Platform | Browsing modes and purpose | Configurable interactions | Compatibility reference |
| --- | --- | --- | --- |
| Xiaohongshu / REDnote | Browse image and video posts from home and search views; filter by keywords | Likes, comments, favorites | Xiaohongshu `9.50.0` |
| Douyin | Browse videos from home and search views; match keywords | Likes, comments | Douyin `40.1.0` |
| WeChat Channels | Browse recommendation and video search views; match title keywords | Likes, comments, favorites | Runs inside WeChat; screen-capture permission required |

Each device can run only one platform at a time. Supported versions may change with product updates. Follow the app's **App version check (应用版本检测)** and the notes supplied with your release. Matching a version number does not establish compatibility with every phone, Android version or page layout.

## Download and installation

### 1 Download the Android APK

Open one of these links in your Android phone's browser:

- [Website download section](https://rpa.yangcongyingyang.com/#download)
- [Download Yanghao Helper v3.0.0](https://download.yangcongyingyang.com/rpa/%E5%85%BB%E5%8F%B7%E5%8A%A9%E6%89%8B_v3.0.0.apk)
- [Website installation guide in Chinese](https://rpa.yangcongyingyang.com/guide)

If downloading inside WeChat fails, use its menu to open the link in your system browser. Use the website download section for future updates.

### 2 Install the assistant

Open the downloaded APK and follow Android's installation prompts. If Android blocks installation from this source, grant installation permission to the browser or file manager used for this download. You can disable that permission after installation.

An in-place update must use the same application package and signing identity. If Android reports a signature conflict, contact support before uninstalling; uninstalling may remove local settings and records.

### 3 Prepare the target app

Manually open Xiaohongshu, Douyin or WeChat, sign in to an account you own or are authorized to use, and confirm that normal browsing works. Handle login, identity verification, CAPTCHAs and account warnings yourself, following the platform's requirements.

Return to the assistant, select the platform and check **App version check (应用版本检测)**. If the check fails, follow the displayed compatibility guidance.

### 4 Enable execution permissions

1. Enable **Accessibility (无障碍功能)** on the assistant's home screen.
2. In Android settings, find Yanghao Helper, enable its accessibility service and return to the app.
3. When starting a task, allow the floating window or **Display over other apps** permission when prompted. It provides execution controls and a way to stop tasks.
4. Keep the phone unlocked, in portrait orientation and connected to the network. Avoid manually changing pages or running another automation tool at the same time.

Settings names vary by phone manufacturer. If Android restricts background execution, adjust the app's battery and background settings as needed, then verify with a short run.

### 5 Additional setup for WeChat Channels

On the home screen, find **Channels screen-capture permission (视频号截图权限)** and tap **Get permission (获取权限)**. In Android's system prompt, choose to **share the entire screen**, keep the phone in portrait orientation and wait for the app to confirm permission.

Screen-capture authorization belongs to the current system session. You may need to grant it again after the app exits, screen sharing stops or authorization expires. If a running Channels task pauses because capture authorization is lost, use the home-screen permission entry to authorize it again and continue. Do not repeatedly request permission during normal execution.

## Usage guide

### Device-local configuration

The free standalone trial and standalone activation keys use settings saved on the phone:

1. **Choose a platform**: Select Xiaohongshu, Douyin or Channels and confirm that permissions and version checks pass.
2. **Configure rules**: Tap **Edit local execution settings (修改本机运行配置)** and enter the settings below.
3. **Save and start**: Return to the home screen and tap **Verify online and start trial (联网核验并开始试用)** or **Verify online and start execution (联网核验并开始运行)**.
4. **Review and stop**: Check status, logs and operation records. Tap **Stop execution (停止运行)**, confirm when prompted and wait for the task to stop.

| Setting | Instructions |
| --- | --- |
| Filter keywords | Required. Separate multiple terms with English or Chinese commas, for example `摄影,构图` for photography and composition |
| Search mode | Enable to browse search results and enter a search term; disable to use the platform's home or recommendation view |
| Dwell time | Xiaohongshu and Douyin support minimum and maximum values from `3` to `600` seconds; minimum must not exceed maximum. Channels has no local dwell-time setting |
| Interaction probabilities | Likes and comments accept `0` to `100`; `0` disables the action. Xiaohongshu and Channels also support a favorites probability |
| Comment text | One entry per line. Required before enabling comments; review whether each entry suits the intended context |
| Time window | Use 24-hour format, such as `09:00` to `09:15`. Identical start and end times mean all day |
| Running days | Monday is `1` and Sunday is `7`. Separate days with commas and select at least one day |

Schedules use **Beijing time (Asia/Shanghai, UTC+8)**. Probabilities do not specify fixed action counts or guarantee results.

For an initial check, disable search mode, set all interaction probabilities to `0` and choose a short time window that includes the current time. Verify browsing, page recognition and stopping before adjusting settings. Stop and restart a task after changing its rules so the new settings take effect.

### Platform-specific notes

**Xiaohongshu**: Choose home or search browsing, configure keywords and dwell time, then set separate probabilities for likes, comments and favorites. If the app remains in a comment dialog or an abnormal view, stop the task and manually return to a normal post list before retrying.

**Douyin**: Choose home browsing or video search, then configure keywords, dwell time, likes and comments. The current local configuration does not provide a Douyin favorites probability. Stop and handle any CAPTCHA or account risk warning yourself.

**WeChat Channels**: Confirm that WeChat opens normally and screen-capture permission is granted before starting recommendation or search browsing. Channels' **Recommend (推荐)** and **Favorite (收藏)** are different actions. A missing explicit favorite entry or an unverifiable result may cause an action to be skipped or shown as unconfirmed.

### Enterprise dashboard configuration

1. In **My (我的)**, enter your enterprise code or the appropriate online activation key, then tap **Register and activate (注册并激活)**.
2. Enterprise-code registrations require administrator approval. Online keys follow their respective activation rules.
3. An administrator configures platform rules, running days and time windows in the web dashboard, then assigns rules to the device.
4. Once the device is approved, enabled and within its authorization period, start the assigned platform on the phone or through an authorized dashboard administrator.

Your service provider supplies the dashboard address and account. A running task uses the rule snapshot taken at startup; rule updates apply on the next start.

## Trial and activation

| Mode | Configuration location | Activation |
| --- | --- | --- |
| Free standalone trial | On the phone | Claim and verify online when the service is enabled and the device is eligible |
| Standalone activation key | On the phone | Redeem a valid standalone key in My (我的) |
| Enterprise online mode | Web dashboard | Register with an enterprise code and receive approval, or redeem the appropriate online key |

Free trial terms:

- The trial lasts **24 consecutive hours** from the first successful claim. All three platforms share one trial entitlement.
- Installing the app, changing settings or checking eligibility does not start the timer.
- Stopping tasks, sleeping, switching platforms, updating in place, clearing app data or ordinarily reinstalling does not pause or reset the period.
- Once claimed, the trial keeps counting down even if the target app fails to launch.
- Every task start requires online verification. Follow the app for trial availability, remaining time and expiry status.

To continue after the trial, open **My (我的)** or **Contact WeChat (联系微信)** and select **Have an activation key or enterprise code? Activate (已有卡密或企业码？正式激活)**. Standalone keys retain local configuration. Enterprise codes, enterprise keys and some existing authorizations use dashboard rules; follow the interface shown after activation.

## Troubleshooting

| Issue | What to check |
| --- | --- |
| APK will not install | Confirm Android is being used and the download is complete and trusted. Contact support before resolving an update conflict by uninstalling |
| Incompatible app version | Check the supported version shown on the home screen, install the appropriate release and tap Recheck (重新检测) |
| Task will not start | Check accessibility, overlay permission, target app version, network, authorization, rules and running dates. Channels also requires screen capture |
| Channels capture authorization expired | Grant permission again from the home screen, share the entire screen and keep portrait orientation |
| Task keeps waiting or performs no interactions | Check the schedule, keyword matches, probabilities and comment text. Browsing alone may not produce interaction records |
| Action is shown as unconfirmed | Inspect the actual result in the target app. Do not repeatedly submit the same comment just to obtain a confirmed record |
| Trial expired | Contact support about activation options. Reinstalling does not reset the trial |
| Recognition fails after an update | Stop the task and contact support with the assistant version, target app version, phone model, Android version and error message |

## Permissions and data

Accessibility services recognize the interface and perform assisted actions defined by the rules. Overlay permission provides execution controls. Channels screen capture supports visual recognition. Avoid opening private chats, payment screens or other sensitive pages while these permissions are in use. You can revoke permissions in Android settings when you stop using the app.

Trial rules and operation records are stored locally. Online verification processes information such as a device identity digest, device code or name, app version and Android version to determine authorization and trial expiry. Enterprise online mode can synchronize execution logs and operation records; Channels diagnostic reports may include screenshots. The applicable scope depends on the mode used and the product's privacy information.

Clearing data or uninstalling may remove local settings and records, but does not delete the trial period stored on the server. Redact private messages and unrelated information before reporting an issue. Do not send passwords, verification codes, complete activation keys or login tokens.

## Disclaimer

1. **Independent tool**: Yanghao Helper is an independent third-party assistant. Xiaohongshu, Douyin, WeChat and Channels names identify supported targets and do not imply platform authorization, endorsement or guaranteed results.
2. **Permitted use**: Use only on accounts and devices you are legally entitled to use, and only where the platform permits the intended actions. Account or device owner permission does not replace platform permission. The [Douyin User Service Agreement in Chinese](https://www.douyin.com/agreements/?id=6773906068725565448) restricts automated program access. Stop using a feature if the intended activity is not permitted. Consult the latest in-app agreements and community rules for Xiaohongshu and WeChat Channels.
3. **No misuse**: Do not use the tool for fake engagement, abusive marketing, harassment, infringement, unlawful content distribution or bypassing CAPTCHAs, security controls or platform risk controls. Users must review their keywords, comments and schedules.
4. **Results and account risks**: No promise is made to improve account ranking, reach, followers, leads or revenue, or to ensure a platform accepts an action. Automation may trigger verification, feature restrictions or account action. Lower probabilities and account ownership do not eliminate these risks.
5. **Compatibility limits**: Changes to Android, target app layouts, networks or platform rules may affect execution. Features, compatibility and support depend on the relevant release notes and actual testing. Stop and contact support if behavior becomes abnormal.
6. **Responsibility**: This guide does not replace a formal service agreement or privacy policy. Responsibility is determined by applicable law, valid agreements and each party's fault. It does not exclude or limit responsibility that cannot legally be excluded or limited.

## Contact

**Support WeChat ID: `yuyishou6`**

Contact us about installation, free trials, activation keys and enterprise device management.

<p>
  <img src="./assets/contact-wechat.png" alt="Support WeChat QR code for yuyishou6" width="240" />
</p>

Scan with WeChat or save the image and select it from your photo library. You can also tap **Contact WeChat (联系微信)** at the top right of the assistant's home screen to copy the ID or save the QR code.

For troubleshooting, include your device code, phone model, assistant and target app versions, the time of the issue and a redacted screenshot. If contact details change, use the latest information on the app's Contact WeChat page.

[Website](https://rpa.yangcongyingyang.com/) · [Downloads](https://rpa.yangcongyingyang.com/#download)

## Related keywords

**Scripting and automation**: AutoJs6, Auto.js 6, autojs6, Auto.js, AutoJS, autojs, JavaScript, Android automation, Android RPA, accessibility automation, Android scripting.

**Platforms and use cases**: Xiaohongshu, REDnote, 小红书, Douyin, 抖音, WeChat Channels, 微信视频号, 视频号, Yanghao Helper, 养号助手, multi-platform operations, keyword filtering, task scheduling, device management.

**GitHub Topics**: `autojs6`, `autojs`, `android-automation`, `android-rpa`, `javascript`, `xiaohongshu`, `douyin`, `wechat-channels`.

Updated: October 19, 2026
