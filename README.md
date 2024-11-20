# RPA Challenge - Input Forms

The classic RPA Challenge from the [rpachallenge.com](https://rpachallenge.com/).<br>
The robot needs to fill in the form correctly 10 times in order to complete the challenge.<br>
The tricky part lies on the form fields: each time the form is submitted, the fields appear at a different spot!<br>
But a good RPA developer always finds a way!<rb>

### 🤖 About the robot

<p>
  The RPA Challenge website provides the excel file with the data that needs to be submitted, which you can find in the "excel_files" folder. I developed this bot using ElectroNeek Community Edition, and it took me about 4h to complete. It has just one workflow with a total of 20 activities. It finishes execution after the "Congratulations" message at the end of the 10 submissions. And if it runs into some kind of problem, it throws an error in te logs, takes a screenshot and sends everything over e-mail.
</p>

### 🪛 Technologies and tools

<p align="left">
  <img src="https://github.com/cristiane-dsc/cristiane-dsc/blob/main/logo_electroneek.png" height=50 width=50/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height=50 width=50/>
</p>

### 🤔 Challenges beyond the one in the name

<p>
  ElectroNeek Community Edition limitations: maximum of 20 activities per workflow and no subprograms. That made everything more difficult and I had to get creative when looping through the excel file and error handling.
  <ul>
    <li>Looping through the excel file: I didn't want to use the 'For each row' activity because everything gets messy and all squished in, which makes the workflow confusing. I considered using a 'Do...While' activity but it would require more than 20 activities total. So the solution I found was to use the 'Congratulations' message as a sort of if statement. If the bot finds it, it's all finished. Otherwise, it must go on. An incremental index variable and some javascript did the trick.</li>
    <li>Error handling: I managed to apply simple error handling. Not ideal, since I'm usually very thorough and careful with that aspect of a project. But I could make it work by connecting similar activities to the same error message.</li>
  </u>
</p>

### ⚠️ Observations

<p>
  As a good practice, I decided to keep sensitive data out of the code in this repository. That includes my personal e-mail and some directories with my Windows username. So those parameters are missing in the code.
</p>
