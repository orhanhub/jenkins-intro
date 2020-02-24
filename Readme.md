install Jenkins on ubuntu

wget -q -O - http://pkg.jenkins-ci.org/debian-stable/jenkins-ci.org.key |
apt-key add -

echo "deb http://pkg.jenkins-ci.org/debian-stable binary/" | tee -a
/etc/apt/sources.list

apt-get update && apt-get upgrade -y

apt-get -y install openjdk-8-jdk

apt-get -y install jenkins

cat /var/lib/jenkins/secrets/initialAdminPassword
