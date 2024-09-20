## `sapmachine:23-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:15065b0d91ce642383d23b29e62a7733a04fb4cbf00b6561fc5dc8bdc4caeb08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:de6ecd228ba20ff408ce46fde4e2f5b0ed17f0c967fee36cb2009b8d724af7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248858470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749822a22ea383ffc7065032e53583076303911e65d00d2a1302f7fce7295056`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68549a32d4110693026aec325d37138ede51eb2f78b6e540298a78cfe7981db3`  
		Last Modified: Fri, 20 Sep 2024 16:58:17 GMT  
		Size: 221.3 MB (221346701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ecf72487ce1c3bbf15b9d232104f6d1f7828a33af9b121c97aeb4a3f53f97acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74760d645d46d74d68a5470bb0facfd398fa1441b1ef9c3d2b4efa6de9ec08`

```dockerfile
```

-	Layers:
	-	`sha256:df53594128815688a469c7cb7b5de9d8c90d2049be59e98a00711ad35a7d1671`  
		Last Modified: Fri, 20 Sep 2024 16:58:11 GMT  
		Size: 3.6 KB (3643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf2e8b5a1e9dac7c764bf37f9848a8eefd8408e612a282736e12c4d5d37d44f`  
		Last Modified: Fri, 20 Sep 2024 16:58:11 GMT  
		Size: 9.8 KB (9807 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7599aefea07c9c5e67ed359095e7462b3dc835b121b1665ac13b00a86a3df789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245284227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f1bc2f50c2484bf252c5b6a2c21932ec83fe60d438e949f88e22903618602e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be62c568dd337bb417cd7aba19acebd7b215fed2ab338946980cb8bf2c54b23f`  
		Last Modified: Fri, 20 Sep 2024 17:11:12 GMT  
		Size: 219.3 MB (219310010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b038af73602fd93a0bb26e82e3ab619583783c9433e34676cba523d7382f9e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3aa2e87bf0c8209d05a67f48ce742a6cce96820374258c93e56602848c49729`

```dockerfile
```

-	Layers:
	-	`sha256:351916633d71aaad118704e0825164273de6b05d4ccc2dc5653681b8a26ef178`  
		Last Modified: Fri, 20 Sep 2024 17:11:07 GMT  
		Size: 2.4 MB (2367423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f1f985deb9e460df8db041a5575c60238f62ec2aa263f66d7c740b1a6998b9`  
		Last Modified: Fri, 20 Sep 2024 17:11:07 GMT  
		Size: 10.2 KB (10155 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:652868795a388760bebde0c1bb9dd5dfb7ce75118e93b08bb90e60e7938883b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254015107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c095481d9f6198890e31996dfda06e8e2a1b0f48a6ce85b991b95ba5c8dace`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98359b626aef571db9b3ef01671631a6dea2f02b07cd2b4bb8a3563130d5590e`  
		Last Modified: Fri, 20 Sep 2024 17:15:27 GMT  
		Size: 221.9 MB (221937967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b704b1efe2c5e8ae6154ed5644a307d93422814969318f40ec47fa184d02d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630b21acb69af474a01eb5632189ea5b90c148f4afef391ba6caabddeedd1879`

```dockerfile
```

-	Layers:
	-	`sha256:40f30f45ec1cd2a1b0d48031d90295ad4500d735a1481a10c113f662ab95bf1d`  
		Last Modified: Fri, 20 Sep 2024 17:15:18 GMT  
		Size: 2.4 MB (2369591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581c24fe899a83bfc15b61d8bbaf6778e46732a2d76a559f4755e7e6261511a0`  
		Last Modified: Fri, 20 Sep 2024 17:15:18 GMT  
		Size: 9.9 KB (9869 bytes)  
		MIME: application/vnd.in-toto+json
