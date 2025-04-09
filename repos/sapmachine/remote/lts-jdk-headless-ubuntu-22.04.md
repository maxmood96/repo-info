## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b12cd448c45233f035efe389424534aa103c94e03fb754b34d365bbe4958db24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b1b1debac4b4e84b59e785253b042a59d5ce15fcce123bc2de0fc05e24d3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242960052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b846504dfdae5b60405b7665f1841e2c35af54407eec912b07682b27eba6453`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b972a199c0500898205bfd93286465163d30469272647a25c3017999350f12fa`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 213.4 MB (213427687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c559e21ccadbe47c46bc7390b3080eade12f05530818a31b84c3d430f8981f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2260079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6cbcf942ba7a6d4f2dc4d2f31c39bc8f7e749d067c5cfa005a646b3a6ddc8c`

```dockerfile
```

-	Layers:
	-	`sha256:98834cc9d5b9c52fca959dc1da44a3bfa329a2f5704140789f5f9142c2cf999f`  
		Last Modified: Wed, 09 Apr 2025 01:20:55 GMT  
		Size: 2.3 MB (2250451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54b631ea00db0986634031612c54099230ce0c3a7409925244bb964f39a8f4d`  
		Last Modified: Wed, 09 Apr 2025 01:20:55 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:380773965ef3ef73415482b336bb0631c3b38979ef47999400794fac31388a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238983243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319d6500426b031dc026e271674dcd77d37c3a23ecd2fe4ff478d74a33657ad5`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ad445f4bb4ed84bca632ff9ee80f92e691591080876b63bdd05d3595889d2`  
		Last Modified: Tue, 04 Feb 2025 15:31:00 GMT  
		Size: 211.6 MB (211625061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7cb696c6b59a8ae0a51cdfe66e1d897053e2a7a9eb65da2523b4a6c7cc3b60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b716a653a3bce5eea029bf57b97f869b8ba3c73d6ae394a5e32f1a7063f2b5d`

```dockerfile
```

-	Layers:
	-	`sha256:ed89ff1c0cc024aae6b8f0bd97b89bde1e8dfd7714424ac048a786263d38e104`  
		Last Modified: Tue, 04 Feb 2025 15:30:55 GMT  
		Size: 2.3 MB (2250059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b485d28a4d8cea6de9bbe4e88e5bdbe7ab055060159764de4643db8239ff2cff`  
		Last Modified: Tue, 04 Feb 2025 15:30:55 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e7744b4e275cace511d4146aa1b9ed89e82009dbe1e13f11bfd6be0117a77b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248989529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80af95cb021935c2cc64c6635f6f802a469e11592902708942e4385db5df0670`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ac9bd2accb673ae6788f21ce5be56cadf0ca4b07573e19db85f5ccdb976c5b`  
		Last Modified: Wed, 09 Apr 2025 06:59:44 GMT  
		Size: 214.5 MB (214546833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9cf4e0b4eaca71e6f5bedf83f5e90eac54f1cbba698d34105439f725bc8dd18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42d38b1739ca99f6b44d829c72d764430bd779ad6156cc45ba1c837a8ffa25a`

```dockerfile
```

-	Layers:
	-	`sha256:c59db07afaafba9ee9d57b0288011a2cebee4716f1ee20dcb9a90c0c80d996cc`  
		Last Modified: Wed, 09 Apr 2025 06:59:39 GMT  
		Size: 2.3 MB (2252428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabc880d2dafabdf69337e62cb8e1be1f6958acb1e1d96822979b3f9ed36e08e`  
		Last Modified: Wed, 09 Apr 2025 06:59:39 GMT  
		Size: 9.7 KB (9684 bytes)  
		MIME: application/vnd.in-toto+json
