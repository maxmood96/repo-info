## `sapmachine:17-alpine-3.21`

```console
$ docker pull sapmachine@sha256:09242f50c7f3595d5a48fee7a9f411d5ba3548683d8e4aa5054fe9f093c1fbf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:a95a691219b73adbb782f6f010ed6434fd52dce17e83e84a4b232bfc7272106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205863653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1514b12949c9703d95c6c94e7c3079c33be215f90115b62f6f1b01fb03bdb436`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:35:10 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Fri, 17 Apr 2026 00:35:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Fri, 17 Apr 2026 00:35:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f6dd6ed45e391db659d55f8ccf3811619bba8f52ec58af31e397d1d8fa154a`  
		Last Modified: Fri, 17 Apr 2026 00:35:30 GMT  
		Size: 202.2 MB (202216778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7272c2a113097546bb1c0d3014660563aa396d8b3ee1fca759b2c64832944da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 KB (521123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c94e3d9fa1de29c4d719f03c7cb229ad564bec669af367dd08ac5206dbe2f69`

```dockerfile
```

-	Layers:
	-	`sha256:6a77d6a366ac77b91edf8209317010f2ab84f85d1d80662a7b999d28ec5250bd`  
		Last Modified: Fri, 17 Apr 2026 00:35:26 GMT  
		Size: 513.5 KB (513501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e68a481017de370c017b239df503e316514b7e014b2774451eff7494c3d770`  
		Last Modified: Fri, 17 Apr 2026 00:35:26 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.in-toto+json
