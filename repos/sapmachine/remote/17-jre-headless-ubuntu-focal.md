## `sapmachine:17-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:9e4cde1cb2dd34abb10ee443c9e4f2c0ef38bf5aa0ee990ec3f045f10fe9a4e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:9a1f66d9073d5c6588696d8e37bbe6a201dd39dca2f2c8334eceee94cf58923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be5039f7b8873c375f0cab57981e9882c0f9dcae563f992af2f4de67751ef8d`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62298323278f50487b79061ee1bb5b0f0aeaf1395d3f406581c7ed273b43b30d`  
		Last Modified: Wed, 16 Oct 2024 18:59:56 GMT  
		Size: 52.1 MB (52081872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b19204dc5f629b166fc85cbc8c03881f3719ed7fea651e9fd3a44a4d64956adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81718bf039557fce4af593291ae2d10a3591cdbd34e206c86c7e0c62f45f0740`

```dockerfile
```

-	Layers:
	-	`sha256:85392f61fa8758e89660439bfc1d19594ac5b3450e5123b030155e4d77feb73d`  
		Last Modified: Wed, 16 Oct 2024 18:59:55 GMT  
		Size: 2.0 MB (2049013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8e4a1e8b3a297adcf3644c9ee885c7b7317216596c77cd65ad3a53753245bb`  
		Last Modified: Wed, 16 Oct 2024 18:59:54 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:743f211c94f00aac683cf2695fe601982c77802cbbb6da65d6270426076f9a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77470541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad0e41edddb294ff0b8782cff71f8d0e93314dabb3060b6a0739f2414786e2a`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae07cc9c87b4224500bd176606f70d2d5c7200c7340f90a1401ba4558452726e`  
		Last Modified: Wed, 16 Oct 2024 19:40:47 GMT  
		Size: 51.5 MB (51496713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3d80dae6a034759f73f7808c5c2e94ec64f0be59add8c1b1853569b5ef17eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474d46f340d1bf52c7bee51f5231c54abf31aad09dd0357fadd101f2fd3e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:267125a6c8abed5fc319420fe9804ef8fe9f271ca8398bfcb1f948eb7a39871c`  
		Last Modified: Wed, 16 Oct 2024 19:40:46 GMT  
		Size: 2.0 MB (2048640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db41c8f8c1346aaf174bb3016c718389daaee2a138fc5f4cffb108abfc91a02`  
		Last Modified: Wed, 16 Oct 2024 19:40:45 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6ade01b262b57e5339dd534b7ee19e48bb87d4ba3cf7651fde8358069a36413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85074878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4677ff991b628dde0ac41118e098bbe8663b7e057ed2b434a40380f02133f88`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4276a4c407ea5d5d74ea880c2faad2a2276b3366172e5614b19c9fa64bc23e43`  
		Last Modified: Wed, 16 Oct 2024 03:08:00 GMT  
		Size: 53.0 MB (52998372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75a06e40a01bc9dac2de684e450ddc710bde5eb8fc9cac648c6f688369ea0932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bc13c5115056f704eecd6f97d51f5267ca14123b5d3aa085fa9ae35f1fcc02`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2046e69e2984b0e7a9f900578263e221154579621b4d1fd1c2e97340b7096`  
		Last Modified: Wed, 16 Oct 2024 03:07:59 GMT  
		Size: 2.0 MB (2046069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3039e696f2b46732b887b6a524045a9634bd130f94ca4a1eb654a0207c073519`  
		Last Modified: Wed, 16 Oct 2024 03:07:59 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json
