## `sapmachine:25-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:fd9372a4d817ceda64d6fc02ac6d14711fb482374ed21b5bbb08be6995b0f82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8cdc2206826e4decc36d9e398b5dba11b45065a3d6dd04b0b4034f0ca0cd0124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249591564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602ed1c7433c7f44e97ff017855a01c6bb83298d41ed4199dfcc81264c8f1aaf`
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
# Wed, 15 Apr 2026 20:58:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac21b916a8efd1898e47c915a36c99f6f7ed1f4d0822dcccf46b232f19221f31`  
		Last Modified: Wed, 15 Apr 2026 20:58:54 GMT  
		Size: 219.9 MB (219855066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:22369abc92b15f914f4555c7285f606c4107d502f83816a82d26d0fd9b63e6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfb572bda6a5316a2d5a638d9fad4f66bb635a2cf911874ebbca58ad3851f94`

```dockerfile
```

-	Layers:
	-	`sha256:0fb1187c6eda077bec6753c70b19e56b20933402548c353993c80f1b0f729689`  
		Last Modified: Wed, 15 Apr 2026 20:58:49 GMT  
		Size: 2.4 MB (2370194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686a87d9e257284c64e4a606d7d499d01242cd521784e54264188066849c3c6c`  
		Last Modified: Wed, 15 Apr 2026 20:58:49 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:016f8be87996da85cce503051c6302f2ea4498c727ee480396bae2b9f0d0edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245225297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112659a1b7f33404d964451df87c3f0958ff6b542ce1c22c119b25ab1496cae2`
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
# Wed, 15 Apr 2026 21:08:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0f1f81ca5ee8f4c546dd6b7531bed0cf282f103439ec8d7b088623fecccedf`  
		Last Modified: Wed, 15 Apr 2026 21:08:57 GMT  
		Size: 217.6 MB (217618754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d1eb07852b5d8d31f3b80adb00071b1c6ec061b55b0ff4af26095e470243a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d932ec26b3ed935bbd0b733a33e2c2c6ae2eb14c7f96e6b8ae24fc1cb365016d`

```dockerfile
```

-	Layers:
	-	`sha256:01feb6e5ee803d7533a395a57c09af154c6d1a8e7f40bc8e39c062c624193133`  
		Last Modified: Wed, 15 Apr 2026 21:08:53 GMT  
		Size: 2.4 MB (2369887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f6694d3d749846df35d8b877a079ed64b4c47b24e253851953e775cc1e8193`  
		Last Modified: Wed, 15 Apr 2026 21:08:53 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3e8eb3277cda38c8c307a621adb827ce7d674062ae775e344b25f13419a3cc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255125444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319f299ac118019f83097ba01c16dfed2438725c3a44411a031fb1da482400fb`
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
# Wed, 01 Apr 2026 20:45:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:45:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:45:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626871d74fba87a0b9c1806031b3cc5ac58fea17a733935a3733aab9b3b61ab8`  
		Last Modified: Wed, 01 Apr 2026 20:45:58 GMT  
		Size: 220.5 MB (220475784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:294c37ec9bed383c98f211d0fc02571baef9c3d6ef3ce5dd79999896c2238e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e411e4c3659b24c555f821b150fcfb797484949d4d01fdab00cf2bb9ea0e1`

```dockerfile
```

-	Layers:
	-	`sha256:52b782ebae149fc98985c0e51001756ba7324186ee1ae897594eaca5ce7ad875`  
		Last Modified: Wed, 01 Apr 2026 20:45:53 GMT  
		Size: 2.4 MB (2367084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98974b543df7dd71ff1e826ccf9191feec87c5876e72569e8ad1119e71b7e578`  
		Last Modified: Wed, 01 Apr 2026 20:45:53 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json
