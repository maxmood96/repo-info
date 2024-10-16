## `sapmachine:11-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:06d0250b680287ac162cd781403556cffa144cc564bb7f9b2689d9154e825cf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:5f5821a1f309af7efba2e374bac34a5c7a5f43ef4844f355429c5f5f799b0e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230987920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5718eb6c92f8e8b34d463935322f183c505dc0bec49f48b974c99231976fac1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a8b9e9f50d7f6a4365629d3b5dc894eeea332242634b23103260a5725bc9ea`  
		Last Modified: Wed, 16 Oct 2024 19:00:38 GMT  
		Size: 201.2 MB (201237557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ed3ba993dd93abe1eeac46ec24e2148786ab310a706fa8a4a17d524b8ebffa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15de509cb3691de7c02b5b122df264e70f56b9fda331b9299f6d392f84010c33`

```dockerfile
```

-	Layers:
	-	`sha256:73f385b1e7ba0d39a0413b393abde2b67651d2bd926fee81f941b624da6862c5`  
		Last Modified: Wed, 16 Oct 2024 19:00:33 GMT  
		Size: 2.5 MB (2467575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ada47c9521e124952ad4387d416faf53b302d0ecd9c3b86ac4edb6da219e9c`  
		Last Modified: Wed, 16 Oct 2024 19:00:33 GMT  
		Size: 11.2 KB (11178 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4b4d48489a91bd48de59a88cbeb871a54fa81d08d2028fc666852dad0b691c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228625192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8d0ffb5d158c69604c93afebcab68581492fa44b926ed1cc8df1dfc8440012`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd9de52288d03f40de8a63a49f3c4291ecfaf25782ace774f069215c1e0c59e`  
		Last Modified: Wed, 16 Oct 2024 19:42:02 GMT  
		Size: 199.7 MB (199739347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7812f92f84f665cc4ea836fea4b8fa9989df9fc3b6fe82a11aacec9210d57378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2480138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bece50d2fec1875b0254f5b9c9a2b621e932b7d32e5af86ace22c90a8d966`

```dockerfile
```

-	Layers:
	-	`sha256:7aad4c5ec15ed0a7359332e3d3a462349b933c2f5d069950e4f2ca829321a0db`  
		Last Modified: Wed, 16 Oct 2024 19:41:57 GMT  
		Size: 2.5 MB (2468766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feea472513ff95e08e353364ccc16dcf018bb7bb807298b5c2a548061927e254`  
		Last Modified: Wed, 16 Oct 2024 19:41:57 GMT  
		Size: 11.4 KB (11372 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e20cc4b0b59aba3740ee0cab5c670ecb8ee2ac8073bd9271c2490ca4e61d2e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222282629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d3952cb11766838ecd0f74e081bf5c1b1b0370ba06357e1dee8dd6c2cdf9a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2311b9c7ed18ae94577e7cb3b57ef542993fdce5c4f27b0812049354f5c1d3a`  
		Last Modified: Wed, 16 Oct 2024 07:06:24 GMT  
		Size: 187.9 MB (187893660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aed687761c640c3944572d49372355be5e2e6247f128f4e1bbe0a8a0f01354a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd38b91827d40ac9f3003b4099aa9a84b2f5aaac72c8b819b704b4d79c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:13357fdf0b707dbf0440dbcf231e5ebce9edf719e33d48906b7b5353f35143be`  
		Last Modified: Wed, 16 Oct 2024 07:06:20 GMT  
		Size: 2.5 MB (2467718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2fa816b659e4d1cc12843ad1997df636cc7d84752262f4b6d193cf20fcc2c6`  
		Last Modified: Wed, 16 Oct 2024 07:06:19 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json
