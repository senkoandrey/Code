document.addEventListener('click', function(event) {
  // Check if the clicked element has the custom attribute 'tt-copy-url'
  if (event.target.getAttribute('tt-copy-url') === 'current-url-id') {
    // Get the current URL
    var currentURL = window.location.href;

    // Get the ID of the clicked element
    var elementID = event.target.id;

    // Check if the current URL already contains a hash symbol
    var hashIndex = currentURL.indexOf('#');
    if (hashIndex !== -1) {
      // If a hash symbol exists, replace the current hash with the new element ID
      var baseURL = currentURL.substring(0, hashIndex);
      currentURL = baseURL + '#' + elementID;
    } else {
      // If no hash symbol exists, simply append the new element ID
      currentURL += '#' + elementID;
    }

    // Copy the modified URL to the clipboard
    copyTextToClipboard(currentURL);

  }
});

// Function to copy text to clipboard
function copyTextToClipboard(text) {
  var textarea = document.createElement("textarea");
  textarea.value = text;
  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
}
