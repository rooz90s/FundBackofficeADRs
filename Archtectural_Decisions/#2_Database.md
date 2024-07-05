# #2 Database
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
            <strong>Option 2 </strong>:Microsoft Sql Server</td>
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
We have to choose database for fund asset management system that covers our needs. There are plenty of options however we narrowed down to two elegant options from Relational database and Document base database.
## Concerns
- It is important to have ***scalable*** database.
- Database should capable of handling ***large amount of data***. 
- Database Should be efficient to handle ***Complex Query***.

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
          <td>Microsoft Sql Server</td>
          <td> Relational Database that ideal for structured schema and it is vertical scalable.</td>
          <td>
            <ul>
              <li>ACID</li>
              <li>Transactional</li>
              <li>Maturity in Organization</li>
              <li>efficient for complex query</li>
              <li>Larger Community</li>
              <li>Better integrity with .Net technologies</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Challenge on scalibility</li>
              <li>Complex HA</li>
              <li>Challenge on complex schema</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Better support in Organization</li>
              <li>being Transactional results in strong Consistency.</li>
              <li>Organization has strong experience</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Since it is vertical saclable it is resource intensive </li>
              <li>Since we adopt DDD and rich data models, there is challenge of design complex schema</li>
            </ul>
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>MongoDb</td>
          <td>
            Document Base Database that ideal structured and semi-structured schema and it is horizontal scalable.
          </td>
          <td>
            <ul>
              <li>Scalability</li>
              <li>Built in partitioning</li>
              <li>Fit for complex data model</li>
              <li>Writing Efficiency</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Not performant on complex query</li>
              <li>HA complexity</li>
              <li>Immuture in organization</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Better fit to our architecture</li>
              <li>Simple management</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Challenging on design and query complex data</li>
              <li>Challenging recuiting experts in the market</li>
              <li>Challenging Support in the organization</li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Decision Consideration
- Due to out architecture we have database per service which results in large numer of databases for such system which makes it challange to support and maintain.
- It could be costly to recuit MongoDb experts in the market and it requires high learning curve for the organization.

## Conclusion
Having such number of databases brings maintenance effort to Database teams and since the Database teams have majority exprience in Microsoft sql server ,it is a good idea to choose it over mongoDb to minimize the riskfor now.
