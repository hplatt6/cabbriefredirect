<!DOCTYPE html>
<html>
<head>
    <title>Redirecting...</title>
    <script>
        // Generate a random unique ID (UUID)
        function generateUUID() {
            return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
                var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
                return v.toString(16);
            });
        }

        // Redirect to Qualtrics survey with uniqueId
        window.onload = function() {
            const uniqueId = generateUUID();
            const surveyUrl = "https://cab.co1.qualtrics.com/jfe/form/SV_07XngQAuuAABEUK"; // Replace with your survey URL
            window.location.href = `${surveyUrl}?uniqueId=${uniqueId}`;
        };
    </script>
</head>
<body>
    <p>Redirecting to the survey...</p>
</body>
</html>
