---
title: Course Site
publishDate: 2024-12-21 08:00:02
img: /assets/django/course-management-system.webp
img_alt: Course Management System Image
description: |
  Developed a advanced digital course website.
tags:
  - Django
  - Python
  - Cloudinary
  - Htmx
---

**Django Course Management System: A Simple Course Site**
- GitHub Code - <a href="https://github.com/Gopal-Khadka/Django-Course-Platform" target="_blank">Link</a>


### Building a Django Course Platform

#### Introduction

As the demand for online learning continues to grow, we're excited to share our journey of building a comprehensive **Django Course Platform**. The goal of this platform is to provide a seamless experience for both learners and instructors, offering a clean, intuitive interface backed by a robust technical stack. From course management to user verification, every detail is crafted to ensure a smooth, secure experience for all users.

In this post, we'll walk through the tech stack we've chosen, key features, and how we're implementing them.

#### The Tech Stack

We’ve carefully chosen each tool in our stack to ensure scalability, maintainability, and an enjoyable user experience. Here's a rundown of the core technologies powering our platform:

- **Django v5.1**: The backbone of our platform, Django allows us to rapidly build secure, scalable web applications. The version 5.1 features improvements that make development smoother.
  
- **Python v3.12**: As the language powering Django, Python provides flexibility and clarity for writing clean, maintainable code.
  
- **HTMX** and **django-htmx**: These tools are key for enabling modern, interactive front-end experiences without needing to fully rely on JavaScript. They allow us to easily create dynamic web pages with minimal overhead.
  
- **Tailwind CSS** and **django-tailwind**: Tailwind CSS brings utility-first styling to the project, making it easier to create clean, responsive designs without writing custom CSS from scratch.
  
- **Flowbite**: A component library that integrates perfectly with Tailwind, helping us quickly assemble polished UI elements.
  
- **Cloudinary**: For managing and delivering images, particularly course thumbnails and video content, Cloudinary ensures fast, optimized media delivery.

#### Core Features

##### 1. Course Management

Our platform allows instructors to create and manage their courses, providing the following essential features:

- **Title, Description, and Thumbnail/Image**: Each course has a title, a description, and an optional thumbnail/image to help users understand what the course is about.
  
- **Access Control**: We offer multiple access levels for each course:
    - **Anyone**: Open for everyone to view.
    - **Email required**: Users need to provide their email to gain access.
    - **Purchase required**: A paid course that requires the user to make a purchase before enrolling.
  
- **Course Status**: Courses can have one of three statuses:
    - **Published**: Available for enrollment.
    - **Coming Soon**: In the process of being created but not yet available.
    - **Draft**: Courses under development that aren’t visible to users yet.
  
- **Lessons**: Courses are made up of lessons, each with:
    - **Title and Description**
    - **Video**: Hosted and streamed within the platform.
    - **Status**: Similar to courses, lessons can be marked as Published, Coming Soon, or Draft.

##### 2. Email Verification for Short-Lived Access

To ensure security and streamline access management, we’ve implemented an email verification system for users who need short-lived access. The flow goes as follows:

- **Collect User Email**: Users provide their email address to gain access to specific courses.
  
- **Verify Email**: After submission, we send a verification email with a short-lived link.
  
- **Activate Session**: Once the user verifies their email, their session is activated, allowing access to the course.

###### Models:
- **Email**: Stores the user’s email address.
- **EmailVerificationToken**: Stores a token linked to the user's email, ensuring they can access the platform after verifying their identity.

#### Why We Chose These Technologies

The combination of **Django**, **Tailwind**, **HTMX**, and **Cloudinary** gives us the flexibility to build a robust platform without compromising on performance or user experience. We prioritize ease of development and scalability, which Django and Python provide in abundance.

Tools like **HTMX** and **Flowbite** ensure that the user experience is dynamic and modern while reducing reliance on heavier JavaScript frameworks. Plus, **Cloudinary** allows us to handle media with minimal hassle, optimizing images and videos for faster load times.