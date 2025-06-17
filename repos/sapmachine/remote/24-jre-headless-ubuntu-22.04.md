## `sapmachine:24-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:9eb351c4e2c826df2aced3557930e43ea786d73293ac07a4ae7f18195b6103cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5f6698c7944474c4b8be514bec5db74c3ed799b2e42929df535bc19d5a0df029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96001012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf627fa0067993d10c5db7a4c650e70c16f7402205ad902f32d2df7228a644e4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816fc2feb46729527c23cb7359e8e748adb2da290703b8f59b6f7787870f1525`  
		Last Modified: Tue, 03 Jun 2025 21:10:59 GMT  
		Size: 66.5 MB (66468009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f7c2b432085a24e544d27970ad372eea82f00f5bb7e7b734c6f397660f5d578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eceaab373f78a366c6eade97061c88283b0f5c5de4e308bdbb7ca81b2faff71`

```dockerfile
```

-	Layers:
	-	`sha256:a07e4429cb7c4ea6e32184b8a7c9c7465c13fbdc317872f2d8983af05ce23f3e`  
		Last Modified: Tue, 17 Jun 2025 09:58:17 GMT  
		Size: 2.2 MB (2197046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de72f1c521e310780407905716a3e42458ac3eacd131e77f329c83d3f0b167c3`  
		Last Modified: Tue, 17 Jun 2025 09:58:19 GMT  
		Size: 9.6 KB (9611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a4122426568f84b9dc8385245d1630b44cf31a49f43b42a66511b28645e6dfee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92811716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dcbd33911b41b2ad173656754574f50867b325a0b721d010762710f954bde4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ca7ac7aa5bade2abd11d2a9f11c1110ac6bf14f31b226beab4de8c34e4de0`  
		Last Modified: Thu, 05 Jun 2025 08:30:25 GMT  
		Size: 65.5 MB (65456135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27e63842d06f62423854fcb014c5f8968d5918b1daa4bb3602ae23df8b027cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2128d71788196f82c0f0f0bab7ae36a1ba119325ca761e41ada15738c175bcad`

```dockerfile
```

-	Layers:
	-	`sha256:b99605ff0436efcdaabf40e4c27d423d35a123794e14f72f58c243c6f4ba6300`  
		Last Modified: Tue, 03 Jun 2025 05:58:18 GMT  
		Size: 2.2 MB (2196739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc7a8dc5930a0ddca9b81133699df55e33da7cf46b4f08bdcfa9bd41ec3ce4d`  
		Last Modified: Tue, 03 Jun 2025 05:58:17 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:653374c47100d839ac7c7cfb4e52e1ec8748e342ef29b9b80ede5328d7174282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101995954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629a4e3d7d6210ea69e7d0103b6f6b7c4dfdad087b26435185586e86f919ad99`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80815ced5d959ea84af3c98140a239741d0c21a4c76aaf1cfcdbc45d6b2636d2`  
		Last Modified: Tue, 03 Jun 2025 05:56:04 GMT  
		Size: 67.6 MB (67555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c81f337987b5fb642da802a8afd98ca21ecce406f197ab40027d257008cc133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931bf23b30847fb1a499177c3d31da68b106febc25d89eee90592fc1add6ec0a`

```dockerfile
```

-	Layers:
	-	`sha256:e599b4d82a1abaea7c377f2e999c8fccdacd35b92a9189d0286fd87ede9c40db`  
		Last Modified: Tue, 03 Jun 2025 05:56:02 GMT  
		Size: 2.2 MB (2200469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2b9b8132fd918b0f105f176965d2a508dfc1934fc9afb20631d3e748a974d4`  
		Last Modified: Tue, 03 Jun 2025 05:56:01 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
