## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:608338b49059299b38380713a98ef2e6cffe9e14e5903cb6157cb7692a01b660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8093e994d3f7787d0ea83eae3b9148372e049caef77a90957059f2c4f8666c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80770469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aee2c3f630c8b21f0a998f0936827a788c11cd3e8ebd618d79adf428f737d5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90900db2b721b8669971a7a528536f52aa48c231c3f7238e50bca9f68c2831b4`  
		Last Modified: Sat, 17 Aug 2024 02:06:08 GMT  
		Size: 53.3 MB (53258700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f42de3ab69976d1c379241683e32710e6bc2a30f219723abb16e0ff9f16d8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1d38e2705d75a1f1227485d0aefe963e7d7091a2c5e9cbb725340c56a8d7`

```dockerfile
```

-	Layers:
	-	`sha256:c746aabcaa9069e2a6c64dfa93926803eb2f4d604e74542b9d73b721d2c233c9`  
		Last Modified: Sat, 17 Aug 2024 02:06:07 GMT  
		Size: 2.3 MB (2279641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d6887f237e965ff919d93a2798692b493f42c709c04d0756d8c2ac7f6af6cd`  
		Last Modified: Sat, 17 Aug 2024 02:06:07 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:37f9f7977f3af62d586f8f9b291436b8aa4c1217258c1966717c935d781650a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78599101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab3e810b3e49eff7a41c0182cf6b666c756078f8fe777317565b3d6d8a063bd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caebb7b0a551e9ddf62f769440a88cdcc42f68bfe92a2a8d08de8435bbc177`  
		Last Modified: Sat, 17 Aug 2024 04:40:01 GMT  
		Size: 52.6 MB (52624884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e477361afb6e4a7d71a6bb986c098cd085aef13f018e03ae556a2594ee7db91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27c99ae7af6aad1a86f274e7f5ab3dddaa6ab9311951c414599da5dd25213d5`

```dockerfile
```

-	Layers:
	-	`sha256:1cc05b3cd6bb5c3bc47cbf803a12691d154165f099b2d15b56c25b3c81047ad0`  
		Last Modified: Sat, 17 Aug 2024 04:40:00 GMT  
		Size: 2.3 MB (2279277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc95bfdaf3b0717a063bb062d44cbaeddf6604d6f2144a5bcf48ad5482a47bd`  
		Last Modified: Sat, 17 Aug 2024 04:39:59 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:217cfb5892c8d21661fe007bbac4dfbc571feea65433b43640286143525d08f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86439270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6723f83ea326db05081cb533ee130f62f363d6a6928f0c14558476b8b00f9a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
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
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe4445cb6473a874f3db6297b402939bc3b8f79058210f92aa443a82a72a703`  
		Last Modified: Sat, 17 Aug 2024 03:24:42 GMT  
		Size: 54.4 MB (54362130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3528323e6457d2dab80ab9a92f82bb76b8b51ebf1646d35b69efd851666ff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9104db5fe879329c054c30cee387b8d121218d501bd553ac36f2050338053ae`

```dockerfile
```

-	Layers:
	-	`sha256:eed02fdf49236d494f375594303199ff86a51db684f4e56e2b465ae97d5cb1ec`  
		Last Modified: Sat, 17 Aug 2024 03:24:41 GMT  
		Size: 2.3 MB (2283406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6987cddc749f62082e6bdb8544ec3e7a77dbece8c51ce544eb7db1146df49148`  
		Last Modified: Sat, 17 Aug 2024 03:24:40 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
