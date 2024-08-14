# #1 Title
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
            1.0
          </td>
        </tr>
        <tr>
          <th>Stakeholders</th>
          <td>
            <ul>
              <li>Issuing Service</li>
              <li>Bank Account Service</li>
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
          <td>2024-08-03</td>
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
                <li>Saber Zahediyan Fard</li>
                <li>Elyas Shirouyeh</li>
                <li>Ardeshir Panahi</li>
                <li>Mahsa Mesbah</li>
                <li>Rouzbeh Zarandi</li>
                <li>Mohammad Reza Mehri</li>
              </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Context
In case of submit new Issue request process, the Issuing service requires to verify the fund Bank Account that investor paid to, which force a domain dependency from Issuing service to bank account service. Team Concerns about
## Concerns
- Dependency of issue process to bank account service where if the bank account service is not available, it ***jeopardizes submit new issue Request process*** which is crucial for Business.
- Since the process ***includes verifying financial transaction*** data, it is very important to work with fresh and UpToDate information in case of verification.

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
          <td>Verification Via Bank Account Service</td>
          <td>Inter-Service Communication Between Issuing and Bank Account Services takes place to overcome bank account verification step in process of new Issue Request Submission. The Bank Account Service will be the single source of truth to verify the eligible bank account for Issue process.</td>
          <td>
            <ul>
              <li>Consistency</li>
              <li>Data Accuracy</li>
              <li>Real Time data</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Service Dependency</li>
              <li>Latency</li>
              <li>Bandwidth Utilization </li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Single Source of Truth</li>
              <li>Immune To Bank Account Data Changes</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Single Point of Failure</li>
              <li>Potential Mesh Communication</li>
              <li>Potential Network Load </li>
              <li>Scalability Interdependence</li>
            </ul>
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>Verification Via Bank Account Shadow Table Within Issuing Service</td>
          <td>
            the Issuing Service will maintain a replicated Bank Account data in a local shadow table. This allows the service to independently verify the eligibility of Bank Account for new Issue requests
          </td>
          <td>
            <ul>
              <li>Availability</li>
              <li>Bandwidth Efficient</li>
              <li>Autonomy</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Eventual Consistency</li>
              <li>Complexity of synchronization</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Independent Scalability</li>
              <li>Independent Issuing Operation</li>
            </ul>
          </td>
          <td>
            <ul>
              <li>Stale Data Risks</li>
              <li>Synchronization Challenges</li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>

## Decision Consideration
- We considered the Bank Account Service has ***low frequency of changes***.
- BA team confirm that, there could be a ***support team*** that can handle and overcome the problem of financial transaction to an un authorized fund bank account due to bank account updates projection latency
