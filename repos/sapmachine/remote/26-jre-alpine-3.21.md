## `sapmachine:26-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:5de6a4b26807d05f9e1af15dfb112785869351149469961ba909461a4417b7fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:99829b90c42be0e3d9947acd53c220b6be4d6f8a53531dc4c5cf026cc98cf14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62847820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b11dc87e690395902bdf18bf88bdd6681c7472e7f01d409b59f2671f2ff96e8`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:10 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Fri, 17 Apr 2026 00:34:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Fri, 17 Apr 2026 00:34:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d964e19ca0bbbce9b27c3402331910a74a9c27e5f93e1dcaf106c0aea144437`  
		Last Modified: Fri, 17 Apr 2026 00:34:22 GMT  
		Size: 59.2 MB (59200945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cc5b7599328a1df550c3f42fbcb26757e112cd948791987bfb0ff7560f95428f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 KB (437536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a588ce96ae9c65fa62f8a6f53d4ced724ed7d42ca8da447f64835f77c01f3313`

```dockerfile
```

-	Layers:
	-	`sha256:ea4843371a1da1ce0215600f43bf6c634ae97c1f8451d4313e36790105e50e67`  
		Last Modified: Fri, 17 Apr 2026 00:34:21 GMT  
		Size: 430.6 KB (430601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160025b650084f013b14bf36fd2f2f000fb28d037142dff28a1264413d77469a`  
		Last Modified: Fri, 17 Apr 2026 00:34:20 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
