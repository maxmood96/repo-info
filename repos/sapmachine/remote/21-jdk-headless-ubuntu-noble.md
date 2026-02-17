## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:fa1d4432815ece0c492cb532a76622521051579150413017330e6eef4b0174ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:cd9412a38c976dd480fbaf2ce343793f55726219bf9f85a7cf8a3e57093c29a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244924249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be3082ce9d6393c6ab570a62b45722d0a337e072d5eea2ff14621409fb33867`
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
# Tue, 17 Feb 2026 20:34:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4ac36c447db4c0d6a7256177253bd819c5c29fd0bef4419be731ec09ab160`  
		Last Modified: Tue, 17 Feb 2026 20:34:53 GMT  
		Size: 215.2 MB (215196638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:143f75df523e58773f55dd563e7013ab792b0451e3017177e4e6944688cb4c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fba1899bf96a6b910a0255dfa21cafc338cf21aedbd6339fc9d3d85db9ee397`

```dockerfile
```

-	Layers:
	-	`sha256:284246697d882ff6cd061c10326a87f0bd7a8d69e0907c417a6b4077080d5b96`  
		Last Modified: Tue, 17 Feb 2026 20:34:49 GMT  
		Size: 2.4 MB (2358719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985fe80e55d16fe9afe3461a783bd615fbc32bf8c9398a49fc7586536d232a45`  
		Last Modified: Tue, 17 Feb 2026 20:34:49 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:606f8118de820a2116c592460c1de9d049154b05a28323653f84dc31ab7414ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242308809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e610cf66797182d3514e66a77d50e22f8782159b46b89e308f009e7ae964d2`
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
# Tue, 17 Feb 2026 20:33:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:33:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e3be1016f22cfc53021b60c0b8e7ad104baf834c73734682c358c31e2d98d6`  
		Last Modified: Tue, 17 Feb 2026 20:33:46 GMT  
		Size: 213.4 MB (213443689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41bd21a35b232979946261dadbadab37cdb355518b10b67d99e4cc5bbf57750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88baebbba729b65c776b9c20c1e779bc4072118a1c37fc1622afda8ba94f9f3`

```dockerfile
```

-	Layers:
	-	`sha256:00e950bdf329239e1971b51af254476855924a4222a767368615024b39a6f480`  
		Last Modified: Tue, 17 Feb 2026 20:33:41 GMT  
		Size: 2.4 MB (2359226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b9281cbaf48bbe71a67ce7162376e32ac6ea8e79275cc403fa91600a7567d6`  
		Last Modified: Tue, 17 Feb 2026 20:33:41 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c740d5ab6f3901a2e911ada420e9ff881742f72cad1f3c979dcedabf7002b89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250351196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf84d5a276b19dd2f7d15c362cc9caf6f9470777bb8a64bc69a5bc70069613a4`
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
# Tue, 17 Feb 2026 21:26:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:26:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:26:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf74dea8115a819329fa4f74a0980e5431f25ed14bbb2344a72dd633d84c193`  
		Last Modified: Tue, 17 Feb 2026 21:26:52 GMT  
		Size: 216.0 MB (216044290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ac8e330320b28b58c5561d2720965e2991196498fce81ced027c28c4a1b0bc2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b391206a7b507322f3210c08d875a5fd8fe3c7982c41460646dc8f77b2ff4af1`

```dockerfile
```

-	Layers:
	-	`sha256:c1274ce465fe811ebf66d7ca432ad7ebaf2e843848a739effbf191c723a69c05`  
		Last Modified: Tue, 17 Feb 2026 21:26:48 GMT  
		Size: 2.4 MB (2356190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00099fe4e6c92299c968f7fb4d2780dc9b4e299e4f6dde80bcf691d0f30499cd`  
		Last Modified: Tue, 17 Feb 2026 21:26:47 GMT  
		Size: 10.3 KB (10300 bytes)  
		MIME: application/vnd.in-toto+json
