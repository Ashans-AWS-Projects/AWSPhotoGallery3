# Photo Gallery Web Application

![Photo Gallery Banner](https://user-images.githubusercontent.com/yourprofile/photo-gallery-banner.png)

## 🌟 Overview

This project is a web-based Photo Gallery application built with HTML, CSS, and Python. The application allows users to upload, search, and view details of photos stored in a database. It also provides the ability to manage photos, including adding descriptions, tags, and viewing metadata such as EXIF data.

## 📋 Table of Contents

- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Key Features](#key-features)
  - [Photo Upload](#photo-upload)
  - [Photo Search](#photo-search)
  - [Photo Details](#photo-details)
- [Screenshots](#screenshots)
- [Contributors](#contributors)
- [License](#license)

## 🚀 Introduction

The Photo Gallery application provides a platform to manage and browse a collection of photos. Users can upload photos, search through them using keywords, and view detailed information about each photo, including tags and EXIF metadata. The application is designed with a responsive UI, ensuring a seamless experience across devices.

## 🛠️ Technologies Used

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
![Jinja2](https://img.shields.io/badge/Jinja2-B41717?style=for-the-badge&logo=jinja2&logoColor=white)

## 🗂️ Project Structure

Here’s an overview of the project structure:

```plaintext
├── assets/
│   ├── css/
│   ├── img/
│   └── js/
├── templates/
│   ├── index.html           # Home page listing all photos
│   ├── form.html            # Photo upload form
│   ├── photodetail.html     # Detailed view of a single photo
│   └── search.html          # Search results page
├── app.py                   # Main Flask application file
├── env.py                   # Environment setup for the application
├── photo-table.py           # Photo management logic
├── sqlcommands.sql          # SQL commands to set up and manage the database
└── README.md                # Project documentation
```

## 🛠️ Setup and Installation

### Prerequisites

- **Python**: Ensure Python 3.x is installed.
- **pip**: Use pip to install Python dependencies.

### Installation Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/photo-gallery.git
   cd photo-gallery
   ```

2. **Set up the environment**:
   ```bash
   python -m venv env
   source env/bin/activate   # On Windows use `env\Scripts\activate`
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database**:
   - Run the SQL commands in `sqlcommands.sql` to create the necessary tables.

5. **Start the application**:
   ```bash
   python app.py
   ```

## ✨ Key Features

### 📸 Photo Upload

Users can upload photos via the **Upload Photo** form. Each photo can have a title, description, and tags associated with it. The form is located at `/add` and is defined in `form.html`.

```html
<form method='post' action="/add" enctype="multipart/form-data">
    <input type="file" name="imagefile" class="form-control">
    <input type="text" name="title" class="form-control" placeholder="Title">
    <textarea name="description" class="form-control" rows="3" placeholder="Description"></textarea>
    <input type="text" name="tags" class="form-control" placeholder="Tags">
    <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

### 🔍 Photo Search

Search functionality allows users to find photos by keywords. The search bar is included in `index.html` and `search.html`.

```html
<form method='get' action="/search">
    <input type="text" name="query" class="form-control" placeholder="Search photos">
</form>
```

### 📋 Photo Details

Each photo has a detailed view accessible by clicking on the photo title from the main gallery or search results. This view, defined in `photodetail.html`, displays the photo, description, tags, and EXIF metadata.

```html
<img class="img-responsive" src="{{photo.URL}}" alt="">
<h2>{{photo.Title}}</h2>
<p>{{photo.Description}}</p>
<p>Tags: {{photo.Tags}}</p>
<p>Uploaded: {{photo.CreationTime}}</p>
```

## 📸 Screenshots

![Home Page](https://user-images.githubusercontent.com/yourprofile/homepage-screenshot.png)
*The homepage of the Photo Gallery application.*

![Upload Photo](https://user-images.githubusercontent.com/yourprofile/upload-screenshot.png)
*The form used for uploading new photos.*

![Photo Details](https://user-images.githubusercontent.com/yourprofile/photo-details-screenshot.png)
*Detailed view of a single photo.*

## 👥 Contributors

- **Your Name** - *Initial work*

