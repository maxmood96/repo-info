## `sapmachine:17-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:85e8ba702436caf7600967919729a01a1c789e1296f2618e24d146ad17f9b8a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:346da42a84a7f5a25dc14cc04184b35a7fe9bc7787dba9e33b3575ab4e5c20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230134900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50824a861e99603269fdc973d57db5c9885124630c444537acc84e3c712125ce`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1c027fc52595e534c43532679a8ea4fc3b94b2e251ca581dd0e3e82c3ffd8003`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 200.4 MB (200429747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bdb69bde54aecbca4b3d670a09e2777426a097db876bbd646b1ad9df2a974c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e8da48f9e1a33f504fe1c077424b91211791915f87873f309231ddf1ff5534`

```dockerfile
```

-	Layers:
	-	`sha256:bf594421dcdbbdf056317c3601df6f283de18da9bd699a03be425546e757a94d`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 2.4 MB (2445162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44a9102536371cd38a129f65aa2af01480e40faa3f842cd5b4177696c485136`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 11.1 KB (11140 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:efc48ad4e0d0c946b371dc14b3b2bee12a5a72e090d5e787e7e284b6fafc40cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227924373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7d28b0ba70afbb42e6d1867a7ccc78208ec01fb0e323c395fc0baf15a7bb77`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b3361a8b683ca2299f7577d4d069386cb4d8757f9ec66a8a17e38205c4a46a18`  
		Last Modified: Sat, 17 Aug 2024 04:29:37 GMT  
		Size: 199.1 MB (199080687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2eb1178f0c2ece386ca972cf180be1abceab14cfc01b9af68ffccd279fa5711e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cf1f84355bf074eb3846d4e8f893763abb8e5e144fd099f60ab579467c091f`

```dockerfile
```

-	Layers:
	-	`sha256:4183b1037d701ad9480d40f7215db6d95dacd67d3c7ea7532839fb78098ccdca`  
		Last Modified: Sat, 17 Aug 2024 04:29:32 GMT  
		Size: 2.4 MB (2445725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf59125c8d29a58c337c8b2d719884a5fc054e7bfe04dedfab23caba796a6a53`  
		Last Modified: Sat, 17 Aug 2024 04:29:32 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4d0e2c76cd48f3347dd40cd79f91821899b1ebf93d3b1a98c3ef015773051a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236148612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba4a965013d98c9e0165d67c8039b0a0320d8f767c1eafb419c09da6130b10a`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1b36f9005db89985ef1ded70a9d6de114ef3819f631618bf1ba9430d45be9bed`  
		Last Modified: Sat, 17 Aug 2024 03:08:41 GMT  
		Size: 201.6 MB (201641040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc04f7e070e0716f5371b82ba20ae09eba59988fee76799ca815bec3dccc9f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11563e022e4c2390fceea8879c19fb49e81acf6bdde299476910c2b6dd1ffb99`

```dockerfile
```

-	Layers:
	-	`sha256:8c47c7eebb69ff97a756224631f15c19a4e344fe7f3f3a0fbc76f5be6fbf53bc`  
		Last Modified: Sat, 17 Aug 2024 03:08:36 GMT  
		Size: 2.4 MB (2447198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83a776b2dbfde25ed47236e4dac7f5019b2301dfdf0009ede3f9da3c56879b9`  
		Last Modified: Sat, 17 Aug 2024 03:08:35 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json
