# MOZA
This is a social platform which will help society to advertise and a market place for business owners
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Social Advertise Platform</title>
    <style>
        /* Inline CSS for simplicity, consider using external CSS files in practice */
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
        }

        h1 {
            margin: 0;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .ad-form {
            padding: 20px;
            background-color: #f9f9f9;
        }

        .ad-list {
            list-style-type: none;
            padding: 0;
        }

        .ad {
            background-color: #fff;
            border: 1px solid #ccc;
            margin: 10px 0;
            padding: 10px;
        }

        .ad-title {
            font-weight: bold;
        }

        .ad-description {
            margin-top: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Social Advertise Platform</h1>
    </header>
    <div class="container">
        <div class="ad-form">
            <h2>Create an Ad</h2>
            <form id="adForm">
                <div>
                    <label for="title">Title:</label>
                    <input type="text" id="title" required>
                </div>
                <div>
                    <label for="description">Description:</label>
                    <textarea id="description" required></textarea>
                </div>
                <div>
                    <button type="submit">Create Ad</button>
                </div>
            </form>
        </div>
        <h2>Ads</h2>
        <ul class="ad-list" id="adList">
            <!-- Ads will be dynamically populated here using JavaScript -->
        </ul>
    </div>

    <script>
        // JavaScript code for handling ad creation and listing
        const adForm = document.getElementById("adForm");
        const adList = document.getElementById("adList");

        adForm.addEventListener("submit", function (e) {
            e.preventDefault();
            
            // Get values from the form
            const title = document.getElementById("title").value;
            const description = document.getElementById("description").value;

            // Create a new ad element
            const adItem = document.createElement("li");
            adItem.classList.add("ad");
            adItem.innerHTML = `
                <div class="ad-title">${title}</div>
                <div class="ad-description">${description}</div>
            `;

            // Add the new ad to the list
            adList.appendChild(adItem);

            // Clear the form
            adForm.reset();
        });
    </script>
</body>
</html>
