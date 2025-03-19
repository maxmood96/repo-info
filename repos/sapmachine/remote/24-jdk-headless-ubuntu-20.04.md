## `sapmachine:24-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:fab9c6f31508f967212a0b93f34301750ec33afc95bcbad62bf2030bba7abd5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f59ade5671361d7657033d6b664b72f7e0cf7a3c5238982d3808a836e47154e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257874656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0581fe3a5aff435438af5b85f461c27ceeb0f9a72522195e03d71dc486cced40`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa97b612bf34386077bf7c4cd71b67d4d348963167da2f957de68f0dcb18b0e`  
		Last Modified: Wed, 19 Mar 2025 20:33:14 GMT  
		Size: 230.4 MB (230363596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4921a706c0a02926194a0ba07c37e5ff27f1c783e2e433c48d762925501e1abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b13369847e306c95b14d0f95e02615a1a1e0b466a1dddf275850672c91dccf`

```dockerfile
```

-	Layers:
	-	`sha256:9144084935c880e38c96524d52b6bf0dcf220e1a6c4ad7ea67dc1ad1c0b2fe2b`  
		Last Modified: Wed, 19 Mar 2025 20:33:10 GMT  
		Size: 2.1 MB (2136813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6a89cfabb5ac4ea5ce42e1d102bf12e661258a40467e1aee6716254a1efb5b`  
		Last Modified: Wed, 19 Mar 2025 20:33:10 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ea8258d508de86531b05f2f921f670744915710ca78c7ef290c5529fad36d17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254254981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2ef12a332e3034ae31c515ac4abfd95022e133c330e856c301793c62cb6ce1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d175a0c4b571b932feb5e0216b5772cd541986711cef8e7cf334507e7634b27f`  
		Last Modified: Wed, 19 Mar 2025 20:41:46 GMT  
		Size: 228.3 MB (228281153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d628250578651dcf9deff93a08f96f7ec877cbdd37a03ec30cb86b141d7917c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3938990aa04ce59c146647ee86cba9e3a1a0279671ede6e7e85b5f2b741371ed`

```dockerfile
```

-	Layers:
	-	`sha256:20cc7ffa8c82a3a9d72d04c80f12f4b4575db11432f63f0344243c33d069f118`  
		Last Modified: Wed, 19 Mar 2025 20:41:41 GMT  
		Size: 2.1 MB (2136439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1258e93486fa7d8c0b452bc1a0e655911549c8b67f7f9e5b8373bc6d777ea64b`  
		Last Modified: Wed, 19 Mar 2025 20:41:41 GMT  
		Size: 9.0 KB (8992 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bdf1d4df9e8e77a3de2df64a015e70f0f76aeb9a22c1faa5d3fbfb0e9e5a6164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263109113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711cfff7d0e4e14b5d0a59767da9aa1e7545ade07bd536fb7bcd47bf55aba9a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660d2483546f8db3efa107924853c1b15d51d87ac53da6887fadcb8c4e9d13c`  
		Last Modified: Wed, 19 Mar 2025 20:51:51 GMT  
		Size: 231.0 MB (231032607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bdfe35ce88cfc2eaa90891ca8485573fc6eb0bf2c80d3f776264482797242a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7076e80a8a853f3e019e247f91f1b95c48171bb39c7545127ad88209e3c51d60`

```dockerfile
```

-	Layers:
	-	`sha256:3a0f852ce7e1390dea0c4e85fe5224ee061903931af29cc53434aec7c8135f83`  
		Last Modified: Wed, 19 Mar 2025 20:51:45 GMT  
		Size: 2.1 MB (2137953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e49a2cb41d06f1caacea83ea0cd8062da198331da379fd363b4a2c5cf75f6ba`  
		Last Modified: Wed, 19 Mar 2025 20:51:45 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
