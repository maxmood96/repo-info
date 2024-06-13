## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:7412290695fb4975abe69bde2abfe56e4ef2b422581f60e4c23122766eb3eef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a40a455e224e378e6c1ba53e49e80d54529f414ccade581cfdb22793781a5cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d76eacecaf0406c82147a394f54794bf4b700f87d152f5020f712da7a5a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728c2a274152156adae707afd4c7acff7c3cda876d9f29783c874f87c6aa6d3`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 10.3 MB (10307527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314584b23585792203e4a076400bf81f382d644fcb124e3f4ddf4f81afd551b8`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da49aa44fbf6acccb4122c994c67ba81c4a6140f03fb144120bd4253a6780cf`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89c183f941a66ae90604d83e0ac30aee3197b51ab7e74b363a9999914ee77`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee6ec2e169249fac98fe23df8d0c1eb252e19df7a7ff3b364d8f3f4fbee094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf9ffef60121c1ac26664f0439c64670b139b6aeaa957af6334c6f9a79f540f`

```dockerfile
```

-	Layers:
	-	`sha256:1832a42524e696b8e542d88ce1fce9959d42d5e7148a1e06a6c337d4a32540bf`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3614377f3b59450f10c8124c7df977ab039c86c05526e2f7ad95c529a4408f`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c88056a47dc5318043679e57676a23e583df1c718e7983a3b57d31f2e4a093f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024422e05673ba9016411a9080801a2e926b1283e23186b85469a2b625cf8fbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b85b4e240f80a499a71af86f86bb3a75a46bc47a84a841fdc6cec3b6fb75e4`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60e9beea383de0d520744c632f02662cfb2ea54b541ff3608e4cd6c258ed5daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c823c4fb2948cba2750dda96dbc5bd93d2fd769c9b0aa6c4fb1a87091d8bfe5`

```dockerfile
```

-	Layers:
	-	`sha256:c502212cb34e8b56ae978bc283f847c2d4d457e1f762d554516348d43afbceef`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78431dc615efd921d0ece65d407291dd8c193f19e87e47543b1a2e182523b064`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 15.7 KB (15713 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json
