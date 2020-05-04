---
title: Azure SDK for .NET (May 2020)
layout: post
date: 2020-05-01
tags: dotnet
sidebar: releases_sidebar
repository: azure/azure-sdk-for-net
---

The Azure SDK team is pleased to announce our {{ page.date | date: "%B %Y" }} client library releases.

#### GA

- Core
- Event Hubs

#### Updates

#### Preview

- Search
- Service Bus

## Installation Instructions

To install any of our packages, please search for them via `Manage NuGet Packages...` in Visual Studio (with `Include prerelease` checked) or copy these commands into your terminal:

    $> dotnet add package Azure.Messaging.EventHubs
    $> dotnet add package Azure.Messaging.EventHubs.Processor

    $> dotnet add package Azure.Messaging.ServiceBus --version 7.0.0-preview.2

    $> dotnet add package Azure.Search.Documents --version 1.0.0-preview.3

## Feedback

If you have a bug or feature request for one of the libraries, please [file an issue in our repo](https://github.com/Azure/azure-sdk-for-net/issues/new/choose).

## Changelog

Detailed changelogs are linked from the [Quick Links](#quick-links) below. Here are some of the highlights:

### Core [Changelog](https://github.com/Azure/azure-sdk-for-net/blob/master/sdk/core/Azure.Core/CHANGELOG.md)

- Read client request ID value used for logging and tracing off the initial request object if available.
- Fixed a bug when using Azure.Core based libraries in Blazor WebAssembly apps.

### Event Hubs [Changelog](https://github.com/Azure/azure-sdk-for-net/blob/master/sdk/eventhub/Azure.Messaging.EventHubs/CHANGELOG.md)

- The set of features from v5.1.0-preview.1 are now generally available.  This includes the `EventProcessor<TPartition>` and `PartitionReceiver` types which focus on advanced application scenarios which require greater low-level control. 

### Event Hubs Processor [Changelog](https://github.com/Azure/azure-sdk-for-net/blob/master/sdk/eventhub/Azure.Messaging.EventHubs.Processor/CHANGELOG.md)

- The set of features from v5.1.0-preview.1 are now generally available.  This includes the enhancements to the `EventProcessorClient` for improved stability, resilience, and performance.

### Search [Changelog](https://github.com/Azure/azure-sdk-for-net/blob/master/sdk/search/Azure.Search.Documents/CHANGELOG.md)

- Renamed `SearchIndexClient` to `SearchClient` and renamed numerous models for search index creation.
- Simplified the use of e-tags.

### Service Bus [Changelog](https://github.com/Azure/azure-sdk-for-net/blob/master/sdk/servicebus/Azure.Messaging.ServiceBus/CHANGELOG.md#700-preview2-2020-05-04)

- Allow specifying a list of named sessions when using ServiceBusSessionProcessor.
- Transactions/Send via support.
- Add SessionInitializingAsync/SessionClosingAsync events in ServiceBusSessionProcessor.
- Do not attempt to autocomplete messages with the processor if the user settled the message in their callback.
- Add SendAsync overload accepting an IEnumerable of ServiceBusMessage.

## Latest Releases

{% assign packages = site.data.releases.latest.dotnet-packages %}
{% include dotnet-packages.html %}

{% include refs.md %}