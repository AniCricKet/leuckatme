<script>
function getHired(age, experience) {
    // Set the minimum age and experience requirements
    const minAge = 21;
    const minExperience = 2;
  
    // Check if the user meets the requirements
    if (age >= minAge && experience >= minExperience) {
      return "Congratulations! You meet the requirements and you may possibly be hired.";
    } else {
      return "Unfortunately, you do not meet the requirements for this position.";
    }
  }
  
  // Get user input
  const age = prompt("Please enter your age: ");
  const experience = prompt("Please enter your work experience (in years): ");
  
  // Convert the age and experience inputs to integers
  const intAge = parseInt(age);
  const intExperience = parseInt(experience);
  
  // Output the result
  alert(getHired(intAge, intExperience));

</script>

## What it Means
If you fit our requirements then we may be interested in you joining us in serving great food to the community. We would love for you to contact us to go submit an application to one of our locations. We hope to see you soon!