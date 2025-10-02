## `sapmachine:21-jdk-headless`

```console
$ docker pull sapmachine@sha256:6cbc90b7cc91cb9f6d9090a8babf423784e11353168a2127586aa44b74c1eb14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:e786596f9fd4de7fa1b77a811db10b9420a7476a0499d9fb8e5f8169e7b3657b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243843976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ed640b7ef2038d6a41cf923288bf0e2575a1620d58a189cb0b139a0e3b4c9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f24f1be2a7057c50930233693c1dc2dee03600267cd53f8bb537da7112d03`  
		Last Modified: Mon, 15 Sep 2025 23:16:35 GMT  
		Size: 214.1 MB (214120526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:03aa4d93cc1723f9a035f246bb613056ad1df036800d4c2b48dae944e27ed650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770ad12bc03437694e1b02bbfa3f03e14ce8f3204f84486aec043e8558e5b99`

```dockerfile
```

-	Layers:
	-	`sha256:f54f974344b0a89a70a5bbd53c4b83d4951373a023819bb0a9bf1933f623dfe8`  
		Last Modified: Tue, 16 Sep 2025 00:08:04 GMT  
		Size: 2.4 MB (2357375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f2b1816e29338665b1e80f0777655dd7e27d05b0799807b39838d76720ae73`  
		Last Modified: Tue, 16 Sep 2025 00:08:06 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1d7bbcc08ae3a370b7b028dc34f41a92e05068c31f9f5bd9679d0f425c9ff8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243421745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a55bf13a47f050d35604ed12c614b0aac53c70875c11e6d424d2d7850b7ee7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055de1fb3ddaa8dc5978c036c1cff1eca71f6d1ec4055409d8a8d63eda7dc35`  
		Last Modified: Thu, 02 Oct 2025 01:34:22 GMT  
		Size: 214.6 MB (214560170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3a0896bfb2de5e1f31223429ef55d2b34de66663e156a925cb33541fd2ad18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c7731935a87e157c478b3a7840b7211a06ff00433a89361095139c48459a49`

```dockerfile
```

-	Layers:
	-	`sha256:6b08337e4f2feac82004920d36d52003113d5b29ae23100ad568c6d05ca9011d`  
		Last Modified: Thu, 02 Oct 2025 03:07:27 GMT  
		Size: 2.4 MB (2356838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5223f23ac099ab938ac3e1089c878647271026126cd7754d0d10485a292fca3b`  
		Last Modified: Thu, 02 Oct 2025 03:07:28 GMT  
		Size: 10.4 KB (10415 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b4aa3a21e85e81ab56317301ffc5700f514d5ac61de055826e8e101d3db9a94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249183238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1d691fae4035d12b214aababd70c92cfcb031dbab5b8004e66654b491700bb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69c27a4bc77c6440d01d527ba37837e94c7632f85c5080d17b1b1c4a054bc16`  
		Last Modified: Tue, 23 Sep 2025 19:19:35 GMT  
		Size: 214.9 MB (214880111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ae5151273c429fd72b9561bd98e828f5511355231cd5b79c146c48d5a5822b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7532f1a028f77677c3d70e2c6b9cd78adeeb33b4a213cc7701cbcb992605a84`

```dockerfile
```

-	Layers:
	-	`sha256:6f81cf4f5b3d76a3c5c087f1e97525f79ec39a091083fd1afe095e2a0a5a38f9`  
		Last Modified: Tue, 16 Sep 2025 03:06:47 GMT  
		Size: 2.4 MB (2353447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cedc35d19b37c8fda6a758c4b01ad38871988d59edf00463b1189a4032ce2b`  
		Last Modified: Tue, 16 Sep 2025 03:06:48 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json
