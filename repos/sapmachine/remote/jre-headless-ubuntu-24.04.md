## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5103c9f2994be2eac14ac0960e9aaf8e5262d23f5ffd2879be3541f2d3b31436
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ea88edde9444384de39f29dcaef31ee41ce7a7433fcb6a4a1020d05df8a4fc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88033603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae750e395da6a1687dd7e9a129af5ce76c8d6522fb7c8e92276d16031c1996d0`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb9ab5384f420e9d77f17e24a6617ca1170a116722d85510c9dd3461d0ec365`  
		Last Modified: Sat, 17 Aug 2024 02:02:12 GMT  
		Size: 58.3 MB (58327305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:da1ed6eb3316a215937f594fe840e1b9e61801f487b6d87e7631c112050f5a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2373821803c8c2fbb983f54594b7431fbad9af14f719c939d8e7331a7629e1b7`

```dockerfile
```

-	Layers:
	-	`sha256:ecb743951f079e3eb4f7843cdd4a75eb0cee7737374709674681d99cbf16a699`  
		Last Modified: Sat, 17 Aug 2024 02:02:12 GMT  
		Size: 2.1 MB (2127650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca1968f01cdffcbc67dc894a3eeaa4964b93a666ac643deab8bbdcdba6d99d9`  
		Last Modified: Sat, 17 Aug 2024 02:02:11 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

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
