---
layout: default
title: Blog Website
---

<header>
    <h1>{{ site.title }}</h1>
</header>
<nav>
    <a href="{{ '/' | relative_url }}">Home</a>
    <a href="{{ '/about/' | relative_url }}">About</a>
    <a href="{{ '/contact/' | relative_url }}">Contact</a>
</nav>
<div class="container">
    <div class="search-bar">
        <input type="text" placeholder="Search for blogs...">
        <button>Search</button>
    </div>
    {% for post in site.posts %}
    <div class="blog-post">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p><strong>Posted on:</strong> {{ post.date | date: "%B %d, %Y" }}</p>
        <p>{{ post.excerpt }}</p>
        <div class="comment-section">
            <h3>Leave a Comment:</h3>
            <textarea rows="4" placeholder="Write your comment here..."></textarea>
            <button>Post Comment</button>
        </div>
    </div>
    {% endfor %}
    <div class="subscription-section">
        <h3>Subscribe for Exclusive Content:</h3>
        <p>Become a member for only $5/month and gain access to premium blogs and features!</p>
        <button onclick="subscribe()">Subscribe Now</button>
    </div>
</div>
<footer class="footer">
    <p>&copy; {{ site.time | date: "%Y" }} {{ site.title }}. All Rights Reserved.</p>
</footer>
<script>
    function subscribe() {
        alert('Subscription functionality will be added soon!');
    }
</script>


