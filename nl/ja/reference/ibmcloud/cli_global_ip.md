---

copyright:

  years: 2018


lastupdated: "2018-11-30"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# グローバル IP の管理

グローバル IP アドレスは、特殊な静的 2 次サブネットです。 これは、アカウントの他の任意の IP アドレスにルーティングできる /32 サブネット (つまり、単一の IP アドレス) としてお客様に配信されます。

以下のコマンドを使用して、{{site.data.keyword.Bluemix}} クラシック・インフラストラクチャーのグローバル IP サービスのグローバル IP を管理します。
{: shortdesc}

<table summary="コマンドの詳細情報を表示するリンクが含まれたアルファベット順の {{site.data.keyword.Bluemix_notm}} クラシック・インフラストラクチャーのグローバル IP コマンド">
 <tbody>
 <tr>
  <td>[ibmcloud sl globalip assign](/docs/cli/reference/ibmcloud/cli_global_ip.html#sl_globalip_assign)</td>
  <td>[ibmcloud sl globalip cancel](/docs/cli/reference/ibmcloud/cli_global_ip.html#sl_globalip_cancel)</td>
  <td>[ibmcloud sl globalip create](/docs/cli/reference/ibmcloud/cli_global_ip.html#sl_globalip_create)</td>
 <td>[ibmcloud sl globalip list](/docs/cli/reference/ibmcloud/cli_global_ip.html#sl_globalip_list)</td>
 <td>[ibmcloud sl globalip unassign](/docs/cli/reference/ibmcloud/cli_global_ip.html#sl_globalip_unassign)</td>
 </tr>
   </tbody>
 </table>

 ## ibmcloud sl globalip assign
{: #sl_globalip_assign}

グローバル IP をターゲットのルーターまたはデバイスに割り当てます。
```
ibmcloud sl globalip assign IDENTIFIER TARGET
```


**例**:
```
ibmcloud sl globalip assign 12345678 9.111.123.456
```
このコマンドは、ID 12345678 の IP アドレスを、IP アドレス 9.111.123.456 のターゲット・デバイスに割り当てます。

## ibmcloud sl globalip cancel
{: #sl_globalip_cancel}

グローバル IP を取り消します。
```
ibmcloud sl globalip cancel IDENTIFIER [OPTIONS]
```

<strong>コマンド・オプション</strong>:
<dl>
<dt>-f, --force</dt>
<dd>確認なしで操作を強制します。</dd>
</dl>

**例**:
```
ibmcloud sl globalip cancel 12345678
```
このコマンドは、ID 12345678 の IP アドレスを取り消します。

 ## ibmcloud sl globalip create
{: #sl_globalip_create}

グローバル IP を作成します。
```
ibmcloud sl globalip create [OPTIONS]
```

<strong>コマンド・オプション</strong>:
<dl>
<dt>--v6</dt>
<dd>IPv6 IP アドレスを注文します。</dd>
<dt>--test</dt>
<dd>テストの注文。</dd>
<dt>-f, --force</dt>
<dd>確認なしで操作を強制します。</dd>
</dl>

**例**:
```
ibmcloud sl globalip create --v6
```
このコマンドは、IP V6 アドレスを作成します。

## ibmcloud sl globalip list
{: #sl_globalip_list}

アカウントのすべてのグローバル IP をリストします。
```
ibmcloud sl globalip list [OPTIONS]
```

<strong>コマンド・オプション</strong>:
<dl>
<dt>--v4</dt>
<dd>IPv4 のみを表示します。</dd>
<dt>--v6</dt>
<dd>IPv6 のみを表示します。</dd>
<dt>--order</dt>
<dd>この IP アドレスを購入した注文の ID を基準にしてフィルター操作します。</dd>
</dl>

**例**:
```
ibmcloud sl globalip list --v4
```
このコマンドは、現行アカウントのすべての IP V4 アドレスをリストします。

## ibmcloud sl globalip unassign
{: #sl_globalip_unassign}

ターゲットのルーターまたはデバイスからグローバル IP を割り当て解除します。
```
ibmcloud sl globalip unassign IDENTIFIER
```


**例**:
```
ibmcloud sl globalip unassign 12345678
```
このコマンドは、ID 12345678 の IP アドレスをターゲット・デバイスから割り当て解除します。
