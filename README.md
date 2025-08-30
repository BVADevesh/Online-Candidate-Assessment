<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
</head>
<body>

  <h1>📝 Online Candidate Assessment (ServiceNow Application)</h1>

  <h2>📌 Overview</h2>
  <p>
    The <strong>Online Candidate Assessment</strong> is a scoped ServiceNow application that streamlines recruitment.
    It captures candidate details, evaluates skills, calculates assessment scores, and helps recruiters manage
    applications in a secure and automated way.
  </p>

  <h2>🚀 Features</h2>
  <ul>
    <li>👤 <strong>Candidate Data Management:</strong> Store candidate profiles, job roles, skills, and assessment results.</li>
    <li>⚙️ <strong>Assessment Workflow:</strong> Automated validation and scoring via Business Rules & Script Includes.</li>
    <li>📊 <strong>Real-Time Scoring:</strong> Client Scripts dynamically display skill scores.</li>
    <li>📨 <strong>Automation:</strong> Flow Designer triggers notifications for recruiters/HR.</li>
    <li>🔒 <strong>Security:</strong> Role-based ACLs for controlled data access.</li>
    <li>🖥️ <strong>Custom UI:</strong> Forms tailored for candidate entry and recruiter review.</li>
  </ul>

  <h2>🏗️ Architecture</h2>
  <h3>📂 Tables</h3>
  <ul>
    <li><code>x_1815655_online_0_candidate_data</code> → Candidate info & scores</li>
    <li><code>x_1815655_online_0_admin_data</code> → Admin & recruiter data</li>
    <li><code>x_1815655_online_0_skill</code> → Skill repository</li>
  </ul>

  <h3>🖥️ Server-Side</h3>
  <ul>
    <li>🔄 Business Rules → Validations, scoring, messages</li>
    <li>🧩 Script Includes → <code>CandidateAssessmentUtils</code> (scoring logic)</li>
  </ul>

  <h3>💻 Client-Side</h3>
  <ul>
    <li>📝 Client Script → <em>Skill Score</em> (live calculation on forms)</li>
  </ul>

  <h3>🤖 Automation</h3>
  <ul>
    <li>⚡ Flow Designer → Notifications & candidate progression</li>
  </ul>

  <h3>🔑 Security</h3>
  <ul>
    <li>Custom roles and ACLs for candidates, recruiters, and admins</li>
  </ul>

  <h2>👥 Roles</h2>
  <ul>
    <li>🙋 Candidate → Submit applications</li>
    <li>🕵️ Recruiter → Review candidates, view scores, update status</li>
    <li>🛠️ Admin → Configure app & manage data</li>
  </ul>

  <h2>⚙️ Installation</h2>
  <ol>
    <li>Clone the repo:
      <pre><code>git clone https://github.com/BVADevesh/Online-Candidate-Assessment.git</code></pre>
    </li>
    <li>Import into ServiceNow Studio via Source Control.</li>
    <li>Verify tables, rules, scripts, and flows.</li>
    <li>Assign roles:
      <ul>
        <li><code>x_1815655_online_0.candidate</code></li>
        <li><code>x_1815655_online_0.recruiter</code></li>
        <li><code>x_1815655_online_0.admin</code></li>
      </ul>
    </li>
    <li>Test by creating a candidate record and verifying score calculation.</li>
  </ol>

  <h2>📊 Example Workflow</h2>
  <ol>
    <li>🙋 Candidate applies with skills & qualifications.</li>
    <li>🧩 Business Rules validate input.</li>
    <li>📈 Score calculated via Script Include.</li>
    <li>📨 Recruiter notified by Flow Designer.</li>
    <li>🕵️ Recruiter reviews and updates status.</li>
  </ol>

  <h2>📂 Repository Structure</h2>
  <pre><code>Online-Candidate-Assessment/
├─ dictionary/               Table dictionary definitions
├─ author_elective_update/   Business Rules, Client Scripts, ACLs, Flows
├─ update/                   Field & table updates
├─ sys_app_*.xml             Scoped app definition
└─ README.md                 Documentation
</code></pre>

  <h2>🧪 Roadmap</h2>
  <ul>
    <li>✅ Automated Test Framework (ATF) coverage</li>
    <li>📊 Recruiter dashboards & reports</li>
    <li>🌐 Candidate self-service portal</li>
    <li>🔗 HR/ATS integrations via REST APIs</li>
  </ul>

  <h2>🤝 Contribution</h2>
  <ol>
    <li>Fork the repo</li>
    <li>Create a branch → <code>feature/your-feature</code></li>
    <li>Commit & push</li>
    <li>Submit a Pull Request</li>
  </ol>

  <h2>📄 License</h2>
  <p>Licensed under the MIT License. Free to use and extend.</p>

</body>
</html>
