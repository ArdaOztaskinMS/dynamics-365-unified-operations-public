--- 
title: Schedule a production order
description: Learn how to schedule a production order, including a step-by-step process for scheduling production orders using the USMF demo data company. 
author: johanhoffmann
ms.author: johanho
ms.topic: how-to
ms.date: 08/29/2018
ms.custom:
ms.reviewer: kamaybac
audience: Application User  
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
---

# Schedule a production order

[!include [banner](../../includes/banner.md)]

This procedure shows how to schedule a production order. The demo data company used to create this procedure is USMF. This is the third procedure out of seven which explains the production order lifecycle.


## Schedule a production order
1. Go to Production control > Production orders > All production orders.
    * Select a production order that has the Estimated status.  
2. On the Action Pane, click Schedule.
3. Click Schedule jobs.
    * The parameters for scheduling are set up on this page. You can set up the parameters for specific users or all users.  
4. In the Scheduling direction field, select 'Forward from today'.
5. In the Scheduling date field, enter a date.
6. Select or clear the Finite capacity check box.
7. Select or clear the Finite material check box.
8. Click OK.

## View the scheduling results
1. On the Action Pane, click Production order.
2. Click All jobs.
    * This page displays the scheduled jobs that you have just generated.  
3. Expand or collapse the Scheduling section.
    * On the Scheduling FastTab, you can view the scheduled date and time.  
4. Click Inquiries.
5. Click Capacity load.
    * The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.  
6. Close the page.
7. Close the page.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]