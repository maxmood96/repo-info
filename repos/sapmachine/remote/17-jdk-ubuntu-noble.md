## `sapmachine:17-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5535109a5ed971ac820848c4f143b919d6dc83ba630eca31f12132a2724f1e00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5bb3680fb9eb6529233507f3d077008d6591164b1e714179bfa027299f1ed7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231415877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12eb57e297015214df46b6b1940ef69f344959140f6be449f82841770faa70d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a48afd434df06b47b33aeb0dad4e1cf69b3fd04ce825430ca0c3cdbe0d38f9`  
		Last Modified: Tue, 17 Feb 2026 20:35:34 GMT  
		Size: 201.7 MB (201688266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:844f755bf0c8ea50d9c11370b288a62b4ff9dafbf5062d5ffa4487f891e70e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007e8717ffd9377bf6c26258bac8cb67de733a3781f88021267943f94963d423`

```dockerfile
```

-	Layers:
	-	`sha256:fffa2ee84762fd8b38d41090303aad2775af22a8c235f31025a9ad7f94db2b00`  
		Last Modified: Tue, 17 Feb 2026 20:35:29 GMT  
		Size: 2.6 MB (2605226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9777d3018c310186cae5156d3b4b154275a3cb8da66c452f4b6e38e6c990d3e8`  
		Last Modified: Tue, 17 Feb 2026 20:35:29 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9f4845c9057477f7c4334c75c55e3d68e8fd92b853d85e1c50339523a0c0bb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229286743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eae004e67fa5cce5de21d8bc1ad2c9cae45395ea1c0c676c7caa9eb568534eb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0b6dc86cf5225d30e4160bd5ee9a80a6dc40c555e8454166d92ee08127ceaa`  
		Last Modified: Tue, 17 Feb 2026 20:34:35 GMT  
		Size: 200.4 MB (200421623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4c86fe132b52baa5ae65329ac329aac638589e0cfe244a85a5ac16b3f4056841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08234e35d15f47786f0d21c16fac5ed6a0d772248f1b277fd616f36dff2af94b`

```dockerfile
```

-	Layers:
	-	`sha256:5a9c7549affdb03ff5c725f63509bc8ea65c8d4b1b24384136c6978e97d9f68c`  
		Last Modified: Tue, 17 Feb 2026 20:34:30 GMT  
		Size: 2.6 MB (2605838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226e4e049fb5142907f4eab473106554b59d22d323a6db05c692f24815a3a741`  
		Last Modified: Tue, 17 Feb 2026 20:34:30 GMT  
		Size: 12.9 KB (12855 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:474d566d317f1f171552c755003f905808da9445b6797628bf553eef79c496f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236882886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c51cc7f7b192bf8f0c84000e2ccd34de9cd04b093baead9a39d69195b88e6a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:33:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:33:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:33:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a10c874c6feabea993f50ba9cb1c5952afac19d83f218ed450342438089f8f`  
		Last Modified: Tue, 17 Feb 2026 21:34:18 GMT  
		Size: 202.6 MB (202575980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b6714490c3c095748678eef3c7377870f3ae0a3ef245d57c28eb10fb44a7e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243a74a6f6245bd841f9aa70294b2220dd40e38e14f221b0f40fee1fd32a19f4`

```dockerfile
```

-	Layers:
	-	`sha256:065b61e6b1e1427fe198033d0c47f3959f9f413febe31ccacb718c26f0e99d79`  
		Last Modified: Tue, 17 Feb 2026 21:34:13 GMT  
		Size: 2.6 MB (2602826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0741a3f3745a872805fccf41b7cdd5a325788547e934744ed2ddf4db877ca42a`  
		Last Modified: Tue, 17 Feb 2026 21:34:13 GMT  
		Size: 12.7 KB (12723 bytes)  
		MIME: application/vnd.in-toto+json
