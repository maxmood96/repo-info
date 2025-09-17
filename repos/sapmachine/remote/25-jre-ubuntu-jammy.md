## `sapmachine:25-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2821fa818628d63e890a3ca79f6766d65ae47e2eae76fbf3be8d42f6e8738262
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:55b8053885c1dc6b0e32193c000c1eff7e9b154c1d61f2cec3b6073dec8f39ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98125193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa47556d3fc43f3622357ba9a69fece82851a758d0b2aa7bc7a270f09832d63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa9fe2cbca0ace220c46d6290d19cff29061a72c53e36f2c28eea12d6c8a23a`  
		Last Modified: Wed, 17 Sep 2025 17:37:05 GMT  
		Size: 68.6 MB (68588258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8a6be36cf5ea23d39a09fa98544879cc8713ff0eb9899f641a9a352107f6fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35e991d1b323336715ad28fd01975264313ebe4ea266344610ad53b46b11a27`

```dockerfile
```

-	Layers:
	-	`sha256:1ce35ff5955d686965ee6e2d228f2cd7a34cd95414127e2005d65f8f804f6572`  
		Last Modified: Wed, 17 Sep 2025 21:12:14 GMT  
		Size: 2.6 MB (2552571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933718b539c362f3f722c3590897c782669496b0521548536595608ebc4e4765`  
		Last Modified: Wed, 17 Sep 2025 21:12:15 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:effdfa9fa0f3fed6f837b031c0db3e684c785f976d098890b4708c7503b50ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94883326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ab92b2745c1b27294f87a5b81dbc11d594644ce5e2dae5238b8ade6c9779d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67195900204b3210b6edf78e78eea60f38fca19493e6ad95ff7353ff8ce24`  
		Last Modified: Wed, 17 Sep 2025 17:40:10 GMT  
		Size: 67.5 MB (67521857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:856a63b70cce8471fe869df17a36bedbd69c9e001384ceda3f891905583c7ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8a438b10556bbc491dd6b8996704b9f48c007ff99726812080236ca8cab101`

```dockerfile
```

-	Layers:
	-	`sha256:d07756bdf4940f82ac76b9549957ba047816fb0d1d751d1d945118570d1faa0a`  
		Last Modified: Wed, 17 Sep 2025 21:12:19 GMT  
		Size: 2.6 MB (2552274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a47d07a3c8439921f1655882484aeb2a470cbad74384d4be00b6389d44b12a`  
		Last Modified: Wed, 17 Sep 2025 21:12:20 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0091afa2bf632be96f88d37c1b053c2a3513ab41db001e03e913d064f1631e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103867004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7206db6c6975f3842e4f59b30c57862d8721f7a9357336afc421c9b96ebb4161`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd8a26bf0bdf337ec2c8588e443367b5709d8bb56335de36894b37f7f0186f`  
		Last Modified: Wed, 17 Sep 2025 17:48:57 GMT  
		Size: 69.4 MB (69423780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1cd235c276cc1914e65f28b3da9fcc4ef2fe18ec6eaf49f3c7cb47437dfea505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9b89124584302cb4bd2ad4762838e3bc57c8cb4692086e9a01759593ae5405`

```dockerfile
```

-	Layers:
	-	`sha256:3920d0228dac7f5928bfa22e7965f1e4e23a1f7b654e21f9d2580aff1fafbffd`  
		Last Modified: Wed, 17 Sep 2025 21:12:23 GMT  
		Size: 2.6 MB (2550068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4205f511f5953767e2c617ab730324eea185728fb4c70ed6a091bbe940ef63d`  
		Last Modified: Wed, 17 Sep 2025 21:12:24 GMT  
		Size: 9.5 KB (9496 bytes)  
		MIME: application/vnd.in-toto+json
