## `sapmachine:jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:a86c8318dc6a0fda9b410b43c9bef91255da2b3336d00ad31a1f74a5128cb09f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0d3987fae016a78b88a230111ba5768b1fba91496f9dc8dcc0dbfe6f26408901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257873856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49458b69f3b2c80b70b3b17d6bb3f6bb899d0009f2d4a25469b9d49e16badf06`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d513b6f1bbb3e0fbf216b9f3eedc5087bab79ce072801a0d0799398babbf6b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:56 GMT  
		Size: 230.4 MB (230363462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:772ddc406e9c9c29265e5856c348d5adb0b3ec397c1b8baa559d479029c95b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2da79f5cbd1b0bef19d8a20fe51a1d487497dbe7bf7c609e53557b7027bdfe3`

```dockerfile
```

-	Layers:
	-	`sha256:53f12884c3497ce3c6e68ce35f14cc6089f09205f29edadf4625688bbec3ba08`  
		Last Modified: Wed, 09 Apr 2025 01:20:52 GMT  
		Size: 2.1 MB (2136879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0c8bc782f2082fc5f2602d52da84ba42aad50a80dfbe69985d9fb4cf7aad4b`  
		Last Modified: Wed, 09 Apr 2025 01:20:52 GMT  
		Size: 8.9 KB (8887 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

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

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; ppc64le

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

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

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
