# Availability & Performance

In the Umbraco Cloud Settings menu you can find a page called _Availability & Performance_.

Umbraco Cloud's "Availability & Performance" feature lets you see get an overview of your cloud projects' past and current health. Leveraging Azure metrics data, the page provides users with valuable insights into the availability and performance of the cloud project enabling them to monitor and address any issues that may impact the user experience.

## Availability & Performance Overview

Under Settings in the Umbraco Cloud Portal, you'll find Availability & Performance. This is where you find the page that shows visualization and statistics for four sections.

In this overview, you will find the usage limitations for your Umbraco Cloud project as well as the plan that the project is on.

![Usage on Cloud](../images/cloud-usage.png)

The usage shown is for the Live environment of your project as it is the usage in this environment that is measured against the plan usage limits. For _media storage_ it is the size of all files in the blob storage including the cache that is considered.

The page consists of the following parts:
- Time range and granularity selector
- Panel view
- Chart and statistics view

Note: The page is initially shown for all project plans. More detailed visualization and tools intended for troubleshooting to be added in the future will be restricted to “Standard” and “Professional” project plans.

### Time range and granularity selector

When you enter the page, you will a default visualization of the failed requests for the last 24 hours with a data point set for every fifth minute. You are able to change the time range to a predefined interval or define a specific start and end time. You can also select the granularity of the data points.

!!!!

Initially, you will only be able to set the time granularity to “5 minutes”.

### Panel view

The panel selector consists of four tiles, each representing a specific segment of data. The four segments are failed request, App Performance, CPU Usage, and Memory Usage.

!!!

Each tile includes relevant statistics and potentially a warning or an error indicator in case there is something you might want to consider.

An error indicator is shown in the following situations:
- Failed Requests: when one or more server errors have occurred in the selected time range.
- CPU Usage: when the maximum CPU time has exceeded 100% of the plan quota in a five-minute period during the selected time range. *
- Memory Usage: when the maximum private time has exceeded 100% the plan quota in a five-minute period during the selected time range. *

A warning is shown in case the CPU Usage or Memory Usage
- Failed Requests: when one or more client errors (but no server errors) have occurred in the selected time range.
- CPU Usage: when the maximum CPU time has exceeded 80% percent of the plan quota in a five-minute period during the selected time range. *
- Memory Usage: when the maximum private time has exceeded 80% percent of the plan quota in a five-minute period during the selected time range. *

* Only shown for cloud projects on a shared plan and with a granularity of five minutes selected.


### Chart and statistics view

For each segment, there will be shown a chart and a set of related statistics.

*Failed request* 
The chart shows the breakdown of HTTP status codes for each data point with the selected granularity. Only responses indicating a client (4xx region) or server errors (5xx region) are shown.

In the statistics panel on the right, you will find the total instances of the status code in the time range.

<> 

*App Performance*
The chart shows the average response time during the selected time range. All requests to the Umbraco solution in the time periods with the length of the selected granularity count to average response time.

The statistics panel shows the average, maximum, and minimum response for the shown data points.

*CPU Usage*
The chart depicts the CPU time consumed by the application in the selected time range with time periods equalling the selected granularity.

For cloud projects using a shared resource and a granularity of 5 minutes, the user will see both the assigned CPU time in seconds and a comparison against the plan quota. The plan quotas are described here<https://docs.umbraco.com/umbraco-cloud/getting-started/umbraco-cloud-plans>. 
In this case, the statistics panel maximum CPU time, average CPU, plan quota, and the maximum and average percentage of the consumed CPU in a 5 minute period compared to the plan quota.

For cloud projects with a dedicated option (or a shared plan with another granularity than 5 minutes), the user will see the average assigned CPU time in seconds.
Here the statistics panel will display the maximum, average, and minimum CPU time based on selected granularity.

*Memory Usage*
The chart shows the memory usage in private bytes consumed by the application in the selected time range with time periods equalling the selected granularity.

For cloud projects using a shared resource and a granularity of 5 minutes, the user will see both the assigned private bytes in mega bytes (MB) and a comparison against the plan quota. The plan quotas are described here<https://docs.umbraco.com/umbraco-cloud/getting-started/umbraco-cloud-plans>. 

For cloud projects with a dedicated option (or a shared plan with another granularity than 5 minutes), the user will see the average assigned private bytes in bytes..
Here the statistics panel will display the maximum, average, and minimum allocation of private bytes based on selected granularity.

## Key benefits
Some of the benefits the “Availability & Performance” feature gives you are as follows.

### Health Monitoring:
Umbraco Cloud's "Availability and Performance" feature allows users to monitor the health of their cloud projects more effectively. By leveraging Azure metrics data, you can access critical information such as HTTPS status codes, response times, CPU time, and memory usage in private bytes.

The CPU and memory usage is particularly important to keep an eye on from time to time in case the cloud project is running on a shared plan to ensure that the plan quotas aren’t exceeded.

### Issue Discovery:
The feature enables users to discover application issues that may impact the overall performance of their Umbraco Cloud projects. By analyzing Azure metrics data, you gain valuable insights into the performance of your app service, including response times and CPU/memory usage.

Real-time monitoring of HTTPS status codes helps you identify any errors or disruptions to your application's availability. This proactive approach allows you to respond swiftly, ensuring that your website or application remains accessible and responsive to users.

### User-Friendly Interface:
Umbraco Cloud provides a user-friendly interface for accessing and interpreting the "Availability and Performance" feature. The interface presents Azure metrics data in a clear and understandable manner, making it easy for users to navigate and gain actionable insights. With intuitive SVG-based visualizations and highlighted statistics for the selected time range, you can monitor the health and performance of your cloud projects effortlessly.

### Future updates
The first version of the “Availability and Performance” feature released on May 26th, 2023 includes a basic visualization and a set of highlighted numbers for failed requests, application performance, CPU time, and memory usage.

More detailed information about each of these domains will be provided for each of the four domains in the future. While the visualization and basic numbers are accessible for any project plan, the detailed information and insight to be added will be exclusive to the upper cloud project plans