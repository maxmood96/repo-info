## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ef0b564f7f270c9aff9709ef4d0932215c5ac9ef93b2b90c84ca442bef2b9c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:8b1465d05decf768567bd09132986ff94ead4affb44bae441c02dd524fd26ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86630529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd38d9ab6ae6c1ab310d5ee86dcf33afdcfa46e52a9545c9ea2ad73e00520735`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c29c52ceb29493bb7022dfcf05a929a4f3fe4f67637cea5b221a8f851bfd7f`  
		Last Modified: Tue, 21 Apr 2026 23:03:47 GMT  
		Size: 56.9 MB (56897551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3a5207c2c1315d8dabac333d038abd20ecba412b24699fc955baab264eb86fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444feee97e18f73be5bbc3e867371de5c22c81466d20ffa5e36045918e1551f5`

```dockerfile
```

-	Layers:
	-	`sha256:efad864f0c7deb7cad14d95ccad2eba7d48ed35bb4ed5eb12f25d56936731c03`  
		Last Modified: Tue, 21 Apr 2026 23:03:45 GMT  
		Size: 2.3 MB (2282058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07bc75717c3baffafb11f2550d73d33d3ddabc9605417c6722098000b7c22e7f`  
		Last Modified: Tue, 21 Apr 2026 23:03:45 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:211659c73fc5357b9ca7ffb17161154d9fe6e2ed83cde022e1f93906af1678fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84719455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03034094872169373f24a53518497c253c037418ced39c705fcf787fa6264176`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f369215ecf4d85561830b1e4d0795a0f2c6997c2c439df85bc501aaa1a9c06`  
		Last Modified: Tue, 21 Apr 2026 23:05:49 GMT  
		Size: 55.8 MB (55843670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc681f7c1c51729a31f074daebee936cd25c59647d07fb049c709ce32a444bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba0d2d137791197b374b18bc52545706d6ee96b10556ff099f3aae6e3a7018e`

```dockerfile
```

-	Layers:
	-	`sha256:fd9c0d8ee868f303ac7952a0fcdcf767181ff44638aafbea9513e2eec8bf703c`  
		Last Modified: Tue, 21 Apr 2026 23:05:46 GMT  
		Size: 2.3 MB (2282598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b8338c9c1aa4bf981056f49bf06b5929e9b7d8f706a4f0ec6c94afd1571913`  
		Last Modified: Tue, 21 Apr 2026 23:05:47 GMT  
		Size: 11.5 KB (11451 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7cf2ae15eedb5f15c3b6e69d963f11e20a6b8ca51c1493edd6188926630a2d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91642081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be98abe0bb7eda26a0055d81f9bb67b345ff79ab69e9fcf2bbddcc17786a66cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:28:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:28:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:28:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e08eea0bc833a30e24ab173e346ce40a72343eb81ddfa4315efa1e05c129813`  
		Last Modified: Wed, 15 Apr 2026 23:29:02 GMT  
		Size: 57.3 MB (57327903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8cda8b54cc921d54f9bc3b4043376d83793e1e026bf589dba57ba70413fe446f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9b74e02442a1a25b119c3e88bb83e1e70d195cc0f089f2fab5b1c3954be59c`

```dockerfile
```

-	Layers:
	-	`sha256:985381c50f2ae1d3d9d17f1a261503592412dc4ac02b30bd40cabce57e8d2d1c`  
		Last Modified: Wed, 15 Apr 2026 23:29:00 GMT  
		Size: 2.3 MB (2280229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1524112834e1856aac2d290c21079ab1a8aae9ebe15a438f103607956b493f`  
		Last Modified: Wed, 15 Apr 2026 23:29:00 GMT  
		Size: 11.3 KB (11350 bytes)  
		MIME: application/vnd.in-toto+json
