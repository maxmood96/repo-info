## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ddfb009f5ae1103a9a92759c2e6974c9caf5bb91e131f067bc9ad30d28e494f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ef8f499b6a3e525ca7b1ff6446d1d5dfeeb0a3fe6e434f5cabdeb47d90c70ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244624395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d221b2cf376d752776b5b1b40601e96bd416a1cbaa1113a96ed46e47d4f13fcb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:59:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2512048c9b8b86d0fc48c7275eca4849d1f2aa00ac482c7b4cbb961aebf3b1d`  
		Last Modified: Wed, 15 Apr 2026 21:00:04 GMT  
		Size: 214.9 MB (214887897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:289241ad3d75f12a080ab6d77b8661c44f62b526ae7cc8eed271bd2e63c9d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b59c75a83ca347e12bcf696169ad8133c84996af79b7c409bd8aa710d262c0`

```dockerfile
```

-	Layers:
	-	`sha256:f9c987c21135d35cbcb8969c8535cc92fbc26f274491599cf522cd26cf265833`  
		Last Modified: Wed, 15 Apr 2026 20:59:58 GMT  
		Size: 2.4 MB (2380058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcc6a5589cbbb53659a681da7ec8a6a6e444add789cee5917aeb7bc7d1da320`  
		Last Modified: Wed, 15 Apr 2026 20:59:58 GMT  
		Size: 8.9 KB (8914 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6a9ec4faf23ef5582c7fd976b57901af233c72a2eb9c360270843e54328e10b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240719333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3318046aeda051822a201a3c491bd2c2ac969fef14310e2d23930edcfed5298d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:09:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:09:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:09:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49170026978874fe6fc1741fd82ce549c05d8e1dc91d65f97f7f503a111cd8`  
		Last Modified: Wed, 15 Apr 2026 21:10:07 GMT  
		Size: 213.1 MB (213112790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c93a17b67c8b80759c8b5306a075bac3761d63fc2fb41c0068ee025cbf96f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d18ba7a57a7f77213dc9686f1532220c5bfdcd4cffed27eeecdb028f6432c4e`

```dockerfile
```

-	Layers:
	-	`sha256:5f69ffce683fac0290d8146477a6f992e54de283d697ad53115e07a34e79ff2f`  
		Last Modified: Wed, 15 Apr 2026 21:10:02 GMT  
		Size: 2.4 MB (2379730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf5933520bd40f3a5405254a7fa2a2a8ed96c9ea05e8fa368b3c2309e4e670dc`  
		Last Modified: Wed, 15 Apr 2026 21:10:02 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a0dc446fadea1cbbbb567caff4a4c9bc77e061c9d0f48534a4b5eecc08df1748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197863b2b238f5091d9c92ee95bab8f8fcbd5ed6f1a30e307374142c486f59e3`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:48:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:48:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef782abb594c49f3e70a0da73cc67baa188e91ae37b5ba9d880212d33ea60e0`  
		Last Modified: Wed, 01 Apr 2026 20:49:00 GMT  
		Size: 215.7 MB (215676282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95af0cd246b7891866d7c7313e7290b24ce87ab300078163313ecb1c32138ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af1cb1ab60f40efc0b2bbf01f7530c79a427a8fb253c2b18b7c519a9aa44771`

```dockerfile
```

-	Layers:
	-	`sha256:7a516213186d2e05c34bf7071c0ad7ad9c7a20f02cdbaf78f7419e89a34cf1f6`  
		Last Modified: Wed, 01 Apr 2026 20:48:54 GMT  
		Size: 2.4 MB (2377554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0519aee2c346b3a7006fb33e9d5235d8ee25248522bcc17453e257c714a774`  
		Last Modified: Wed, 01 Apr 2026 20:48:54 GMT  
		Size: 9.0 KB (8957 bytes)  
		MIME: application/vnd.in-toto+json
