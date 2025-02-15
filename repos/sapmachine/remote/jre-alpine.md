## `sapmachine:jre-alpine`

```console
$ docker pull sapmachine@sha256:dc028a278f230c042f2ec3b6d3f994aa41a4d47471744dec7c65ec0fa89be301
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:ec9c8c6e95184a8cbd443713b8b2c982efe5536999f9e1e8d09c5561bb87655b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63730629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9d8ae5999793250c4f1cc252e71b4e00bc17cb35b49ff050ba365a5d38c135`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-23-jre=23.0.2-r0 # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-sapmachine-jre
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d887c71d7f63bef90a3c1b836864394cdd4bd7e7a56f97d00cca6e6b2d4311`  
		Last Modified: Sat, 15 Feb 2025 21:03:11 GMT  
		Size: 60.1 MB (60088382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b57fc08c2069e99c1f977c3516b3e51df29490a8563dda2b89ba9146e063c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 KB (432281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde02c8a143fa2228437d98b1c42e6d0bc0d695f12ed47230c596fba4f409a17`

```dockerfile
```

-	Layers:
	-	`sha256:574b8445e1a4e3850671baeff9746d9e9b40561166852069e5b97819feb4d039`  
		Last Modified: Fri, 14 Feb 2025 22:07:01 GMT  
		Size: 424.0 KB (423991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269708942f670af22c58523e0e1166f72ea3567bb7fbc60c6c7700cd95cb3de5`  
		Last Modified: Fri, 14 Feb 2025 22:07:01 GMT  
		Size: 8.3 KB (8290 bytes)  
		MIME: application/vnd.in-toto+json
