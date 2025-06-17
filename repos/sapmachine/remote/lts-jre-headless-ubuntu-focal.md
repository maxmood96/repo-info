## `sapmachine:lts-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:209cf0491bd705a9f29400f165fcc1d08a39599ade8a9a831fe0fb1e731541d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:9c22674989bab421410b8982450cea3aae5a7c1b3644cad3eac8d86b08cb4197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85583631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f13be58e1d287f9fffc5a771fff60411983878b41256970b660855e718aee49`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f01bda02dc956eb2f2d455cd0346edfe2ca0736c9623a2d271c34c8892ed2`  
		Last Modified: Mon, 19 May 2025 15:45:21 GMT  
		Size: 58.1 MB (58073237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9646d8bf2209ec0bc944ce196539c48cee5ac96be421167e6fa907842361030b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2073007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dfb33cc671ec114aa737308ce8953efad239e21184d7e54ec6e15859e217c4`

```dockerfile
```

-	Layers:
	-	`sha256:111175b8fc6678b36d30cd418157aa8956dd0bf7545c813eee42c95966dc6563`  
		Last Modified: Tue, 17 Jun 2025 09:54:22 GMT  
		Size: 2.1 MB (2063380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8adcee45e4991ddf73d2dc771de4ffa2f9946baf8da30fb58ae617b5cba9133`  
		Last Modified: Tue, 17 Jun 2025 09:54:23 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ae1804dda23a6e337e53eef11d7812026cf6fd1890a28a2d6428da44665ff61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83239595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fef7cd98113f5d8167183e654b602e2719d0ea8331f171a72c2e0255db37b80`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c51b427c6b5a9937b8f682c751231227a967181616ebf81500e323f4298dc91`  
		Last Modified: Wed, 16 Apr 2025 16:35:44 GMT  
		Size: 57.3 MB (57261934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:43532910e65464cf3eccbafe2d14d80a925680696fa337b5108bfd871e2c1f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90104e603c27d5fb96f19be2bfe8654af8d70dfdeee51d2e3eb7c52173bd3a13`

```dockerfile
```

-	Layers:
	-	`sha256:e603a657e31f0d084ad6d0e1191827136309ae922b2c606940b01c4a053d6b32`  
		Last Modified: Wed, 16 Apr 2025 16:35:43 GMT  
		Size: 2.1 MB (2063033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac61734115b31584c72069d8c11e20b603a451c04021a47f702ccf057dc70024`  
		Last Modified: Wed, 16 Apr 2025 16:35:42 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5a6960e7ff0e69cf4a493a763e13fbcfe19a8958d804aa0408514717b0dfd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91187683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6950c71ba1265fb24167a6ea019ecb26f53d57a5de5633294f2051ea216c668d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518735d72f1185d8a079030bb34b21be1939db9b877b6cce7c5ff1299d4f47c1`  
		Last Modified: Wed, 16 Apr 2025 17:00:56 GMT  
		Size: 59.1 MB (59110737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:03248e8568a39e0c0b62b4bb6af34d52523ed94a58e34d4e4471d6285057fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2076779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce86ce3abc48fd2ff48f166dadbb6ac76ec9c16854e7608a7416b4a815a72219`

```dockerfile
```

-	Layers:
	-	`sha256:c17dfe6b4406a36bcc7452a3cbfde199674b4108510b521e38df64ec1d1e63a2`  
		Last Modified: Wed, 16 Apr 2025 17:00:54 GMT  
		Size: 2.1 MB (2067096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2a388d3e936955f0ec26fbb164c1cca08a1bc67172235d935136094614b5a2`  
		Last Modified: Wed, 16 Apr 2025 17:00:53 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
