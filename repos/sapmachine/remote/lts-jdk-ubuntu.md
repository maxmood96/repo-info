## `sapmachine:lts-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:93b7c458d4715498b3237b2375ff3744abc1d91542535c8551fa4c0dbe9f7e5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e014fed844d19d550cac97002bb7bf147c70d68797b3763e92a2985345ae4138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245302326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bfcc724b1a1b224cfb2d286d264908dc19f796c00d7cf9815d71dd5f389a56`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:799e6c8a18494d282df4c820ebf58962cdbe65114f284259876e154b4c38e63d`  
		Last Modified: Sat, 17 Aug 2024 02:05:55 GMT  
		Size: 215.6 MB (215596028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92288595279afbce32b495d42a31cbe75be877e17d8e662cd9ff58b3b2cb77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4786524acad3da86114b20fcc1045367ccd95ead063cbc1e9317e6e7953551e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f765719eea909fb0bcca34460c48873d477a5e6ecf83c504cdf102087b0daf2`  
		Last Modified: Sat, 17 Aug 2024 02:05:50 GMT  
		Size: 2.4 MB (2449605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cb1e1dd687f02aef3473f52d56b1969fb93e03c464f6228111d4d069d48eed`  
		Last Modified: Sat, 17 Aug 2024 02:05:50 GMT  
		Size: 13.1 KB (13065 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e0235d94b201cdd5d18ac72df02f12037eca6b0a46dcce4e56329c24ff9446de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242544510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c2a0aa8867d0ff5d262acd1941e02e2992f31e1d2a4b019ea5edfeb831a35`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:65e0702038986356c3440bf49ddb10e4b1c8337d5136aaf103ab8043f0dba6a3`  
		Last Modified: Sat, 17 Aug 2024 04:16:13 GMT  
		Size: 213.7 MB (213700824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca4dadc3a3ffbdc8dda65db9c74845ed2e5fa2f62088790597cb778be760e0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be48549f49df927dacec25eda2e5e0571ec2936214ee23615a090bebe4152023`

```dockerfile
```

-	Layers:
	-	`sha256:f4fe49919b873fc64988db2142c16bbf9bbacc3e70318fe69a580d0a50ef2b02`  
		Last Modified: Sat, 17 Aug 2024 04:16:09 GMT  
		Size: 2.5 MB (2450240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35a4ff2701aef7b6322b8804380a022cf0eb3d8bd29db4da1271fe7c178a8c9`  
		Last Modified: Sat, 17 Aug 2024 04:16:08 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5487d35b0b34fbdf412f694586b1f12b8159515c9e27d6d38df92a4cc57261fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251565744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35501eee086a67d2ffab39c0f3a69022d27507f3f4d76e45fff6a8fd9c9d3269`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e0b635f6eb6a60370f38c733b410c2c5c704b50b31485a59ebb304b4975e12d0`  
		Last Modified: Sat, 17 Aug 2024 02:46:41 GMT  
		Size: 217.1 MB (217058172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b9307dc54eb579dfe51c69fc40df176dc9673daed6c8127d745c72c7e0942478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486f6dae696c04e012c950a981b5cdaa57c382fb8f26a75141e77964f1d660f5`

```dockerfile
```

-	Layers:
	-	`sha256:251f3425df60f23b4d90b55f66e983e3fce51e32369a21aecbb785611f890f53`  
		Last Modified: Sat, 17 Aug 2024 02:46:35 GMT  
		Size: 2.5 MB (2451677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27fd18a9f035efde98cb8bc6a67f91e32db84db3a47bdfdc5e57074e7abfb751`  
		Last Modified: Sat, 17 Aug 2024 02:46:35 GMT  
		Size: 13.2 KB (13186 bytes)  
		MIME: application/vnd.in-toto+json
