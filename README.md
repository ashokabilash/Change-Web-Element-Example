<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Change Web Element Example</title>
</head>
<body>

  <p id="elementToChange">This is the initial text.</p>
  
  <!-- Placeholder text input -->
  <input type="text" placeholder="Enter new ID" id="newIdInput">

  <button id="changeButton" onclick="changeElement()">Change Element</button>

  <script>
    // Function to be executed when the button is clicked
    function changeElement() {
      // Get the element by its ID
      var element = document.getElementById('elementToChange');
      
      // Get the input element by its ID
      var newIdInput = document.getElementById('newIdInput');

      // Array of alternative IDs
      var alternativeIds = ['koney', 'uony', 'jony', 'lony'];

      // If the input has a value, use it as the next ID
      var nextId = newIdInput.value || alternativeIds[0];

      // Change the ID of the element
      element.id = nextId;

      // Change the content of the element
      element.innerHTML = 'Element ID has been changed to: ' + nextId;

      // Clear the input value
      newIdInput.value = '';
    }
  </script>

</body>
</html>
