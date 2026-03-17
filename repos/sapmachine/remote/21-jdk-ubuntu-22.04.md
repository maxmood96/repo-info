## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:d3ad0ab894fe2616501f6b84f5e4bfc8c45032cb3e6be8afef0392a3dcf5f5ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a65927fb0f3af0ce8d81ac68771ad4e46cf580cfa5d4588551bc1be7f47d3269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245647728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4595bbef422fe73b192541222da000264822dcddd7f5a441483fb6bc2b7174d0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138bcd3d3c7999ca0fdf14529bda217f6a3d9889af7c71cae273e62d3ee51a86`  
		Last Modified: Tue, 17 Mar 2026 02:25:15 GMT  
		Size: 216.1 MB (216109208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b02034ecabe5ec5cdab931f6eb6f9069e907e5a4e55f363049ce3e477225d826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92be1de14b37c3f4f8d6c041a33187637cd921f56d650275b5ed89b9c2eee4b5`

```dockerfile
```

-	Layers:
	-	`sha256:7e41705561a139d917ef543787b5260617524258a6d555d1500c6e3bb756de1e`  
		Last Modified: Tue, 17 Mar 2026 02:25:11 GMT  
		Size: 2.6 MB (2632170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081fe087f80403bfd3543fd1ba9c818dc4daf7774ed42c4097604e696b6b2011`  
		Last Modified: Tue, 17 Mar 2026 02:25:10 GMT  
		Size: 10.1 KB (10135 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:199448ec79b0b6b4084f91ece31aacea0fb9c2b3a636e843209e83addfd5bd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241711527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40255bdb1ca39f15227e943359f4028c054adb07bdab8ffbd14dbc42aae84b72`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:31:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf6ea9de52968acc0d290f6a3bb781e1dd60cad7c9caea4fa6e0e4aedacb356`  
		Last Modified: Tue, 17 Mar 2026 02:31:26 GMT  
		Size: 214.3 MB (214322502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38cb813e4b2de97fa4211d73a1556373ad7b04a2eb3f62854def7e2c35edfbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce829f99438e2d1588b54760fdb2bb3350efc37c200557e503a134e7106c7d`

```dockerfile
```

-	Layers:
	-	`sha256:c80b8fc5ec38514fb7179b38d298202bf151be047f442f4e4a5ede8781bfb4aa`  
		Last Modified: Tue, 17 Mar 2026 02:31:22 GMT  
		Size: 2.6 MB (2631900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31363b19d6095b34c9b8b59720bd1a32c6d5abf54bf442f789aa6a943e0da5d6`  
		Last Modified: Tue, 17 Mar 2026 02:31:21 GMT  
		Size: 10.3 KB (10287 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ac3aa0d2ab9d14601b0213b470aeac4779a7c473188c7701b94713122f49a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251526850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65ca3a4c4a5d7f151cab6b822aac49e6c5dfc3b7fbab3ba3aa37365bdbe8bdc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:45:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:45:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 09:45:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d5e65848a32e306405f6c97b3f94e71831d01c936dd82ebb379c0c4baa1727`  
		Last Modified: Tue, 17 Mar 2026 09:46:25 GMT  
		Size: 217.1 MB (217073402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1276d34e0e41beb5f5e08c485a10a7ea8df736c57459bd7d0b4817cba47f3139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf4792326428ed9f966b399146df4a9a3b7f24fd611b3593678d223ab4495fe`

```dockerfile
```

-	Layers:
	-	`sha256:c9e876608e2e8089be2f40ebee4b74608da9b9ba64e51a07980275079b09e759`  
		Last Modified: Tue, 17 Mar 2026 09:46:20 GMT  
		Size: 2.6 MB (2629780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0905dcc502f73b3ad747b4f88aecdebade6bdc6a4da0911d72e9b1cb343a93b`  
		Last Modified: Tue, 17 Mar 2026 09:46:20 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
