
# **AI Blog Generator**

This project utilizes artificial intelligence (AI) to generate blog posts based on user-provided titles. It integrates with Pexels API for fetching images and Google's GenAI model for generating content. The generated blog posts are then posted to a Blogger platform using the Google Blogger API.

## Features
Generate attractive blog post titles based on user input.
Create high-quality blog content using Google's GenAI model.
Fetch relevant images from Pexels API based on generated keywords.
Post generated blog content to a Blogger platform automatically.
## Prerequisites
Before running the application, ensure you have the following installed:

        Python >=3.10
        git
- You need to have a blogger account, if you don't have one create one at https://blogger.com/ and get `BLOG_ID`.
- Copy the blogid from the url https://www.blogger.com/blog/posts/BLOG_ID

## Installation
**Clone the repository:**

    git clone https://github.com/sree-charan/ai-blog-generator.git

**Navigate to the project directory:**

    cd ai-blog-generator

**Install dependencies:**

    pip install -r requirements.txt

### Obtain API keys:

- Get a Pexels API key from Pexels API.
- Obtain a Gemini API from https://aistudio.google.com/app/apikey
- Download a client secrets file for the Google Blogger API and name it config.json.
#### Here's how to download a client secrets file for the Google Blogger API and name it config.json:**

1. Enable the Blogger API:

- Visit the Google Cloud Console: https://console.cloud.google.com/ and log in with your Google account.

- If this is your first time using the Console, you might need to create a new project. You can find instructions on doing so in the Console itself.

- Once you're in your project, navigate to the APIs & Services section in the left-hand menu.

- In the search bar, type "Blogger API" and select it from the results.

- Click on "ENABLE" to activate the Blogger API for your project.

2. Create Client Credentials:

- In the left-hand menu, navigate to Credentials and then select OAuth client ID.

- Now, select "Create credentials" and choose "OAuth client ID".

- In the application type dropdown menu, pick "Web app".

- For the `redirect_uris` field type http://localhost:8080/

- Click "Create" and a popup window will appear.

- Click "Download JSON" to download a file containing your client secrets. This file will be automatically named something like "client_secret_desktop.json".

3. Rename the Downloaded File:

- Locate the downloaded file (usually in your Downloads folder).

- Rename the downloaded file (e.g., "client_secret_desktop.json") to "config.json".

## Usage
Set the obtained API keys and client secrets file path in the app.py file:

    PEXELS_API_KEY = "YOUR_PEXELS_API_KEY"
    GOOGLE_API_KEY = "GEMINI_API_KEY"
    CLIENT_SECRET = 'config.json'

Replace YOUR_BLOG_ID with the value from your blogger
            

    BLOG_ID = 'YOUR_BLOG_ID'

## Run the Flask application:

    flask run
Access the application in your web browser at http://localhost:5000.

Enter a title for your blog post and click on "Generate and Post" to generate content and post it to the Blogger platform.


## Screenshots

![App Screenshot](https://blogger.googleusercontent.com/img/a/AVvXsEh2qZeXhqTVYk-0o5t0Fm8OezQqguDGgUsWzADxY-sf2hizQpjvPtjclXJJAdfURL4Ecblt2ocCoD3xtRc718RG4RcLpTe8EBUnd01yEH9DQ0Vd7b2qjfPUpTKFQesJH81d-nzVwFjix9Y150m7LgOFnILo9rJIiMB5HmlGOxm8_x0y4736tUezGh049KAU)

![App Screenshot](https://blogger.googleusercontent.com/img/a/AVvXsEjZbcffgUWdvdnkNyI79IBsyCiwxvNuB9I9J1LdKECadpUZJ5RjKAWsDXQJZMVCcX-sdv26OeBTcGuEYDQphbiEGnliNUQ4kV_xJ-bCTlYvX5mZ2BZLzv-ZNVUY5MWvmOJs9i4DR9VtoiSn0me8OWW2bhbUNvBxph4Bp1hQlK4JF0xAXqecL3BEHDLCVxeq)

![App Screenshot](https://blogger.googleusercontent.com/img/a/AVvXsEjngC2BlE6FSIayVtHlhUEre91CZNjWSMnmSdUphGuXqya77VzOpJ9etzNk-7g09Qs1e2mO6_ndG02G6UdINRwz_LDqepuMX_bYuBq9u0ZJWz7jp7ZknYQEd_r6GBQzejL_kE1RCkaxhtkYATaU8YVHt0VOSKlJP1Iogz7XHlq70eDyxknmgSwJMXE5uNSK)

![App Screenshot](https://blogger.googleusercontent.com/img/a/AVvXsEg1tzLTgK-wleNiReNHrZdePeACuRqr0D0pstNXdEE_lE7GWAK0x6jyQakntg9RMjo8kN4paJICgiYD-h6yxqfDvKFrIXuYACVOg2v3o1bZ7SLqSP8YtFJLChUbPeRdAwV_Diy-Ju38wRqS62dQzFUf7TqHTrExct13RI-sO1H_rFtpAOF-mBjHKh0gF_Ip)