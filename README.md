<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Indeed Jobs Portal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff; /* Alice Blue */
            color: #333;
            margin: 0;
            padding: 20px;
        }
        h1, h2 {
            color: #0056b3; /* A shade of blue */
        }
        .job {
            margin-bottom: 20px;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #fff; /* White background for job details */
        }
        .job-title {
            font-size: 1.5em;
            margin-bottom: 10px;
        }
        .form-container {
            margin-top: 20px;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #fff;
        }
        .form-container input, .form-container select {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .form-container button {
            padding: 10px;
            background-color: #0056b3; /* A shade of blue */
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .form-container button:hover {
            background-color: #004494; /* Darker shade on hover */
        }
    </style>
</head>
<body>
    <h1>Indeed Jobs Portal</h1>

    <div class="job">
        <h2 class="job-title">1: Software Developer</h2>
        <p>Job Description:</p>
        <p>Development of applications using C#, VB.Net, ASP.NET, HTML, CSS & JavaScript/JQuery.</p>
        <p>Designing user interfaces, gathering technical requirements, writing technical specifications and documentation, troubleshooting, debugging, testing, and writing database queries.</p>
        <p><strong>Qualifications:</strong></p>
        <ul>
            <li>B.Tech in Computer Science, M.Tech in Computer Science</li>
            <li>Other relevant courses</li>
        </ul>
        <p><strong>Experience:</strong> Fresher/Experience</p>
    </div>

    <div class="job">
        <h2 class="job-title">2: Web Designer</h2>
        <p>Job Description:</p>
        <p>UI & UX design skills are crucial for a web designer.</p>
        <p><strong>Qualifications:</strong></p>
        <ul>
            <li>B.Tech in Computer Science, Graphic Design</li>
            <li>Other relevant courses</li>
        </ul>
        <p><strong>Experience:</strong> Fresher/Experience</p>
    </div>

    <div class="job">
        <h2 class="job-title">3: Graphic Designer</h2>
        <p>Job Description:</p>
        <p>Graphic Designers should be familiar with bleeds, slug, crop, and fold marks, as well as with ink limits, dot gains, and transparency.</p>
        <p><strong>Qualifications:</strong></p>
        <ul>
            <li>Diploma in Graphic Design</li>
            <li>Other relevant courses</li>
        </ul>
        <p><strong>Experience:</strong> Fresher/Experience</p>
    </div>

    <div class="form-container">
        <h2>Apply for a Job</h2>
        <form id="jobApplicationForm">
            <label for="jobSelect">Select Job:</label>
            <select id="jobSelect">
                <option value="1">Software Developer</option>
                <option value="2">Web Designer</option>
                <option value="3">Graphic Designer</option>
            </select>

            <label for="name">Enter Your Name:</label>
            <input type="text" id="name" required>

            <label for="college">Enter Your College Name:</label>
            <input type="text" id="college" required>

            <label for="experience">Enter Your Experience (years):</label>
            <input type="number" id="experience" min="0">

            <label for="qualification">Select Your Qualification:</label>
            <select id="qualification">
                <option value="1">B.Tech in Computer Science</option>
                <option value="2">Graphic Design</option>
                <option value="3">Diploma in Graphic Design</option>
                <option value="4">Other</option>
            </select>

            <button type="submit">Submit Application</button>
        </form>
    </div>

    <script>
        document.getElementById('jobApplicationForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const jobSelected = document.getElementById('jobSelect').value;
            const name = document.getElementById('name').value;
            const college = document.getElementById('college').value;
            const experience = document.getElementById('experience').value;
            const qualification = document.getElementById('qualification').value;

            let companyName = '';
            let jobTitle = '';

            switch (jobSelected) {
                case '1':
                    companyName = 'Microsoft';
                    jobTitle = 'Software Developer';
                    break;
                case '2':
                    companyName = 'Google';
                    jobTitle = 'Web Designer';
                    break;
                case '3':
                    companyName = 'Microsoft';
                    jobTitle = 'Graphic Designer';
                    break;
                default:
                    alert('Invalid job selection.');
                    return;
            }

            alert(`You are applying for ${jobTitle} at ${companyName}.\n\nDetails:\nName: ${name}\nCollege: ${college}\nExperience: ${experience} years\nQualification: ${qualification}`);
        });
    </script>
</body>
</html>
