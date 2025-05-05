## `sapmachine:lts-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:630ec8e69a99f762006f10dab056c05b0980edd756fbc1b91e3bf9a51e1543f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:645a7affb2f06f85b3b46b24702c88f32e9041f9f46c88beff696947f06a568a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89270718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e50d45622578b89be6ed92ca272c1eea50455a0fb189bfdacef8820c6f629c5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31a96f2225f25cbcdba29ae53496ef5578b5a93db2f4c3f3aa61068693641c5`  
		Last Modified: Mon, 05 May 2025 16:36:48 GMT  
		Size: 59.7 MB (59738104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:83b0b2be3dcacea391e737d23b330168bae5d56eeb293bc721a304ff95d75811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff7abc230e09da8a39d091392ab1baabe682de2ea68a5a92f0adb4467536cda`

```dockerfile
```

-	Layers:
	-	`sha256:9abf1f9417f1c2c31f8c931757ece884dd9ea7b776669963d5f113aa280b57e6`  
		Last Modified: Mon, 05 May 2025 16:36:47 GMT  
		Size: 2.4 MB (2409372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf29cdd3c9288d5df0e114795bafffb8f4ef3f1333d27b30bc8bdaee79ff413`  
		Last Modified: Mon, 05 May 2025 16:36:47 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a09cdf83efa643bfc36205bfefce33bd482ec21741af55b49c2f27f6c33a8d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86221042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc68cbb972026b135da96e60aeddc853e73683cf7084ce107285c62163b2f9b7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0a9b384628c4e92811bcd00f5a509ed43a1d985ede23c5d883b7cc067e1728`  
		Last Modified: Wed, 16 Apr 2025 16:31:21 GMT  
		Size: 58.9 MB (58866811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6164340fdaedf3ec384cb5630c1365322bc1dc927606cf4308ca5c569b702db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39be22287fc4a720c5e6ae1222525ea82059db9b43b5b522efaa734196ba419d`

```dockerfile
```

-	Layers:
	-	`sha256:07aac63041edbe9fd64b5adf1044649920252ef069c2f22f1c20a6051df1dd67`  
		Last Modified: Wed, 16 Apr 2025 16:31:20 GMT  
		Size: 2.4 MB (2409078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a262873bd5cb6e1a4b29ec74e9899fbf1b412182cd4d1a728778921442e008e`  
		Last Modified: Wed, 16 Apr 2025 16:31:19 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3d29138d0cbe7c708d0b266f908aa68beca1c80e761d67389db6493b4dce37d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95754907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2bc4295f705073149b5ed470acd45631e7c780c4e10ef052589d764fea4609`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891b1cdc85a5858df0b16c30e1e065cd546b50f183f3438bd63b10ba48cea89`  
		Last Modified: Wed, 16 Apr 2025 16:51:35 GMT  
		Size: 61.3 MB (61312211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:545a67182811a5411942c18567f86ff9a793e92447ca5bbf824d87a29f7ffb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ade922aa035f417a3a08fe77ea0f5a1e6c7c6f8c802fda61743775edc1c51a4`

```dockerfile
```

-	Layers:
	-	`sha256:eaa246ca1d5d6830baf5342617e02762ed7ddf9a51ae5cc99a291d06a41ff615`  
		Last Modified: Wed, 16 Apr 2025 16:51:34 GMT  
		Size: 2.4 MB (2413365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a78cccfa8a283c58752df79ed23c91c256b4f9f50e774afe5e3ea8e04d2c91`  
		Last Modified: Wed, 16 Apr 2025 16:51:33 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json
