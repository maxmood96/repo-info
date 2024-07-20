## `sapmachine:11-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:52b009e058028761ce6beb3bf29e9f2c44aaea2e1b09695a3b079ada752562ad
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
$ docker pull sapmachine@sha256:9afa91db0c624c8eb25aa8a38121c44148adccb348c2037fd4c75358675749bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74790713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e740cb3484f365b2abc632c5bf51c16b5415919abe97ce73c15413e2536a1a`
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
	-	`sha256:52cbfc8899bdc69f5371d80f642d9f8cb916a1d9ac27e37cc7f54b8a419db5a2`  
		Last Modified: Sat, 20 Jul 2024 00:43:49 GMT  
		Size: 48.8 MB (48816496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a08011e5273c28ab34892767fadf2c979dede487858dd2f5b71977e94ac9372d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9aca8d74540976e3f83a59bc959faf2b186439fc1b6f262aec008d1a23d1c2`

```dockerfile
```

-	Layers:
	-	`sha256:c70ed5ffe116bbc82edd4de62bddce8c3438799acb0a05f578f703a43f46b8fe`  
		Last Modified: Sat, 20 Jul 2024 00:43:46 GMT  
		Size: 2.3 MB (2291971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8718aee05119a27ab8b8331e3c2a8342503c2b01b6366a383b54acf5eb2bbd41`  
		Last Modified: Sat, 20 Jul 2024 00:43:46 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fc8ad624053ad366c112bb18265a8f1e17144420228640833180a10ba7207258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79822587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f457674a1cea17e3a72fcd07323abb380ac08bb691b93488c46648646c9645db`
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
	-	`sha256:3f4d4d21e39c14868592c12d205088871dfe301faaa41d90ecd3cc48f525e68b`  
		Last Modified: Sat, 20 Jul 2024 00:07:55 GMT  
		Size: 47.7 MB (47745447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:20ebe043a864b72a0da0c6df5f90c9f8e03b08e2878441dff994bd20bfc12042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cd80984022aa97584a531f2aa8186ddd490783609c343ffd7947019ee74438`

```dockerfile
```

-	Layers:
	-	`sha256:859a5c948dbbc75640073051b95975c5a3847cc7486b11526bc1b91621b1d66b`  
		Last Modified: Sat, 20 Jul 2024 00:07:54 GMT  
		Size: 2.3 MB (2295478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68341c580bf64d468762f3ce134f3827decf71441a19748fb6f0733d891f78e5`  
		Last Modified: Sat, 20 Jul 2024 00:07:53 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
