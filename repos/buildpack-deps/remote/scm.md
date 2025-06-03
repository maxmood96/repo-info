## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:7185490f81c4b14a53fcf3819a96dccb35db36968ebaf06bf2cef3752bbf1022
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fd7256e511bdd98e85a40db1bd7a1b8e39b18c6d8c265e8e909c7e8f03b5fdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136903738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f54b194ae8db7f4d900e9d9865a4963e7d4bdae215655cb817f9abc44a1a56f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9c84e1373f6a0f33efe820de395d0fafbd8ed4782ba5210532e115990adbe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7789218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d2f5c70f2597a1c2080b68bf1f4bb73c584a132a6900109d4d12a13537283e`

```dockerfile
```

-	Layers:
	-	`sha256:d6010076daeb80eed4182577bf4b5cec122c02eee21330c4e3cf8d261410439b`  
		Last Modified: Wed, 21 May 2025 23:37:24 GMT  
		Size: 7.8 MB (7781564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee767308db983fae8705e4ddc3826f1bce8514f1a151188384bd1d3278068f75`  
		Last Modified: Wed, 21 May 2025 23:37:24 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1e2c08680c06b677de9720d000c5bdb898c517254e6b277dd92013ff4f9f6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130713683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd8dd9d0dba5e0a0e92394a231cc2e8844c9c0f98221cd8cc897c1dd37fd375`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b51cc5977be0e2fae0a0314b991e4f90fafc6823a929775d09884dc18bcd7`  
		Last Modified: Thu, 22 May 2025 01:13:36 GMT  
		Size: 22.7 MB (22694185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662df94d663c1ee85e74f3b73f3f19049f9727ed40e72aa3497df0e6f9da2a46`  
		Last Modified: Thu, 22 May 2025 04:44:17 GMT  
		Size: 62.0 MB (61998014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9c4803d6fd574a2d683e8ef0465ded7334c7705977fea6affda729e9504ed18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967b2c065080bd6e4b227ea9917755b5f778543b9ef9b938757f459c1e5b83bc`

```dockerfile
```

-	Layers:
	-	`sha256:0344386c13c3193bd4ee0968dffd57ed8d89af6e4d11ee39578b2523eb0a1e81`  
		Last Modified: Thu, 22 May 2025 04:44:15 GMT  
		Size: 7.8 MB (7783430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c2ae2267436e4f2b190b5629ef848967699c8309867d919fcbac5d16f95a14`  
		Last Modified: Thu, 22 May 2025 04:44:14 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

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

### `buildpack-deps:scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 12:11:27 GMT  
		Size: 7.8 MB (7782849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca45339406d44569ee66cfcbd9ca8c8b628176a816959de8f05e7b11fe88bc62`  
		Last Modified: Thu, 22 May 2025 12:11:27 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

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

### `buildpack-deps:scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 09:17:56 GMT  
		Size: 7.8 MB (7787969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528316c30e71d3b7488535d8f668e398c4ea0380074116069b13878f45c1703c`  
		Last Modified: Thu, 22 May 2025 09:17:56 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b8c09da5478b39e948c6c710b60824ad899869c2b0d69f4460a14ebbaebc0119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140551345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6b1cca919b1fcb5f97a03f292dbe3d6c99ebc172e5cc4b1328d0f6471eaca7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Tue, 03 Jun 2025 14:02:05 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Tue, 03 Jun 2025 14:02:15 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96bd90c406e2e2776ff2ed8c3125612e1d429a746bbedf9666ba9015e625eddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7785350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0e942113ebf8c426461b8a1897a25ad471b660681fe7af992e304add69782f`

```dockerfile
```

-	Layers:
	-	`sha256:83100c4dce9029d7d5ff249a04acb37693e11530c695f433a811bf7bf364e34f`  
		Last Modified: Wed, 21 May 2025 23:37:28 GMT  
		Size: 7.8 MB (7777723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb352857f9d0f04104be455c005eae56f20b91b3ccc4af5292059db691392d2`  
		Last Modified: Wed, 21 May 2025 23:37:28 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

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
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Thu, 22 May 2025 06:16:24 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Thu, 22 May 2025 14:29:03 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 14:28:57 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

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

### `buildpack-deps:scm` - unknown; unknown

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
		Last Modified: Thu, 22 May 2025 16:52:01 GMT  
		Size: 7.8 MB (7789431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab40958ae021c5cd12e0ae0a2e40d409b012f00b638bfe35c9a809550c6e1aa`  
		Last Modified: Thu, 22 May 2025 16:52:00 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:89add8e3acd203fcbf20fb626d06e1d925bbb76e027fb8044204f7afe1181724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134657225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b0a509437a62b7e7de1422066d6c0c20b4cc489a727a101ec0daeac8e76d29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:910a452044b0fecd89f499974431e9a8ad1926a4896aaa9a07ea253d318a6fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7788424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c3c80be76c4d3277323be2c388ced556f54b4c63250fcb19ec2899ebfbaf6b`

```dockerfile
```

-	Layers:
	-	`sha256:676a2c6a9cc65f962ac74faae476d456ef41d471b0866ad9769e1bd2fa72ae6c`  
		Last Modified: Thu, 22 May 2025 04:37:15 GMT  
		Size: 7.8 MB (7780769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec79d86eecdc21676a70cc0d3ba1c72f12c802605f0ad844b8c2d1be03c1d2db`  
		Last Modified: Thu, 22 May 2025 04:37:15 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
