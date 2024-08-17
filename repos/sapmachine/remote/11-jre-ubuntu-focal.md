## `sapmachine:11-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:7b99d4afe0b5404dc208a10ba1b45c522d6e5b4d30282fafa9137447d5e95685
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:31126f5c4d2e37fed296043c8898c8b13ba94bfd9ceedab3e67a44ee3ed21959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77014232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5970b832aa63e9bb52e0aa33efbe465f510ec4b713539bdcb4b4c49b9a7df3`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e0788f6734bb1772649ceb85bd2e6fab783c543d934bb0aca423b01221b558`  
		Last Modified: Fri, 19 Jul 2024 18:00:14 GMT  
		Size: 49.5 MB (49502463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6635f95bf7ef7ebd1941466a092f828e8a0a0b9d9108624f93784bd21c4e60e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1633a74d6f08815251a8ba026881dd065f21e7300da0cc4efa061d89eb678a`

```dockerfile
```

-	Layers:
	-	`sha256:a7bda87546ed36d3e818285386baffe3ac72f291bb25e840e8d6e1c8d32901b2`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 2.3 MB (2291707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7503707c910303944adf6a4014e0ec3f78326567997665d25121053cb76f22f`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:58fe729744b453320f561b6021a3c47cc8b9d840695bcdb5158998a02e00a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74790774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9e885071c2e8dcd3df8f141181dc2d080944679de7a399639e62bbde91aa82`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd543ac38b3edd5c70bcbb85ef8d3f227288901f2c5380789c7c7355c2a3220`  
		Last Modified: Sat, 17 Aug 2024 04:51:26 GMT  
		Size: 48.8 MB (48816557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ad08a7a2c92f95b673984ef9c2a5ca891fefa983064ce585ce07de171cd82f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c22e42f9bc888a5cd025a59a3374883d91a211aeb0f89d8f1a51c8223454d2a`

```dockerfile
```

-	Layers:
	-	`sha256:9627f6ce69462bc6fe9a07f9ce06d2cbe1784c4353b3902de42d204bdf42370a`  
		Last Modified: Sat, 17 Aug 2024 04:51:24 GMT  
		Size: 2.3 MB (2291971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8219f8b4cdf509821f94f02f9a16747b8a61132dae66dcd338f76e884b16f5e4`  
		Last Modified: Sat, 17 Aug 2024 04:51:23 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:554f6203be05e4d0e95401ca7396166fcf4eb0cbe3a9442e071e31eb8840ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79822820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdb6bebaa2be4bd13f4211e03f756bd39bbd2abe7c81d800d19a43d1da080fb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9cb4b4c481f10c1b10554c3f74f678dbfe7a689d46e43845e732309249151b`  
		Last Modified: Sat, 17 Aug 2024 03:43:37 GMT  
		Size: 47.7 MB (47745680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3aff9a1be5c578501c036e4c362d022102cafcd55c132fb906cb39d4fe3b574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c0ce1b5743a329704d73fb6f02a62e76344b637152c801b3ddac9eedf58007`

```dockerfile
```

-	Layers:
	-	`sha256:98ea205e5f148ef01a6c4d943b04ff76c096fd3f55bede42160109d667053593`  
		Last Modified: Sat, 17 Aug 2024 03:43:36 GMT  
		Size: 2.3 MB (2295478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bbb1eb1f26df163bfc7525fe04c1ea5c67982c56826a2866afa141adbe6f4b`  
		Last Modified: Sat, 17 Aug 2024 03:43:35 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
