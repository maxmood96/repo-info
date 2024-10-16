## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:4264596d0475b9838618eae2eac4d8feb290603e79e20d0fd7873765d3d3a8fd
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
$ docker pull sapmachine@sha256:496e387b5db0742c8550a4dcf0746c21d3e323007df0d2413869adec9dce27c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83881283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989cd1cbccefb3d6325e68fd62ae75aa98d59fda49f72bcfccf3a3614981bda5`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4936d16a35e6552f504324aab87717655638e688261173fee7d691f3659ff19`  
		Last Modified: Wed, 16 Oct 2024 18:59:37 GMT  
		Size: 54.1 MB (54130920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0300d695011e3edc0341f480d40803c824165d929aad7b708c3d14e225a80552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbfbbe2874faedcfe08b5dfbc21d3b7f25f35174e3b25c799ff3b1a25f665d1`

```dockerfile
```

-	Layers:
	-	`sha256:458ace5fc1bdb462a10daa1c6613211aa47f4207216e0b8bdd0ca9d884101e29`  
		Last Modified: Wed, 16 Oct 2024 18:59:36 GMT  
		Size: 2.4 MB (2370057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b25a34381e631854de81db529d276f07118a143e14b2405cb2fdfa714007bf`  
		Last Modified: Wed, 16 Oct 2024 18:59:37 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f1a9ce4939910ded5aa0c57d3fe8238b6da4876fbb953af351fa57023ea10477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82444511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2986de52fa123fd104d59bfb4aaaf5e5f5a41bce76ce4ed68b4316cf01e6df`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d5d5931a9166a645b430ab939989ea6f3960b45ef1dbd84720e89a5ab0ff2d`  
		Last Modified: Wed, 16 Oct 2024 19:30:20 GMT  
		Size: 53.6 MB (53558666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eac97d830c971aa4113bb191458d9ea3304382470ffa99ca99f4908b980e0d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de4a491aae6dbc426b035b9a78272209cea24ffcd78573058325cd9848d4cf7`

```dockerfile
```

-	Layers:
	-	`sha256:a39ca9f169d5689b9e887f73ea5166ca955e263bc60d2674b9be975bd4fbc4c6`  
		Last Modified: Wed, 16 Oct 2024 19:30:19 GMT  
		Size: 2.4 MB (2370548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2f48975421b1ab075abd239991518b3859f3a25b147341a5a5ce26297a6d1f`  
		Last Modified: Wed, 16 Oct 2024 19:30:19 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3e70b79ad20fa948bcab4360367176d19b50efc6a2ff6a7fe4f2c11328589b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90097187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a71b065eb3ea0debff18a925e57a67ab7f9dfbc59d8a95f59384a6db356e9b`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e162af10dbf0e0fe992a6f68dd0f8e36b65cb64d7b155fa9517a721ac3284bf0`  
		Last Modified: Wed, 16 Oct 2024 03:00:13 GMT  
		Size: 55.7 MB (55708218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f294732b7e1d82e54a93e8b4ef670395265eccfbc438b520bdc41eb808c926ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0456549140fa3ece047d69d417f33c56e0a8cafe90aa3559e2df21bddd2e2`

```dockerfile
```

-	Layers:
	-	`sha256:6c677893ebb8df5c42180e06a9d31e64ba6c03f8172b7fa3f76ad269f4e2a78d`  
		Last Modified: Wed, 16 Oct 2024 03:00:12 GMT  
		Size: 2.4 MB (2367360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f84301c5ed8e5a1195d83743e671a6bbefd02bc463afd9f43b00eebc550f37`  
		Last Modified: Wed, 16 Oct 2024 03:00:11 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
