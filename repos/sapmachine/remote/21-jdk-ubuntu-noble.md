## `sapmachine:21-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:7ed3b77227512cbd055eba4e639d65542d966576e46c7d34422cbb438f5de453
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:9da5588a7e87afd3a189a4765ef909c922f8cf7f40ac9a450ed6dabcffe51ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245033267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab3129e990bd5a1dd5274cae30f0bd93affbf839ed74257bec2a0a6239be34a`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b236bf7e641a8ca8d959874639a1a4fbd53ce4c2bad36e37e073ceec0b796173`  
		Last Modified: Thu, 09 Oct 2025 22:54:19 GMT  
		Size: 215.3 MB (215310120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e1d007284bd0e8abd08a9949d5f3f215e38e1c30f35901085a73ffa40a5c141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416fab5b45f4e2a18d0a5c9312858aaacc49ea1b5755761c64728a25962a8135`

```dockerfile
```

-	Layers:
	-	`sha256:24ef0df95f08d68eb7124602d8076402409c2fcceac4628b748bc28248a06f4e`  
		Last Modified: Fri, 10 Oct 2025 00:08:40 GMT  
		Size: 2.6 MB (2604701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bc6ce8faec3f310a1a50f2b5c0408a2831a46ff4b1c59900d73a45a3816733`  
		Last Modified: Fri, 10 Oct 2025 00:08:42 GMT  
		Size: 12.6 KB (12628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0bcc54a6529ec8a458731f5aa9445d6ccccbc89d2cc9859146ab6bdd9d1c0814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242479492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5440abc36b4de94cc5469413e262e7e7b26ea11eed36f06ac98378272bdfa3b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7071e302a1a5dff6b5e6e89543863d918141db2376a55576de31929df5e87150`  
		Last Modified: Wed, 22 Oct 2025 00:10:00 GMT  
		Size: 213.6 MB (213617780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d1d08a1e3bec1b377d1e27bdbe2ead9d9bb3103368598178fa29aac223327610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308c0d39901eaa11ee25b27d0d7d152ab00d47a5a0f36e99415ad0ad72b22573`

```dockerfile
```

-	Layers:
	-	`sha256:2896bfc3236060019e127df0f0cc9757511047b4ba1e966cb1055affa7b6fcc1`  
		Last Modified: Wed, 22 Oct 2025 03:07:05 GMT  
		Size: 2.6 MB (2605313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ea532c0794c77b204943f5ccacb1a144e439440b63e9c513bea1b140106027`  
		Last Modified: Wed, 22 Oct 2025 03:07:05 GMT  
		Size: 12.9 KB (12877 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c26147c2c3fb21a8b7bed88654089b3a808f56d408b69e95da98b37e09309bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250567495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce955d52f0d17e87cecf6a846b56fbd8ee8d2a844c2c56421adeca99c43d4270`
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
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d2882075951f3ee2fdf8ad13505181ab6c080a467f19ff20eff69f3081fba3`  
		Last Modified: Thu, 09 Oct 2025 23:12:03 GMT  
		Size: 216.3 MB (216263970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c0b3a30f566a078fdf8d22dc98ca14051eb9263a766d6aed462bb500eec48722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477ee6175d4a7824af3cd632851d4674045aee9cd10ddeea679973c63be10f4b`

```dockerfile
```

-	Layers:
	-	`sha256:413e2d0a6f25621f8f90717dec721938796df9b351e584a542b040f3784a88d0`  
		Last Modified: Fri, 10 Oct 2025 00:09:00 GMT  
		Size: 2.6 MB (2600884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b1ce4b4df7530cb37f5fceea89084c34de980ccebca70f75c30e5a31c05783c`  
		Last Modified: Fri, 10 Oct 2025 00:09:06 GMT  
		Size: 12.7 KB (12745 bytes)  
		MIME: application/vnd.in-toto+json
