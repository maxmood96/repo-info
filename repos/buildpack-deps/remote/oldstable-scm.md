## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c87f9a411ab3acf9f947c2cdcf231ee23e877e52df3660cfa5ea128413474e5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9d86dade34934566e6c18f040ba53c0e11dd999a277a8a0a9e65c01e48eb1a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29afb157b269f26701a2b9d44f585fb56abb102239135d8a365d1ab0a0cfad28`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8839e2bc871ae3753120cc90b7579e8420af27a9a923ddaf6fffb6f313805ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba323cb8e2a91309487a0f9963c334265a8dc6451e81e476c8fa468774ef2c`

```dockerfile
```

-	Layers:
	-	`sha256:61908d48b58147a945338cb667a471444fcabc278cf8b1aa10e9145d0cc76d85`  
		Last Modified: Tue, 25 Feb 2025 03:13:47 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a559df725d634c8ac5a06672936b50ff8cf27261380f9c58553729acff18a12`  
		Last Modified: Tue, 25 Feb 2025 03:13:46 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55fb0cf0351ec6c97ad75602ca85c0077a515dfdd17ba66b912036fab7b00630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114340805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b476620822977a405925eefca57f646ace23215205bb518216ac1a483fb26fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be1c50cddcd3ab98244d946e9a2bc219c3a1dd25946d555d6d7a186db3bbf427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7717000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7769c18fa7b3b8b680323353446c6b9ceac5f2427ec1e81f2005d3331181cb`

```dockerfile
```

-	Layers:
	-	`sha256:418de649e0fddc0c78910e3fb8517d6f978b2eec8fcd02029a698aa02552c064`  
		Last Modified: Tue, 25 Feb 2025 14:18:50 GMT  
		Size: 7.7 MB (7709588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b72b66337313604e9b7cb86aec7caa829f664cebafdc5b326e488a513245fa`  
		Last Modified: Tue, 25 Feb 2025 14:18:49 GMT  
		Size: 7.4 KB (7412 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e34d8d3fa7f100ccd54265a309872fc419db7b15491bf92fff3431fe12435001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122648211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d391b3f729d49ce9d62de6ae8063efc2f04d2fbbd73e2a5dc32cfb64d5b231`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b816b6ae34ba0df916a8c857c969ff2a93810bea66b32bb8f87d6fa1dd64ccf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768dd5c59ec84b899d7dde5ee117b614fc432589eb886ca5f367c95fb8be022f`

```dockerfile
```

-	Layers:
	-	`sha256:a4c5ecb9c737137fea0430eb137b7dc883b11a36c98df66a43e34c7ee2701f73`  
		Last Modified: Tue, 25 Feb 2025 11:54:40 GMT  
		Size: 7.7 MB (7713920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d1ec0cff06b54897dfb086f173350fac0408a66543816b0fb8f068a52932c4`  
		Last Modified: Tue, 25 Feb 2025 11:54:40 GMT  
		Size: 7.4 KB (7431 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c47f7fcd7509e06d8f28c0d9708bc40d2fc930ce7839373f7484dc8a29431323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126771063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb3b28d97abe71cd7cc96adc0237d71719f7e07d906d16a70b8a5e50a18ad7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d1be050999cb7935766008eed6d6c4c054de5ae2d30274f03f83b84dbb3b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6b40348db8bca6028e75ce907a7de8226aa43018a5463f8f00e249901eb485`

```dockerfile
```

-	Layers:
	-	`sha256:8757edb440e90354a28d2e404c16bf60a77f788cb52d4968fe1fd9b7f3a58ddb`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043ecac4f8f54e0a88050166c3ff290a4acbc411a2a4d023bdc2eb4c369e4884`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json
