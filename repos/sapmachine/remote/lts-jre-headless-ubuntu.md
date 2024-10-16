## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:5a544d99eec11191bace5fb9387824472ac23a519d0de4b17e61419fecbca383
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
$ docker pull sapmachine@sha256:b23c5d34a675a24d419d6c19c855114b36c959e213c1f3dcd28421a6b2192c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88894093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb14952489bc91afaf44d519e7665bc5e6e77af3be3cd653010a86df40d5e266`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e24a9a5839f531bddd4aa4f2dfab0cb3941793ab508120e21967bf5df19c013`  
		Last Modified: Wed, 16 Oct 2024 16:17:50 GMT  
		Size: 59.1 MB (59143730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:374d6ec2d028a72a7c3d8a9533a9d38ff99fc11b56bbc7ed2738030a673e0565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf154744df933d5a805798773006544de51dbe487b431d2f891b31bd043b0f5`

```dockerfile
```

-	Layers:
	-	`sha256:9bb319849ee7aa113474323bf61104de146cb8293ef974cfa0bab029402ef626`  
		Last Modified: Wed, 16 Oct 2024 16:17:49 GMT  
		Size: 2.1 MB (2130253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033beace19f40084fdd4c59a39b63c105afddc33aeaed05a32779cae9423655a`  
		Last Modified: Wed, 16 Oct 2024 16:17:49 GMT  
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
