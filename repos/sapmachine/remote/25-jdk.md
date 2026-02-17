## `sapmachine:25-jdk`

```console
$ docker pull sapmachine@sha256:5e49011e472cd8b65dcfd228ebc81aafdc24127b2c0e46d1a3a92bcd2e68d8e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk` - linux; amd64

```console
$ docker pull sapmachine@sha256:875e1a42e7fad6842189e805d575ff0b40848c79694258483b98ad22d3648a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251180452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf2e4e6973e4100b5ef5a3635c491b77fe8678a1c30a8ea08d945e4e6de5cff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:32:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dd241bd37e489d34f787cd165d1a11f24b0c28a00cfa30c44e70c91094c547`  
		Last Modified: Tue, 17 Feb 2026 20:32:38 GMT  
		Size: 221.5 MB (221452841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6c34ab137ffce2166cf93555f0957a11888a4ff353d17577e488120a7c7015c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbcb4af04e58f692db5bfde98a80a27d7029acdabd2393b0e72f1c007953b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f1f5ba2806ad0fe67521576bded69c3bbe5da22ff47240921618bacce95d8715`  
		Last Modified: Tue, 17 Feb 2026 20:32:32 GMT  
		Size: 2.6 MB (2601301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16512266edaf3747319a780c6ecb9526d01e9f1d976dd5d0094e1e42c58e9ae8`  
		Last Modified: Tue, 17 Feb 2026 20:32:32 GMT  
		Size: 17.4 KB (17356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a05290e3c5e616755c7b8fd1b5848a5cf0b9e7a4c4a307f4e1ac72f44e9b2811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248131112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf07bd5534adcf17cf6fdf1ea41560b23b34afeb0b91a7253b63da9837e2af48`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63210ec8e29a90dd08e5d25f72bdeb405e7aa2e604119720f6cb0ee9275c1387`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 219.3 MB (219265992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d2f0d557ff020fb61270cc16ceb3d04a81d1ae1c9f5f45c4381faf249da3c9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b959587456f2051aeafc9af6dd0a6494aa6de4d0a013a4ad4d09228ad7b969`

```dockerfile
```

-	Layers:
	-	`sha256:facb4a30d6114cfb4f274aafe6576d9a1f6f5f9dd4bd71f36b054eed5291ab3b`  
		Last Modified: Tue, 17 Feb 2026 20:31:41 GMT  
		Size: 2.6 MB (2602090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8dd7872da9d5df54bd651440751bc200855afa57d2aa3065ddc8e283a8eb85`  
		Last Modified: Tue, 17 Feb 2026 20:31:41 GMT  
		Size: 17.8 KB (17784 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ae0df8335e012bf9df5a8df2aea7b91a0d5f9588c80cb8842bc376cd12a0cc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256689529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269e6b76f66941d06f264cdb667e72d87f808ff2d5a80402711c7c44aafa80cf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:15:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:15:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffd89d86dbd458a58533c359a539d854ce70cdc772c7d9f919cfaf14f31435`  
		Last Modified: Tue, 17 Feb 2026 21:16:03 GMT  
		Size: 222.4 MB (222382623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99bb52a8d0d4f13d33fc77c4b2b0f3ddac2b2e177d752d7318ddbdd1fc13ea67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68ff99b340fc473ff69a2359b5ad4cecee0b71cc71f1e4857d1cf3798089c33`

```dockerfile
```

-	Layers:
	-	`sha256:e85088dd2fd86c02bf04a4158de7fefaf61c88583dd1405998b5a60565027089`  
		Last Modified: Tue, 17 Feb 2026 21:15:58 GMT  
		Size: 2.6 MB (2598373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e99e08d91720a35ab7e00d1e522fba7d6ac86265dc6a0ee47feeb6434b78436`  
		Last Modified: Tue, 17 Feb 2026 21:15:58 GMT  
		Size: 17.6 KB (17561 bytes)  
		MIME: application/vnd.in-toto+json
