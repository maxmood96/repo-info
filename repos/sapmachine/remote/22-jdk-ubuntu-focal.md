## `sapmachine:22-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:261ef63cd5d11482276b5fdefdd604948eae502b70ed55b85787d65043cb035e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:fd458fc046a898650d07c265dd77efed4741ad169c8a5fc0c3729fb230180771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240285867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75c30d7538648c4bb1f288a21ee0814b0c03a23c5c73e386a874db7b36dfb23`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd43881ef17d31b4a2e07937fdd914975edddf3a0aba044740e09445b25905`  
		Last Modified: Fri, 19 Jul 2024 17:59:38 GMT  
		Size: 212.8 MB (212774098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e15fd1545c58b632390342fa658714cd053911cb5998e108385374c77b88cd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba628c59e0142f70c40681021b2965dd7abe714a0b3f78ae619e8d357cd8dea`

```dockerfile
```

-	Layers:
	-	`sha256:559b56df0086ebb2da77702b44c2c8d52b15da4013460010c3f6e68d8e718c44`  
		Last Modified: Fri, 19 Jul 2024 17:59:33 GMT  
		Size: 2.4 MB (2368408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4c167e09f29076e67fef7421dd7706a8e5e315f6b1d94c2f7bc76f36589374`  
		Last Modified: Fri, 19 Jul 2024 17:59:33 GMT  
		Size: 11.2 KB (11158 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:63db669b3f04e28e4a56b4b4ce50f13d823061ddb8faf5f22286bd611c0c0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236729817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9f3421efeac94ea825cb495c4c4794d9a58a10090ddf6d69b29085ad4af33d`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbdb22a36d3d2140f9b878c1bcdc692c5eeec574947f0918fcba408a5e604`  
		Last Modified: Sat, 20 Jul 2024 00:05:03 GMT  
		Size: 210.8 MB (210755600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd6ca420f0c86e4785506d6ea7002bec79f0d65b832f077ccb21c7493779418c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea389269f1b876a76f4a4b772b879ec86011ddd03ef3be42106f782953062646`

```dockerfile
```

-	Layers:
	-	`sha256:aae8844c594107f82b0e89dea92c0556b5e0507d1d77b83ab6fd5aee65cb3d59`  
		Last Modified: Sat, 20 Jul 2024 00:04:58 GMT  
		Size: 2.4 MB (2367509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a502ced4ab47ab15d9a13789d1be3c6e4fb7100bc1148467bf5c6029370ec8`  
		Last Modified: Sat, 20 Jul 2024 00:04:57 GMT  
		Size: 11.6 KB (11555 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:af993506254b6d63a195672a88e9219ef6533bed3ebd332c1f35d5a174d8a125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245556390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9601a35914a9e0c7bd441b05c6c49c6b3afc229c2e06edc5f97ae60ec82295ac`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3870ff48be2df8cb82622d0a3247542c157bfc123fc9603cd886cd70feb7c2b5`  
		Last Modified: Fri, 19 Jul 2024 23:04:37 GMT  
		Size: 213.5 MB (213479250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f9242505a46d73351fb75f42990763a1007d81a8fa0a81a566f476a284059ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04477f25304665476b81f2a824b97a5164ae98bf886036e3238bef25459ec125`

```dockerfile
```

-	Layers:
	-	`sha256:a9a21abaad01d4cd0416cca4574bb3e3057caa02e7cae8eb22331d9a95e8cdb8`  
		Last Modified: Fri, 19 Jul 2024 23:04:29 GMT  
		Size: 2.4 MB (2369653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:740927e232d8d45679039183f8546a3ee92a614b600ac142ff947fa5d287de57`  
		Last Modified: Fri, 19 Jul 2024 23:04:29 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json
