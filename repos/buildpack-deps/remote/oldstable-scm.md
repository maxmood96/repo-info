## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:150417c4594908cce902dda4d37c66eaa3550740ef33c47e5e7a61247470562b
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
$ docker pull buildpack-deps@sha256:aebd2f18325a41cc96681233ecd703cfbfb1b859a043672938ae7f5b7dc3a11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124277639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bac40962cf757d93169bca6fa5401f309980d3aceb90435bd0aa3f466b80bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c8ba8101530427dc94994f23fb7674f74b7d4a3c7ba8b7b83d1cda6d16dd1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374914e720dbea407c2162624ca599462a0baf8bdb0d065b60135aa3c7d02e39`

```dockerfile
```

-	Layers:
	-	`sha256:b663aff7aa03425a5215933d2eeed5779612127d5831434d2b9adbbb7a4f5e6e`  
		Last Modified: Tue, 01 Jul 2025 04:20:05 GMT  
		Size: 7.9 MB (7912154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b97ad802dd3a81250e2cd9a76c090cdbe77d8751c85ab3167597fea478adb73`  
		Last Modified: Tue, 01 Jul 2025 04:20:06 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:82dd90093594f953c34d1e519c1f6bf42bbe8f7e15761c019775ac0eb861f366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114556054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc772d9849a6661b2d140052ccdeba36af956ce1e490302b32e2e103dbff55`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3cd898925dde7144b3eb09eedb10dcff5ea662f65eb58a12a069d95da2499cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b131ef640c254fee0d23a0f96f61ff861604e6b954ef3dfcd4ac3b310b881e`

```dockerfile
```

-	Layers:
	-	`sha256:23b03f95e5d0ac6ce4fc4421ef6710088bdf05803d146f1e58c0b34376b21992`  
		Last Modified: Tue, 01 Jul 2025 19:20:06 GMT  
		Size: 7.9 MB (7913556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f49ce7f6eed1c05e044d3f53c065f932c2cb7a9e8a4f690cd23924773974a4a3`  
		Last Modified: Tue, 01 Jul 2025 19:20:07 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:121bc1e9a04cb2b2a104d64e1937cf8b856cc0c80be92eb096082a721af0682a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122858692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d712c4b71eb1a503532574c108b409642012532d2a890d6dea4762ec14f1de2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6724e623fcfd38beec4b6292025d615f3f9313d71dc519e21d39f486b2370c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f10e45a31ac508747e80d43a888f8c7db1bf1cd1b6a334700653282fcddf57`

```dockerfile
```

-	Layers:
	-	`sha256:8225f13a3e7d443a805e24720bd8f929573ff6e5159af815ebada6838cb8cde6`  
		Last Modified: Tue, 01 Jul 2025 16:20:01 GMT  
		Size: 7.9 MB (7917888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146b14a62de95a5905ad56e89092f64b4f6d5e1ede4ffdcc75bd1d48bb67826b`  
		Last Modified: Tue, 01 Jul 2025 16:20:01 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fdba36a14921d17a845cfec8cfcf5c82b994fae5f1a24834a371176e4dd0cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127008778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bc9481776b6063f6cfde157fe7d571ba1121034d475dc45de748d219d81393`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d006d5e7d71524b98b0c95b15930436f551b2be990b9a7bfc0f38b0557ba7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe60979650c1cddf1356d6ce18c2786636be1316d989dc23e5cb87fd8a5c45cb`

```dockerfile
```

-	Layers:
	-	`sha256:a7bc53c81442fdb75119ba97e93d5ae4028d8a5162adb5864344f5c725ae5451`  
		Last Modified: Tue, 01 Jul 2025 04:20:26 GMT  
		Size: 7.9 MB (7907724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cce3240cb0fb879e74ab783416e16790d07f344d8061f791abc1de4bd88bbc`  
		Last Modified: Tue, 01 Jul 2025 04:20:27 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
