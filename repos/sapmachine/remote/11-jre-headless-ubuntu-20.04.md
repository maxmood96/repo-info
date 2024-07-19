## `sapmachine:11-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:aa627322510bf19365de68a4e8c8a111e1908aa0fd869ffb084872e65c869b5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:da5a156c6f6304d53460295f9a2cddc99962b1b380a4d6c4ecbd4978f5825e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75802649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2407d98072cadad81d9a5d4758297481501cfb9beef390204e05bc2c6e4e0cf`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7e1c7a4eebd6b56d557804f667efc6e3aabc15c5368000684997f40f5f032ade`  
		Last Modified: Fri, 19 Jul 2024 18:00:20 GMT  
		Size: 48.3 MB (48290880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bd38877be9fc6db42c0e2105c90ed51f6304aac1cf66f878fd52ba087f61cd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8643fd24aa8f1204b3aa98b00fada1463e450bd3e3acbab6c2325c0c089bfe6`

```dockerfile
```

-	Layers:
	-	`sha256:942eeeec2cc32fa1fe1659d93cbc5c76a9e16b861a645ca5a07b6d98137e5138`  
		Last Modified: Fri, 19 Jul 2024 18:00:20 GMT  
		Size: 2.1 MB (2054420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b075664ad4c76865ab6d576320038aad5ed69ff01426789767313f9ad2fe7c`  
		Last Modified: Fri, 19 Jul 2024 18:00:20 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:734f29b1623bedbcde697d639cf67457f50f55f0c12fa4ebb3052e5058d50ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73583240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b5e8738ac047561007b790b6377849697295eae855f035b7d432e1cce11ac3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de49f0c108faaaadf85bf1d1e6929c6e5987242a657fc638cb2fe7b0f50bc3`  
		Last Modified: Wed, 26 Jun 2024 00:38:39 GMT  
		Size: 47.6 MB (47609023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ad2f6ee9f0ed6f51f5e869068c2dacbeaf7a8f15df9f8861c465d5349d0023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2041355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b34e0c6c9c74173031fd587b011f45576dd2630e595586134817a8cdb76a381`

```dockerfile
```

-	Layers:
	-	`sha256:b96732f6bc349f76c2ba8ea962fef52c39cc5427290fbecbc1691e4340cf1508`  
		Last Modified: Wed, 26 Jun 2024 00:38:37 GMT  
		Size: 2.0 MB (2032358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191744083c15b82ba46ddb37d66c8cabf9679e3b2fbd1e1ef9fd5fe697d7b4e0`  
		Last Modified: Wed, 26 Jun 2024 00:38:37 GMT  
		Size: 9.0 KB (8997 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e652752f1ce2f94fe1eadf7fb4ff1d07df9e6ce2ef0dc88db6f95329971be516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78444630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81ac3f7d1f1c1120d96efb91dcd15e16a759a495922c035486dd074a3a70f21`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5206121e513de67fbdd75e79e5df8210965dd8cb205296befaad465f829a27b`  
		Last Modified: Wed, 26 Jun 2024 01:25:42 GMT  
		Size: 46.4 MB (46367490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7c8bc2deb3a5e9f0fa5ac211a38ea59efad949cfb7e449a069a531b4c5433e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2044545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7bb311e5d4f22d718144b9d96f54543bd24524ff8241db5781df4d50c9bf0f`

```dockerfile
```

-	Layers:
	-	`sha256:d2e385846bdae8d7fb9c10e5c33ccb1a5e8b0f02fc9754e660da029c5c7e80e3`  
		Last Modified: Wed, 26 Jun 2024 01:25:40 GMT  
		Size: 2.0 MB (2035811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fc5daad050f288a5e41d5d7ef081f9d02bcbc85b8397d06c773893283596d8`  
		Last Modified: Wed, 26 Jun 2024 01:25:40 GMT  
		Size: 8.7 KB (8734 bytes)  
		MIME: application/vnd.in-toto+json
