## `sapmachine:21-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:00d874d5b2e85eea94db17f455aae7dd1c1baff1bf4cac0bbb42f0ac26b7b2d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:e39147bb1c2898968e78f345a348185d690ddfdfd62763db6bf4c9f7ce610f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246432364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e4a9e11eff35f11f05ce2f68c49773e95f4fc39e0378d892d940a73232cec9`
-	Default Command: `["jshell"]`

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
# Tue, 21 Apr 2026 23:04:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:04:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68cd0672d5527b4d1f51e79d5d9b22a33242ede81b09f9778fc83882ea259`  
		Last Modified: Tue, 21 Apr 2026 23:04:56 GMT  
		Size: 216.7 MB (216699386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:21452b60eb4649eb43d75b83cfa5393adda648a2d95e5b2a3ceedc8a6689c0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817fd8c48917c8189b0f423106eed5561dd5dc92a14216ebbd2ed26be7fedd31`

```dockerfile
```

-	Layers:
	-	`sha256:c7c88df5489663fdcea2ff4cb1ba8a7c4d6f90afaeb3e6be9a51e5d813a69b5c`  
		Last Modified: Tue, 21 Apr 2026 23:04:52 GMT  
		Size: 2.6 MB (2607771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ad06b5500b15aa3033c17cb1ef94ebac3471342be8c533144c11043667eaac`  
		Last Modified: Tue, 21 Apr 2026 23:04:52 GMT  
		Size: 12.6 KB (12606 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e138d968691c5aa8fa9b6e57b3fb7a001aa8033892a6de8e43d0278493411ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243843170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50f0ab5ac8a7e06bd666136a082ec4ca2402c20d1afb342097ef1b7d101f18b`
-	Default Command: `["jshell"]`

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
# Tue, 21 Apr 2026 23:06:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:06:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116c8f695f5bbc3d9af2a934785ba0357feff2fbc9093b115cf8a15b38ddc84b`  
		Last Modified: Tue, 21 Apr 2026 23:06:28 GMT  
		Size: 215.0 MB (214967385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e98fb1f2bd29d225873d629e2d56dd5fb2c32bee457a2adcb9fdbfa81dd8909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d462de40ccbc0dd932cd443fb047bfa165e0e34d507139a099714bc4ec1c1f8`

```dockerfile
```

-	Layers:
	-	`sha256:4ca66c6b840137322c1e48b29e246897da2a23087f7f71cc2707edead21162d5`  
		Last Modified: Tue, 21 Apr 2026 23:06:21 GMT  
		Size: 2.6 MB (2608383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f9ef1696509e5e4ec0e55f33ea03ec8e1305702ba569ba40012dcc0b5d3109`  
		Last Modified: Tue, 21 Apr 2026 23:06:21 GMT  
		Size: 12.9 KB (12855 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6185bbf213bf06960651158c8b4fb7477ded358916f4380cb85aa32b9d95bf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252081029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52720b2928118af4cb5f3aab6a5210dff156bd7a9ebd042f00cb06ede24aff2`
-	Default Command: `["jshell"]`

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
# Tue, 21 Apr 2026 23:20:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:20:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:20:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24057afa9cf35b99427158d98968c9a3ad3bf4110d2f01ca36f4eab8fe57f506`  
		Last Modified: Tue, 21 Apr 2026 23:21:47 GMT  
		Size: 217.8 MB (217766851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d946524eb630c0ba017e8ed5d10caa3700809ec18063156381aecc82eeecb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069121cc2d52b5e59cf971f5fdd731cd1a5855611b016f2c26b7544d121ff611`

```dockerfile
```

-	Layers:
	-	`sha256:c0b3af7800a6ee67f1fd824c90014e14422dc222015002c77c5b9bcc13099bf2`  
		Last Modified: Tue, 21 Apr 2026 23:21:41 GMT  
		Size: 2.6 MB (2605371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1f7750fd12d6e7a802b26c44929a8071fddbecbc9717b72d330659009307ad`  
		Last Modified: Tue, 21 Apr 2026 23:21:41 GMT  
		Size: 12.7 KB (12722 bytes)  
		MIME: application/vnd.in-toto+json
