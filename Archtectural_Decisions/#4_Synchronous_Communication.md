# #4 Synchronous Communication Media
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
            <strong>Option 1</strong> Http Restful</td>
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
                <li>Saber Zahedian Fard</li>
                <li>Mahsa Mesbah</li>
                <li>Ardeshir Panahi</li>
                <li>Rouzbeh Zarandi</li>
                <li>Mohammad Reza Mehri</li>
              </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Context
We have to select a media for our synchronous communication between services where immediate response is needed.
## Concerns
- We need ***secure*** communication.
- It should be ***adoptable*** in Organization.

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
          <td>Http RESTful</td>
          <td> We can use Http communication within Restful design. </td>
          <td>
            <ul>
              <li>Mature in the organization</li>
              <li>Require less development effort</li>
              <li>Readable</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Less performant</li>
              <li>Not efficient for streaming</li>
              <li>Payload size</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Since it is mature in organization among teams it could be adopt easily in our project.</li>
              <li>Broad accessibility among different contexts.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Slow adoption of requirement changes.</li>
              <li>Challenge on big payload.</li>
            </ul>
          </td>
        <tr>
          <td>2</td>
          <td>gRPC</td>
          <td>
            High performance remote procedure call framework that communicates using protobuff.
          </td>
          <td>
            <ul>
              <li>Performant</li>
              <li>Stream capability</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Not human readable since its binary.</li>
              <li>Reqauire development effort.</li>
              <li>Form strong couplig between server and client.</li>
              <li>High learning curve.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Opportunity of streaming if it is required.</li>
              <li>Less waiting time since it is performant.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Require complex infrastructure</li>
              <li>Increases maintenance cost</li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Decision Consideration
- It is very important to ***easily adopt*** the communication media with ***less effort***.
- It is important to have communication media which is ***well known by other contaext*** in case of ***broad communication***.

## Conclusion
The http RESTful can be adopt with the system easily with less effort.
