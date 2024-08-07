---
title: "Portfolio"
meta_title: "My Portfolio"
description: "Showcasing my skills and Projects as developer"
draft: false
---

### Tools and Technologies 

<span style= "margin-top: 15px;"> </span>

**Front-end library and state-managment**:  React.js, Redux, tanstack query
<br>

**Styling**: Tailwind Css
<br>

**Runtime enviroments**:  Nodejs and Bun
<br>

**Back-end Frameworks**:  Express.js and hono.js
<br>

**Full-stack Framework**:  Next.js
<br>

**ORMs**:  Prisma and Mongoose
<br>

**Databases**:  PostgreSQL and Mongodb
<br>

**Version Control**:  Git and Github
<br>

**Security testing**:  Burp Suite
<br>

**Authentication and Session Managment**:  Auth.js and Supabase
<br>

**Hosting and Deployment**:  Vercel and Netlify


<hr>

#### Projects related to my personal pain points

<br>

##### Freelance Ethiopia Clone


This project aims to create a clone of <a href="https://www.freelanceethiopia.com/"> Freelance Ethiopia's web </a> app with additional features and improvements to enhance the user experience. As a frequent user of their platform for finding jobs, I often encountered various inconveniences related to both the UI and functionality. 

Instead of simply complaining about these issues or wishing for certain features, I challenged myself to tackle them head-on and find solutions. Through this project, I have successfully addressed the following issues:

</p>

<br>

##### Problems I encountered

<span style= "margin-top: 10px;"> </span>

1. **Inconvenient Login Process**: 

I found it annoying to repeatedly provide login credentials whenever I left the platform temporarily. It would be more user-friendly to have a persistent user session that remembers me and maintains the session upon returning.

2. **Lack of Job Application Tracking**: 

 I faced difficulties in keeping track of the jobs I had applied for. It would be beneficial to have a simple and easy to navigate space where users can easily monitor and manage their job applications, including the ability to view application statuses and relevant details.

3. **No Feedback on Rejected Applications**: 

When my job applications were rejected, I received no feedback, making it challenging to understand why my applications were unsuccessful. It would greatly enhance the user experience to provide more detailed and specific feedback on rejected applications, helping users identify areas for improvement.

4. **Complex Job Filtering**: 

The existing job filtering system allowed users to select multiple sectors simultaneously, but this often made it challenging to query the database effectively. To simplify the filtering process and improve database query efficiency, it would be helpful to implement a more intuitive filtering where only one sector can only be checked at a time.

5. **Lack of Personalized Job Search**: 

The platform did not offer a user preferences section where individuals could customize their job search experience. Having the ability to save preferences, such as preferred job categories, locations, or other criteria, would allow users to tailor their job search and receive more relevant posts instead of being bombarded with irrelevant job posts. 

6. **No Option to Update Password**: 

The platform did not offer a way for users to update their passwords. This lack of functionality made it inconvenient for users who wanted to change their passwords for security reasons or update it periodically. Providing a password update feature would enhance the overall user experience and security of the platform. 

<br>

{{< gallery dir="images/freelance" lightbox="true" carousel="true" autoplay="true" webp="true" command="Fit" zoomable="true" >}}

<!-- ##### Challenges Faced

<br>

During the development of this project, I encountered the following challenges:

1. **N + 1 Problem when Fetching User Application Data**: When fetching user application data for a specific job post, I faced the N + 1 problem, where the application data had to be fetched for each individual user separately, resulting in unnecessary database queries and decreased performance. I had to implement a Global state mechanism to address the N + 1 problem and improve the efficiency of fetching user application data.

2. **Designing a New UI for User Profile**: Redesigning the user profile UI, especially for updating user information, posed a challenge in terms of creating a visually appealing and user-friendly interface. I had to think creatively and consider various design alternatives to develop an intuitive and responsive UI for the user profile section.

3. **Creating Reusable React Components**: I aimed to make my React components as reusable as possible to enhance code maintainability and reduce redundancy. However, achieving a high level of reusability while accommodating different use cases required careful consideration of component structure and props. I continuously worked on refining my component architecture to strike a balance between reusability and specificity.

4. **Performance-Related Issues**: As my code base grew in complexity, I encountered performance-related issues, such as slow rendering times and suboptimal code execution. I had to analyze and Memoize critical components of the code, including implementing efficient hooks, and optimizing database queries to improve the overall performance of the platform.

<br>

##### What I have gained

<br>

1. **Enhanced Technical and Problem-Solving Skills**: Through the process of successfully completing this project, I have significantly strengthened my technical skills, including proficiency in TypeScript, React 18, Tailwind CSS, and Superbase. Additionally, I have honed my problem-solving abilities by overcoming challenges and finding effective solutions.

2. **Motivation to Address other Real-World Problems**: This project has served as a catalyst for my motivation to explore and address other real-world problems.

3. **Increased Confidence**: Successfully completing a complex project like this has boosted my confidence as a developer. The knowledge and experience gained throughout the project have validated my skills and abilities, providing me with the confidence to take on more ambitious projects in the future. -->

<br>

##### Tech Stack used


React 18, Tailwind Css, TanStack Query, Supabase, Shadcn-UI, Zod



 {{< button label="View Project" link="https://freelance-ethiopia-clone.vercel.app/" style="solid" class="max-sm:text-sm mt-5" >}} 
    <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/freelance-ethiopia-clone" style="solid" class="max-sm:text-sm" >}} <span/>

<hr>

##### Arada dictionary


Introducing Arada Dictionary: your new spot to understand slang and informal talk! Ever felt lost in conversations because of unfamiliar words? I've been there too. That's why I decided to create Arada Dictionary. I couldn't find any reliable online resources for Amharic slang words and phrases, so I built one using Nextjs 14. 


Arada Dictionary isn't just about defining words. It's a place where everyone can help each other understand slang language. Think of it as a community-driven project where we all pitch in to keep up with the latest lingo. 

Imagine this: you're traveling to a new city, let's say Dire Dawa and suddenly, people are using words and phrases you've never heard before. It can feel isolating, right? That's where Arada Dictionary comes in. It's like having a local guide to the slang and informal language of different cities, helping you feel more connected no matter where you go.

<br>

##### Challenges Faced


During the development of this Nextjs project, I faced several challenges:
<br>

1. **Database Service Reliability** : 

Finding a reliable, free cloud PostgreSQL database service was difficult due to limitations such as frequent sleep cycles. This resulted in the need to restart my database connection repeatedly during development.


2. **keeping balance between caching and up-to date data**: 

Striking a balance between caching data for improved performance and avoiding stale data required me to think carefully. I used the revalidatePath function on my server actions only at the points where data can be mutated.

3. **Security Oversight** : 

 I recently made a mistake where I accidentally exposed sensitive database information due to client-side data fetching. I fully acknowledge that this was a significant security oversight for me. It prompted me to shift fetching data on server components securely and passing it to the client-side as props. ensuring that sensitive information remains protected.

4. **Email Service Limitations**: 

 The email service provider I used requires custom domain to send emials for different addresses. since I have no custom domain, it restricted the functionality to send emails to only one address (harunbekri6@gmail.com).


<br>

{{< gallery dir="images/arada" lightbox="true" height="200" width="400" carousel="true" autoplay="true" webp="true" command="Fit" zoomable="true" >}}

<br> 

##### Tech Stack used


Nextjs 14, Tailwind Css, Auth.js, Neon's Serverless Postgres , Shadcn-UI,  Zod,  Resend


{{< button label="View Project" link="https://arada-dictionary.vercel.app/" style="solid" class="max-sm:text-sm mt-5" >}} 
    <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/Arada-dictionary" style="solid" class="max-sm:text-sm" >}} <span/>

<hr>

##### Yegarabet


Introducing Yegarabet: Your Path for finding compatible roommates 


Nowdays living alone is the most expensive thing you can do. specially if you are a young adult like me. That's why I'm developing Yegarabet – a web app designed to connect individuals who want to share rooms and other expenses. Imagine the financial relief of sharing expenses with roommates compared to bearing the burden of solo living. 

With Yegarabet, you can significantly cut down on costs while still enjoying a comfortable and harmonious living environment. Share a home, Save you money. Yegarabet is currently in active development. Stay tuned for updates. 


{{< gallery dir="images/yegarabet" lightbox="true" carousel="true" autoplay="true" webp="true" command="Fit" zoomable="true" class="mt-10" >}}

<br>

##### Tech Stack used


Nextjs 14, Cloudinary, Mongodb, Prisma, Google reCAPTCHA



{{< button label="View Project" link="https://yegarabet.vercel.app/" style="solid" class="max-sm:text-sm mt-5" >}} 
  <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/Yegarabet" style="solid" class="max-sm:text-sm" >}} <span/>

<hr>

##### Face to Sticker Chrome extension

In an effort to broaden my skill set beyond web application development, I sought out new challenges. One such opportunity arose during the application process for a remote software developer position. I was tasked with creating a Chrome extension that generates fake credit card information, including card numbers, CVV codes, PINs, postal codes, and addresses. After successfully completing this challenge, I took on an additional challenge for fun intended for another developer. It was creating a Chrome extension that converts face images into AI-generated stickers. 

This project was particularly exciting to me as it combined my interest in artificial intelligence with frontend development. I encountered and resolved numerous technical issues along the way, which provided me valuable hands-on experience with image processing and AI integration. Ultimately, I successfully developed the extension, which transforms face images into creative and fun AI-generated stickers.

{{< image src="images/facetosticker.png" alt="before-and-after" height="360" width="700" class="mt-7">}}

<br>

{{< button label="source code" link="https://github.com/hariyebk/Face-to-Sticker-AI-chrome-extension" style="solid" class="max-sm:text-sm mt-5" >}}

<hr>


### Internship Experience


I got an internship opportunity at <a href="https:/`/www.trip.com/"> Trip.com </a> after applying through LinkedIn. During my internship, I had the privilege of working as a backend developer for 4 months, followed by 3 months as a frontend developer. This invaluable experience has allowed me to refine my skills in both areas of development and provided me with hands-on experience collaborating with a remote team.

<br>

##### Frontend Developer Intern | Trip.com | Remote

JUNE 2023 – AUGEST 2023


During my 3-month Internship, as a Frontend developer, I worked on an Internal Hotel Management Project that serves as a central hub for hotel staff, providing them with the necessary tools to efficiently manage check-ins, bookings, cabin availability, and guest information. One of my key responsibilities was to convert conceptual Figma mockups into user Interfaces using React, JavaScript styled components and Rechart library. 

I was able to create Layout for the cabin, booking, and guest management sections where It utilizes React’s compound component pattern to create a flexible and reusable Table structure. Additionally, I implemented a Visually intuitive home page dashboard powered by stats and charts to give insights on recent bookings and sales data.

<br>

{{< button label="View Certification" link="https://utfs.io/f/30b70780-9f9b-45e6-8f06-0ffd7f488646-4t070p.jpg" style="solid" class="max-sm:text-sm" >}} 

<br>
<br>
  
  **Note**

  If you experienced difficulties logging into the application, please consider that the project utilizes Superbase with a free plan as its backend. for resource utilization if the project is not active , There is a possibility that they may pause the project temporarily. If you really want to check it out, you can contact me and I will restart the project for you. Login credentials: email- harunbekri6@gmail.com, password: testtest1234
  


  {{< button label="View project" link="https://the-wild-oasis-hariyebk.vercel.app/" style="solid" class="max-sm:text-sm mt-5" >}} <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/The-Wild-Oasis" style="solid" class="max-sm:text-sm" >}} <span/>

   <hr>

##### Backend Developer Intern | Trip.com | Remote


MARCH 2023 – JUNE 2023


During my 4-month internship, as a Backend developer, I actively contributed to an exciting project assigned to me by my mentors. The aim of the project was to build an extensive selection of captivating tour packages tailored to meet the diverse needs and preferences of travelers. My primary focus was developing public and protected RESTful API endpoints using Express.js, while adhering to the Model-View-Controller (MVC) software architecture principle.


Security was a top priority throughout the development process, and I implemented a range of essential security features like HTTP Only Cookies and Cross-Site Scripting prevention measures by using Middleware's. I also designed compressive MongoDB database Schemas and Aggregation pipelines to efficiently handle various API requests.

</p>

{{< button label="View Certification" link="https://utfs.io/f/a7f6c7ea-d8a5-4e0b-8edb-a7d9a8d7add9-fviinp.jpg" style="solid" class="max-sm:text-sm mt-5" >}} <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/Natours" style="solid" class="max-sm:text-sm" >}} <span/>
 

<hr>



### Other Projects
<br>

##### Girum Pizza


A pizza delivery application where users can Browse through an extensive menu of delicious pizzas, Add their desired pizzas to the cart and track the status of their order as it goes through the preparation, delivery, and arrival process.

Tech-Stack - **React** , **Redux**, **Tailwindcss**


{{< button label="view project" link="https://girum-pizza.vercel.app/" style="solid" class="max-sm:text-sm mt-5" >}}  <span style = "margin-left: 30px;"> {{< button label="source code" link="https://github.com/hariyebk/Girum-Pizza" style="solid" class="max-sm:text-sm" >}} <span/>

<br>
<br>


##### EPL Insights


This project is designed to analyze the match results of the English Premier League for the 2018/2019 season. It takes input data from a CSV file containing match details and generates a comprehensive report summarizing the outcomes and statistics of the matches.

Tech-Stack - **Typescript**

</p>

<br>

<span style = "display: flex; gap: 20px;">
{{< button label="source code" link="https://github.com/hariyebk/EPLInsights" style="solid" class="max-sm:text-sm" >}}</span>

<hr>
<br>

{{< button label="Download Resume (PDF)" link="https://utfs.io/f/0f0f673b-2e47-427d-bfda-e95a83fd449e-t2e56u.pdf" target="_blank" style="solid" class="max-sm:text-sm" >}}

<br>
