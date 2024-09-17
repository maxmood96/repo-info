## `sapmachine:lts-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:7b3a3a7ec49c122eeb3279a00befd786c256eeb136d54d24826a213189883264
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c6355b9f926815bb6a33bbacf6a13caadc2881a3894df169c5cc94449cc9d997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92481410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ba00199b0952bb257d1325b746a52903208806d5ab058d00ebffad44168ae`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0327078d0a7996abffc3715608cd237be7d852fded96311131acfe546ff91cfc`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 62.7 MB (62731582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:51e5954900e3ef1454e3ed2b2cde15592fc3dd15b322c6c769a0581ff0f35bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc99e8d5b7a045099abb0817aa9a7a2d51b75c2593d5865ebb9d8e2651daf67`

```dockerfile
```

-	Layers:
	-	`sha256:91b12a147d52c8ce3429bb485ac57e88641df2668a8ad5078303f7e02f97d584`  
		Last Modified: Tue, 17 Sep 2024 01:00:34 GMT  
		Size: 2.4 MB (2365642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86beb1bc7cf6fb90090743b79652daf1c7dcdfe4a872f127c8d0ba0fd38ab188`  
		Last Modified: Tue, 17 Sep 2024 01:00:34 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e2fccc8bc2b03d9682adb9062004261135628c00dc65cde97abf6dcd651db0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88280908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccccb6b304f2390233b32c3ff9bd74d7e59c7fc48e240e5ef6adb773a24d615`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b83469d0e4eed01471a3a26646af72a27f7ebbe9afbe593e679c659a56d6ce`  
		Last Modified: Sat, 17 Aug 2024 04:18:15 GMT  
		Size: 59.4 MB (59437222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d540116068f2cd69316b8c9eac7d8da9dd80afd45d1b2b8416a5016b86ac24de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b7b5cd4912ff69bcbd869258d456629c47a809235436d11ad0ddec4399cda7`

```dockerfile
```

-	Layers:
	-	`sha256:dce342020f2f71b85e9eaa2f8395b7c3ad9ebc6d5a215ea127b6f99c22910ede`  
		Last Modified: Sat, 17 Aug 2024 04:18:13 GMT  
		Size: 2.4 MB (2363611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845ec7b388ed8258b1336e5deab2da8288fcfa3d24894a4345b50ab64c247377`  
		Last Modified: Sat, 17 Aug 2024 04:18:13 GMT  
		Size: 10.6 KB (10557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c0aa1ae7c6e1ec132e4ecfeae8f57fcc30114f90f3d4459da112d9d2f4ead00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96528358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e900889ea1af47c9b3852352e95d71b19b80ae770805781fa10cfb2c532c5d0`
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
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccae5f022e65d33051030a97e56c53ad6b37d916e334b5631284c6d71d998f1`  
		Last Modified: Sat, 17 Aug 2024 02:49:52 GMT  
		Size: 62.0 MB (62020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0bb3624fd50b9aaa6dd0ee328a0cafced1753aecf48563ecd7ff1d0d5afb108a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d164a38b4fc84169821d6d7c1968bff0303cce0d858fea6aa4cdd721835f1331`

```dockerfile
```

-	Layers:
	-	`sha256:3412dd36a1948761c4d1aebc9500baa1dbf9df4b87774cfa2ce6c16ca20f50f1`  
		Last Modified: Sat, 17 Aug 2024 02:49:50 GMT  
		Size: 2.4 MB (2367051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d047223e05e61ad8767f56028024750cb405b5120e213224c5479770489ecf`  
		Last Modified: Sat, 17 Aug 2024 02:49:49 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json
