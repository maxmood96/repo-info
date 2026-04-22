## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:0c5dc98d340901b617bfeb9482c6264c50fbf2468506fa0a5331eab4a34e1dbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:9f23834805dd368c7c408452defacf7ac7fcb8a0e665a67d79bf3e61c4714881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254924265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a453bdfdff06818cf19ab23d1298830e55d5146d6d39c67c13c94b80750a34`
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
# Tue, 21 Apr 2026 23:03:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:03:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144ce9634a14c21a81e4fe871d78661445bd7df6be44e66c280a141c6314998f`  
		Last Modified: Tue, 21 Apr 2026 23:04:02 GMT  
		Size: 225.2 MB (225191287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37d932bc5ccd01b11b096cc29c2139c3d3a3192580c6342b4ecbdbc44d1ecda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d5a14072a7997a69a2aa5d014c64ea8d182586b4c5fee2c5d271fd42f6cc3c`

```dockerfile
```

-	Layers:
	-	`sha256:c77434295eb6c3e4cd1676eded15ca0e2603243ad5a104f80625eb4458391ee9`  
		Last Modified: Tue, 21 Apr 2026 23:03:57 GMT  
		Size: 2.3 MB (2347658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922a59c47fb173d1c4330f16e916cb82a3c05cbfd01c92a1eb0938715a076337`  
		Last Modified: Tue, 21 Apr 2026 23:03:57 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f8787a7ac3c1c1bd5696bc39412f9a406506cec02dce9bf6b22912a0d911a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251928465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1800d93d5cebf4c5fad840d76669703f33b6305672c5adc6086f896adb03d41f`
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
# Tue, 21 Apr 2026 23:04:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bdbdbff63e274721c12a72ca070203b19125fab524ff93ddc65c476355c20c`  
		Last Modified: Tue, 21 Apr 2026 23:05:18 GMT  
		Size: 223.1 MB (223052680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:324432248bece99c6a14c40028c3259883ec6072a51b2e64004962c7b10e0eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9583229187444db347638ad5b813fc611168d1ee7631c0fff7809e60b6fdf3`

```dockerfile
```

-	Layers:
	-	`sha256:29cbe921f15e665477afa8c42de2bd3dcdda6d5ef9f8a763bfedf3f3fe8c974f`  
		Last Modified: Tue, 21 Apr 2026 23:05:12 GMT  
		Size: 2.3 MB (2348210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b51cfef284e5ef0e9c4a7499d2a64760bf721d2d87c72882c1b3bb34ac70e92`  
		Last Modified: Tue, 21 Apr 2026 23:05:12 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:28b1bcb4392a576edd1b9ec0e2a07cce02d125db59405d946b9a6d284563acfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260575387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e47eca44ad8476a9b186c10ded9f156dd5d8b4db39f57eabdeee4c35363b811`
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
# Tue, 21 Apr 2026 23:03:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:03:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff116522614db73ba39b0c513e42288b30ce5926f762f756bdd7bf445a772df8`  
		Last Modified: Tue, 21 Apr 2026 23:03:54 GMT  
		Size: 226.3 MB (226261209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e5a85002e9a2b3aea26b73af5ffcc059dc66d14174e18aff73c944ccd7b1cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e6320c9c1a0803cff5cdb8285f634f95f71af6b8d4614c755af8ca6fdd56ef`

```dockerfile
```

-	Layers:
	-	`sha256:b57b6b8d2b7b4441392fd80c3e19dbf024176ef8bacde3cdd3ef6222cdfdffe8`  
		Last Modified: Tue, 21 Apr 2026 23:03:49 GMT  
		Size: 2.3 MB (2344535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:048a32ec3de66845e931f887d10c2429ac6f6b6c79cda42be26dcc2f0189d4cc`  
		Last Modified: Tue, 21 Apr 2026 23:03:49 GMT  
		Size: 11.7 KB (11651 bytes)  
		MIME: application/vnd.in-toto+json
