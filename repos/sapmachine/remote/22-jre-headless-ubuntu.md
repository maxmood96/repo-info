## `sapmachine:22-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:6475285c5f5a28859758ff0e05f3d81b42fbb499a80d887f8c06a98d6fddd76f
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
$ docker pull sapmachine@sha256:f7dd9f2c9d2d4d8e942aea4ba28dab4124248e81e041db8925334c0965ec0a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88032542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e4106dab35a09743b2577e382fe61a79965f2328e27996156f4f0609d1d43f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf31b85a51781b2cb15507a47bf83dae5a4c63dd24cae6293f445cbe028fc80b`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 58.3 MB (58327389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0fac1e087395ef2c9a9b82f5917b2609e05480c3da4f209e5b75d7d99744cfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441788a92ba06faf833dd91f9bd3d1e28bb6b92c098b374940d799e87ba4a7d2`

```dockerfile
```

-	Layers:
	-	`sha256:03fb54ee45818ef026abee19ea1ddbfb05f613005e9b14fa0ed52bafb459d199`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 2.1 MB (2127650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dada7925b60b08846353cf806d72b42fd1768c26c7ddafa9b32d90a06a02503`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 10.4 KB (10373 bytes)  
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
