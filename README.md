# Coding-Raja-Technologies-Internship

This is the code for a RESUME BUILDER website. It shows clearly the available templates to choose from and download options like pdf and word.

<!DOCTYPE html>
<html>
<head>
    <title>Resume Builder</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        .resume-template {
            margin-bottom: 20px;
            padding: 20px;
            border: 1px solid #ccc;
            background-color: #f9f9f9;
        }

        .resume-template .header {
            margin-bottom: 20px;
        }
        
        .resume-template .header h1 {
            margin: 0;
            font-size: 24px;
        }
        
        .resume-template .header p {
            margin: 5px 0 0;
            font-size: 18px;
            color: #666;
        }
        
        .resume-template .section {
            margin-bottom: 20px;
        }
        
        .resume-template .section h2 {
            margin-bottom: 10px;
            font-size: 20px;
        }
        
        .resume-template ul {
            list-style-type: none;
            padding-left: 0;
        }
        
        .resume-template ul li {
            margin-bottom: 5px;
            font-size: 16px;
        }

        /* Template 1: Modern */
        #template1 {
            background-color: #dfacf6;
        }

        #template1 .header {
            background-color: white;
            color: black;
            padding: 10px;
            border-radius: 5px 5px 0 0;
        }

        #template1 .section {
            border: 1px solid #ccc;
            border-top: none;
            border-radius: 0 0 5px 5px;
        }

        /* Template 2: Creative */
        #template2 {
            background-color: #f8f9fa;
        }

        #template2 .header {
            background-color: #28a745;
            color: rgb(220, 218, 218);
            padding: 10px;
            border-radius: 5px 5px 0 0;
        }

        #template2 .section {
            border: 1px solid black;
            border-top: none;
            border-radius: 0 0 5px 5px;
        }
    </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-dark bg-dark">
    <span class="navbar-brand mb-0 h1">Resume Builder</span>
</nav>

<div class="container mt-4">
    <div class="row">
        <div class="col-md-4">
            <!-- Template Selection -->
            <div class="card">
                <div class="card-header">Choose Template</div>
                <div class="card-body">
                    <div class="form-group">
                        <label for="templateSelect">Select Template:</label>
                        <select id="templateSelect" class="form-control">
                            <option value="template1">Template 1 (Modern)</option>
                            <option value="template2">Template 2 (Creative)</option>
                            <!-- Add more template options as needeed--->
                        </select>
                    </div>
                </div>
            </div>
            <!-- Download Options -->
            <div class="card mt-3">
                <div class="card-header">Download Options</div>
                <div class="card-body">
                    <div class="form-group">
                        <label for="downloadFormat">Select Format:</label>
                        <select id="downloadFormat" class="form-control">
                            <option value="pdf">PDF</option>
                            <option value="word">Word</option>
                        </select>
                    </div>
                    <button type="button" id="downloadBtn" class="btn btn-primary">Download Resume</button>
                </div>
            </div>
        </div>
        <div class="col-md-8">
            <!-- Resume Form -->
            <form id="resumeForm">
                <div class="card">
                    <div class="card-header">Resume Information</div>
                    <div class="card-body">
                        <!-- Add form fields for personal information, education, work experience, skills, etc. -->
                        <!-- Example field -->
                        <div class="form-group">
                            <label for="firstName">First Name:</label>
                            <input type="text" id="firstName" class="form-control" required>
                            <label for="lastname">Last Name:</label>
                            <input type="text" id="firstName" class="form-control" required>
                            <label for="firstName">Occupation(can be Student):</label>
                            <input type="text" id="firstName" class="form-control" required>
                            <label for="firstName">Education:</label>
                            <input type="text" id="firstName" class="form-control" required>
                        </div>
                        <!-- Add more form fields as needed -->
                    </div>
                </div>
                <!-- Preview Section -->
                <div class="card mt-3">
                    <div class="card-header">Preview</div>
                    <div class="card-body">
                        <div id="previewArea"></div>
                    </div>
                </div>
            </form>
        </div>
    </div>
</div>

<!-- Resume Template 1: Modern -->
<div id="template1" class="resume-template">
    <div class="header">
        <h1 id="fullName">John Doe</h1>
        <p id="jobTitle">Web Developer</p>
    </div>
    <div class="section">
        <h2>Education</h2>
        <ul id="educationList">
            <li>Bachelor of Science in Computer Science - ABC University</li>
            <li>Web Development Bootcamp - XYZ Coding School</li>
        </ul>
    </div>
    <div class="section">
        <h2>Experience</h2>
        <ul id="experienceList">
            <li>Senior Frontend Developer - Tech Solutions Inc.</li>
            <li>Web Developer Intern - ABC Company</li>
        </ul>
    </div>
    <div class="section">
        <h2>Skills</h2>
        <ul id="skillsList">
            <li>HTML5, CSS3, JavaScript</li>
            <li>React, Angular, Vue.js</li>
            <li>Node.js, Express.js, MongoDB</li>
        </ul>
    </div>
</div>

<!-- Resume Template 2: Creative -->
<div id="template2" class="resume-template">
    <div class="header">
        <h1 id="fullName">Jane Smith</h1>
        <p id="jobTitle">Graphic Designer</p>
    </div>
    <div class="section">
        <h2>Education</h2>
        <ul id="educationList">
            <li>Bachelor of Fine Arts in Graphic Design - Art Institute</li>
            <li>Graphic Design Certification - Design Academy</li>
        </ul>
    </div>
    <div class="section">
        <h2>Experience</h2>
        <ul id="experienceList">
            <li>Senior Graphic Designer - Creative Agency</li>
            <li>Freelance Graphic Designer</li>
        </ul>
    </div>
    <div class="section">
        <h2>Skills</h2>
        <ul id="skillsList">
            <li>Adobe Photoshop, Illustrator, InDesign</li>
            <li>UI/UX Design, Branding</li>
            <li>Typography, Illustration</li>
        </ul>
    </div>
</div>

<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.9.2/html2pdf.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.0/FileSaver.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.7.1/jszip.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/docxtemplater/3.21.1/docxtemplater.js"></script>
<script>
    // JavaScript code for dynamic form handling, preview functionality, and downloading resume
    $(document).ready(function() {
        // Function to update preview based on form inputs and selected template
        function updatePreview() {
            // Get form values
            var firstName = $('#firstName').val();
            var lastName = $('#lastName').val();
            var occupation = $('#occupation').val();
            var education = $('#education').val();
            
            // Update preview area with form values
            var selectedTemplate = $('#templateSelect').val();
            var previewContent = $('#' + selectedTemplate).html();
            previewContent = previewContent.replace('{{firstName}}', firstName);
            previewContent = previewContent.replace('{{lastName}}', lastName);
            previewContent = previewContent.replace('{{occupation}}', occupation);
            previewContent = previewContent.replace('{{education}}', education);
            $('#previewArea').html(previewContent);
        }
        
        // Event listener for form inputs change
        $('#resumeForm input').on('input', function() {
            updatePreview();
        });
        
        // Event listener for template selection change
        $('#templateSelect').on('change', function() {
            // Update preview when template changes
            updatePreview();
        });
        
        // Event listener for download button click
        $('#downloadBtn').on('click', function() {
            // Get resume content from preview area
            var resumeContent = $('#previewArea').html();
            // Get selected download format
            var downloadFormat = $('#downloadFormat').val();
            // Download resume based on selected format
            if (downloadFormat === 'pdf') {
                // Generate PDF and download
                html2pdf().from($('#previewArea')[0]).save('resume.pdf');
            } else if (downloadFormat === 'word') {
                // Generate Word document and download
                var content = $('#previewArea').html();
                var zip = new JSZip();
                var doc = new window.docxtemplater();
                doc.loadZip(new JSZip(content));
                doc.loadZip(new JSZip(content));
                var data = doc.getZip().generate({type: 'blob'});
                saveAs(data, 'resume.docx');
            }
        });
    });
</script>
<script>
    // JavaScript code for dynamic form handling, preview functionality, and downloading resume
    $(document).ready(function() {
        // Function to update preview based on form inputs and selected template
        function updatePreview() {
            // Get form values
            var firstName = $('#firstName').val();
            var lastName = $('#lastName').val();
            var occupation = $('#occupation').val();
            var education = $('#education').val();
            
            // Update preview area with form values
            var selectedTemplate = $('#templateSelect').val();
            var previewContent = $('#' + selectedTemplate).html();
            previewContent = previewContent.replace('{{firstName}}', firstName);
            previewContent = previewContent.replace('{{lastName}}', lastName);
            previewContent = previewContent.replace('{{occupation}}', occupation);
            previewContent = previewContent.replace('{{education}}', education);
            $('#previewArea').html(previewContent);
        }
        
        // Event listener for form inputs change
        $('#resumeForm input').on('input', function() {
            updatePreview();
        });
        
        // Event listener for template selection change
        $('#templateSelect').on('change', function() {
            // Update preview when template changes
            updatePreview();
        });
        
        // Event listener for download button click
        $('#downloadBtn').on('click', function() {
            // Get resume content from preview area
            var resumeContent = $('#previewArea').html();
            // Get selected download format
            var downloadFormat = $('#downloadFormat').val();
            // Download resume based on selected format
            if (downloadFormat === 'pdf') {
                // Generate PDF and download
                html2pdf().from($('#previewArea')[0]).save('resume.pdf');
            } else if (downloadFormat === 'word') {
                // Generate Word document and download
                var content = $('#previewArea').html();
                var zip = new JSZip();
                var doc = new window.docxtemplater();
                doc.loadZip(new JSZip(content));
                doc.loadZip(new JSZip(content));
                var data = doc.getZip().generate({type: 'blob'});
                saveAs(data, 'resume.docx');
            }
        });
        
        // Update preview on page load
        updatePreview();
    });
</script>



</body>
</html>
