# GL.iNet GoodCloud

## コンテンツ

- [はじめに](#introduction)
- [セットアップ](#setup)
    - [ルーターでGoodCloudを有効にする](#enable-goodcloud-on-router)
    - [GoodCloudアカウントを登録する](#sign-up-goodcloud-account)
    - [サーバー地域を選択する](#select-server-region)
    - [新しいグループを追加する](#add-a-new-group)
    - [デバイスを追加する](#add-device)
    - [ルーターウェブ管理パネルのバウンド情報](#bound-info-on-router-web-admin-panel)
    - [ルーターのバインドを解除する](#unbind-router)
- [デバイスを管理する](#manage-your-devices)
    - [デバイス情報とステータス](#devices-info-and-status)
    - [LTE信号](#lte-signal)
    - [デバイス詳細情報](#device-detail-info)
    - [リモートアクセス管理パネル](#remote-access-web-admin-panel)
    - [リモートアクセスルータの端末](#remote-access-routers-terminal)
    - [アラームメールを設定する](#set-email-alarm)
- [サイト・ツー・サイト](#site-to-site)
    - [はじめに](#introduction_1)
    - [条件](#conditions)
    - [サイト・ツー・サイトネットワークを構築する手順](#steps-to-build-a-site-to-site-network)
    - [サイト・ツー・サイト接続のテスト](#testing-the-site-to-site-connection)
    - [ルートとその他のオプション](#route-and-other-options)
- [バッチ設定](#batch-setting)
    - [単一デバイスのバッチ設定](#batch-setting-of-single-device)
    - [複数デバイスのバッチ設定](#batch-setting-of-mutiple-devices)
    - [その他のバッチ操作](#other-batch-operations)
- [テンプレート管理](#template-management)
    - [テンプレートを追加する](#add-a-template)
    - [アップグレード](#upgrade)
    - [テンプレートをルーターに適用する](#apply-a-template-to-a-router)
    - [複数のルーターにテンプレートを適用する](#apply-a-template-to-multiple-routers)
- [タスクリスト](#task-list)
- [GoodCloud と VPN](#goodcloud-and-vpn)
- [クラウドをオフにする](#turn-off-cloud)

## はじめに

GL.iNet [GoodCloud](https://www.goodcloud.xyz){target="_blank"} cloud管理サービスは、ルーターにリモートでアクセスとルーターの管理ための簡単かつシンプルな方法を提供します。 以下に動画による紹介があります。

リモートデバイス管理ソリューション、GoodCloudのご紹介。

<iframe width="560" height="315" src="https://www.youtube.com/embed/JkV2PAy-_Og" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

中小企業向けGoodCloud Wi-Fi管理システムの簡単設定ガイド。

<iframe width="560" height="315" src="https://www.youtube.com/embed/7U1CwpKOKDM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

特徴：

* ライブルーターのステータスを確認する
    - ライブオンライン/オフラインステータス チェック
    - ライブRAMと負荷平均チェック
    - LTE信号
    - オンライン、オフラインのステータス更新に関する電子メール アラーム

* ルーターのリモート設定
    - ルーターの設定（SSIDやキーなど）をリモートで行う
    - リモートSSH
    - リモート アクセス Web 管理パネル

* ルーターのクライアントをリモートで監視
    - ネットワークに接続しているユーザーをチェックする
    - リアルタイムトラフィック監視とブロッククライアント
    - 新規顧客とブロックに関する電子メールアラーム

* ルーターのバッチ操作
    - コンフィグテンプレートを設定し、バッチでルーターを設定する
    - ルーターをバッチで再起動またはアップグレード

* ルーターをグループで管理する
    - デバイスをグループごとに分ける
    - デバイスを1つのページで管理

* サイト・ツー・サイト
    - バーチャルオフィス：オフィスのネットワークを他のオフィスへ拡張
    - 出張：オフィスのOA、CRM、MySQLシステムにリモートアクセス
    - スマートホーム：自宅のIPカメラ、NAS、その他のデバイスにリモートアクセス

## セットアップ

cloud機能を有効にし、GoodCloudにバインドする方法については、以下にチュートリアル動画を掲載しています。

<iframe width="560" height="315" src="https://www.youtube.com/embed/mvJQZphSO1A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### ルーターでGoodCloudを有効にする

ウェブ管理画面の左側→アプリケーション→GoodCloud

![enable goodcloud](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/enable_goodcloud.png){class="glboxshadow"}

上記の手順に従ってcloud機能を有効にすると、ルーターがGoodCloudサーバーに接続できるようになります。

* **リモートSSH** は、GoodCloud経由でルーターの端末にリモートアクセスするためのものです。チェックアウト [ここ](#remote-access-routers-terminal)。

* **リモート Web アクセス** GoodCloud経由でルーターのウェブ管理パネルにリモートアクセスするためのものです。チェックアウト [ここ](#remote-access-web-admin-panel)。

* **データサーバー**、お使いのデバイスに最も近いサーバーを選択してください。 データサーバーは3つあります、**アジア太平洋地域**(Japan), **アメリカ**(Oregon) と**ヨーロッパ**(Ireland)。

### GoodCloudアカウント登録

  [https://www.goodcloud.xyz](https://www.goodcloud.xyz){target="_blank"}を訪問、 サインアップしてサインインする。確認メールが見つからない場合は、スパムを確認するか、後でメールを確認してください。登録に問題がある場合、[support@glinet.biz](mailto:support@glinet.biz) までメールでお問い合わせください。 

### サーバー地域選択

初めてサインインすると、地域を選択するためのダイアログが表示されます。 ウェブ管理パネルで選択したデータサーバーと同じ地域を選択してください。([ルーターでGoodCloudを有効にする手順](#enable-goodcloud-on-router))。

右上隅でいつでも地域を変更できます。

![select region button](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/select_region_button.png){class="glboxshadow"}

### 新しいグループを追加する

左側 -> グループリスト -> グループの追加

新しいグループを追加するには、以下の手順に従ってください。

![add group](https://static.gl-inet.com/goodcloud/docs/add-group.png){class="glboxshadow"}

グループ名、会社名、説明、所在地を設定してください。

各デバイスはグループに属していなければなりません。

### デバイスを追加する

左側 -> デバイスリスト -> デバイスの追加。デバイスを GoodCloud アカウントにバインドするには、**自動検出**、**手動で追加** と**一括輸入** 3 つの方法があります。

=== "自動検出"

    ルーターとPC(GoodCloudウェブサイトを開いたPC)が同じネットワーク内にある場合は、**自動検出**をお試しください。
    
    以下の手順に従って、デバイスを追加ください。

    ![add device](https://static.gl-inet.com/goodcloud/docs/add-device.png){class="glboxshadow"}

    デバイスID[こちら](../where_to_find_the_device_id_mac_sn) をチェックしてください。

        注意: ここで「DDNS/デバイス ID」を入力するのは、ルーターが本当にオリジナル/有効であることを確認するためです。

        グループを追加したことがない場合は、自動的にデフォルトのグループが作成されます。

    `Refresh` をクリックすると、強制的にデバイスの自動検出を再開します。

    ![自動検出](https://static.gl-inet.com/goodcloud/docs/auto-discover.png){class="glboxshadow"}

=== "Manually add"

    If it can't discover automatically, try `Manually add`. All information that need to input can be found on the back of the router.

        Note: Input "MAC", "SN" and "DDNS" / "Device ID" here just to verify that the 
        router is really original and valid.

    For new models, it has **Device ID** on the back of router.

    ![manually add device](https://static.gl-inet.com/goodcloud/docs/manually-add-device-device-id.png){class="glboxshadow"}

    For old models, it has **DDNS** on the back of the router. Only the first 7 characters of **DDNS** are needed.

    ![manually add device](https://static.gl-inet.com/goodcloud/docs/manually-add-device.png){class="glboxshadow"}

=== "Bulk import"

    `Bulk import` is for user who have a great number of devices to add. By `Bulk import` you can import many devices by a Microsoft excel file.

### Bound info on router web Admin Panel

After you seccessfully add router to GoodCloud, go back to router web Admin Panel, on the left side, APPLICATION -> GoodCloud, 

refresh this page, It will display the bound GoodCloud username and date.

![goodcloud bound](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/goodcloud_bound_info.png){class="glboxshadow"}

### Unbind router

If you want to unbind the router, go to router web Admin Panel, on the left side, APPLICATION -> GoodCloud, click **Unbind** button.

![goodcloud unbind](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/goodcloud_unbind.png){class="glboxshadow"}

## Manage your devices

### Devices info and status

Sign in [Goodcloud](https://www.goodcloud.xyz), check at left side -> Device List

![device list table](https://static.gl-inet.com/goodcloud/docs/device_list_table.png){class="glboxshadow"}

there is icon at the first column of this table, 

![online icon](https://static.gl-inet.com/goodcloud/docs/online_icon.png) means this device is online.

![offline icon](https://static.gl-inet.com/goodcloud/docs/offline_icon.png) means this device is offline.

![deactovate icon](https://static.gl-inet.com/goodcloud/docs/deactivate_icon.png) means this device is deactivated, it has never connected to GoodCloud before.

![column selector](https://static.gl-inet.com/goodcloud/docs/column_selector.png){class="glboxshadow"}

Select the column you want to display.

`Online time` is the latest time when device connected GoodCloud.

`Offline time` is the latest time when device disconnected GoodCloud.

`Update time` is the latest time when device connected or disconnected GoodCloud.

`IP`, if your router run VPN client, this IP will be your VPN IP by default. <a href="#goodcloud-and-vpn">Learn More</a>

### LTE Signal

Only available for 4G devices, e.g. GL-MiFi, GL-X750

Toggle the column on Device List page.

![device LTE signal](https://static.gl-inet.com/goodcloud/docs/lte_signal.png){class="glboxshadow"}

It will show Signal strength, Type, and relavant parameters.

![device LTE signal](https://static.gl-inet.com/goodcloud/docs/lte_signal_2.png){class="glboxshadow"}

### Device detail info

At left side -> Device List, click the name of an online device, it will open a page to manage this device of WiFi, Clients and view router info, memory usage, up time, load average and log.

![to device detail page](https://static.gl-inet.com/goodcloud/docs/to_device_detail.png){class="glboxshadow"}

#### Device info

![device info](https://static.gl-inet.com/goodcloud/docs/edit-device-device-info.png){class="glboxshadow"}

#### WiFi

![device info](https://static.gl-inet.com/goodcloud/docs/edit-device-wifi.png){class="glboxshadow"}

Modify all WiFi settings.

#### Router status

![device info](https://static.gl-inet.com/goodcloud/docs/edit-device-router-status.png){class="glboxshadow"}

#### Client list

![device info](https://static.gl-inet.com/goodcloud/docs/edit-device-client-list.png){class="glboxshadow"}

#### Timeline

Timeline tab display the activities of router, and messages uploaded by the router's associated IoT device.

![device timeline](https://static.gl-inet.com/goodcloud/docs/timeline.png){class="glboxshadow"}

#### Tools

There are two tools, `Ping` and `Traceroute`.

![tools ping traceroute](https://static.gl-inet.com/goodcloud/docs/tools_ping_traceroute.png){class="glboxshadow"}

### Remote access web Admin Panel

Note: Please upgrade to 3.211 to use this feature.

If you can't find these icons, please make sure you have enable it, check out [here](#enable-goodcloud-on-router).

If this feature not work, please try the incognito mode of browser.

![remote access web admin panel](https://static.gl-inet.com/goodcloud/docs/remote_access_web_admin_panel.png){class="glboxshadow"}

### Remote access router's terminal

Note: Please upgrade to 3.211 to use this feature.

If you can't find these icons, please make sure you have enable it, check out [here](#enable-goodcloud-on-router).

If this feature not work, please try the incognito mode of browser.

![remote access web admin panel](https://static.gl-inet.com/goodcloud/docs/remote_access_terminal.png){class="glboxshadow"}

### Set email alarm

You can set email alarm when a device is online, offline, and new client connected.

At left side -> Setting -> Alarm Setting, create alarm rules

![create alarm rules](https://static.gl-inet.com/goodcloud/docs/create-alarm-rules.png){class="glboxshadow"}

Then set the email you want to receive notification. To ensure you get email successful, please add admin@goodcloud.xyz to your email address book.

![alarm rules](https://static.gl-inet.com/goodcloud/docs/alarm-rules.png){class="glboxshadow"}

## Site to Site

### Introduction

Site to Site allows offices in multiple locations to establish secure connections with each other over internet. It extends the company's network, making computers resources from one location available to employees at other locations. 

<a href="https://static.gl-inet.com/www/images/solutions/s2s/s2s_main_5.png" target="_blank"><img alt="site to site diagram" src="https://static.gl-inet.com/www/images/solutions/s2s/s2s_main_5.png"></a>

Senerio 1: A company has dozens of branch offices that they wish to join in a single private network to share resources.

Senerio 2: A company has a close relationship with a partner company, the Site to Site allows the companies to work together in a secure, shared network environment.

Senerio 3: A family has IP camera and when they are not at home, the Site to Site allows to remote access the IP camera.

### Conditions

It requires at least two routers, each in a different location, one of which has a public IP address. Please [check if your ISP assigns you a public IP address](../how_to_check_if_isp_assigns_you_a_public_ip_address). It requires firmware version 3.026 and above.

Note: It is not recommended to run Site to Site while its nodes are also running VPN client, which can make the network particularly complex.

### Steps to build a Site to Site network

1. Bind your routers to GoodCloud. (<a href="#add-device">how?</a>)

2. Follow the steps below to create a Site to Site network.

    ![create a site to site network](https://static.gl-inet.com/goodcloud/docs/create-s2s-01.png){class="glboxshadow"}

    Default port is 51830, if you want to use another port, find the `Advanced` option at the lower left corner.

    Due to the device's performance, each Site to Site network can have up to 10 devices.

    After you had chosen the devices, click Continue.

    ![create a site to site network](https://static.gl-inet.com/goodcloud/docs/create-s2s-02.png){class="glboxshadow"}

    Then, it will test each device if it can be set as the Main Node of Site to Site.

    We suggest that the router with strong performance and best network speed to be the Main Node.

    ![testing each device](https://static.gl-inet.com/goodcloud/docs/testing-s2s-01.png){class="glboxshadow"}

    If none of the devices can be used as the Main Node, make sure that:

    - One of routers has a public IP, either static public IP or dynamic public IP.
    - Port is open, default is 51830.
    - If the router is behind NAT, you may need to set up port forwading.

    You can also change port and try again.

    ![testing each device](https://static.gl-inet.com/goodcloud/docs/testing-s2s-02.png){class="glboxshadow"}

    If there are more than one device can be set as the Main Node, you need to choose one to continue.

    ![testing each device](https://static.gl-inet.com/goodcloud/docs/testing-s2s-03.png){class="glboxshadow"}

    If there is only one device can be set as the Main Node, it will go to the Site to Site detail page directly.

    The network is stopped by default, check the LAN IP, if it is OK then you need to click Start button, otherwise click Setting to change LAN IP.

    ![detail s2s](https://static.gl-inet.com/goodcloud/docs/detail-s2s-00.png){class="glboxshadow"}

    Wait a few minutes, the node's connect status will display as lines. Solid line means connected, dashed line means disconnected.

    ![detail s2s](https://static.gl-inet.com/goodcloud/docs/detail-s2s-01.png){class="glboxshadow"}

### Testing the Site to Site connection

Now the Site to Site network is created and started, let's test the connection.

Use your PC or Phone to connect to one of the Node of this Site to Site, and use browser to access another Node's LAN ip, if you see the login page, the connection between these two nodes is worked.

For example, my PC connect to Node 1 device, and then I use browser to access Main Node's LAN IP (192.168.48.1), if I see the login page, it means the connection between Node1 and Main Node is worked.

### Route and other options

You can change each device's LAN IP and routes.

![LAN IP and routes](https://static.gl-inet.com/goodcloud/docs/lanip-routes-s2s.png){class="glboxshadow"}

By default, each node can access other's LAN, based on security, we recommend only open the corresponding service IPs.

E.g. There is a Server A(172.30.97.100) in Node 1's subnet, if you want other Site to Site nodes  only can access Node 1's Service A, you can set it like below:

![LAN IP and routes](https://static.gl-inet.com/goodcloud/docs/lanip-routes-s2s-02.png){class="glboxshadow"}

You can add node's parent routes too.

Each sub Node build an encrypted tunnel netwrok to Main Node, if you want to change the IP of tunnel subnet. Click 'IP Address Range'.

![Tunnel IP Address Range](https://static.gl-inet.com/goodcloud/docs/tunnel-ip-address-range-s2s.png){class="glboxshadow"}

## Batch Setting

You can use this feature to configure multiple parameters for a single device, or you can configure multiple parameters for multiple devices.

    Note: This feature is only available to business users.

### Batch Setting of Single Device

To configure single device, as show below.

  <a href="https://static.gl-inet.com/goodcloud/docs/modify_configuration.png" target="_blank"><img alt="Modify Configuration" src="https://static.gl-inet.com/goodcloud/docs/modify_configuration.png"></a>

The left side of image below is correct. If your interface is like the right side of image below, please upgrade to latest testing firmware.

  <a href="https://static.gl-inet.com/goodcloud/docs/single_configuration.png" target="_blank"><img alt="Single Configuration" src="https://static.gl-inet.com/goodcloud/docs/single_configuration.png"></a>

Check the configuration that needs to be modified and input value.
  
![Add Configuration](https://static.gl-inet.com/goodcloud/docs/add_configuration.png){class="glboxshadow"}

The checked configuration is required, and only the configuration that conforms to the rule can be filled out. After the configuration is delivered, it does not take effect immediately. The configuration takes effect and the device needs to be restarted. You can check the Restart now option in the lower right corner of the above figure. After the configuration is completed, the device will restart immediately.

Preview the configuration and confirm the delivery.

![Preview Configuration](https://static.gl-inet.com/goodcloud/docs/preview_configuration.png){class="glboxshadow"}

Unchecked **Restart now** option will prompt.

<a href="https://static.gl-inet.com/goodcloud/docs/config_not_take_effect.png" target="_blank"><img alt="config not take effect" src="https://static.gl-inet.com/goodcloud/docs/config_not_take_effect.png"></a>

### Batch Setting of Mutiple Devices

Select the devices you want to configure.

![mutiple configuration](https://static.gl-inet.com/goodcloud/docs/mutiple_configuration.png){class="glboxshadow" width="800"}

Other operations are the same as when operating a single device.

### Other Batch Operations

Other Batch Operations: Move to other group, upgrade, restart, delete.

![Task](https://static.gl-inet.com/goodcloud/docs/task.png){class="glboxshadow"}

## Template Management

Save frequently used configurations as templates and quickly apply them when you modify configurations in batches.

    Note: This feature is only available to business users.

### Add a Template

Check the configuration that needs to be modified and input value. Most of the options are the same as those on web Admin Panel.

![Add Template](https://static.gl-inet.com/goodcloud/docs/add_template.png){class="glboxshadow"}

#### Upgrade

**Upgrade Path** is for upgrading custom firmware. Put the firmware and a text file on a web server, then put the url path on the **Upgrade Path**. For example, [https://fw.gl-inet.com/firmware/ar750/v1/](https://fw.gl-inet.com/firmware/ar750/v1/) is a Upgrade Path, it has a **list-sha256.txt** file [https://fw.gl-inet.com/firmware/ar750/v1/list-sha256.txt](https://fw.gl-inet.com/firmware/ar750/v1/list-sha256.txt) and a corresponding firmware file [https://fw.gl-inet.com/firmware/ar750/v1/openwrt-ar750-3.203-0701.bin](https://fw.gl-inet.com/firmware/ar750/v1/openwrt-ar750-3.203-0701.bin).

    Note: GL-AX1800, GL-S1300, GL-B1300, GL-AP1300 only support http path for now.

![Template info](https://static.gl-inet.com/goodcloud/docs/template_upgrade_path.png){class="glboxshadow"}

The content of the text file is like [this](https://fw.gl-inet.com/firmware/ar750/v1/list-sha256.txt), its name should be **list-sha256.txt**. It has 4 columns, the first column is firmware version, the second column is the name of firmware file, the thrid column is the sha256 of firmware file, the forth column is the size of firmware file.

![gl-ar750 sha256](https://static.gl-inet.com/goodcloud/docs/ar750-sha256.png){class="glboxshadow"}

Give the template a name and description.

![Template info](https://static.gl-inet.com/goodcloud/docs/template_info.png){class="glboxshadow"}

### Apply a template to a router

If you have created a template, then want to apply this template to a router. On the **Device List** page, find the router that you want to apply the template, make sure it is online, on the Actions column, click the cog icon, click **Modify Configuration** item. It will pop up a dialog **Configure batch modification**.

On the top right corner of the dialog, you can choose a template that has already created. Then click **Apply** button on the bottom right corner.

It will pop up another dialog to review the configuration of the template, scroll down to the bottom to click the **Confirm** button, it will load the configuration of template overwrite to this time modification.

Click **Apply** button, please note that the router will restart to take effect after click the **Apply** button.

### Apply a template to multiple routers

If you have created a template, then want to apply this template to multiple routers. This procedure is similar to that applied to a single router. On the **Device List** page, multiple select routers, then click **Bulk Action**, click **Modify Configuration** item. It will pop up a dialog **Configure batch modification**.

On the top right corner of the dialog, you can choose a template that has already created. Then click **Apply** button on the bottom right corner.

It will pop up another dialog to review the configuration of the template, scroll down to the bottom to click the **Confirm** button, it will load the configuration of template overwrite to this time modification.

Click **Apply** button, please note that the router will restart to take effect after click the **Apply** button.

## Task List

At task list page, it shows the execution result of the configuration template.

    Note: This feature is only available to business users.

![Task list](https://static.gl-inet.com/goodcloud/docs/task_list.png){class="glboxshadow"}

You can view the execution result of each device and configuration.

![Task list detail info](https://static.gl-inet.com/goodcloud/docs/task_list_detail_info.png){class="glboxshadow"}

## GoodCloud and VPN

If you enable GoodCloud function and running VPN client at the same time on router, by default, the connection between the router and the GoodCloud server will also go through the VPN, but sometimes the VPN connection is unstable, or the VPN provider mistakenly filters the GoodCloud connection, you can make the GoodCloud connection not go through the VPN by using the following settings.

Go to web Admin Panel, on the left side, VPN -> VPN Dashboard -> VPN Client -> Global Options.

![Services from GL.iNet doesn't Use VPN](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/goodcloud_donot_use_vpn.png){class="glboxshadow"}

It is not recommended to run Site to Site while its nodes are also running VPN client, which can make the network particularly complex.

## Turn off cloud

To stop GoodCloud service, turn it off on router web Admin Panel. Please follow the steps below. No action needed on the GoodCloud website.

![disable cloud](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/turn_off_cloud.png){class="glboxshadow"}

After disable Cloud, the interface is like below.

![after disable cloud](https://static.gl-inet.com/docs/router/en/4/tutorials/cloud/after_turn_off_cloud.png){class="glboxshadow"}

---

Still have questions? Visit our [Community Forum](https://forum.gl-inet.com){target="_blank"}.
