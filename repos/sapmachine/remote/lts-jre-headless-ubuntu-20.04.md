## `sapmachine:lts-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:30a632824ce8b945bc37f3cdd421a0d4e0905b917fefb56617c68a4007718e04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:be6e6c47517e3464c11c2c12017ba4c7fb1336897c6fe0109eef0a26e5796a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85514141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c175c0cd0c708a1785f8581d948b9a6e5ee0fb8cdecae80557dc05fedf1f308`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb491b311d0a20a140d54dd7241eecf968e79bd9233776ba879111aa81f47370`  
		Size: 58.0 MB (58003081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e69ddfce66cce407cab45f78170bc8d6bfc75726b60b334b83645e942b21565f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2060380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca0f51484f3d67368025a30010a3f865ba239b105679e7c0822d9513fb20459`

```dockerfile
```

-	Layers:
	-	`sha256:003928332a4fcdef34bd9b40f3b8b503be686a586ad9fde33f42083ebfa68362`  
		Last Modified: Wed, 16 Oct 2024 18:59:49 GMT  
		Size: 2.1 MB (2050969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85bd0b76f722be531f32d7a5b12fa813fd0b49ac0bf87452b77c9c7c0735bd5`  
		Last Modified: Wed, 16 Oct 2024 18:59:49 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:94d03a51e1b3a5a532da5ac2dfd01c923c1194ac92a6e0838976f88e495102d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83121084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742163228890caef34fca94cfddc370757e6a3ca1da4704b87c88d4509ac9981`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb6fdd9735721f2d701461a52783413daabe7f7e297c4b4b3d0513d1b0130f3`  
		Size: 57.1 MB (57147256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:21dda6c92d4e33a27259988eb1a4f8f15c061400bd23527d1dbdf1b86446fefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2060153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9721e072a85d3e873a086904859ea1e99a29a38071313ebb876982cc6795396`

```dockerfile
```

-	Layers:
	-	`sha256:f2df453ad1bf2d034b345120f609bde0fef4a9ada7ca78714fe08a26df63915b`  
		Last Modified: Wed, 16 Oct 2024 19:26:52 GMT  
		Size: 2.1 MB (2050620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ae5470369c16342acabdeb0c8f8812595f47824b6b743244bc1bb260c905a8`  
		Last Modified: Wed, 16 Oct 2024 19:26:52 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4cba414b6cc8420b775c042c0c50c4a8fd7d7cb4486068c8878b3cf12caa216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91116734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39499ba9d93ee5db4ae4525441e0868d9710d887ec46b03f0c0d87aceda9e68c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350cf81d8a8bca679cd7239a9c7f3b3b6dde24939974420df3baa5727e962ac`  
		Size: 59.0 MB (59040228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a0e7950a6c5c379a61d27f7024abc0d1195a896c5a0fa25174e6e850ce05b6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323cb55455ccf8be78ffaf1120289d63a52da221781f649a04ee62c7bcc98503`

```dockerfile
```

-	Layers:
	-	`sha256:6031af41160feccd7ea202efea3bb92e10bd599c8905fd3f348e99928b303465`  
		Last Modified: Wed, 16 Oct 2024 19:47:16 GMT  
		Size: 2.1 MB (2054683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a9f0f496798c88c0df70a234ddf4de1ed08013cf9eec62ea4a0a1b6ba3090f`  
		Last Modified: Wed, 16 Oct 2024 19:47:15 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
