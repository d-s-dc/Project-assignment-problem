## <i> Project-assignment-problem </i>
### 🏗️ About:
 This is project to solve the problem of project assignment through the simulated annealing approach.
 
 ### ❓ Problem:
 We have a list of students with the projects they want to take on. Also, the projects are given in order of their preference. Now we have to help the institute assign students to the teachers in such a way that no teacher is assigned more than their capacity and we can achieve maximum student satisfaction. Other constraints include that no project can be assigned to more than one student.
 
 ### 📄 Algorithm:
  - Draw a random student x project matrix where we assign a project to student.
  - Then check for the following constraints
    - The project allocated belongs to student's choice list
    - No. of possible projects under a teacher are not more than their capacity
    - One project is taken by only one student
  - Now we assign some scores to the assignment of projects according to the following formula <br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S = p<sub>1</sub> + p<sub>2</sub> + p<sub>3</sub> + ... + p<sub>n</sub>
  <i> <p> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; where p<sub>i</sub> denotes the preference offered to student s<sub>i</sub> (here greater value of p<sub>i</sub> denotes higher preference </p> </i>
  - We iterate over as many no. of combinations of allocation possible, calculate score of each, compare it with the current maxima and make it the new maxima based upon the following calculation <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If the current score is greater than maxima then accept the current state as the maxima <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; else, calculate probability to accept this state with the following formula <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src = "https://user-images.githubusercontent.com/68206552/165034614-6b16614e-7399-4a10-97df-e26d24c2d461.png" height = "80">
  - We finally return the maxima as the solution to the allocation.
