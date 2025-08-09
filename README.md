```html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishimwe Egîdë - Portfolio</title>

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #4facfe, #00f2fe);
            color: #333;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 15px 0;
        }

        .container {
            width: 80%;
            max-width: 1200px;
            margin: auto;
        }

        .logo {
            float: left;
            font-size: 24px;
            font-weight: bold;
        }

        nav {
            float: right;
        }

        nav ul {
            list-style: none;
        }

        nav ul li {
            display: inline;
            margin-left: 20px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        #home {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 100px 0;
            background-color: rgba(235, 243, 252, 0.9);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-top: 50px;
        }

        .home-content h2, .home-content h3 {
            color: #333;
        }

        .home-content p {
            color: #555;
        }

        .btn {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border-radius: 5px;
            text-decoration: none;
            display: inline-block;
            margin-top: 10px;
        }

        .profile-image img {
            max-width: 500px;
            border-radius: 10px;
        }

        section {
            padding: 60px 0;
        }

        #profile .profile-details,
        #profile .additional-info {
            margin-bottom: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .home-extra {
    margin-top: 20px;
    padding: 10px 0;
    color: #333;
}

.home-extra ul {
    list-style: none;
    padding: 0;
}

.home-extra ul li {
    font-size: 1.2rem;
    margin: 10px 0;
    display: flex;
    align-items: center;
}

#skills {
    padding: 60px 0;
    background: linear-gradient(135deg, #74a7f5 0%, #6cddff 100%); /* Reuse home background */
    color: #eee8e8; /* Ensure text is visible */
    text-align: center;
    border-radius: 10px;
    box-shadow: 0 9px 8px rgba(0, 0, 0, 0.1);
    margin-top: 20px;
}

#skills h2 {
    font-size: 2rem;
    color: #fff; /* Adjust text color to match new background */
    margin-bottom: 20px;
    text-transform: uppercase;
    font-weight: bold;
}

#skills ul {
    list-style: none;
    padding: 0;
    margin: 0 auto;
    max-width: 600px; /* Center and limit width */
}

#skills ul li {
    background-color: rgba(255, 255, 255, 0.1); /* Semi-transparent background for contrast */
    color: #fff;
    font-size: 1.2rem;
    padding: 15px;
    margin: 10px 0;
    border-radius: 5px;
    display: flex;
    align-items: center;
    gap: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    text-align: left; /* Align text to the left */
}

#skills ul li i {
    font-size: 1.5rem;
    flex-shrink: 0; /* Prevent icon from resizing */
}

#skills ul li:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
    background-color: rgba(255, 255, 255, 0.2); /* Highlight effect */
}

  /* Projects Section */
  #projects {
            background-color: rgba(255, 255, 255, 0.9);
            padding: 60px 0;
        }

        #projects h2 {
            text-align: center;
            margin-bottom: 40px;
            font-size: 2rem;
            color: #007bff;
        }

        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .course-card {
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 20px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .course-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
        }

        .course-card .course-image {
            text-align: center;
            margin-bottom: 20px;
        }

        .course-card .course-image i {
            font-size: 3rem;
            color: #007bff;
        }

        .course-card h3 {
            font-size: 1.5rem;
            color: #333;
            margin-bottom: 10px;
        }

        .course-card p {
            color: #555;
            margin-bottom: 10px;
        }

        .course-card .price {
            font-weight: bold;
            color: #007bff;
        }

        .course-card .enroll-btn,
        .course-card .download-btn {
            margin-top: 10px;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            text-align: center;
            text-decoration: none;
            cursor: pointer;
            font-size: 0.9rem;
            display: block;
        }

        .course-card .enroll-btn:hover,
        .course-card .download-btn:hover {
            background-color: #0056b3;
        }

        .course-card .download-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }


        .connect-with-us {
            text-align: center;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            box-shadow: 7px 4px 10px rgba(0, 0, 0, 0.1);
        }

        .connect-with-us h2 {
            font-size: 2rem;
            color: #0c1114;
            margin-bottom: 0.5rem;
        }

        .connect-with-us p {
            font-size: 1rem;
            color: #010202;
            margin-bottom: 1.5rem;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }

        .social-link {
            color: #fff;
            background-color: #007bff;
            font-size: 1.5rem;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            text-decoration: none;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .social-link:hover {
            transform: scale(1.1);
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 20px 0;
            margin-top: 20px;
        }

        footer p {
            margin: 0;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1 class="logo">Ishimwe Egîdë</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#profile">Profile</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <section id="home">
        <div class="container">
            <div class="home-content">
                <h2>Hi, I'm Ishimwe Egîdë.</h2>
                <h3>Software Engineer</h3>
                <p>Based in Kigali, Nyarugenge, Kimisagara</p>
                <a href="#contact" class="btn">Hire Me</a>

            </div>
            <div class="profile-image">
                <img src="DSC_2858.JPG" alt="Ishimwe Egîdë Profile">
            </div>
        </div>
    </section>
    

    <section id="profile">
        <div class="container">
            <h2>Personal Profile</h2>
            <div class="profile-details">
                <p><strong>Name:</strong> Ishimwe Egîdë</p>
                <p><strong>Field of Study:</strong> Software Engineering</p>
                <p><strong>University:</strong> Adventist of Central Africa (AUCA), Year 2</p>
                <p><strong>Location:</strong> Kimisagara, Kigali, Rwanda</p>
            </div>

            <div class="additional-info">
                <h3>Digital Tools</h3>
                <p>In my studies, I use various digital tools, especially development environments, version control systems like Git, and cloud platforms to enhance my software engineering skills.</p>

                <h3>Expectation for the Course</h3>
                <p>I aim to deepen my understanding of database development with PL/SQL, focusing on efficiently managing and designing databases in real-world applications.</p>

                <h3>Unique Fact</h3>
                <p>I have a passion for building innovative software solutions that can solve everyday challenges in my community.</p>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2>Skills</h2>
            <ul>
                <li><i class="fas fa-code"></i> Software Development</li>
                <li><i class="fas fa-laptop-code"></i> Web Development</li>
                <li><i class="fas fa-database"></i> Database Management</li>
                <li><i class="fas fa-mobile-alt"></i> Mobile App Development</li>
                <li><i class="fas fa-paint-brush"></i> Web Design</li>
                <li><i class="fas fa-tools"></i> Proficient in various computer applications</li>
            </ul>
        </div>
    </section>
    

    <section id="projects">
        <div class="container">
            <h2>Projects</h2>
            <div class="projects-container">
                <!-- Project Card 1 -->
                <div class="course-card">
                    <div class="course-image">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>Healthcare Management System</h3>
                    <p>A system designed for efficient management of healthcare records and operations.</p>
                    <p class="price">Free</p>
                    <a href="#" class="enroll-btn">Enroll Now <i class="fa-solid fa-arrow-right"></i></a>
                    <a href="#" class="download-btn">
                        <i class="fas fa-download"></i> Download Materials
                    </a>
                </div>
                <!-- Project Card 2 -->
                <div class="course-card">
                    <div class="course-image">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3>Housing and Rental Platform</h3>
                    <p>A web-based platform to browse and manage rental properties in Kigali.</p>
                    <p class="price">Free</p>
                    <a href="#" class="enroll-btn">Enroll Now <i class="fa-solid fa-arrow-right"></i></a>
                    <a href="#" class="download-btn">
                        <i class="fas fa-download"></i> Download Materials
                    </a>
                </div>
                <!-- Project Card 3 -->
                <div class="course-card">
                    <div class="course-image">
                        <i class="fas fa-dumbbell"></i>
                    </div>
                    <h3>Fitness Tracking System</h3>
                    <p>An application to track fitness activities and manage health goals.</p>
                    <p class="price">Free</p>
                    <a href="#" class="enroll-btn">Enroll Now <i class="fa-solid fa-arrow-right"></i></a>
                    <a href="#" class="download-btn">
                        <i class="fas fa-download"></i> Download Materials
                    </a>
                </div>
                <!-- Project Card 4 -->
                
            </div>
        </div>
    </section>

    <section class="connect-with-us">
        <h2>Contact Me</h2>
        <p>Feel free to reach out to me through the following platforms:</p>
        <div class="social-icons">
          <a href="https://web.facebook.com/ishimwe.kwibuka/" target="_blank" class="social-link">
            <i class="fab fa-facebook-f"></i>
          </a>
          <a href="https://twitter.com" target="_blank" class="social-link">
            <i class="fab fa-twitter"></i>
          </a>
          <a href="https://www.instagram.com/__k.w.i.b.u.k.a_/" target="_blank" class="social-link">
            <i class="fab fa-instagram"></i>
          </a>
          <a href="https://www.linkedin.com/in/ishimwe-egide-56926132a/" target="_blank" class="social-link">
            <i class="fab fa-linkedin-in"></i>
          </a>
          <a href="https://youtube.com" target="_blank" class="social-link">
            <i class="fab fa-youtube"></i>
          </a>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 Ishimwe Egîdë. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```
