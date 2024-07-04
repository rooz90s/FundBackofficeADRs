# #1 Architecture Style
 <table>
      <tbody>
        <tr>
          <th>Status</th>
          <td>
            Decided
          </td>
        </tr>
        <tr>
          <th>Version</th>
          <td>
            1
          </td>
        </tr>
        <tr>
          <th>Stakeholders</th>
          <td>
            <ul>
              <li>Fund Backoffice Context</li>
            </ul>
          </td>
        </tr>
        <tr>
          <th>
            <strong>Outcome</strong>
          </th>
          <td>
            <strong>Option 2 </strong>: To Have Independent Shadow Table of Eligible Bank Accounts for issue process Within Issuing Service.</td>
        </tr>
        <tr>
          <th>Due date</th>
          <td>2023</td>
        </tr>
        <tr>
          <th>Owner</th>
          <td>
            <ul>
              <li>
              Mahsa Mesbah
              </li>
            </ul>
          </td>
        </tr>
        <tr>
          <th>
            <p>
              <strong>Participants</strong>
            </p>
          </th>
          <td>
              <ul>
                <li>Sajjad Shirazi</li>
                <li>Saber Zahedian Fard</li>
                <li>Mahsa Mesbah</li>
                <li>Ardeshir Panahi</li>
              </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Context
The organization is taked with developing a fund backoffice management system that is designed to handle complex fund assest operations.Such system includes many business flows and regulations and communications with outter contexts to cover the fund asset management processes.The challenge lies in adopting an archtecture to achieve agility to regulation and flows changes within reliablity and scalability. 
## Concerns
- Fund asset management operation involves ***complex business*** model
- In such business domain there may be ***frequent regulation changes*** force so the system must **be agile to changes**. 
- ***System is vast*** and requires many chained processes from different area to achive the Goal.

## Options

<table>
      <tbody>
        <tr>
          <th>Option</th>
          <th>Title</th>
          <th>Description</th>
          <th>Strengths</th>
          <th>Weakness</th>
          <th>Opportunities</th>
          <th>Threats</th>
        </tr>
        <tr>
          <td>1</td>
          <td>Monolithic</td>
          <td>Build entire application in a single project that handle all business concerns and processes. </td>
          <td>
            <ul>
              <li>Cost efficient in short term</li>
              <li>Data consistency</li>
              <li>Availability</li>
              <li>Easy testability</li>
              <li>Maturity in organization</li>
              <li>Smooth learning curve</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Potential large code base</li>
              <li>Scalability Challange</li>
              <li>Maintainibility challange on large code base</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Adopt easily</li>
              <li>Faster Prototype delivery</li>
              <li>Organization has strong experience</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Slow adoption of requirement changes</li>
              <li>Require tight coordination with other responsible teams</li>
            </ul>
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>Microservices</td>
          <td>
            Devide the business concerns and build atonomous services/projects accordingly that each of them is responsible for handling specific concern and may communicate togather to fulfill the business goals.
          </td>
          <td>
            <ul>
              <li>Scalable</li>
              <li>Smaller code base on each service</li>
              <li>Independent deployment</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Consistency Challenge</li>
              <li>Fragile reliablity</li>
              <li>Challenging testability</li>
              <li>In-maturity in Organization</li>
              <li>Complex inter-service dependencies</li>
              <li>High lerning curve</li>
              <li>Expensive</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Agile to requirement changes</li>
              <li>Reduce coordinations</li>
              <li>Independent Scaling</li>
              <li>Independent development</li>
              <li>Simpler code mainainability</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Require complex infrastructure</li>
              <li>Increases maintenance cost</li>
              <li>Challenge on recuite experts</li>
              <li>Challenge on training</li>
              <li>Challenge on adopting in the organization</li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Decision Consideration
- To create a table with list items in one cell using Markdown on GitHub, you can utilize HTML within your Markdown file
- To create a table with list items in one cell using Markdown on GitHub, you can utilize HTML within your Markdown file
- To create a table with list items in one cell using Markdown on GitHub, you can utilize HTML within your Markdown file

## Conclusion
To create a table with list items in one cell using Markdown on GitHub, you can utilize HTML within your Markdown file since GitHub Flavored Markdown supports basic HTML.
