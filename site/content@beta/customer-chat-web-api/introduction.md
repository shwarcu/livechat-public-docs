---
weight: 10
---

# Introduction

## Versioning

This documentation describes the version **v3.0** of the **Customer Chat Web API**.

## What is Web API
Web API is similar to REST API. Client can send a **request message** that results in getting a **response message**. It's also possible to get webhooks. 

## When to use Web API
If you're wondering which API to use - Customer Chat **RTM API** or **Web API**, keep on reading.

**Web API** allows for building stateless integrations. The communication is done via **XHR requests**. The implementation is easier than with RTM API, but you need to take possible time delays into consideration.

**Not what you're looking for?** Perhaps, you need to use [**Customer Chat RTM API**](../customer-chat-rtm-api)<sup>[![LiveChat Link](link.svg)](../customer-chat-rtm-api)</sup> instead.


## Authentication

**Customer authentication** is handled by access tokens. Find out how to get an **access token** from [Customer authorization flows](https://developers.livechatinc.com/docs/authorization/)<sup>[![LiveChat Link](link.svg)](../authorization/#customer-authorization-flows)</sup>. If a method requires particular authorization scopes, you'll find them included in the method description. Keep in mind that Web API requires authorization every time you make a request.

## Data centers

LiveChat system operates in two data centers: `dal` and `fra`. The default data center is `dal`.

All the LiveChat OAuth2.0 access tokens have a prefix: `dal-` or `fra-`. This prefix indicates the data center they belong to. If you need to specify the data center while making an API call, simply add the `X-Region: <token_prefix>` optional header.

Summing up, if the user token starts with `fra-`, you should add the `X-Region: fra` header. If the token starts with `dal-` you don’t have to specify the header.

## Postman collection

You can find all the requests from the **Customer Chat Web API v3.0** in Postman.

<a href="https://www.getpostman.com/collections/07cbb1599d95db0c7d85" target="_blank"><img src="https://run.pstmn.io/button.svg"></a>