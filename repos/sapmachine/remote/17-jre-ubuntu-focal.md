## `sapmachine:17-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:6b8c4fc74a5358887a249b4ef07349abf3cb31d846585755d5e71e60db3e4b8b
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
$ docker pull sapmachine@sha256:01a6b1d45eca73b3bcc00157da9732e1b766c8d82c37336cdc4fa47ceb48071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78598992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7d19920e0bb7120cdddf717f1eb650ea9d45c12e64eb5c69d15e464b4e5e2b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
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
	-	`sha256:bbade618f2580f31c95af58f64fcae655654ccebbe8f26f60b7bf72413d8f33f`  
		Last Modified: Sat, 20 Jul 2024 00:32:39 GMT  
		Size: 52.6 MB (52624775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa44c947957d83e6b9e546f3902a27cf3a42947c3753ac51de9a6a43d480b35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858b7943290f3ce770b4855ea605e22415bff93f1b4542ad75ecae6ce6d9ca87`

```dockerfile
```

-	Layers:
	-	`sha256:4f8c1e34efe8fbaa44564b45d1cc5e15fab9b4e8fb000f89801494e6dc66c0db`  
		Last Modified: Sat, 20 Jul 2024 00:32:37 GMT  
		Size: 2.3 MB (2279277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcaab90b9d459a3d0eede41331d22bcb85749fa728ca422b0a686db68c7de18`  
		Last Modified: Sat, 20 Jul 2024 00:32:37 GMT  
		Size: 8.9 KB (8866 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c9df68428f23c6835eb16244478272ec723594837cc164acef7905795b793e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86439159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e7706f02563f3a6674ee05e3cdc6a379694fc6168225e22640e5c3f5e02434`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
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
	-	`sha256:8a3a50154415de4c5ad98f9c22ab6f9ea44f9956015f985f2c0f9f9dc67b9555`  
		Last Modified: Fri, 19 Jul 2024 23:47:34 GMT  
		Size: 54.4 MB (54362019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5fec79abc4aefae259eb1631fa0156f7889dc0cb48005540be9583329524480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c7da11953cc8c01df8bcdf1169b94e4f3dcdcdee303896febe95f2e725d4e3`

```dockerfile
```

-	Layers:
	-	`sha256:2e3524d502b854333a7bef618d9344303d5dd532415a84c7ccdea0c92c66d507`  
		Last Modified: Fri, 19 Jul 2024 23:47:32 GMT  
		Size: 2.3 MB (2283406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3518bfa721f0d82ec083439773454e4fe9146207b6cba0e49365b1adcecd63f3`  
		Last Modified: Fri, 19 Jul 2024 23:47:31 GMT  
		Size: 8.6 KB (8604 bytes)  
		MIME: application/vnd.in-toto+json
