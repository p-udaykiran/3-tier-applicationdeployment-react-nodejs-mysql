<h1>🚀 3-Tier Web Application Deployment on EKS with CI/CD & Monitoring</h1>

<!-- Stack Icons -->
<div align="center">
    <img src="https://img.shields.io/badge/Docker-Container-blue?logo=docker" alt="Docker">
    <img src="https://img.shields.io/badge/Slack-Notification-purple?logo=slack" alt="Slack">
    <img src="https://img.shields.io/badge/EKS-Kubernetes-blue?logo=kubernetes" alt="EKS">
    <img src="https://img.shields.io/badge/Jenkins-CI/CD-blue?logo=jenkins" alt="Jenkins">
    <img src="https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws" alt="AWS">
</div>



<hr>

<h2>🌟 Project Overview</h2>
<p align="justify">
This project demonstrates a <strong>full 3-tier application deployment</strong> on <strong>Amazon EKS</strong> using <strong>Jenkins CI/CD</strong>, <strong>Docker</strong>, <strong>Kubernetes</strong>, and <strong>Helm</strong>. 
The deployment integrates <strong>monitoring tools</strong> (Prometheus & Grafana), <strong>Slack notifications</strong> for pipeline events, and an <strong>Ingress controller with a custom domain</strong> for the application.
</p>

<p><strong>Architecture</strong><br>
<img src="https://raw.githubusercontent.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql/refs/heads/main/client/public/Screenshot%202025-09-23%20014735.png" alt="Grafana Screenshot" width="600"></p>

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

<h2>📸 Screenshots</h2>

<p><strong>Frontend UI:</strong><br>
<img src="https://raw.githubusercontent.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql/main/client/public/main.png" alt="Frontend Screenshot" width="800"></p>

<p><strong>Kubernetes Resources:</strong><br>
<img src="https://github.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql/blob/main/client/public/eks.png?raw=true" alt="Kubernetes Screenshot" width="800"></p>

<p><strong>Grafana Dashboard:</strong><br>
<img src="https://github.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql/blob/main/client/public/grafana.png?raw=true" alt="Grafana Screenshot" width="800"></p>

<p><strong>Slack Notifications:</strong><br>
<img src="https://github.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql/blob/main/client/public/slack.png?raw=true" alt="Slack Screenshot" width="800"></p>

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
        <pre>
git clone https://github.com/p-udaykiran/3-tier-applicationdeployment-react-nodejs-mysql-.git
cd 3-tier-applicationdeployment-react-nodejs-mysql-
        </pre>
    </li>
    <li>Setup Jenkins CI/CD:
        <ul>
            <li>Configure NodeJS, Docker, SonarQube, Trivy</li>
            <li>Create Jenkins pipeline with provided Jenkinsfile</li>
            <li><strong>Note:</strong> Manual approval required after CI finishes for CD to production.</li>
        </ul>
    </li>
    <li>Deploy Application to EKS:
        <pre>kubectl apply -f k8s-prod/</pre>
    </li>
   <li>Access Monitoring Tools:
    <ul>
        <li>Prometheus: <code>&lt;custom-domain&gt;</code></li>
        <li>Grafana: <code>&lt;custom-domain&gt;</code></li>
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

<h2>💡 Contact</h2>
<p>
    <img src="https://www.svgrepo.com/show/452213/gmail.svg" alt="Email" width="20" height="20" style="vertical-align:middle;"> 
    <strong>Email:</strong> <a href="mailto:pagidimariuday@gmail.com">pagidimariuday@gmail.com</a>
</p>
<p>
    <img src="https://www.svgrepo.com/show/331724/github-code-source.svg" alt="GitHub" width="20" height="20" style="vertical-align:middle;"> 
    <strong>GitHub:</strong> <a href="https://github.com/p-udaykiran">p-udaykiran</a>
</p>
<p>
    <img src="https://www.svgrepo.com/show/448234/linkedin.svg" alt="LinkedIn" width="20" height="20" style="vertical-align:middle;"> 
    <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/p-udaykiran/">p-udaykiran</a>
</p>

