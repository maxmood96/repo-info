## `sapmachine:17-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:e200875ee3ca45614b413afa65347063a327f23ff3ddb008174d1b0c465cf89e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:6a464b5aeb591a433e44d559f003cbd61ca05f48751bf53068ed7b546ecf6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58878846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2da17c957da964acde1eb9481fcd5aa21013c547f1e1e3ccc50472f2270ade8`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:46 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.19-r0 # buildkit
# Mon, 22 Jun 2026 20:08:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Mon, 22 Jun 2026 20:08:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c3312b34532018d841f7510b9f995d88c6a054b7b70c5a675418a7f8649aa`  
		Last Modified: Mon, 22 Jun 2026 20:08:57 GMT  
		Size: 55.1 MB (55091251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fef52be924674725f46eb6e576dfdaeae239ba7aa9bdaa7343043a55cb94fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.0 KB (432954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c15b94245e5d4f972a42db7bbd9b5271059ac37e3adc0992fb6ea41ab33935`

```dockerfile
```

-	Layers:
	-	`sha256:a9d58e3b7785c8a3b97a273c9f93680712822ddd79d9f42f6efe5315c56fb49e`  
		Last Modified: Mon, 22 Jun 2026 20:08:56 GMT  
		Size: 426.0 KB (425994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a437737653b7e5b375669400975c375ce16ac8e05b6279e21665e389d8f196`  
		Last Modified: Mon, 22 Jun 2026 20:08:56 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
