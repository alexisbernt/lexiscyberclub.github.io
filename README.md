# Starting Webpage for Lexi's Cyber Club 

## Directions to configure a GitHub pages:
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## List of Activities to be done:
- Email collection.
- Sample code for email collection: <script>
        // Function to prompt for email and save to CSV
        function promptEmail() {
            // Show a prompt for email input
            const email = prompt("Enter your email:");

            if (email) {
                // Convert email to a CSV format
                const csvContent = "data:text/csv;charset=utf-8,Email\n" + email;

                // Create a download link for the CSV file
                const encodedUri = encodeURI(csvContent);
                const link = document.createElement("a");
                link.setAttribute("href", encodedUri);
                link.setAttribute("download", "emails.csv");
                document.body.appendChild(link);

                // Trigger the download
                link.click();

                // Remove the link element
                document.body.removeChild(link);

                alert("Thank you! Your email has been saved.");
            } else {
                alert("Email input was cancelled.");
            }
        }

        // Show the popup when the page loads
        window.onload = promptEmail;
    </script>
