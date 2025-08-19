# Aniruddha Saha's Academic Webpage (Based on Martin Saveski's template)

## [PLEASE READ] Instructions for cloning this

P.S. - I used Gemini AI for suggestions because what I did a few years back might be outdated.

### Change the Google Analytics information.
Adding Google Analytics to GitHub Pages, especially for Jekyll-based sites, involves embedding the Google Analytics tracking code into your site's files. 
For Jekyll-based GitHub Pages sites: 

- Obtain Google Analytics Measurement ID: 
	- Log in to your Google Analytics account. 
	- Create a new property for your GitHub Pages website if you haven't already. 
	- Locate and note down your Measurement ID (e.g., G-XXXXXXXXXX). 

- Create an include file for the tracking code: 
	- In your Jekyll project, create a new file named analytics.html inside the _includes directory. If the _includes directory doesn't exist, create it. 

- Add the Google Analytics tracking code: 
	- Paste the Google Analytics tracking code snippet into the _includes/analytics.html file. This snippet typically includes your Measurement ID. An example of the code structure is: 

  ```
  <script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_MEASUREMENT_ID"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'YOUR_MEASUREMENT_ID');
  </script>
  ```

Replace YOUR_MEASUREMENT_ID with your actual Measurement ID. 

- Include the tracking code in your layout: 
	- Open your site's default layout file, typically located at _layouts/default.html. 
	- Just before the closing &lt;/head&gt; tag, add the following line to include the analytics.html file: 

        {% include analytics.html %}

- Commit and push changes: 
	- Save the changes to your files. 
	- Commit the changes to your local repository and push them to your GitHub Pages repository. 

### Verification of website
To verify your website ownership with Google Search Console using an HTML verification file, follow these steps: 

- Access Google Search Console: Log in to your Google Search Console account. 
- Add a Property: Click on "Add Property" and enter the full URL of your website (e.g., https://www.example.com) in the URL prefix property type. Click "Continue." 
- Download the HTML Verification File: On the "Verify ownership" window, select the "HTML file upload" method. You will be prompted to download a unique HTML verification file (e.g., google[unique-alphanumeric-string].html). Save this file to your computer. 
- Upload the File to Your Website's Root Directory: Use an FTP client or your website's file manager (often found in your hosting control panel like cPanel) to upload the downloaded HTML file to the root directory of your website. The root directory is the highest-level directory where your website's main files (like index.html or wp-config.php for WordPress sites) are located. 
- Verify the File's Accessibility: Open a web browser and navigate to the URL where you uploaded the file (e.g., https://www.example.com/google[unique-alphanumeric-string].html). Ensure that the file is publicly accessible and can be viewed in your browser. 
- Complete Verification in Search Console: Return to Google Search Console and click the "Verify" button on the ownership verification page. Google will then check for the presence of the uploaded file and, if found, will verify your site ownership. 

## External Libraries
- Framework: [Jekyll](http://jekyllrb.com/)
- CSS
  - [Skeleton](getskeleton.com)
  - Tabs: [Skeleton Tabs](https://github.com/nathancahill/skeleton-tabs)
  - Experience: [Timeline](https://codepen.io/NilsWe/pen/FemfK)
  - Icons: [Font Awesome](http://fontawesome.io/)
- JS
  - [Jquery (3.7.1)](https://jquery.com/)
