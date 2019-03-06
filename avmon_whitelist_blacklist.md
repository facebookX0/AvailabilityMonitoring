---

copyright:
  years: 2015, 2019
lastupdated: "2018-02-15"

keywords: filters, blacklist, whitelist, filter rules

subcollection: availability-monitoring

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Blocking and filtering with the whitelist and blacklist
{: #avmon_filters}

Use the whitelist and blacklist to determine which resources to send requests to and which resources contribute to the metrics and status of your application tests. Whitelists and blacklists are only available for webpage and scripted behavior tests.
{: shortdesc}

The **Whitelist** and **Blacklist** fields define the resources that your test can or cannot access and the resources that contribute to the metrics and status of your tests. The Whitelist and Blacklist can control which dependencies and resources contribute to the response times of your tested web applications, such as third-party metrics. You can configure your Whitelist and Blacklist when you create a webpage or scripted behavior test.

You can use the **Whitelist** to define allowed schemes, domains and URLs; then, use the **Blacklist** to block specific elements of your allowed locations.

## Syntax

Use commas (,) to separate items in the Blacklist and Whitelist. Use the wildcard symbol (\*) to filter elements of each URL or domain.

If your URL filter includes "http://" or "https://", you must include the wildcard symbol (\*) directly after the URL, for example, `https://www.ibm.com*`.
{: tip}

## Whitelist

Add URLs, schemes, or domains that you want to include in request and metric calculations to the Whitelist field. You can list up to 10 items in your Whitelist. Each item length cannot exceed 200 characters. All domains, schemes, and URLs that do not match the items on your Whitelist are blocked.

For example:
```
ibm.com, *developerworks*, *.s81c.com/*, https://*
```
{: codeblock}

## Blacklist

Add URLs, schemes, or domains that you want to block from requests and metric calculations to the Blacklist field. You can list up to 20 items in your Blacklist. Each item length cannot exceed 200 characters.

For example:
```
*.profile.*.cloudfront.net/*.png, http://*
```
{: codeblock}

## Filtering and blocking behavior

Tests can have both a Whitelist and a Blacklist. When determining which locations are allowed or blocked, the Blacklist always overrides the Whitelist. The following table displays filtering and blocking behavior for all scenarios involving the Whitelist and Blacklist.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Table 1. Filtering and blocking behavior for Whitelist and Blacklist</caption>
<thead>
<tr>
<th>Blacklist</th>
<th>Whitelist</th>
<th>Behavior</th>
<th>Reason</th>
</tr>
</thead>
<tbody>
<tr>
<td>Empty</td>
<td>Empty</td>
<td>Allow access</td>
<td>No filtering rules entered.</td>
</tr>
<tr>
<td>Empty</td>
<td>URL does not match list entry</td>
<td>Block access</td>
<td>URL is not in the whitelist.</td>
</tr>
<tr>
<td>Empty</td>
<td>URL matches list entry</td>
<td>Allow access</td>
<td>URL is in the whitelist. No blacklist entry to block access.</td>
</tr>
<tr>
<td>URL does not match list entry</td>
<td>Empty</td>
<td>Allow access</td>
<td>URL is not in the blacklist. No whitelist entry to block access.</td>
</tr>
<tr>
<td>URL matches list entry</td>
<td>Empty</td>
<td>Block access</td>
<td>URL is in the blacklist.</td>
</tr>
<tr>
<td>URL does not match list entry</td>
<td>URL does not match list entry</td>
<td>Block access</td>
<td>URL is not in the whitelist.</td>
</tr>
<tr>
<td>URL does not match list entry</td>
<td>URL matches list entry</td>
<td>Allow access</td>
<td>URL is in the whitelist. URL is not in the blacklist.</td>
</tr>
<tr>
<td>URL matches list entry</td>
<td>URL does not match list entry</td>
<td>Block access</td>
<td>URL is not in the whitelist. URL is in the blacklist.</td>
</tr>
<tr>
<td>URL matches list entry</td>
<td>URL matches list entry</td>
<td>Block access</td>
<td>URL is in the blacklist. The blacklist entry overrides the whitelist entry.</td>
</tr>
</tbody>
</table>
