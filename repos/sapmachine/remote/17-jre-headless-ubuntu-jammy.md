## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f808b4643a400977d9cc60ca88a1a01e1fb47e5f20209e42b5c90078005a3217
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7a32e6e533f72a71f3b67e37d0b47fa5d87c9faf89d596981948bf8762b01c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82125368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3defdf0f5668e6ce0bb99dc32608aa0150091a149796c1d0580852dada84741d`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34098271ccaa8672b56d402b8e73d6f36141ceb7d3a2280004596b9256e5a2c8`  
		Last Modified: Tue, 28 Jan 2025 01:30:55 GMT  
		Size: 52.6 MB (52589680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee194bad669fb1df2b02d841bcac269d9504886ed36920a95005a1affb356ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2049fa5dd7614b3a3f3f1d697960baae1672d014346ea980938ded5f91d7c021`

```dockerfile
```

-	Layers:
	-	`sha256:90d2dda842cb09c92e088aaad927833b03bf6091b78ea873dff474fcdcf14dba`  
		Last Modified: Tue, 28 Jan 2025 01:30:53 GMT  
		Size: 2.2 MB (2164888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086064db30e42338c6a04c2fb48d55b16a3aa732c30b70924317e0cafc131453`  
		Last Modified: Tue, 28 Jan 2025 01:30:53 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:478dc8ffd9b03cbf02d22d535651bd6071a17b045ff129d75f551f0cac5d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79347193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92db70beb2ea1fff22299a4ad79566892dcfebaf16a063a53489e9092cade585`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f006547f280e0002ce93ac65f8a762dabd96eb36bbfeef938cbd47d4e320f24c`  
		Last Modified: Tue, 28 Jan 2025 02:55:27 GMT  
		Size: 52.0 MB (51988864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:70400532a0e891c703859841e80150747c361d167636f275b43d86ba388c26ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c906d9a60932e41cb1cb6a224585db78920835148a7348e8f2d5b9796185a60`

```dockerfile
```

-	Layers:
	-	`sha256:ba8cbf2553e1c65e2f6fcd13a55467ae912a2060fca1424abae91731f8447a8a`  
		Last Modified: Tue, 28 Jan 2025 02:55:26 GMT  
		Size: 2.2 MB (2164560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b8ace4b35b2ad7e342a1879cbf15b44e2347af38abd678c31f900f1727c448`  
		Last Modified: Tue, 28 Jan 2025 02:55:25 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8a8eda8863c943b9dd80987469a488e0ab36707c8c570db4a7ec76011610df5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88380177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3702fa1af2733b2aa8ff7c8171004c2aab7bd6e68df6d3d1fd793c42eef82756`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaecd75fbd087f8ec2c89ec29ae8b4b186e7c618d63027666ab41ade084621f`  
		Last Modified: Tue, 28 Jan 2025 06:23:50 GMT  
		Size: 53.9 MB (53931935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3760d865a63e69de07a4574945112980eb787c15120af90d6b569179740d95d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b78501c0830cd3b88a9de76027faba720c0fabe11124b886484c7f652c5f22e`

```dockerfile
```

-	Layers:
	-	`sha256:726db0aadbb0cbfba6b4bb6cd1b935b8db6598c42e83600ecbf67f57c507f78f`  
		Last Modified: Tue, 28 Jan 2025 06:23:48 GMT  
		Size: 2.2 MB (2168799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e22ae98d5a3fbaa1850f1645381ad0372f8a9b11e8cee44fd30d3587df95fe`  
		Last Modified: Tue, 28 Jan 2025 06:23:48 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
