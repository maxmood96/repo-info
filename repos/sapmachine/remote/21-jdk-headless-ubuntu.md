## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:fe33425130d9309dcd44d9492867f292f1e8b02a0063b1e02956541ce9add62f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

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

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

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

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

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

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2016ac42f1b8c343f0c3024d022de5af06b3307e320826d4cc6e9c3d2296f99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249209500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f90741fef4167bfaf4d4ebe5000dcbe91acb89afdd27636619113f438aca446`
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
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae02ac5881e1b3cf16c7bee2fd17f35f39bb7cf535132429319624f3c06e29`  
		Last Modified: Tue, 02 Sep 2025 02:03:26 GMT  
		Size: 214.9 MB (214879967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6e465dd66ea6035bf4a0dd4c58e49b0dccc2ff94ddf021da04550df05d41cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58bc4f5d50e88de4be62bc9e8e07c5154f15db76e5981a9db813c08254460d`

```dockerfile
```

-	Layers:
	-	`sha256:3d144e4969b50d43fb2b4b0381d898ee0b238ddd988ae7cef05f44ebc6b336fd`  
		Last Modified: Tue, 02 Sep 2025 03:07:27 GMT  
		Size: 2.4 MB (2353443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bf5e743734c256901b34f1cb08073b23abc17057e6a59a49c458842b24e7f4`  
		Last Modified: Tue, 02 Sep 2025 03:07:28 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json
