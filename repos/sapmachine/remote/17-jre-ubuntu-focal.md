## `sapmachine:17-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:39cb960f33620eac947f7e8a18de2377bec59b24f85f92fab8ea7ae01285c080
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:34363ebe6c83542ba90804e64edee66add1d4b418ea52e62df25f63c6390469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80770275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547ec9213d9663bbb2d19ae1c32a11824ea072596ca6da04ec06a02631640cce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6908e05148638bd2a7b9f4b0ebce6e587992491f09b90cd4339ed0eda5d291c4`  
		Last Modified: Fri, 19 Jul 2024 18:00:16 GMT  
		Size: 53.3 MB (53258506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2be33eefc839fb8b834990a5d33751d2274aaea0b2cad1756016c090ea7b7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39623cd5f36c1ac009241cf4047aa7a4574fd38d6545409a78494268c17fee42`

```dockerfile
```

-	Layers:
	-	`sha256:e8c1600ff4bb4e46a45953c0e913afec0dde38f66313bba4dfc063cd85916285`  
		Last Modified: Fri, 19 Jul 2024 18:00:15 GMT  
		Size: 2.3 MB (2279641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0605bb8d3bb9fa3d106ffe8862044bffe6e4452a1401d5ec4f6b8ff432ce29`  
		Last Modified: Fri, 19 Jul 2024 18:00:15 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

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

### `sapmachine:17-jre-ubuntu-focal` - linux; ppc64le

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

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

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
