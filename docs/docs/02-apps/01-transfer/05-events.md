---
title: Events
sidebar_label: Events
sidebar_position: 5
slug: /apps/transfer/events
---


# Events

## `MsgTransfer`

| Type         | Attribute Key | Attribute Value |
|--------------|---------------|-----------------|
| ibc_transfer | sender        | \{sender\}      |
| ibc_transfer | receiver      | \{receiver\}    |
| message      | action        | transfer        |
| message      | module        | transfer        |

## `OnRecvPacket` callback

| Type                  | Attribute Key | Attribute Value |
|-----------------------|---------------|-----------------|
| fungible_token_packet | module        | transfer        |
| fungible_token_packet | sender        | \{sender\}      | 
| fungible_token_packet | receiver      | \{receiver\}    | 
| fungible_token_packet | denom         | \{denom\}       | 
| fungible_token_packet | amount        | \{amount\}      | 
| fungible_token_packet | success       | \{ackSuccess\}  | 
| fungible_token_packet | memo          | \{memo\}        | 
| denomination_trace    | trace_hash    | \{hex_hash\}    | 

## `OnAcknowledgePacket` callback

| Type                  | Attribute Key   | Attribute Value   |
|-----------------------|-----------------|-------------------|
| fungible_token_packet | module          | transfer          |
| fungible_token_packet | sender          | \{sender\}        |
| fungible_token_packet | receiver        | \{receiver\}      |
| fungible_token_packet | denom           | \{denom\}         |
| fungible_token_packet | amount          | \{amount\}        |
| fungible_token_packet | memo            | \{memo\}          |
| fungible_token_packet | acknowledgement | \{ack.String()\}  |
| fungible_token_packet | success | error | \{ack.Response\}  |

## `OnTimeoutPacket` callback

| Type                  | Attribute Key   | Attribute Value |
|-----------------------|-----------------|-----------------|
| fungible_token_packet | module          | transfer        |
| fungible_token_packet | refund_receiver | \{receiver\}    |
| fungible_token_packet | denom           | \{denom\}       |
| fungible_token_packet | amount          | \{amount\}      |
| fungible_token_packet | memo            | \{memo\}        |
