## `sapmachine:17-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:29d946628b34d0ca4cb108ed7fa42e22c65c48d41fe728a3693d8799b46cec13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:82ff551fef6d78ed9b54ff3996a4564112b13947e4e661bcf331572df2d8d309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206158924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd80fc6882c50a62090708780a11527def0d594367f92d3b7c3421a97d8c857f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:35:04 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Fri, 17 Apr 2026 00:35:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Fri, 17 Apr 2026 00:35:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4444f27513c4e64bfebba859f4845a47b80a4aa74158613867d9b1945f0351da`  
		Last Modified: Fri, 17 Apr 2026 00:35:25 GMT  
		Size: 202.4 MB (202350735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c759c501bbec6dde53d7f8756aee831ac9f5bdfe55b086808b609c87c33bd327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.7 KB (517697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6f18065e696dcab449a1954cabb410e974ff5586c8c3ecef9fe0793bd3a16f`

```dockerfile
```

-	Layers:
	-	`sha256:170e0399c99429b9c1a2ac6dc58225e5f771f4a5db73d392fe3f599fe362f73f`  
		Last Modified: Fri, 17 Apr 2026 00:35:20 GMT  
		Size: 510.1 KB (510075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4ff757fb66865047d774a97facf43cf89989b4428f9641e22af76bb7dcad02`  
		Last Modified: Fri, 17 Apr 2026 00:35:20 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.in-toto+json
