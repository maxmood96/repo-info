## `sapmachine:jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:3a144fc8384b6d47b9f7c0c09d45c7b7646c7ca861c2e0c96ae285c1cbc07fca
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
$ docker pull sapmachine@sha256:b0bbe4e63f66c2eed4489cb37be99973658dcd8bf4f7e6bb0aaa90da4d7014ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254258802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6303d1b8d1ac20ef47a2619aaeaa997b6a11ec669253ce6a09a5dc300111bcf9`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dda2cb621c07912a2e63ea1cf08544d274b0bb5036e2ae12f8dbd4df5fb6ce`  
		Last Modified: Wed, 09 Apr 2025 09:26:40 GMT  
		Size: 228.3 MB (228281141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c328e7bee07f48c8f88b7e0a589de59f6053982d9549613b80aa97bb384c1b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eb54516f344acff4a297e42f58b6f04a76b3d53e0e971843220ec8899f120e`

```dockerfile
```

-	Layers:
	-	`sha256:7952ac2d2ff3bef2e0b6bf2c2039ca4c25131400848d8d607193fdf51e64f74e`  
		Last Modified: Wed, 09 Apr 2025 09:26:35 GMT  
		Size: 2.1 MB (2136505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b1260e377ccbcb1f550a715e3cc634b86dbf9b4e8b09e79833ebfcdf03e7c2`  
		Last Modified: Wed, 09 Apr 2025 09:26:35 GMT  
		Size: 9.0 KB (8992 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5e6e4f32ec309e64f7b7ce7c0d08f50606360412565b8d782704721db444d35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263109461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f27d54032b5c012578558a7bb4844cb4ee1b0d341b675d941551036a5294608`
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
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
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
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1250f60edbe1b9f6730842788f5bee9cd98622f89cbfbb346c704d38463c4e`  
		Last Modified: Wed, 09 Apr 2025 06:47:16 GMT  
		Size: 231.0 MB (231032515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41f945b0ae14fef3f4555fae5c787a840c95b5385051223cd2b4b7442f948b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07f2415f7267769116dae1cfcd3e3489e00cde76e13927e7485a42b679aeeb2`

```dockerfile
```

-	Layers:
	-	`sha256:515e0bcb6349c05a8758068bfce47ad5b0643267787d93965255fd564f5b99ff`  
		Last Modified: Wed, 09 Apr 2025 06:47:10 GMT  
		Size: 2.1 MB (2138019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9bfab7de92c1a41544a3061708f003af494db65fdf58cf26226ddf746eb433`  
		Last Modified: Wed, 09 Apr 2025 06:47:09 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
