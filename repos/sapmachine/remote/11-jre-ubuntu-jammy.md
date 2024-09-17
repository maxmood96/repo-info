## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:908a95f98501b63e0ad9426326c6c8544c79dfac87bd6daf83ec354076679f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b62ad2ae998db6fe5a833673d16974c28027646d2802f7bc65edf5f5004d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79492603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781a6f70beac34662c0e1826367c1411843f6e6448f98870dcd6a660dc3eacb3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99014950e9e112700b6519cac77e8e06c643df25677f347695025700c2e1373`  
		Last Modified: Tue, 17 Sep 2024 01:00:50 GMT  
		Size: 50.0 MB (49956915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:67801027e6a9f915f22af1590cb5560ec83ade1c6ccb0f3eaeb305510700c1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8291390bc338e63fd3cfea1d74dc476ba1f94186b299c61d7eb3fd1f6cd7430a`

```dockerfile
```

-	Layers:
	-	`sha256:88bf778b7d89b59273a64c965dffea7e092cc419332112748dc07e9770ad7f5c`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 2.4 MB (2398928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24c640a37b5f88529dd5994d5de87464739584590e24e0b673f2fa9cc8b448f`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e9ba95101b483763e7cd349f7234b37691e154a1fa8da9ac9b511b67463f0265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76597764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc9797324729fa28ad8385caa368c2d6066edf13abf4740f60ca14d5928e51a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfcb7ba2ec6480cc08cc935055145cf8f635efa3d0dfa7b1a2e4681ea8e83ec`  
		Last Modified: Tue, 17 Sep 2024 03:41:44 GMT  
		Size: 49.2 MB (49239435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ef5d17fdc2bafe6df8b833a09cafa2cd760ff7caf7a92d29ca730b66727c5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397bc6c87992518552d49119ce9de0148ffe6cc97c5c9eda01dc19e7d8cc7b11`

```dockerfile
```

-	Layers:
	-	`sha256:e0b4c16a42813299e60e5034b26970449f5ecd78f363a84b94783249bcbac029`  
		Last Modified: Tue, 17 Sep 2024 03:41:42 GMT  
		Size: 2.4 MB (2399236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35da2944ef68cb9f775c7aa584583bb2032b4e1e098b84de6d8e00aae4448c2`  
		Last Modified: Tue, 17 Sep 2024 03:41:42 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:70bc943e2868b3fae1d1c43edfe3fbd2a885bcabd0144769a8397807546a8901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83033305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d920bccccf848b9e2ffb5254c24c17daf188734e2e6c97de0b5e92774f9d4a72`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b38ef83ff7da4869c13edafa6bdd2be183e48257844cb8fb6879b99c304864`  
		Last Modified: Tue, 17 Sep 2024 03:09:16 GMT  
		Size: 48.6 MB (48585063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f29125bfd0250c07948748d3ec3289202a2b8ceb84e403e83ff986a1a429d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfedf81bc4feff26bed8cbbbc04b55bceb6c1e2f04808848c27c40e017ad92c`

```dockerfile
```

-	Layers:
	-	`sha256:8ab5e95af71ea6ced882667ec243d2c25643a9e2394a080cf6c38059060aa08d`  
		Last Modified: Tue, 17 Sep 2024 03:09:14 GMT  
		Size: 2.4 MB (2402913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9936f09e4567ced2cfa89e2361fe62b55e05c25efc3caf0079e24579ba1b5cc0`  
		Last Modified: Tue, 17 Sep 2024 03:09:14 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
