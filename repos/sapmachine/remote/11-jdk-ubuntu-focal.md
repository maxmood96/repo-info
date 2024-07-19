## `sapmachine:11-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:75fca1f0d5774f89ebc73ec55956200513239e9789b2d78a60c09923b3d8d200
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:2566ca7a9841b61064d0cc2dd2321f96da9d9cab6d6552f3a74cc0ac89fcaeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227794719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af86f42b2654dbabf75652764aa148c77fc7fe02bc6138b362c048b994ab9d39`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a120efa7584cdf21b6fad6334ade663aaf0186d7632bcccec0f5236e8b4fb517`  
		Last Modified: Fri, 19 Jul 2024 18:00:51 GMT  
		Size: 200.3 MB (200282950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd673bfb6a247a470c2723a278a96551000f4e831a20b644e98788d64138256e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231090864064fdc0d4f482a4558d560eeac84aabf64fbac9a67479d7106b1b5`

```dockerfile
```

-	Layers:
	-	`sha256:de23ff95db20fef07f328ae8159653fbb56ba47b8c0a9ec987d0313650722854`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 2.4 MB (2381931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b9d7684d2a1b0cdac02776b49af930fe35db361eeae2dcf935487ccba626ce`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:da185750fcf14ba2f3c50992675097fd9834987fd75580df642c75643f0512d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224711732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af3e2ac30f67c102e36fe390b90b926a6bdf087ad14a9cab3d36fb26380988`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce143e3b10b3edea29b3becd857c2508c084b7652c2f5871de70c51c8814bc60`  
		Last Modified: Wed, 26 Jun 2024 00:35:50 GMT  
		Size: 198.7 MB (198737515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:59969edc0cc4463eba31916f75ceb7585bd5f90dfa1bf53132f5c2861e2d4829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd590a9acc31a51eb96c0d559386652eef1034893ad377ae389b87efa86af19e`

```dockerfile
```

-	Layers:
	-	`sha256:5cc9e0f8dd428bfa953410bd5cfe68dcdf3a1ec9285dd6f2f8bed05db785d01c`  
		Last Modified: Wed, 26 Jun 2024 00:35:46 GMT  
		Size: 2.4 MB (2356923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c0e5d566cbc198571738845a50b814f72518921ef160cd2421ab59a1dd86e0`  
		Last Modified: Wed, 26 Jun 2024 00:35:45 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f4cb7892df3c1815d0d37e7aa9a2a71a3d21f26d1700d4ad8ef29bd93ad7e20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218598696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f742459404773a8db35926a0bd47d61108e5d3a200dd284b2e0e1af1b699729`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca6563859fb9ce70183d50c53feb79fab9867c9a6963d3fb70ba5c81f69306`  
		Last Modified: Wed, 26 Jun 2024 01:20:53 GMT  
		Size: 186.5 MB (186521556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47a9c785f3a1178d9b84270cc64aeb1c11e1e6c2caf38eaf2f1d1d66c0c977bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536886caf175f0ae78c65da60665f714d732ce8ccbf07de7ccd4b49f697efd8a`

```dockerfile
```

-	Layers:
	-	`sha256:52f35da338af780e624a773d19e6a922330b42e3f2c59fc575c3ccd91cd04060`  
		Last Modified: Wed, 26 Jun 2024 01:20:48 GMT  
		Size: 2.4 MB (2357826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2624b991090c53b64985a45db5723967ec9e95080f410eb5d558ac0939e7ad4e`  
		Last Modified: Wed, 26 Jun 2024 01:20:48 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
