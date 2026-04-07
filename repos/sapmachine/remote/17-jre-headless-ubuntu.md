## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:1d6eb5e005dadb4831fb6fb9352bb1d9561eb8ea3309f0d09df43d46a49cc293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:45fe8810e3a3329d69dbc0a4263f761ffe6fda1362daabf7cf3fe5aa610f0d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83321646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06043ace7ab59b3d4e743525cbd71846b987041c86ae21d0e7104515fb74ff94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:33:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:33:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f251e8a902ee6c03f600dc93388ac856678961fbf10a83b06433b936e8a5fda8`  
		Last Modified: Tue, 07 Apr 2026 02:33:46 GMT  
		Size: 53.6 MB (53588187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7983ec56c2861a0dcdd9cd2ddec362e1a05d8dff6b63ab8d87592624bc46aa79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7b023b742492e0a0e67d9eeb791869288a2295406784f578ebf6b7de777770`

```dockerfile
```

-	Layers:
	-	`sha256:a9c88a83963e7c4012b232e77c937d0ab0c30265f989a6719fed3e67e7c11d26`  
		Last Modified: Tue, 07 Apr 2026 02:33:45 GMT  
		Size: 2.3 MB (2273980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc777ba811b1587c56bb6f3a4daec92437deec0f3c22ec95c53c886824dc507c`  
		Last Modified: Tue, 07 Apr 2026 02:33:45 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:be690f63f3f947009cb0be08e66dfad0003fc952cae255649e73345f10c8c198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81883310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5432a5504d9fae7ca25aeb2da44daa8bffc026fd6c7883de195e1ca01a842f64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:39:58 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:39:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9118555b82875de62abfa4476aec9a8abb5f7e7e08e93b59d3b8511b1e9d05`  
		Last Modified: Tue, 07 Apr 2026 02:40:11 GMT  
		Size: 53.0 MB (53009235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c97550afeca08f90a17d7ad6fc7b0dde9514e2fb5ce2722aec3bd265183c0e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2284868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894a9f99f6fd85e1f412f386e9d28e8518d37ab497048fa4ba52f73d3af47d98`

```dockerfile
```

-	Layers:
	-	`sha256:3681038d60b067ca6fee97f2782bd3b3028dd30581176244cfdac8d3320862b9`  
		Last Modified: Tue, 07 Apr 2026 02:40:09 GMT  
		Size: 2.3 MB (2274487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a557f8837b53f534c950232cf4ddc564fb7d8f9739a2d77e2bce4319d64ff495`  
		Last Modified: Tue, 07 Apr 2026 02:40:09 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e7b3a39fb5d5fe0d3b492c72ab08293a8f8d8af4cf54565934dbb2079113990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88977034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b9ba02edeb0da62123adc22cfffb5db430281925751408a66011fde5f0ec0d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:13:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:13:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 09:13:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cbbe35154c2c8bc5669b266a41d3058832fe205529f0dc74669b3c3c43ca69`  
		Last Modified: Tue, 07 Apr 2026 09:13:40 GMT  
		Size: 54.7 MB (54663700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:77327db81a7870099af8b1815e5833e97dbd604b7170352993608b0280b8291e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e981567207318ad60ae746fb5b0515431e2214eccb9f437dba4a8542248deaf`

```dockerfile
```

-	Layers:
	-	`sha256:b375583842e79dc1645588c1b104e8b8f90945fdc5d29b98afb5a5cba4b80b53`  
		Last Modified: Tue, 07 Apr 2026 09:13:38 GMT  
		Size: 2.3 MB (2273397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a498d728b0393f9994c2b3c9ce1521ca3e90f151115aa6589ad686cf01efa01a`  
		Last Modified: Tue, 07 Apr 2026 09:13:38 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.in-toto+json
