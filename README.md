# NotificationsAzure
Transmitting notifications/events from PostgreSQL to web browsers via Message Oriented Middleware (Azure Service Bus) and Events, on Microsoft Azure.

**File "Notifications and messages from PostgreSQL to ASP.NET Core Web App - v.2.0.0.pdf":**

Full description of the asset and of the different demo projects involved.

**DBeProc1.zip**

Archive file with two main folders:

* "EventHubPublisher": Visual Studio .NET 2022 solution file "EventHubPublisher.sln" with the project **EventHubPublisher**. It is a .NET Framework 4.8 project with the function of both receiving PostgreSQL notifications and loading data into the MOM (Message Oriented Middleware) that here is Azure Service Bus.  It represents the "**Proc1**" block in the overall demo, bridging the PostgreSQL DB to the MOM (here the Azure Service Bus) component.
* "SQL Script": sql DDL (data Definition Language) with schema and triggers functions for the PostgreSQL database.

**Proc2.zip**

Archive file with a Visual Studio .NET 2022 Solution file "publisher.sln", with the project **publisher**. It is a .NET 7 project for a console application acting as both a dequeuer from the Azure Service Bus and a loader in the Azure Web PubSub service notification system.

It represents the "**Proc2**" block in the overall demo, bridging the "MOM" (Message Oriented Middleware, here Azure Service Bus), to the WEBNOTIFY component (here the Azure Web PubSub Service).

**BlazorServerSignalR3Soln.zip**

Archive file with a Visual Studio .NET 2022 Solution file "BlazorServerSignalRSoln.sln", with the project **BlazorServerSignalR**. It is a .NET 7 project for an ASP.NET Core Blazor Server Web App that receives notifications from the Azure Web PubSub service subsystem and presents them on screen. It is pobbible to open multiple frontend sessions in different browsers pointing to this web app, to receive the notifications on each one of the connected browser instances/sessions.

It represents the last "block" of the sample, that is the "**Web App**" component.

