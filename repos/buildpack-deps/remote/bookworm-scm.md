## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:b5d201135a78ab844445fe1cdfff5962a381d2e6f1e38ce50437d3f2241d5a01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fab1b6389a07a117b06169a1c2bc5a4a3d3f5d7315dea5ebf4d7ad49606d7f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136909774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184202217278e8f818fab1583a99bbd9a5899a5d461e1fbf45efb3e3bf02dae1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11e44d930a2f569bf0fa1a303f10f1aebc4f579351fabc75178981a453284443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7965233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9519b3e2b7eb9fd89b6722558ef430c8b9b2f927613ce81e24bc085c9a3af`

```dockerfile
```

-	Layers:
	-	`sha256:2c4a4e6e6d9c9a2d2628943c7e558ad6c32d7c26b62d59ec013e043b548f60ff`  
		Last Modified: Wed, 11 Jun 2025 02:23:50 GMT  
		Size: 8.0 MB (7957578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e5556a6a3d30aa93a721e0ffbafa0679def010d6d8d83615fd0eac148f6f901`  
		Last Modified: Wed, 11 Jun 2025 02:23:51 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cdfcb170210ec6c51287c3177bb79057400d58cb84f4a84fd1989592591c950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130718688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f6fbefe8b727cb31305ba562577b346203bf161c2ea7f39c1ba7907a902f9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973a0421a43933f783f2da8c4e6210bbcb63636694bdb47f5939d46f0cd8e74`  
		Last Modified: Wed, 11 Jun 2025 03:12:54 GMT  
		Size: 22.7 MB (22694196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd263284be736a4785fb0c489cf441580757a05d8cb52c26f07ba8f071d621a`  
		Last Modified: Wed, 11 Jun 2025 06:33:53 GMT  
		Size: 62.0 MB (61997905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0314cedd08a06fd1588c2af9b91cb4b081afb72ff3ce961654dbbb80b980d569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7967167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43b876192810068fe65aef4941d76241e1a48a423989cb377fb316529cd5966`

```dockerfile
```

-	Layers:
	-	`sha256:9749d89ef0486d90b067b898cec7d94f9288de39b764254ed572e9a1e1d9b38d`  
		Last Modified: Wed, 11 Jun 2025 07:19:47 GMT  
		Size: 8.0 MB (7959444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf27f80968b372da4324bf3438d9f73d11248ba8ed9c8deba30b3864cd3dce9`  
		Last Modified: Wed, 11 Jun 2025 07:19:48 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a494ab532062022a63dcd7ffe1b835737a3041a6971579e30484be4bf1f3b138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125783692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f19baa86b905f0a4aa70e38acc6c6f1c59649d19b188a29d03488f89bf1a7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed1073a08b7920df34f8501046a0a9e213d99c50f5c72e8cd221c5d4da223d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58353a7d286d7bdbacad83e1017ac8654bf204b7e004a21024342fab03a2f5d`

```dockerfile
```

-	Layers:
	-	`sha256:68c7f8467e777652ce247dcaeb7d0fcee95f4d2daca0c8a0c80510ab3041de0c`  
		Last Modified: Wed, 04 Jun 2025 01:03:57 GMT  
		Size: 7.8 MB (7782849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45339406d44569ee66cfcbd9ca8c8b628176a816959de8f05e7b11fe88bc62`  
		Last Modified: Wed, 04 Jun 2025 01:03:58 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8d0e5b1e129ecfbdc5de2ae5364f33a94a4b0d7f78f84d03ab044a4daaf55683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136240568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6382198dfc5858038911d9289138a011778ff08758c8426dcddf1ae211c5181`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05558ecb499efc999b57cdc07f15e1162358f7a855272d1e40f62e624651bd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7795716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e579b8252845c80ad92fb7d6a94e916470e56ee0e41c8b04135f16161f99ebde`

```dockerfile
```

-	Layers:
	-	`sha256:4550a29f1c52f80439e56474ec2dc0f684d303e738ca1135261f4adc6223b0ed`  
		Last Modified: Wed, 04 Jun 2025 01:03:59 GMT  
		Size: 7.8 MB (7787969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528316c30e71d3b7488535d8f668e398c4ea0380074116069b13878f45c1703c`  
		Last Modified: Wed, 04 Jun 2025 01:04:00 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c74958a566d5041ae127d50b48507881bc32539867b4a25a6b6648c6aeba7ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140558420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae9a1ab4ff186b5f9e546cd97d7453aededf0668773e49953bf8da35493ecbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a96671828d2e8c840c37ed68cb848e369f872016ff7cfebc2d166c92a792ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7961365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791a381acee8d789918102da767396ce3cfdc1f024b3e715f2e2e63dce80a489`

```dockerfile
```

-	Layers:
	-	`sha256:9550ac41b35b66f1a5df65cc2d9b61c812a595daec70d6a5a987a00bc07bd611`  
		Last Modified: Wed, 11 Jun 2025 01:20:10 GMT  
		Size: 8.0 MB (7953737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15214116a36754cc91dcc6b07914d3a57ccf3bb56a792282c3d4013d825326a9`  
		Last Modified: Wed, 11 Jun 2025 01:20:11 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ca4cd54452727bce449ca10ca21489f2db1fd5683429439c916c96424d000fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135676838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37acf266ab5c5ff9cf76b78f0c1d682a891cdd53d7fde970972a88c66382b310`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Tue, 03 Jun 2025 14:36:20 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08a3a020be9aa177ec5209625628a949eac2a7a1f679e9735e8bddbf073affb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b2ccdabc43257b90f0b21aafa750e7667e7a7bcf6658094775dbb21c424972`

```dockerfile
```

-	Layers:
	-	`sha256:a6c9199a56e7270dec790a03c8a14c2888afa244ffd99851c5dc4489e2c3f0b4`  
		Last Modified: Wed, 04 Jun 2025 01:04:27 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ec2c919101050cb036e5719bd396a530b3879678086a2e76e7bfdc3b3e1551f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147828594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec1e0e70bd6dfa509419a7673b8c2268c45aef24aef63540e7d8e67864afdd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:512550d50b82a94eeee9b1eef797fe7b02462d49cf4efec7706663d2471baa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7797124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d8f10edf61cd2a6061f51472866d1fe5d2cde5a18c9156293027089e199bd2`

```dockerfile
```

-	Layers:
	-	`sha256:de6201b4710a98964905ba9b5613a8ab9a46c6567a7ebefd493f029a5d99421f`  
		Last Modified: Wed, 04 Jun 2025 01:04:04 GMT  
		Size: 7.8 MB (7789431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab40958ae021c5cd12e0ae0a2e40d409b012f00b638bfe35c9a809550c6e1aa`  
		Last Modified: Wed, 04 Jun 2025 01:04:05 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ed843001f1b3f45c73bfe95d6c5c067510fa8f1b86cfd16c6307b6c49791de72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134662657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b864fb3b6a800dac1ce099df7d0b6216bba96b9e317391dc4209230fe361be0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c056714c54676358218cd75dc0c5d3298e3c0e7e53c127fdefd363c4380d95`  
		Last Modified: Wed, 11 Jun 2025 07:19:38 GMT  
		Size: 63.5 MB (63498247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc32bbdf9d44466eaedff6acc5ad7bdeabfdc4beb5ab74791492facc4256004a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7961546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c2bb39e400e75651d2dc5efa9cde5f82cba83e6951377c19db2b4a41c109ef`

```dockerfile
```

-	Layers:
	-	`sha256:58c2b4dfcaaaecfbd54d26cdd3dd84504db2f75c6f408381ec6c1852140bd577`  
		Last Modified: Wed, 11 Jun 2025 10:20:06 GMT  
		Size: 8.0 MB (7953891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3346c436426297438c1589aa23161365020410347a2df0f78b9103958a5cfa`  
		Last Modified: Wed, 11 Jun 2025 10:20:07 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
