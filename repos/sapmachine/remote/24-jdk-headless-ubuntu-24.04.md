## `sapmachine:24-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2434f49baff32e8cfed029e7b5312b21acde4bacd7d685c092d85eb8575c2cc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7ae2d1fc8717b4ec72103d4ab1d27ccab412add9a39d3a5661f86fc277e2a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260973844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3e63d71c4a7835f0b82ee730d9c59fbc56f1083d31160bbfc9274aa766454f`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0071928ec8174c0675155b2d764cb90d4851c96cd327b9922877d7f8d281251`  
		Last Modified: Tue, 03 Jun 2025 04:18:02 GMT  
		Size: 231.3 MB (231258507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:379821affc2a5b76deadd77b8330fbc48488eae9c18d5ab3ec0944d329a36547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c94c931020c207787887d45716504511d329bfdc42584f9bcf73f1ff5700a92`

```dockerfile
```

-	Layers:
	-	`sha256:7cea45ea1ad2e1b88dccdb78bb9c298a2f95dcd2c38d65470dee2d55972b21ca`  
		Last Modified: Tue, 03 Jun 2025 04:17:56 GMT  
		Size: 2.2 MB (2246455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f3979320d434add9956888ee429cf6d255bcae35651a7f26690d8e7007436e`  
		Last Modified: Tue, 03 Jun 2025 04:17:56 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

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
