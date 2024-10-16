## `sapmachine:lts-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:95a4741be6af5c9e9b4d224b9e78ac770775a5b1dbe140c2e82313d2ea34bfc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5f23100390c7f9bfc5b6fdbab02bbc34794cea7479500cba8de02fcbf900ebd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88607275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d16a1fe3b11b85297555466631b27f38fa1b9c0c90ffbbb842ecd3297bf4a6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b63ff5ee5f42da29c5548aec2c9cf2636c7bd867278c650231eb5bc23fd804`  
		Last Modified: Wed, 16 Oct 2024 18:58:44 GMT  
		Size: 58.9 MB (58856912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8dc6f88a15aa814924950d3f134e364ff478588d9202b5d7ba4907b2306bfb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08edec918bebcc59ff5b26a5c25fad8b5b20994ded4bf9cb83be98b8951394b`

```dockerfile
```

-	Layers:
	-	`sha256:0b5945ff5f4efc0fc39cbaed80c04e5ee336bc71709445a3e01d19b0e83aadc2`  
		Last Modified: Wed, 16 Oct 2024 18:58:43 GMT  
		Size: 2.1 MB (2136256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f7537c5ddcc17c7ee3b0ac4a319294b484a524ef751fd0ff2940db9ea0ad0e`  
		Last Modified: Wed, 16 Oct 2024 18:58:42 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:45328dcbf5add8d01e093a144b020552a3e66514104d81eac93b427a81fab0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86895431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e054a20e062890704ae61b3f378594ccf8a598e0b21616cfd1edaa2676bb033a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c88131a87328e4ada5b94fa9ad30211fcac764f4381ef5faf677dcdd87790`  
		Last Modified: Wed, 16 Oct 2024 19:16:31 GMT  
		Size: 58.0 MB (58009586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a86ffc1463f46af6fd7d4f24a314f5427d41e453c712fc34708751e98973f79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2147366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba565e239420c63bc49ca841d730d837dc94f9f12665043a6ebdb429a89be8`

```dockerfile
```

-	Layers:
	-	`sha256:b413a81b983f08ed2ea2571bb599649d6a8c079a48582d72fd307f7ab10f5231`  
		Last Modified: Wed, 16 Oct 2024 19:16:30 GMT  
		Size: 2.1 MB (2136774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e2fbbae906fc1adf39a622003868c39696be93d925822584182f16c94bf242`  
		Last Modified: Wed, 16 Oct 2024 19:16:29 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b195c95c2efee74e3a94cddb85704d317676d8f7d688a60c1f8bd6e014a011c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94753497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4087f45e5d3d4f575807af4a6dbb435b5b694961f8a65ccd748067dddc9b84`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1617d1f74080ee37390670cd650afbab8604a0493e884e93cb8dfb26db972f`  
		Last Modified: Wed, 16 Oct 2024 19:30:27 GMT  
		Size: 60.4 MB (60364528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e001fe3d905315367e2b67ef27c0b391460bddde7a5b3a79aa2a515ab0d3f67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b491d45363335093ce74a65480d62724eef68eedbb8c0967c844cb11b5e6a0d`

```dockerfile
```

-	Layers:
	-	`sha256:0f0ce3ab211300c4e84aefd6f1a2b6a206168f49bd303ad80e0cf466522386a7`  
		Last Modified: Wed, 16 Oct 2024 19:30:25 GMT  
		Size: 2.1 MB (2140160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffbc2b3852e8b9c4c60b26e258664dbe3b46772e4b64c6c19136e86e7062f7f`  
		Last Modified: Wed, 16 Oct 2024 19:30:24 GMT  
		Size: 10.5 KB (10503 bytes)  
		MIME: application/vnd.in-toto+json
