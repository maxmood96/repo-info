## `sapmachine:24-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:cceba3d53251c93fa29126e17d2f034a1fcc4ab3ad02013fd3ebb251de5f7d76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4265ee1f0f6433df8f54bb326e2e024f987377ad4c14aa89de851f3b0ee93924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261550944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2692392480f258656eb7e9fa04ca29a5225ec3bbc045c22cb21e40e031d42d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4dea772c810200e8eddd0c5358bc28bbe3b2bac51b27a7b053812ce7328751`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 232.0 MB (232018579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:212a73d830ab0b92b18e8cbf84be3782f05eb71b3585cfc4972e506e89f0e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ed3f02d69dfc33daecd485ebc91f49c38763e51ffbfdb0af353e52850d10cf`

```dockerfile
```

-	Layers:
	-	`sha256:5cc1ca4230ec1321146555a47b873ff336157ed260c1276614c188b9c5318986`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 2.5 MB (2484191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b867043e1d6c488b5c5d223e4c9ecc04d29793ca6e1adc3beb9eb6f869ada4`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:01541a44930824dbaa7672902692efe193d257b827283804c36f1612ae9de3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257259425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefee42f866e91fe5e2db0329bb200513f49443cb9b53d34c0e2ca9ab5596f9d`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe07d4837160fd506363d91e9b2ce8f4baf58e81730e49e30dcc829135ea4b`  
		Last Modified: Wed, 19 Mar 2025 20:36:44 GMT  
		Size: 229.9 MB (229901243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b7bba02fed963ddd87d62a60a5abf0022e0342170a27caa43005f40b136b502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683141a7a62c20fc1ca7680b60ea03d477ed8f02511403d55059b6417d2dd5b`

```dockerfile
```

-	Layers:
	-	`sha256:0e22b868b945143389ae96ed44d8ed7bfcada312177e9a3716f60de568ee0a65`  
		Last Modified: Wed, 19 Mar 2025 20:36:38 GMT  
		Size: 2.5 MB (2483796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73074ad9d08a98a93f24ff413bb296515916e2b80afcef38d7195f1e8084c4b9`  
		Last Modified: Wed, 19 Mar 2025 20:36:38 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a962429c30667176c8232a8d13ebdd347fd3511592002b5f850c7db83f6da37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267685386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfbfe0c3986d5530752ec115f27578e0e38a35a623be5609f936869f3ce755a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91757d648f86453351af5df59e05e10af027a7b7830e05e76a67647e16cbf6`  
		Last Modified: Wed, 09 Apr 2025 06:38:50 GMT  
		Size: 233.2 MB (233242690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b6f1c3a05d3d1368cf4924d9f54fb0af747bb2cb2ff9887b822f4bbe5f20faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bffe315346a287b54fbcfbaf0ca1fa42367c5eb19e0fe8fcb9c590397d5c697`

```dockerfile
```

-	Layers:
	-	`sha256:43a9b06a3aead0d9b61cb6b7294ce205b2f9351601f94002d7a33184177dd312`  
		Last Modified: Wed, 09 Apr 2025 06:38:44 GMT  
		Size: 2.5 MB (2485632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93578ef29437b525abc13b91d60dd32f9fb69ed06fa8107f1186d8a8ce00792`  
		Last Modified: Wed, 09 Apr 2025 06:38:43 GMT  
		Size: 10.1 KB (10129 bytes)  
		MIME: application/vnd.in-toto+json
