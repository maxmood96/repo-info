## `sapmachine:21-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:9825ef4d19a96174486ab95bb783b6167c5bbf0f364591e05d5e6939450425d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; amd64

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

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b3bc9ba251e51b58b81d7507e0bbdb4a764f085fc794380534da5b7cf42b60c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241210078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b8ab83d77cee8b37711405028414211a3b2f571887dd4ffd441b8f639c0a06`
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
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e5af87aad4cf5003dc97b681825ff1b1de943ee7396a789bf7a7cff33d97e`  
		Last Modified: Mon, 15 Sep 2025 23:16:45 GMT  
		Size: 212.3 MB (212348761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c4d270ae9053d6e7bd637dbc9cc065feed4e26319fedc13d321c2860d22d8d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee9a062f701be6fbfa66657beb25d5200d7e9f39d709d0cd6f3f0296f5b3bfc`

```dockerfile
```

-	Layers:
	-	`sha256:641c14757e69229ea615d65b9da8a84bf59dfbc207aa832f867794d219c6477e`  
		Last Modified: Tue, 16 Sep 2025 00:08:10 GMT  
		Size: 2.4 MB (2357918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29c3854caf25c8c4305a5314c919afe621a5c3e8f8fff58db17f9c34f3734b1`  
		Last Modified: Tue, 16 Sep 2025 00:08:11 GMT  
		Size: 11.5 KB (11496 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; ppc64le

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
		Last Modified: Mon, 15 Sep 2025 23:42:49 GMT  
		Size: 214.9 MB (214880111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

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
