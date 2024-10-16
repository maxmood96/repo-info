## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:8e4e7c919cfa16e1d1785d7290a6aeab4770c8a63691189c660173635ac918de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:5c29cae421261e9af7a149bff5a47623d933b2160c28f36f13f95b0d3a0e814f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88894182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020c1d5baf3467bc0d436eff8434dc194526da2dd4ed1ac234b80ed02f13bff8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeedc6c4ab9b0556672dc0ca2650f5d01e545057afe3efcf31ac19b6a72ed09`  
		Last Modified: Sat, 12 Oct 2024 00:01:08 GMT  
		Size: 59.1 MB (59143725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23840438fc1fdc7cdc253ad5fb90f50d97287200c96db23c449579796ecc164d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc2acc6a7b488ffd3e4747a49b28e83d5c775ca1c1b3f7d39df76ed84814b0d`

```dockerfile
```

-	Layers:
	-	`sha256:cd3768b7afd07249333c4bb9973a806c831759cdc1299cf9a2b80b06daa80aec`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 2.1 MB (2130253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4fd43698bac2bd8bc84ea9ed045995a702978e73d523cc70f2e209ace31ef7`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3fc86c510dd28be2e3b4a05583f642e8e34c3d7c124032a57c7669158f52389b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87129912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cb7c74dbdab8005c38cecb4ba60fe90230e1e5b34ef2768dde144950befe94`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3c7bc0611e2ace540c639a697979f278c9e9ae863249235afcc140d303fd7`  
		Last Modified: Wed, 16 Oct 2024 04:32:36 GMT  
		Size: 58.2 MB (58244067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32d5d2c9cff113c6b49bdafee81df1c934651c250001f43401e533333622abdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a6e449870a93db929ef7100ef18870695f7d0369d8d580cc12b8a7dad30b88`

```dockerfile
```

-	Layers:
	-	`sha256:c455477981a030f6259640e23e16e6049c4302f33aab80fe048c4791ca61608c`  
		Last Modified: Wed, 16 Oct 2024 04:32:34 GMT  
		Size: 2.1 MB (2130771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc9742da98c126c9d1b4ced21f5e0e39d60567c78bc3b99e7285c3d288fe12b`  
		Last Modified: Wed, 16 Oct 2024 04:32:34 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c8c817518be987ee8cb70612eea7708d94db564e864bdb39bc48a153ef71b11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95018618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf457803235709ed6601c307c862a7b0c3566818ac9a6c37317985bdaad322b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79be113dbcfa3017cedc148ee8b1052de6d856d98e75f9eb17c2c84834c10`  
		Last Modified: Wed, 16 Oct 2024 02:49:17 GMT  
		Size: 60.6 MB (60629649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb620d9a6ccbd953004d7d54f0ceafa2a01442f1a8d03fa571faec3bfae01d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2144660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5d3926e638e4968d8e1cd572470436bcda90e34a48f8b7edd0928858cc93a8`

```dockerfile
```

-	Layers:
	-	`sha256:c7bc789965194ff05ed2cb2513ffda695cd7820e6c48ee556aaf15584860e6ba`  
		Last Modified: Wed, 16 Oct 2024 02:49:16 GMT  
		Size: 2.1 MB (2134157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c886af2428bc605ae8ff6e7c6fed5b3ddaea45778e8359a7308d989d28dc6c79`  
		Last Modified: Wed, 16 Oct 2024 02:49:15 GMT  
		Size: 10.5 KB (10503 bytes)  
		MIME: application/vnd.in-toto+json
