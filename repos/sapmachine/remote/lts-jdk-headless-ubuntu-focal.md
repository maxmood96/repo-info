## `sapmachine:lts-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:5b5c695a227e25dc30258cff4a633380c8ba1cd82a6997f50635623c1b659f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba0d8bdf4630860da748e74b79d546ec5ad5762ffb3442b08c1c42f3e50b149a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241067571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b10e64223afa36ce063573c64d7dedc112d6642471fc0ab55e5066407d10567`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0dfc0b30c96fdce32abd1fcb78d6278d7decfcaf45cc7cde7a057f2da83d42`  
		Last Modified: Wed, 02 Oct 2024 02:00:13 GMT  
		Size: 213.6 MB (213556519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:427794d14cf9ac35e32afb3a5f34ab1bf684f80b01682b9f236572b4ea62a27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0abd9cc7ca2b3f74f65fde29bb2116e263142c21010a253d23d6620875c804`

```dockerfile
```

-	Layers:
	-	`sha256:2090c504a041ebaf7a5d16d1b7a00a56e82bc93c798d13d79a284c3331723ae9`  
		Last Modified: Wed, 02 Oct 2024 02:00:12 GMT  
		Size: 2.1 MB (2128619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc0cd6418b165e32311a6f0b70512578c52691e903f399d351027a2abacc51e`  
		Last Modified: Wed, 02 Oct 2024 02:00:12 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e1c509af573d6bf6c100b5639173b504810e05fff44e1ab6d45ee47dc189f329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237623920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636b7933f0e3f22402764b7ea61c2c307a5b9396cae5209ca973d6a93e925b5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1773f9ef49efc81e2132e7d34337fedcbccb10429555566b46ffa189a26cd13`  
		Last Modified: Wed, 02 Oct 2024 03:54:44 GMT  
		Size: 211.7 MB (211650328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41e7e6cb06b17def1b698f85263e4bde07124c63f99b64ed2f70f4025bb044f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5538016c98f84f26b0b43b56e065b3c4181fa629a1aaeee408ab1b58e76d120`

```dockerfile
```

-	Layers:
	-	`sha256:6d74e6f845f6686f88134854a7472cceea506797f0de497008c9642033b9b8ee`  
		Last Modified: Wed, 02 Oct 2024 03:54:40 GMT  
		Size: 2.1 MB (2128270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83587191e78a18646773f9be28ebcfbda72d3b46c057e5b852b9ca1f02a7c7f2`  
		Last Modified: Wed, 02 Oct 2024 03:54:39 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:33173ff9b5d95b515046e6ff27b3604358cde7fc22ed53e0678e33c5b285aa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246416394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299350e086faf468003f906f874854d4189380c20fa1becf14b80f9894eacc0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a4fb115104e499fae4056a3b1c0ac3af79cd9c3dc4c916515bb68873676c40`  
		Last Modified: Wed, 02 Oct 2024 03:06:05 GMT  
		Size: 214.3 MB (214340060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8dcbcb2881a88015c606fe58de6d7a2968b0e4865f9bdd9a431fa7995eaf5b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34eb7c8d9876536c302b52a3e4ad6cf358ee0d67696ef6c95dd7b7ceb630e699`

```dockerfile
```

-	Layers:
	-	`sha256:99aa306de821d63bc7df14f75f80930701f46f7a28adc08251517da989000a5a`  
		Last Modified: Wed, 02 Oct 2024 03:05:58 GMT  
		Size: 2.1 MB (2130384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df57fe7b5add0790b5861595fde71cc8e1850568bc3d23b0af72ecbfd42e83cc`  
		Last Modified: Wed, 02 Oct 2024 03:05:58 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json
