## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:51bea640c3f2e401ea59b8c57ccc1bece6d0f2965a0386843980439c5417f090
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:662e0d7d089ba7c95b01d9f8e643f8376a35609c19615dfa099ae988140d9df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89314834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755202ba378a2ca9968548c13db208ef031686a0ff48d24cd3f120cd71a87a4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b177fc3b45cd0b1995b91243f9b3309d2ff5f02b32111b13781a2aeefb0d2f8`  
		Last Modified: Tue, 28 Jan 2025 01:30:03 GMT  
		Size: 59.8 MB (59779146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b2f39712d93802e044e996faf48c363a0d23daf3fa5e737e93321f4b74fc7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae8d3127d131cbf16fed406323f5ddece52be60a3c762569fe56d10594d72a4`

```dockerfile
```

-	Layers:
	-	`sha256:59fe0d20dd3171c414ce7feaf37f34d9f02acbb1c2fdbbdaaf0f3aa9f3778347`  
		Last Modified: Tue, 28 Jan 2025 01:30:01 GMT  
		Size: 2.4 MB (2410512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41eb6c2d3e7178a308cbec47ff0da11da32199e9dd13b49cb16043f4f86f54d`  
		Last Modified: Tue, 28 Jan 2025 01:30:01 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6498366cc75726b5dea33173bde70cd8b26e15816c5b66367c9f5953f6384ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86153692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6368d2686a1f75329166746b6fd30f7aed1b52700ed573abe8df93c311458677`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d33e43c082841c47df9136e7838d646dd187b524bf17d6e083af6035218f58`  
		Last Modified: Tue, 28 Jan 2025 02:27:54 GMT  
		Size: 58.8 MB (58795363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d05e725c8a98c95f929a249d3b82b4d7d15ff6b0403c41c2fbcc5545f97279c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad23a44fda2a7943c21233a8a7b283ee9073977c0b053337f3e00d242e423f35`

```dockerfile
```

-	Layers:
	-	`sha256:f84605bf7f64b9e45c10444dba3dbce487083f48801ebccc59ebb4411d78e53c`  
		Last Modified: Tue, 28 Jan 2025 02:27:52 GMT  
		Size: 2.4 MB (2409588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29f7697f7285d4e26f0c5a540bc7b419cf5a5e6b4ef11058eea203455ef19b7`  
		Last Modified: Tue, 28 Jan 2025 02:27:52 GMT  
		Size: 9.6 KB (9591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c3236ab2c3f418199aa37058750325af8952c60027bc5e84684087b9e037786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95672038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4e611ebc87c620b93fff4316acf48e3e7bdb0a2661d486a956c55df8a25d85`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113ec8d238253ee5c4da70fd859ac78931fbeb96b309fbffd3cc7c64a59e7674`  
		Last Modified: Tue, 28 Jan 2025 02:31:08 GMT  
		Size: 61.2 MB (61223796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82ffd354eb7e1aa1b49ab08677774392aa1bb5c3c27cd9065040776ef01029dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3871553e9676e98e448426280bb5c38116378e6078bc91f59c639cef7a8deaef`

```dockerfile
```

-	Layers:
	-	`sha256:4fd38a03291fd9954884f56b527e3fe58dcd0641e7e85dd980f30f1bc4f96cd7`  
		Last Modified: Tue, 28 Jan 2025 02:31:06 GMT  
		Size: 2.4 MB (2413875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9308d306682a9e73d2402cde967b3497359e822127e35b00041ec93f3eac0c3b`  
		Last Modified: Tue, 28 Jan 2025 02:31:05 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
