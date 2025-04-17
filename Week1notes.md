# 🗓️ Week 1: HTML Basics Summary
## 📄 1. HTML Document Structure
- Every HTML file starts with `<!DOCTYPE html>`
- Basic tags: `<html>`, `<head>`, `<body>`. Every HTML document begins with `<html>` and ends with `</html>`.
- HTML tags are declared as <tagname>..content..</tagname>
- `<br>` is an empty tag for a line break. `<hr>` is an empty tag for a horizontal rule in a page.
- The `<head>` contains metadata, title, favicon, etc.
- The `<body>` holds all visible content.
- The `<img>` tag is used to define images with the src(image source file) , alt(alternate text) , width and height(always specify the width and height) attributes.
- The favicon is the small icon that is visible on the page tab on the browser and is placed in the <head> tag.
- Use `<video>` and `<audio>` tags with controls to add media. You can autoplay, mute and loop as needed.
- The `<iframe>` tag embeds a YouTube video directly into a webpage.
- Forms are used to collect user input like text, passwords, selections.
- Lists are used to display items in a structured format. Lists can be ordered `<ol>`, unordered `<ul>`, nested(lists within lists) or description lists `<dl>`. 
- Each item in a list is the defined by the `<li>` tag. The ordered list has a type attribute that defines the type of item marker.
- The `<table>` element is used to define a table. `<td>` tag defines table cells. `<tr>` tag defines the table row. `<th>` tag defines table headers, bolded by default.
### Example
```html
<!DOCTYPE html>
<html>
   <head>
        <meta charset="UTF-8"> <!-- UTF-8 is a character encoding that represents vast range of characters and ensures global support -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- this makes the page responsive on all screen sizes -->
        <title>A well structured html document</title> <!-- this is what will be displayed in the page tab -->
        <meta name="description" content="This html document implements lists, tables, forms and input types"> <!-- this describes the page content for Search Engines -->
        <style> 
            body{
                background-color: black; /* sets the background color of the entire page to black*/
                color: white; /* sets the text color of the page to white*/
            }
        </style>
    </head>
    <body>
        <h1>HTML5 elements and forms</h1> <!-- this is the first heading, written only once -->
        <ol type="I"> /*the type used is for uppercase Roman numerals*/
            <li>images</li>
            <li>lists</li>
            <li>tables</li>
            <li>forms</li>
            <li>input types</li> 
            <li>multimedia</li>  
        </ol>
            <h2>Image </h2>
            <img src="https://images.pexels.com/photos/6907077/pexels-photo-6907077.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="German Shepherd Puppy" width="300" height="300">

            <h2>Video</h2>
            <iframe width="800" height="300" <!-- the video frame size is set -->
            <!-- the video will automatically start playing at 110 seconds, but is muted -->
            src="https://www.youtube.com/embed/5-MbjJVq_HI?start=110&autoplay=1&mute=1" 
            ></iframe>
    
            <h2>Table </h2>
            <style> 
                table, th, td {
                    border: 1px solid white; /*adds a white border of 1px thickness to table elements*/
                    border-collapse: collapse; /* collapses the border into a single one*/
                    padding: 4px; /* adds space inside the cells for better readability*/

                }

            </style>
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Address</th>
                        <th>Mobile</th>
                        <th>Emails</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Hailey Boss</td>
                        <td>Kisumu</td>
                        <td>0745678901</td>
                        <td>haileyboss5@gmail.com</td>
                    </tr>
                </tbody>
            </table>
            <br>
            <h2>Form</h2>
            <form>
                <label for="name">Name:</label><br>
                <input type="text" id="name" name="name" required><br>

                <label for="email">Email:</label><br>
                <input type="email" id="email" name="email" placeholder="example@gmail.com" required><br>

                <label for="password">Password:</label><br>
                <input type="password" id="password" name="password" placeholder="Enter your password" required><br>

                <label for="date">Date:</label><br>
                <input type="date" id="date" name="date" required><br>
                
                <label for="country">Country:</label><br>
                <select id="country" name="country">
                    <option value="Kenya">Kenya</option>
                    <option value="Uganda">Uganda</option>
                    <option value="Tanzania">Tanzania</option>
                    <option value="Burundi">Burundi</option>
                </select><br>
                <label for="gender">Gender:</label><br>
                <input type="radio" id="male" name="gender" value="male">
                <label for="male">Male</label><br>
                <input type="radio" id="female" name="gender" value="female">
                <label for="female">Female</label><br>
                <input type="radio" id="I prefer not to say" name="gender" value="I prefer not to say">
                <label for="I prefer not to say">I prefer not to say</label><br>

                <label for="Hobbies">Hobbies:</label><br>
                <input type="checkbox" id="reading" name="hobbies" value="reading">
                <label for="reading">Reading</label><br>
                <input type="checkbox" id="painting" name="hobbies" value="painting">
                <label for="painting">Painting</label><br>
                <input type="checkbox" id="coding" name="hobbies" value="coding">
                <label for="coding">Coding</label><br>
                <br>

                <input type="submit" value="submit">
                
            </form>
    </body>
</html>



