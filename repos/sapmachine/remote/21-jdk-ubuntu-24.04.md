## `sapmachine:21-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:0a5d62c21d225556a9d092ea5a75c9aee6b2522eac7a8dc7b303fab7e98722ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2042197f8f0fd4709ae7c8afcab0d960258329676e079aad5a6062695f143845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b054258782c6de57023deebe750b4404e90b6656143f0384165c74b6654056`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 02:33:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:33:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d69ca621c74574d68258bac36ae735a6f5fe77d3ff411a0e19de3e0c40e9ec`  
		Last Modified: Tue, 07 Apr 2026 02:33:32 GMT  
		Size: 216.5 MB (216495095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe31174d8b4814143f38c5298861ebcc05690b8de05cf7670cefa20631536f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acca36da19af8db1b0fe14552721c598204f04e5df3a197ac1e5f1ba78ad5b94`

```dockerfile
```

-	Layers:
	-	`sha256:aed0e28267756e236e2abfbf5afc8fa363ee1e6669d97e9268dab20754ec7003`  
		Last Modified: Tue, 07 Apr 2026 02:33:27 GMT  
		Size: 2.6 MB (2607217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e9e4d2340b137ee94b7e91854e67e6fb0a0728d690c973115ac70f7ee40fed`  
		Last Modified: Tue, 07 Apr 2026 02:33:27 GMT  
		Size: 12.7 KB (12679 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:883c31e9ff9a41161ebbac04b1b1c492fd9c909b34ba880ef555e51f78d8fea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243631524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fa47236e8325c44fd5fffaa09b57cc58010ead8d2d0b41999358edd3eb147e`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 02:39:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:39:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d2c8ba4a368da69159477c621e5cc46f9014f12dc6af819fda02f300f77600`  
		Last Modified: Tue, 07 Apr 2026 02:39:41 GMT  
		Size: 214.8 MB (214757449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6cc12dd3318cc3b85a6c391b88e615a64f708bf8bea02eb8adba2ad6b1316f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442885f1b7d2f9f945d1846589525a3acb1e554be9ad6ca37569d5c51efd9fa`

```dockerfile
```

-	Layers:
	-	`sha256:981d375a045ad765adad5a9bfc1942da8f5f357e1499e8ae74b0aa4702b7fe12`  
		Last Modified: Tue, 07 Apr 2026 02:39:36 GMT  
		Size: 2.6 MB (2607829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86176e4cd00d5a254c3037b85c64b254d3dcca236ac33df3cfc401b690c3bf53`  
		Last Modified: Tue, 07 Apr 2026 02:39:36 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3161ad792323f0397e737daedd3970b913844ce86953da121f206de4ccf3e6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251863006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2775e28bedafaa99d6e323bac3ffa5388c46420ff820d1b6d46b722b1cb7f392`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 09:06:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:06:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 09:06:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c69d8852230d2dfb6fed00c66e3798aa5e535669e39348fb04b7344ac66a09b`  
		Last Modified: Tue, 07 Apr 2026 09:06:56 GMT  
		Size: 217.5 MB (217549672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:785e496c36533bd8e39a95583524d99c28d79fbf36b554c20349a18b3ebd88e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513afb4d0834582361728b003310d809b4c658dc1804815379cc65b4ab0ef3bb`

```dockerfile
```

-	Layers:
	-	`sha256:e7e16887ae4b51072bb5c66d3151c5ce94ab973807a890b6284f7594387c536b`  
		Last Modified: Tue, 07 Apr 2026 09:06:51 GMT  
		Size: 2.6 MB (2604817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5fce3602744fbeef29ab7edbe88b5e3fdd13f329780c6b11478b60200261db`  
		Last Modified: Tue, 07 Apr 2026 09:06:50 GMT  
		Size: 12.8 KB (12795 bytes)  
		MIME: application/vnd.in-toto+json
