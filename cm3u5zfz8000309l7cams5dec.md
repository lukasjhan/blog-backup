---
title: "Building a High-Performance, Worldwide Status Page"
datePublished: Sun Jun 09 2024 15:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cm3u5zfz8000309l7cams5dec
slug: building-a-high-performance-worldwide-status-page
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1732365902299/b07cb029-9ef9-4751-84ec-78b7d84f9631.avif
tags: performance, software-engineering, performance-optimization

---

# **Introduction**

It is important to quickly access HeartBeat which I was previously created the service status page Sass, from around the world and check the results. This post will guide you through setting up a worldwide server architecture that leverages modern web technologies to achieve high performance and reliability. Let's dive into the key components of this setup:

## **Backend Server: Deploying Edge CDN Servers for API Service**

The backbone of a fast status page is a network of edge CDN (Content Delivery Network) servers. These servers are strategically located across the globe to serve content from the nearest point to the user, significantly reducing latency.

* **Why Edge CDN for APIs?** Most status page interactions are read-based, querying the current state of your services. By deploying your API service across edge servers, you can serve these read requests much faster.
    

* **Caching Results:** Since the data served by the API is predominantly read-only and changes infrequently (e.g., service uptime, incident reports), caching the results on the edge servers can dramatically reduce the need for repeated database queries, further speeding up response times.
    

*  **Geo-DNS:** Implement Geo-DNS to route users to the nearest edge server based on their geographic location, reducing latency.
    

## **Database: Asynchronous Edge Database Updates**

Real-time data consistency across global locations can be challenging and resource-intensive. Here's a more practical approach:

* **Semi-Real-Time Synchronization:** Update your edge databases asynchronously. While not real-time, this method ensures data is refreshed frequently enough to keep users informed without the overhead of constant synchronization.
    
* **Efficiency and Scalability:** This approach balances the need for up-to-date information with system resource efficiency, allowing you to scale your status page service more effectively.
    

## **Caching CORS Preflight Requests**

Cross-Origin Resource Sharing (CORS) is a security feature that can add latency to web requests. Here’s how to optimize it:

* **Understanding Preflight Requests:** A preflight request is made to determine whether the browser has permission to make a specific cross-origin request. Learn more [here](https://developer.mozilla.org/en-US/docs/Glossary/Preflight_request?utm_source=vertex.beehiiv.com&utm_medium=referral&utm_campaign=building-a-high-performance-worldwide-status-page).
    
* **Cache Max Age:** By setting the `Access-Control-Max-Age` header, you can instruct browsers to cache the results of the preflight check, reducing the need for repeated checks. Detailed guidance can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Max-Age?utm_source=vertex.beehiiv.com&utm_medium=referral&utm_campaign=building-a-high-performance-worldwide-status-page).
    

## **Conclusion**

Building a worldwide server setup for a fast and reliable status page requires careful consideration of backend architecture, database synchronization, and optimization techniques like caching CORS preflight requests. By leveraging edge CDN servers, asynchronous database updates, and strategic caching, you can ensure that your status page meets the demands of a global audience.