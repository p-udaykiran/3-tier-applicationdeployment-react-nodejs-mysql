<div>
    <!-- Stack Icons -->
    <img src="https://img.shields.io/badge/Docker-Container-blue?logo=docker" alt="Docker">
    <img src="https://img.shields.io/badge/Slack-Notification-purple?logo=slack" alt="Slack">
    <img src="https://img.shields.io/badge/EKS-Kubernetes-blue?logo=kubernetes" alt="EKS">
    <img src="https://img.shields.io/badge/Jenkins-CI-blue?logo=jenkins" alt="Jenkins">
    <img src="https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws" alt="AWS">
</div>

<h1>🚀 3-Tier Web Application Deployment on EKS with CI/CD & Monitoring</h1>

<h2>🌟 Project Overview</h2>
<p>This project demonstrates a <strong>full 3-tier application deployment</strong> on <strong>Amazon EKS</strong> using <strong>Jenkins CI/CD</strong>, <strong>Docker</strong>, and <strong>Kubernetes</strong>. The deployment integrates <strong>monitoring tools</strong> (Prometheus & Grafana) and <strong>Slack notifications</strong> for pipeline events.</p>

<h2>Architecture Overview</h2>
<pre>
Frontend React App --> Backend Node.js API --> MySQL Database
                      |
                      --> Metrics --> Prometheus --> Grafana Dashboard
Jenkins --> CI/CD --> Frontend & Backend
Jenkins --> Slack Notifications
</pre>

<h2>📂 Project Structure</h2>
<pre>
3-tier-app/
├── client/              # React frontend
├── api/                 # Node.js backend
├── k8s-prod/            # Kubernetes manifests (Deployment, Service, Ingress)
├── charts/              # Helm charts for monitoring
├── Jenkinsfile          # CI/CD pipeline
└── docs/                # Documentation & screenshots
</pre>

<h2>⚙️ Features</h2>
<ul>
    <li><strong>CI/CD Pipeline:</strong> Fully automated with Jenkins including:
        <ul>
            <li>Source code checkout</li>
            <li>Syntax validation</li>
            <li>Secret scanning (GitLeaks)</li>
            <li>SonarQube quality analysis</li>
            <li>Docker build & push</li>
            <li>Kubernetes deployment to EKS</li>
            <li>Slack notifications</li>
            <li><strong>Manual approval step:</strong> Deployment to production only runs after human approval.</li>
        </ul>
    </li>
    <li><strong>3-Tier Architecture:</strong> Frontend (React.js), Backend (Node.js API), Database (MySQL)</li>
    <li><strong>Monitoring & Observability:</strong> Prometheus collects metrics; Grafana visualizes dashboards and alerts.</li>
</ul>

<h2>📈 Screenshots (Placeholders)</h2>
<ul>
    <li>Frontend UI: <em>docs/screenshots/frontend.png</em></li>
    <li>Backend API: <em>docs/screenshots/backend.png</em></li>
    <li>Kubernetes Resources: <em>docs/screenshots/k8s.png</em></li>
    <li>Grafana Dashboard: <em>docs/screenshots/grafana.png</em></li>
    <li>Slack Notifications: <em>docs/screenshots/slack.png</em></li>
</ul>

<h2>🛠️ Tools & Tech Stack</h2>
<table>
    <tr><th>Layer</th><th>Technology</th></tr>
    <tr><td>CI/CD</td><td>Jenkins</td></tr>
    <tr><td>Containerization</td><td>Docker</td></tr>
    <tr><td>Orchestration</td><td>Kubernetes (EKS)</td></tr>
    <tr><td>Frontend</td><td>React.js</td></tr>
    <tr><td>Backend</td><td>Node.js, Express</td></tr>
    <tr><td>Database</td><td>MySQL</td></tr>
    <tr><td>Monitoring</td><td>Prometheus, Grafana</td></tr>
    <tr><td>Notifications</td><td>Slack</td></tr>
</table>

<h2>🚀 Deployment Steps</h2>
<ol>
    <li>Clone the repository:
        <pre>git clone https://github.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql-.git
cd 3-tier-applicationdeployment-react-nodejs-mysql-</pre>
    </li>
    <li>Setup Jenkins CI/CD:
        <ul>
            <li>Configure NodeJS, Docker, SonarQube, Trivy</li>
            <li>Create Jenkins pipeline with provided Jenkinsfile</li>
            <li>Note: <strong>Manual approval required after CI finishes for CD to production.</strong></li>
        </ul>
    </li>
    <li>Deploy Application to EKS:
        <pre>kubectl apply -f k8s-prod/</pre>
    </li>
    <li>Access Monitoring Tools:
        <ul>
            <li>Prometheus: http://&lt;prometheus-service-ip&gt;:9090</li>
            <li>Grafana: http://&lt;grafana-service-ip&gt;:3000 (default login: admin/admin)</li>
        </ul>
    </li>
    <li>Verify Slack Notifications for build/deployment status</li>
</ol>

<h2>🔒 Security</h2>
<ul>
    <li>Kubernetes Secrets manage sensitive data</li>
    <li>GitLeaks scans code for exposed secrets</li>
    <li>Trivy scans Docker images for vulnerabilities</li>
</ul>

<h2>📌 Notes</h2>
<ul>
    <li>AWS IAM permissions must allow EKS operations</li>
    <li>Configure your own Slack webhook for notifications</li>
    <li>Customize Grafana dashboards based on application metrics</li>
</ul>

<h2>📜 License</h2>
<p>MIT License © Uday Kiran</p>

<h2>💡 Contact</h2>
<p>Email: pagidimariuday@gmail.com</p>
<p>GitHub: <a href="https://github.com/p-udaykiran">p-udaykiran</a></p>
