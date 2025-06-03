## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:ac05c0cae1fa17c0633f9419cc3d9bc5e06f86876b93ef59c8dc7ceaf80515de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:13cbe86177d26240eb3fb1e0c9ccdbc812203e4296c7a9f04bb71ede598de009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88648702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ac9207f3c57f23a647df9bcc410d7194b4b7ab26d02fe30a5479ca4be0268a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c0e548c1069442f05f321f03b191edcdfd790df2394ef9d65b155361182018`  
		Last Modified: Tue, 03 Jun 2025 04:17:36 GMT  
		Size: 58.9 MB (58933365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8db465ee4313a4b01518bfa2f1ec412c652260a27cac45bcf96ddc58b98474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffeceab40bb054d348312a5fbbbb230e5cd187e36e3140601da5627da8ee2b9`

```dockerfile
```

-	Layers:
	-	`sha256:83a487056ca1636681dfa06fb4ef849db3db9531535102ced83eaf6afbcd04b8`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 2.2 MB (2172232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f938e0229f9ccee59a64287b354cb1ec65074e24e2c6cb05279dfa993d28ff`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:195203ade7d74cb88fe3492d0b3c024e7056ef3b099f2d021a14401a06110a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86962679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ed43dd26fade699231880b1c092603f5348c14638e3d83b4ae8416f2d6937b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295ca1d67463079f6fb1f7afc020200a6d2d45d57514bf3d8df447e84ac3839`  
		Last Modified: Mon, 05 May 2025 18:33:22 GMT  
		Size: 58.1 MB (58115803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f2783b59678fae6c6e4ac48b363240eb5257c4297091d961099bb816f31fc0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dbdbf0fac37885626d2f2c0ae099ea13e2c48abcee59fa4b397e46103669d1`

```dockerfile
```

-	Layers:
	-	`sha256:155e2e88ca036ffd535f09723c919feb71ba1237370830d7e4ae09d7bf42b8b9`  
		Last Modified: Mon, 05 May 2025 18:33:20 GMT  
		Size: 2.2 MB (2151507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62e814683ad637377cc61a9321b310f6a6054bc483f1ae18c610c9f9a8ca1c69`  
		Last Modified: Mon, 05 May 2025 18:33:20 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:169f44fbb359266a1eea58612315f51794007658cca519a54a340af12deb9b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ef9e8f8b87448cbb0ed9e917f99a38a6a6bc3bf34d3b90f5e394c370db5325`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6bd7184a86d9a6ddc1cd2ca921843270aa3fd3ba74d4c417e10cf74ecd05fb`  
		Last Modified: Mon, 05 May 2025 18:26:33 GMT  
		Size: 60.4 MB (60421539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39bf5dc33d04420451606f6f2b9e127ac3943e4bbcca75f6481692115f38463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ac6cf9cafa5f93e326b8f46332b95fdc69e2234e465f0b3a6fd0d9b18e866c`

```dockerfile
```

-	Layers:
	-	`sha256:7c9f68b4e063732793af901ca944fa030bed86228e91ccebfc675a43ad430976`  
		Last Modified: Mon, 05 May 2025 18:26:32 GMT  
		Size: 2.2 MB (2154894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47113bc9002ea9b7fe0c40ddddf20eac5ba25c2b37ff588569ab7d65cd9d4ba8`  
		Last Modified: Mon, 05 May 2025 18:26:31 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
