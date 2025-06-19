# QA Engineer Test Assessment

## Section 1: Multiple Choice Questions

1. **Which of the following are MySQL comments?**    
   - A. `# this is the comment`  
   - B. `-- this is the comment`  
   - C. `/* this is the comment */`  
   - D. `<!-- this is the comment →`
   **Answer:** A, B & C

2. **The tester receives a new build with changes affecting existing functionalities. What kind of additional testing is conducted to uncover issues in the existing functionalities?**  
   - A. Integration testing
   - B. Positive testing
   - C. Sanity testing
   - D. Regression testing
   **Answer:** D. Regression testing

3. **Which of the following approaches will a tester adopt when confronted with the challenge of inadequate input documentation for testing?**    
   - A. Rely on screenshots and the previous versions of the application  
   - B. Talk to the developer and business  
   - C. Make a document based on experience with another application
   - D. Both A and B
   **Answer:** D. Both A and B

4. **How can an application run on 2 different Android devices using Appium in parallel?**    
   - A. Start two Appium servers on the same port number. Use this URL in both of the scripts
        and run them in parallel using TestNG.
   - B. This is not possible.
   - C. Start two Appium servers on two different remote servers. Use this URL for both of the
        scripts.
   - D. Start two Appium servers on different ports. Use the URL in both of the scripts and run
         them in parallel using TestNG.
   **Answer:** D


5. **Consider the following HTML code. What is the XPath expression to find the label for the input element with `id="name"`?**  
   - A. //label[@for='name']
   - B. ancestor::label[1]
   - C. preceding-sibling::label[2]
   - D. A and C
   **Answer:** A. `//label[@for='name']`


## Section 2: API Test

### Tool Used: Postman

### API Reference: [GoREST API](https://gorest.co.in)

---

### Test Scenarios

#### **Scenario 1: Create a New User**
- **Endpoint:** `POST https://gorest.co.in/public/v2/users`
- **Fields:** Name, Gender, Email, Status (active/inactive)
- **Validation:** Verify the returned `id` is in numerical format

#### **Scenario 2: Verify Status of First User**
- **Endpoint:** `GET https://gorest.co.in/public/v2/users`
- **Validation:** Ensure the `status` of the first user is either `"active"` or `"inactive"`

---

### Files Included

- `**API_TEST.postman_collection.json**`: This is the Postman collection file included in the repository. It contains automated API test scripts for the scenarios defined in this assessment.

### How to Run the Test Collection

1. Open **Postman**
2. Go to `File > Import`
3. Import the file: `API_TEST.postman_collection.json`
4. Create a new **Environment** with the following variable:
   - `access_token` → *(Paste your GoREST API token here)*
5. Select the environment from the top-right dropdown
6. Go to **Collections**, select `API_TEST`, and click **Run**
7. In the **Collection Runner**, execute the tests
8. View results in the **Test Results** tab


