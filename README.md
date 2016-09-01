# os-sample-java-web
Sample Hello World Java Web Application for Red Hat OpenShift

To build and deploy in OpenShift:
```
$ oc new-app jboss-eap64-openshift~https://github.com/wicksy/os-sample-java-web.git --name=hello-java
```

To verify deployment:
```
$ curl http://$(oc get svc | awk '/^hello-java/ {print $2}'):8080
<html>
<body>
<h2>Hello World with OpenShift!</h2></br>
My second commit to an OpenShift App
</body>
</html>
$
```
