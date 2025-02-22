---
title: "Breaking Down Barriers in Digital Identity"
datePublished: Thu Feb 20 2025 15:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cm7g8elvj000009la3ke38dul
slug: breaking-down-barriers-in-digital-identity
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/ivG8LkDrtjs/upload/822dfabf2bf815b9aaeb5af277078b9c.jpeg
tags: opensource, mdl, digital-identity

---

## Introduction

Digital Identity has emerged as a crucial infrastructure in the modern digital economy, creating new business opportunities and enhancing our lives through identity verification, credentials, and access control. However, after working in this field for two years, I've observed significant barriers to adoption that continue to persist.

## Current Challenges in Digital Identity Adoption

The main challenges organizations face when implementing Digital Identity solutions include:

1. High Implementation Costs: Extended development periods and difficulties in securing specialized talent due to technical complexity
    
2. Lack of Interoperability: Limited scalability due to compatibility issues between different systems
    
3. Sustainability Issues: Complex maintenance and update procedures making operations difficult
    

The root cause of these problems ultimately comes down to the "lack of appropriate infrastructure" - particularly the shortage of developer-friendly tools and frameworks.

## Solution: Developer-Friendly Open Source Tools

My proposed solution is the development and distribution of "developer-friendly open source tools" that adhere to the following core principles:

### 1\. Simply Working

Looking at successful authentication/authorization SaaS products like Furo or Clerk, we can see the importance of "simply working." They provide an environment that works immediately after project creation. In contrast, current Digital Identity frameworks require lengthy configuration lists before you can even start.

Think about React.js - you create a project with `create-react-app` or `vite`, type `npm start`, and immediately see results in your browser. Digital Identity tools should work the same way. Instead of wrestling with lengthy configuration documents, developers should be able to start with defaults and customize progressively.

### 2\. Zero Protocol Knowledge Required

When implementing JWT, developers don't need to read RFC 6749 or 6750. They just find the `jsonwebtoken` library and set the secret and payload. Similarly with React - you learn by manipulating HTML tags and CSS values without understanding the internal workings.

Currently, Digital Identity libraries are only used by a small number of developers who understand the underlying standards and protocols. However, 99% of web developers aren't familiar with these underlying standards. They just want to focus on their business logic.

### 3\. Security by Design

Consider CORS - it enforces security rules by default, and exceptions must be explicitly configured. You can't turn off CORS. Similarly, Digital Identity tools should provide security by default while guiding users on why these security measures are necessary and how they can achieve their business objectives within these security boundaries.

## Implementation Example

Based on these principles, I started the [Verifiable Digital Credentials](https://github.com/lukasjhan/Verifiable-Digital-Credentials) project, which features:

* Ready-to-use default configurations
    
* Simple APIs that don't require protocol knowledge
    
* Built-in security by design
    

## Conclusion

The field of Digital Identity holds immense potential, but its complexity shouldn't be a barrier to adoption. By focusing on developer experience and providing the right tools, we can make this technology more accessible and practical for everyone. Through open source communities and easily accessible resources, we can build a more inclusive and efficient digital identity ecosystem.