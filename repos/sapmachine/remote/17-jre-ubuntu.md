## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:ca7e94f5d512fd6dc89cb0ee25c8301e0e641693d55d8a7755a6e68f0f0a7a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d33b202699e49c0cfb7ae20af52d1e58541e20ba18d5d7d250a5c0baa0f7304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83798719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da140402abf95d6b3337785cea8c2ae0fab3d8e8fba902d922a06c8521d662`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d50ecfd29d9bcab126ec78bc6a1f931ccf4fa4170cd0e45c9d9c43ff67f47ea`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 54.1 MB (54093566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17ec148cf3ac7a11505548e64ffdac8f12d1bed6ead215825dffa299e70c91c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314b8ad168c5edb2d5687667d74bdb3b5b011faa8f164d6d0b322b03dbf3325b`

```dockerfile
```

-	Layers:
	-	`sha256:efb9d74785485eeef994daad68eea9ca45e5afa4512aa0b022594fa66f1ef6a2`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 2.4 MB (2360201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d41d5b86f49c2deca47b971191ba6a0a9cbce545ed97f9de16f0defc795463`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7ed645a1f75a6917a0628c1d01de65bf7c92b180df4c49c0abfe265d842446e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82327906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0813c9c581f55219d92847d39bd0b7e0559a5b195651dcb93059a81b515d9221`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7c452e43e6bea2f62dedf454694b613b68a52506af059744a32bcf91d66702`  
		Last Modified: Sat, 17 Aug 2024 04:31:37 GMT  
		Size: 53.5 MB (53484220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebbba2da021e14d5786385dc92685867395be0559cc8908aaf12f331002f6b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2370234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c85d6520f7687c18a143561ca927a38f3a8d05b186b4cb9fa43f13cee013338`

```dockerfile
```

-	Layers:
	-	`sha256:5463f33fa98fcd44d28c4861fee5a460e6a8e12b96660d551ec827b821cd8ee0`  
		Last Modified: Sat, 17 Aug 2024 04:31:35 GMT  
		Size: 2.4 MB (2360692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994a269988d7057b177a46eea1ed4da072229c215c8fe598f5d71bedea6968cd`  
		Last Modified: Sat, 17 Aug 2024 04:31:34 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:767a71452a6e70f9684a60f3ef9649b5aef28b87e19afb75846191cd6967cbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90222857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd418e19a1f90e31a0283a0e81ec81b311b6488183ba43bd78f9f65970157c19`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233558843c3bdfd8fd17e1cd2738dda7af1fc85c033913fc402ad5628802c6d`  
		Last Modified: Sat, 17 Aug 2024 03:11:41 GMT  
		Size: 55.7 MB (55715285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7989b794e4267237776770d31d7f2ed943ac1dc7a9c3c64e05f270e6bb985e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6593294867ab533eda748b5de0d67ec25413f6c4750dab28bf340d10ed1dc57`

```dockerfile
```

-	Layers:
	-	`sha256:59adfd0320c6463a9d88f641412848adf4b5ab07afb3e3f748321d1f42224a22`  
		Last Modified: Sat, 17 Aug 2024 03:11:39 GMT  
		Size: 2.4 MB (2364150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80f56640a2c412b8410b6a95238401768912a096ba7d43ae8e06ec8a98bf13c`  
		Last Modified: Sat, 17 Aug 2024 03:11:39 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json
