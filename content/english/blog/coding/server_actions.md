---
title: "Next.js Server Actions : A Simple Guide"
meta_title: "server actions, data fecthing , data manipulation"
description: "This blog article explains what nextjs server actions are"
date: 2023-11-20T04:14:00Z
image: "/images/serveractions.png"
categories: ["coding"]
author: "Harun Bekri"
tags: ["server-actions", "data-fetching"]
draft: false
---

In the traditional approch, you need to make network requests to your API endpoints using a separate client-side library like Axios or the fetch API. Server Actions are designed to simplify this process. you can use server actions directly within your components with automatic UI updates based on data changes and without a need for separate API routes.

Next.js introduces an innovative feature called Server Actions that revolutionizes how you handle server-side logic in your applications. These actions work seamlessly with the App Router, simplifying data fetching, form submissions, and more.

Imagine this: You're building an e-commerce store. A user clicks "Add to Cart" on a product page. Previously, you needed separate API routes to handle this action. Now, with Server Actions, you can write the code directly within your component, keeping your logic organized and streamlined.


## What makes Server Actions powerful

- **Simplified Code**: No need for separate API routes. Just define your action within your component.
- **Improved Performance**: Server Actions offload data fetching and mutations to the server, resulting in faster loading times.
- **Progressive Enhancement**: Forms can work without JavaScript, ensuring accessibility.
- **Flexible Integration**: Works beautifully with the App Router for seamless navigation and data updates.

Let's see how Server Actions work with the App Router:

1. **User Interaction**: A user clicks a button or submits a form.
2. **Server Action Triggered**: The user interaction triggers a Server Action defined within the component.
3. **Server-Side Execution**: The Server Action runs on the server, performing its designated task, like updating data or sending emails.
4. **Data Fetching & Revalidation**: If data is involved, it's retrieved and sent back to the client. The App Router automatically updates the UI and revalidates cached data.
5. **User Experience**: The user sees the updated UI and interacts with the application seamlessly.

Here are some everyday examples of Server Actions in action:

- Fetching product information based on user selection.
- Submitting a contact form and receiving a confirmation message.
- Adding items to a shopping cart and seeing the updated total.
- Authenticating users and managing user sessions.

Server Actions and the App Router are a game-changer for Next.js development. They simplify server-side logic, improve performance, and offer a more intuitive way to build dynamic and interactive applications.