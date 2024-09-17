## `sapmachine:22-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:95de2f5bc28ae45c29edac3b5f14cf4fbdaaae9c4f46b3dbee465ff5b3b123df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:46716eddad12eb8bbcc3c7fa36ef12e74f7b25629f72ad3e217cb389d289b369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90478590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94149e635910e820eddc635a2f13877fbcb932c535071f1f053fc682c0dbc12`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d743a32465d8eefee7d0eef080018e2a0ca198147a6389219a4d6fc4eb4d7807`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 60.7 MB (60728762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:860cbdaf7219fe764654e26870cf8070597ff565feeb7887617a4a83723e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690581e6cac4bcd056fd7c78232c47d5e3486cbcae0448829aeed296ac6d0d88`

```dockerfile
```

-	Layers:
	-	`sha256:d2295efa9adcd69cfef6559c7967855289ffd031d3cf60d6745a04537c6af919`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 2.1 MB (2130208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9aae2f84d9c9c0e9fd773b82573be73b89bc08519f1ef32da2ae7ee447f159d`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 10.4 KB (10372 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3e2ec45e58a7ab5e0c4912363986a2e34422a6296ffe6340062a66c0876e575b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86218303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1841dc58a2d55f05d5110b3628749ee6bc0c26be6d0eb5d830b699ba7fa14c26`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e11eb4f5894417a7711ed88abacf5251f63a5fd7a8635e67171cca8de5d5467`  
		Last Modified: Sat, 17 Aug 2024 04:06:45 GMT  
		Size: 57.4 MB (57374617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a42ba16bc908a1118aa55f3f032bef8dafc0638fd394532c1b7cece14bda3b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb415ddcab8dd9f7c6f795e39562e071010674649ccbb6265fc29a8ee841d7d`

```dockerfile
```

-	Layers:
	-	`sha256:da801cfd2ce6082fd734cdd25c73eed0ede6db32c057d9344736fc1f1e1d689b`  
		Last Modified: Sat, 17 Aug 2024 04:06:43 GMT  
		Size: 2.1 MB (2127537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23a7d023937ef4f0f81f929eb4094eebb355d6cd4a6fdedd415c79e97bdb421`  
		Last Modified: Sat, 17 Aug 2024 04:06:43 GMT  
		Size: 10.7 KB (10734 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d583fe81e86e5538995a31a98c51583100db817ad420cf34d52798809254ed5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94218218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d079c00a5c136430efd4b5dc5086cab06e63581a4fbf8bf15680cf8da1be73`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2dee9e9b5d75b53250bdb446b2a9e6b8d049f1d8f0d33af1e6ba7d7e31a16`  
		Last Modified: Sat, 17 Aug 2024 02:30:23 GMT  
		Size: 59.7 MB (59710646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7dd88d8634515273419fca7188b147562b0f91d4bf6bb0a6bb1af5c80f459072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be13a4c28dee98b54abe93f1355dfe8be35d168aed687318afb110d0d2e89ba`

```dockerfile
```

-	Layers:
	-	`sha256:99c83b50aa287f95e97709fa81c50e8398ab09ded894c8b193e724204ab41f34`  
		Last Modified: Sat, 17 Aug 2024 02:30:21 GMT  
		Size: 2.1 MB (2130923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7905dbec3f6f648c7c060dcb8c700c6db70eca727f848833df1517c04ad6100a`  
		Last Modified: Sat, 17 Aug 2024 02:30:20 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.in-toto+json
