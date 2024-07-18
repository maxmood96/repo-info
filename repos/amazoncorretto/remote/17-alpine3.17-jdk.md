## `amazoncorretto:17-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:bcf0c20e08d9ba74ee2a42ad2a4429b9f6f91a50e09606ed3ff2293b3ce976f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6151eb29ea21932f3ceae035a3296e9bc04dbee60f7523231ab1d962394fd5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149408070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c85a0b25bde58458d981fc0b37a8493a9828691643a9e9650aadc7abdd65db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bbe7fd68720518b419ffbc5c0903eddf072d2f026aca68f5e06b40691903bb`  
		Last Modified: Thu, 18 Jul 2024 00:55:47 GMT  
		Size: 146.0 MB (146018107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1cb3d863b2fd0ffa5062eb71c2592aa89ebafc0e32e0cd691b197688639e0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6662b6034377951937baa632ab2a8a336c5a8be3c6a009d1f670312ab1529a46`

```dockerfile
```

-	Layers:
	-	`sha256:2de41ea70e58b0a4e5f349aed08f000b35a69af1d768c71c3e7621b11eb7d930`  
		Last Modified: Thu, 18 Jul 2024 00:55:45 GMT  
		Size: 379.5 KB (379501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8295b395fd06c1861e4466edef213de896526526e0b1c0bbc5590b2a9d832b43`  
		Last Modified: Thu, 18 Jul 2024 00:55:45 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3d70ce879996b01af72714190d02feea29adb40e38bad066ba70a38c1c55f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147623511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7881df873c80f5991af8d8e9d6d89bf24e65c06e9a76b5eb9bbf3e6f647189eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75035188f4768e3587991901f6eeb889b5d7f5fabb6016ea6d345358c93926da`  
		Last Modified: Thu, 18 Jul 2024 01:16:22 GMT  
		Size: 144.4 MB (144350925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0887cfc80b499f5b7ad36c857809ec6bd7c1b442dc4231bb069cdebfd4d1998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 KB (388390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8cbcc9cd056ca34e056beca90d6be439f196d1bbd5d1c59fb8db3832954951`

```dockerfile
```

-	Layers:
	-	`sha256:e464e80c91d8e7edd8e6d32fb4cf6bc6e11fdb7a33fa43651f7dbad4f7d0f244`  
		Last Modified: Thu, 18 Jul 2024 01:16:18 GMT  
		Size: 378.9 KB (378919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293b3050803a1f10b55cefaeec2ab35773e19e1a4b6a5e903fbb3e873d25e563`  
		Last Modified: Thu, 18 Jul 2024 01:16:18 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
