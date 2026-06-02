## `sapmachine:17-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d977ca60362dc870fa799d0e99922539c696cc83d62aaafc427856666af5944b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0816f8b9eab39f3947fd1e98d17047c39a41de2f44c166350f2c94f4063e8f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231750634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6e7c75502fb713afd083fb415f5d72c3e9959bfdfa9bbef94a7334f243c90a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Jun 2026 08:24:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da46350d213f113e73532d4178989ed5d698ad1bd3d462291e7374084de1d17f`  
		Last Modified: Tue, 02 Jun 2026 08:25:17 GMT  
		Size: 202.0 MB (202017829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb9f17db7a4d8f3ba411a820700b702f0a2350686a62deb60e344201baebc6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63655ba7839b44a52098a07b2eb3aba08db9cb9fc62065b7b7eaef6c5b02e17a`

```dockerfile
```

-	Layers:
	-	`sha256:18e54c263b0c5e914909e32ad050384d239dfdd9f4dcce59499544c6a720cd2d`  
		Last Modified: Tue, 02 Jun 2026 08:25:12 GMT  
		Size: 2.6 MB (2606177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3680e706183a9b9a17b1dbbee3fcec0e64fe46af5a0b7263e6573515fc1294`  
		Last Modified: Tue, 02 Jun 2026 08:25:12 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:912f6c78ae53c57d1796a636aabe2c2167bb7087be34d21eb4f8f5c4acd11478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229643824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1805316f854863cf5ef36129bb7a9ea517c5734646d81654dc47dad3da4ec09b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Jun 2026 08:25:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737c2ccd0541eeddd6663de59542d49e280d0358245bd3432e9d730d8559e3ed`  
		Last Modified: Tue, 02 Jun 2026 08:25:46 GMT  
		Size: 200.8 MB (200767418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:751130bc43701177e46af4aa28fee3667d03935b741f4865aad24feb9c631a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d7a04fe6af8a78cb1e428996dea169a41370e535145dc5cc95fee9fd0bf092`

```dockerfile
```

-	Layers:
	-	`sha256:6d6dedb047f5f0940f7af233e8e979a95e8095215e472a3932f4b9e505f039f4`  
		Last Modified: Tue, 02 Jun 2026 08:25:41 GMT  
		Size: 2.6 MB (2606789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c62c18a711cc000670ac959babfc9b71dc298485026213c8c63703af2fab00`  
		Last Modified: Tue, 02 Jun 2026 08:25:41 GMT  
		Size: 12.9 KB (12854 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f0e1b8f8715a67aeaa6351783b73bc316198956967e4659ad81d27fabcaae58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237247591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f29ce9961d3a10d7af38267eec1e45c2692bbc06422416df7f8917291f7487`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 09:01:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:01:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Jun 2026 09:01:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2683fec7be5d052baee597afacadc5444b2c2a7505120f6845f56f8ec3b89e59`  
		Last Modified: Tue, 02 Jun 2026 09:02:06 GMT  
		Size: 202.9 MB (202933492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ae3dbc7f296401434a4139480dd4f209d9196f61a95a12606d31d9fd7532a2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc36567eac70bb6ab22527cfcfc15a7c9baf4a1c7d02bf4ad6b1bd3ea95d5764`

```dockerfile
```

-	Layers:
	-	`sha256:7510c19368241ea72a1193b2b943013d548df5d1d0ca66ef38523335c9cb92c4`  
		Last Modified: Tue, 02 Jun 2026 09:02:01 GMT  
		Size: 2.6 MB (2603777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7421401697864f514a12fbea63e7f330141b5593840fc8bd7bfc9f30a1ddbdb9`  
		Last Modified: Tue, 02 Jun 2026 09:02:01 GMT  
		Size: 12.7 KB (12722 bytes)  
		MIME: application/vnd.in-toto+json
