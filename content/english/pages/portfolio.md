---
title: "Portfolio"
meta_title: "My Portfolio"
description: "Showcasing my skills and experience as a front-end developer"
draft: false
---

### Main Technologies I work on

<br />

  | &nbsp; **Next.js** &nbsp; | &nbsp; **React.js** &nbsp; | &nbsp; **TailwindCss** &nbsp; | &nbsp; **Express.js** &nbsp; | &nbsp; **TypeScript** &nbsp; | &nbsp; **PostgreSQL** &nbsp; | &nbsp; **Prisma**  &nbsp; |

<hr>

### Projects related to my personal pain points

<br>
<br>

##### Freelance Ethiopia Clone

<br>

This project aims to create a clone of [Freelance Ethiopia's web app](https://www.freelanceethiopia.com/) with additional features and improvements to enhance the user experience. As a frequent user of their platform for finding jobs, I often encountered various inconveniences related to both the UI and functionality. Instead of simply complaining about these issues or wishing for certain features, I challenged myself to tackle them head-on and find solutions. Through this project, I have successfully addressed the following issues:

<!-- ![project demo](https://utfs.io/f/0971462c-ec8d-4819-b767-90d2e27abe96-27kpi9.png) -->

<br>

##### Issues Faced

<br>

1. **Inconvenient Login Process**: I found it annoying to repeatedly provide login credentials whenever I left the platform temporarily. It would be more user-friendly to have a persistent user session that remembers me and maintains the session upon returning.

2. **Lack of Job Application Tracking**: I faced difficulties in keeping track of the jobs I had applied for. It would be beneficial to have a simple and easy to navigate space where users can easily monitor and manage their job applications, including the ability to view application statuses and relevant details.

3. **No Feedback on Rejected Applications**: When my job applications were rejected, I received no feedback, making it challenging to understand why my applications were unsuccessful. It would greatly enhance the user experience to provide more detailed and specific feedback on rejected applications, helping users identify areas for improvement.

4. **Complex Job Filtering**: The existing job filtering system allowed users to select multiple sectors simultaneously, but this often made it challenging to query the database effectively. To simplify the filtering process and improve database query efficiency, it would be helpful to implement a more intuitive filtering where only one sector can only be checked at a time.

5. **Lack of Personalized Job Search**: The platform did not offer a user preferences section where individuals could customize their job search experience. Having the ability to save preferences, such as preferred job categories, locations, or other criteria, would allow users to tailor their job search and receive more relevant recommendations instead of being bombarded with irrelevant job posts.

6. **No Option to Update Password**: The platform did not offer a way for users to update their passwords. This lack of functionality made it inconvenient for users who wanted to change their passwords for security reasons or update it periodically. Providing a password update feature would enhance the overall user experience and security of the platform.

<br>

##### Challenges Faced

<br>

During the development of this project, I encountered the following challenges:

1. **N + 1 Problem when Fetching User Application Data**: When fetching user application data for a specific job post, I faced the N + 1 problem, where the application data had to be fetched for each individual user separately, resulting in unnecessary database queries and decreased performance. I had to implement a Global state mechanism to minimize the N + 1 problem and improve the efficiency of fetching user application data.

2. **Designing a New UI for User Profile**: Redesigning the user profile UI, especially for updating user information, posed a challenge in terms of creating a visually appealing and user-friendly interface. I had to think creatively and consider various design principles to develop an intuitive and responsive UI for the user profile section.

3. **Creating Reusable React Components**: I aimed to make my React components as reusable as possible to enhance code maintainability and reduce redundancy. However, achieving a high level of reusability while accommodating different use cases required careful consideration of component structure and props. I continuously worked on refining my component architecture to strike a balance between reusability and specificity.

4. **Performance-Related Issues**: As the project grew in complexity, I encountered performance-related issues, such as slow rendering times and suboptimal code execution. I had to analyze and Memoize critical components of the code, including implementing efficient hooks, and optimizing database queries to improve the overall performance of the platform.

<br>

##### What I have gained

<br>

1. **Enhanced Technical and Problem-Solving Skills**: Through the process of successfully completing this project, I have significantly strengthened my technical skills, including proficiency in TypeScript, React 18, Tailwind CSS, and Superbase. Additionally, I have honed my problem-solving abilities by overcoming challenges and finding effective solutions.

2. **Motivation to Address other Real-World Problems**: This project has served as a catalyst for my motivation to explore and address other real-world problems.

3. **Increased Confidence**: Successfully completing a complex project like this has boosted my confidence as a developer. The knowledge and experience gained throughout the project have validated my skills and abilities, providing me with the confidence to take on more ambitious projects in the future.

4. **Enhanced Knowledge of Performance Optimization Techniques**: Throughout the development process, I have delved into performance optimization techniques to ensure the application performs optimally. This hands-on experience has expanded my knowledge and understanding of optimizing software to improve efficiency, responsiveness, and overall user experience.

<br>

##### Future Features

<br>

In future iterations of the project, I have planned to include the following features:

- Password reset functionality for easy account recovery
- Company verification steps to enhance trust and credibility
- Payment integration using [chapa](https://chapa.co/)
- Multi-account support for users managing different roles
- In-platform chat feature to facilitate direct communication between employers and job applicants

<br>

 {{< button label="View Project" link="https://freelance-ethiopia-clone.vercel.app/" style="solid" >}} 
    <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/freelance-ethiopia-clone" style="solid" >}} <span/>

<hr>

##### Arada dictionary

<br>

Introducing Arada Dictionary: your new spot to understand slang and informal talk! Ever felt lost in conversations because of unfamiliar words? I've been there too. That's why I decided to create Arada Dictionary. I couldn't find any online resources for our language, so I'm building one using Nextjs.

Arada Dictionary isn't just about defining words. It's a place where everyone can help each other understand slang language. Think of it as a community-driven project where we all pitch in to keep up with the latest lingo.

Imagine this: you're traveling to a new city, let's say Dire Dawa and suddenly, people are using words and phrases you've never heard before. It can feel isolating, right? That's where Arada Dictionary comes in. It's like having a local guide to the slang and informal language of different cities, helping you feel more connected no matter where you go.

Whether you're curious about new phrases or just want to feel more in tune with how people talk today, Arada Dictionary is here to help. It's in early development stage and I'm actively working on it to make it cool.

<br>
{{< button label="source code" link="https://github.com/hariyebk/Arada-dictionary" style="solid" >}}


<hr>

### Internship Experience

<br>

I got an internship opportunity at [Trip.com](https://www.trip.com/) after applying through LinkedIn. During my internship, I had the privilege of working as a backend developer for 4 months, followed by 3 months as a frontend developer. This invaluable experience has allowed me to refine my skills in both areas of development and provided me with hands-on experience collaborating with a remote team.

<br>

##### Frontend Developer Intern | Trip.com | Remote

JUNE 2023 – AUGEST 2023

During my 3-month Internship, as a Frontend developer, I worked on an Internal Hotel Management Project that serves as a central hub for hotel staff, providing them with the necessary tools to efficiently manage check-ins, bookings, cabin availability, and guest information. One of my key responsibilities was to convert conceptual Figma mockups into user Interfaces using React, JavaScript styled components and Rechart library. I was able to create Layout for the cabin, booking, and guest management sections where It utilizes React’s compound component pattern to create a flexible and reusable Table structure. Additionally, I implemented a Visually intuitive home page dashboard powered by stats and charts to give insights on recent bookings and sales data.

<br>

{{< button label="View Certification" link="https://utfs.io/f/30b70780-9f9b-45e6-8f06-0ffd7f488646-4t070p.jpg" style="solid" >}} 

<br>
<br>

**Project Demo**

<br>

 {{< youtube qwmY5zy4IGA >}}

  <br>

  
  **Note**
  
   If you experienced difficulties logging into the application, please consider that the project utilizes Superbase with a free plan as its backend. for resource utilization if the project is not active , There is a possibility that they may pause the project temporarily. If you really want to check it out, you can contact me and I will restart the project for you. Login credentials: email- harunbekri6@gmail.com, password: testtest1234

   <br>


  {{< button label="View project" link="https://the-wild-oasis-hariyebk.vercel.app/" style="solid" >}} <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/The-Wild-Oasis" style="solid" >}} <span/>

   <hr>

##### Backend Developer Intern | Trip.com | Remote

<br>

MARCH 2023 – JUNE 2023

During my 4-month internship, as a Backend developer, I actively contributed to an exciting project assigned to me by my mentors. The aim of the project was to build an extensive selection of captivating tour packages tailored to meet the diverse needs and preferences of travelers. My primary focus was developing public and protected RESTful API endpoints using Express.js, while adhering to the Model-View-Controller (MVC) software architecture principle. Security was a top priority throughout the development process, and I implemented a range of essential security features like HTTP Only Cookies and Cross-Site Scripting prevention measures by using Middleware's. I also designed compressive MongoDB database Schemas and Aggregation pipelines to efficiently handle various API requests.

<br>

{{< button label="View Certification" link="https://utfs.io/f/a7f6c7ea-d8a5-4e0b-8edb-a7d9a8d7add9-fviinp.jpg" style="solid" >}} 

<br>
<br>


**Project Demo**

<br>

  {{< youtube l06kRcBt-0Q >}}

  <br>
  <br>

  {{< button label="source code" link="https://github.com/hariyebk/Natours" style="solid" >}} 

<hr>



### Other Projects

<br>

##### Girum Pizza

A pizza delivery application where users can Browse through an extensive menu of delicious pizzas, Add their desired pizzas to the cart and track the status of their order as it goes through the preparation, delivery, and arrival process.

Tech-Stack - **React** , **Redux**, **Tailwindcss**

<br>

{{< button label="view project" link="https://girum-pizza.vercel.app/" style="solid" >}}  <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/Girum-Pizza" style="solid" >}} <span/>

<br>
<br>


##### EPL Insights


This project is designed to analyze the match results of the English Premier League for the 2018/2019 season. It takes input data from a CSV file containing match details and generates a comprehensive report summarizing the outcomes and statistics of the matches.

Tech-Stack - **Typescript**

<br>

<span style = "display: flex; gap: 20px;">
{{< button label="source code" link="https://github.com/hariyebk/EPLInsights" style="solid" >}}</span>

<hr>
<br>

{{< button label="Download Resume (PDF)" link="https://harunbekri.vercel.app/static/media/Harun_CV.3913103d4b31503c2d78.pdf" style="solid" >}}


<br>
<br>
<br>