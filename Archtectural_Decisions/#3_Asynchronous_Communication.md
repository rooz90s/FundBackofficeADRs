# #4 Asynchronous Communication Medium
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
            <strong>Option 2</strong> Kafka </td>
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
We have to select a medium for our asynchronous communication between services.
## Concerns
- We need to ***decouple services*** as mutch as possible.
- It is important to consider ***resiliency***. 
- the system may ***produce large number of messages***.

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
          <td>RabbitMQ</td>
          <td> Messaging borker provides message queuing mechanism.</td>
          <td>
            <ul>
              <li>Mature in the organization.</li>
              <li>Scalability.</li>
              <li>Consumer acknowledgment.</li>
              <li>Persist mechanism.</li>
              <li>At-least-once-delivery</li>
              <li>Built in user friendly monitoring. </li>
              <li>Smooth learning cureve.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Not garanteed that message is not consumed more than once</li>
              <li>Less performant</li>
              <li>Not efficient for streaming</li>
              <li>Payload size</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Since it is mature in organization among teams it could be adopt easily in our system.</li>
              <li>Suitable for asynchronous command messaging</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Potential complex routing.</li>
              <li>Challenging on handling large volume of data</li>
              <li>Development effort to garantee that message will be consumed once.</li>
            </ul>
          </td>
        <tr>
          <td>2</td>
          <td>Kafka</td>
          <td>
            Topic based event streaming broker..
          </td>
          <td>
            <ul>
              <li>Highly scalable</li>
              <li>High throughput</li>
              <li>Offset Tracking</li>
              <li>Persist mechanism.</li>
              <li>At-least-once-delivery</li>
               <li>Event source in nature</li>
              <li>Better performance</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Complex setup.</li>
              <li>Not garanteed that event is not consumedmore than once</li>
              <li>Immature in Organization.</li>
              <li>Hard to recuit experts in the market.</li>
              <li>High learning curve.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Suitable for event driven.</li>
              <li>Significantly reduces coupling among services.</li>
              <li>Can rewind events to reach the services to current state.</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Development effort to garantee that events will be consumed once.</li>
              <li>Hard to recuit experts.</li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Decision Consideration
- Base on microservices archirecture, it is important our ***services maintain atonomy and independent*** 
- ***Coupling increases coordination*** which is ***contradict to our goals of microservices adoption***, so we might wants to use more decouple approach.
- Organization also tends to ***adopt Event driven architecture*** with kafka backbone.
## Conclusion
Kafka seem results in more decoupled services and also we can leverage its mature capabilities in event driven archtecture such as event sourcing and ordering by keys and etc.
