## `sapmachine:24-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:cb97d3690a5a3120394f346ad9d9e906a92b1026cf786cba371fee960e153783
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:24ee21b6c9b3daeba07b777eb2bce940f06e825929cbd5bc1d1e538657c010db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260975548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93b8eb9a9f5a9fb6cdba6758377cfce27317001d7eaf9b3b1b5b8712af4c802`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502f314a3e4ebf1c6b3c001b5bab30b38f64b7b74cdafb8a0eb53154b55f844e`  
		Last Modified: Mon, 05 May 2025 16:36:50 GMT  
		Size: 231.3 MB (231258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:094c8b7761b599c12de9578e1c0bf006a98647b338352b2f42251a622ce27f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518582aca0165fa29e836cd44f5594afd220452e6ff8e99b58630a0a1de9406`

```dockerfile
```

-	Layers:
	-	`sha256:fb496d656f5d30ce07bfdb32bfb3d39f5a7b6bc9a9c828aad20f6f5e8dd2325e`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 2.2 MB (2225211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb9198ce1ead9fb911f687169d04920b958c1647f557f9eba91ed5fc47282b5`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:90d0cf1828b4209d69bc1708a08edf5f591796b730c1975239ccb5b5948ab5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258012350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a82845631d2a1c1da110ed5a9560fca87f5c798903b7c1ff5f859bd4e4199b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf1b64783bc8062a70b41ddf4f130dd6c9579da8b410dd199627832b4aa70d7`  
		Last Modified: Mon, 05 May 2025 18:24:27 GMT  
		Size: 229.2 MB (229165474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3064cb06b32cb71092447c69af04c8ed2804683772897dbe434c8f38dc2a6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c9287f048d3df6e40e3a59f179698c2e2c63edf36c88ca439da8e7a36f0fa7`

```dockerfile
```

-	Layers:
	-	`sha256:ebb49127300f3630ba0b6eb58c276d539db728396de8e459dd4437e5e1a76318`  
		Last Modified: Mon, 05 May 2025 18:24:20 GMT  
		Size: 2.2 MB (2225727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d8a04a46c41ae86eccc62cd8d96475d9a99672ef3b9aa70ba70ceaf5240930`  
		Last Modified: Mon, 05 May 2025 18:24:20 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aaa242b47e4b48179f64389e9c695c0624cb177b6536f013fcd3e11b5d52e78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266717922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804936cf42ad0a56d5a7a577e34bec0d195c961135a99b32b9b7d633fdc3facb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4325d5c7eff603b8fbb3e3e8103b8c2731787bd6d1b83081b24a76083a72a34`  
		Last Modified: Mon, 05 May 2025 18:12:47 GMT  
		Size: 232.4 MB (232377084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2020a17a32d0ab56824a2a2c345c4f91eaac3f5c5f7fdc71695d0b8f30299922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2488770a1cfe3033f4a739b5d5872bee5dade2118b6f8e8e1eef5203b8b5db35`

```dockerfile
```

-	Layers:
	-	`sha256:34b7da38ef3563a636b89b0f49b6a80607c355b05c36d67efafc1e462819ea35`  
		Last Modified: Mon, 05 May 2025 18:12:41 GMT  
		Size: 2.2 MB (2226553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49821d883fcd6c23f1ec9b6e1ce6be40f80aff20f71cecba38d80f2e9f52a50`  
		Last Modified: Mon, 05 May 2025 18:12:41 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
