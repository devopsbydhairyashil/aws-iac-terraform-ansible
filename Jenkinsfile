// Optional Jenkins job to run terraform plan/apply and ansible playbook
node {
  stage('Checkout') { checkout scm }
  stage('Terraform Init') {
    sh 'cd terraform && terraform init || true'
  }
  stage('Terraform Plan') {
    sh 'cd terraform && terraform plan || true'
  }
  stage('Run Ansible') {
    sh 'ansible-playbook -i ansible/hosts.ini ansible/playbook.yml || true'
  }
}
