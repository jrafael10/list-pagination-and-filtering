# list-pagination-and-filtering-webapp

This project is called List pagination and filtering. This is a web page that shows a list of student names and allows the user to search the name of the students by typing the name in the search bar, which is located at the top-right portion of the page. When the user types a letter or word in the search bar, the list of students is filtered and only the names that match the letters or words typed by the user are shown on the screen. The web app also has page buttons and links at the bottom that, when clicked, takes the user to other page that contains the additional list of students.  

# Skills, Techniques, Process, and the Extra Credit features
1.  Global variables are declared by selecting the necessary element nodes from the Document Object Model that represents the HTML document.

2. The search component is built using the concepts of DOM manipulation and DOM traversal. A div, button, and
input elements are created to display the input field and search button.

3.showPage function accepts the list of student names and the page number. The page number is used to set the start index and the end index. Li elements with index  number that is greater than or equal the start index and less than the end index  are going to be dispayed on the page. For example, on page one, Li elements with the student names that have indeces from zero to 9 are displayed.

4. appendPageLinks function is created to build a list of page buttons and append it to a div. Each button has a page number and is a link that takes the user to other page that contains another set of 10 students.  

5. searchName function accepts the input from the search component and the list of students as arguments. If the value of the input is not empty and any student names on the list match with the string typed by user in the input field, these student names on the list will be displayed and stored in an array. The list of students in this array is passed in to the showpage and 
appendPageLinks functions to display the page buttons and the list of students on each page and paginate the search results. To avoid duplication of the page number every time the appendPageLinks function is called, the pagination div is removed before calling the showPage and appendPageLinks functions. To display the message 'no results found' when there are no matches between a student name on the list and the name typed by user on the search bar, a count variable tracks the number of undisplayed li elements. When the count reaches to the overall number of li elements, that means all li elements are not displayed. As a result, 'no results found' message is displayed. 

6.Event listeners are attached to the searh button and the search input field so that when the user types a string on the field or clicks the searh button, the searchName function runs.


