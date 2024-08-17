## `sapmachine:21-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f328eec5a618644cebad258202b6ecb526b2ae9fbdecc079195c240d1a682e9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:54d6df46c6db994cef586f046d69922100a3d45c37f4838cb1382d780bdf8c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4474e3df61f9cad5b8893a38969cc5d99160fe0701124e1dcbb3414b2d06425b`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e720ceca83ba7b4773e717db38672149649f1108a5a420c91dff2a34758f15f`  
		Last Modified: Sat, 17 Aug 2024 02:09:34 GMT  
		Size: 60.3 MB (60327335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1df752b26300da505894b9c4f643111d6bdac33b5c11fb1df265b33c78f3ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5be3d7407093cc58637257f6603865d398bc9c89828e7dd962cc96c4c566a`

```dockerfile
```

-	Layers:
	-	`sha256:f991fa734bd01c6b161ccea81b34c1931cb0a50fe64f63ff6373926c71e893e2`  
		Last Modified: Sat, 17 Aug 2024 02:09:33 GMT  
		Size: 2.4 MB (2363084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19912fce5845ed829217a3931eec5e0ae97b817834d4f032332347b5f629c15c`  
		Last Modified: Sat, 17 Aug 2024 02:09:33 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:21-jre-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

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
