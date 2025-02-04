## `sapmachine:23-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ff34c4894ab8df8c1c11b00c4ef4bc7cc67985b845498c7f52d7d8124818aac5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:ae39d95573862c65321db8bda81301e1b25476cdf2196ebdb7e613b1defdd95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251213392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0b2ad4161eeeef88264f1c629ba4fdbef4d507e4ae4a6e3b747677cee1616c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3665cb0abca416fdba2ab3af8adf81e7b7bc108495752edd9f94d23f542890`  
		Last Modified: Tue, 04 Feb 2025 04:48:11 GMT  
		Size: 221.5 MB (221459102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08c8b4b17ca27c380325d0dd011c1ffaf610e1aea55afa9a7c15d68f4a374384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79641d1cc371de8c7e8a2f152d13a62e7d8fdfb7b53fcfe1e23ff019e68c1d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0d2322514d98ff157e62473c002d203cb8545bb41e2dc4c8d5ed1c9627b91bd3`  
		Last Modified: Tue, 04 Feb 2025 04:48:08 GMT  
		Size: 2.2 MB (2238638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e4d028db40e41f3b3c57aa7a3036f09eda073df5a4237344d27b248e7172b2`  
		Last Modified: Tue, 04 Feb 2025 04:48:08 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7c13e388fce74732ab83584b704e923dcd9ca88be59de722c0c52a522259e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248359697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecbbe1c9d4f379f0192a7da56ad3b562608a3e38f9e812176a46c8a88dd3704`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8fbf250468cd49ff01cf2d0d41bf9ad14b52f66e55a04c1c7ceb1b89d2c303`  
		Last Modified: Tue, 28 Jan 2025 02:21:32 GMT  
		Size: 219.5 MB (219467026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c9707b9998caeb3924dc64c0a8fa1a4a2da07fa1cc190749c2fe88384360577b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6e3ab73a5bcc4ff79bc97d3b9f0318dea6ba1ea444cc9c59f80b2601954c4`

```dockerfile
```

-	Layers:
	-	`sha256:c9d883c3fd801a3d8764ddaa0dbb6021f9b5fd88cc7bb1b7c1232ca842aa6581`  
		Last Modified: Tue, 28 Jan 2025 02:21:27 GMT  
		Size: 2.2 MB (2234565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad47b54be1330eca884bf90b64021de4fdb99244a06b1be21c625ef700057bb9`  
		Last Modified: Tue, 28 Jan 2025 02:21:26 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:dc0b50a7da747dcdac064cab005a606b79338a9ddced3790e01fd5c66c641c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256792971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54c882f1bd86e7be61b17b2d31452d4e9510ed67093cc38f1662ad51fa0a2e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb6d125283f978ab79705f4aeae2c41f68db18dc9bf1403783b3acd23361534`  
		Last Modified: Tue, 04 Feb 2025 14:22:02 GMT  
		Size: 222.4 MB (222403147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e801350ccb323c5f904763172f7bf14634c0caf718414c49c6ed448c6269560c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9974f302e481c79cdd73a596bc85026699300d2a38b5d762399d8c66c2b3a1d`

```dockerfile
```

-	Layers:
	-	`sha256:689a1ae77d9ec8096c201100cd58d7b3c6d600b6070bd47e930f868496617416`  
		Last Modified: Tue, 04 Feb 2025 14:21:56 GMT  
		Size: 2.2 MB (2239980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301f7e1d849dc74e40c1bb7326ec41d2936466c6beff17dd83a4b1d10491d94c`  
		Last Modified: Tue, 04 Feb 2025 14:21:55 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
