---
layout: page
title: Contact
permalink: /contact/
---

<div class="contact-content">
    <div>
        <i class="fas fa-envelope fa-3x"></i>
        <h3>Email</h3>
        <p><a href="mailto:mariusz.michna.j@gmail.com">mariusz.michna.j@gmail.com</a></p>
    </div>
    <div>
        <i class="fab fa-linkedin fa-3x"></i>
        <h3>LinkedIn</h3>
        <p><a href="https://www.linkedin.com/in/mariusz-michna-6a2599193/" target="_blank">My LinkedIn Profile</a></p>
    </div>
    <div>
        <i class="fab fa-github fa-3x"></i>
        <h3>GitHub</h3>
        <p><a href="https://github.com/MariuszJM" target="_blank">My GitHub Profile</a></p>
    </div>
</div>

<style>
.contact-content {
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
    text-align: center;
    flex-wrap: wrap;
    margin-top: 20px;
    padding: 20px;
    width: 100%;
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
}

.contact-content div {
    margin: 20px;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 10px;
    transition: transform 0.3s, background-color 0.3s;
}

.contact-content div:hover {
    transform: scale(1.05);
    background-color: #f0f0f0;
}

.contact-content i {
    color: #007acc;
    margin-bottom: 10px;
    transition: color 0.3s;
}

.contact-content div:hover i {
    color: #005bb5;
}

.contact-content h3 {
    margin: 10px 0;
    font-size: 1.8rem;
    font-weight: bold;
}

.contact-content p {
    font-size: 1.2rem;
    margin-bottom: 10px;
    color: #555;
}

.contact-content a {
    color: #007acc;
    text-decoration: none;
    font-weight: bold;
}

.contact-content a:hover {
    text-decoration: underline;
}

@media (max-width: 768px) {
    .contact-content {
        flex-direction: column;
    }

    .contact-content div {
        width: 100%;
        margin: 10px 0;
    }
}
</style>
