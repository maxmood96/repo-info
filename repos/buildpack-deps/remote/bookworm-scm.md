## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:0ea04f9d77f1a72a19d216e4a8bd5b5a52157d175b3908aff4877b7decef77e3
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
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e84734c30f13c18d6992c1c8727bb8b40882c6fdeae16a5843f077f3fe6bfbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7500e38651ecd4000c3c51402836e16017faa7b97eaa859b930eb79968220de2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Mon, 28 Apr 2025 21:07:39 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Tue, 29 Apr 2025 06:01:08 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461cae6835e6d9e4c238b202d114b5fb2f2b659479fcad91acee966b7bf3bcc9`  
		Last Modified: Tue, 29 Apr 2025 06:21:48 GMT  
		Size: 62.0 MB (62005790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a712f9d1124705170ee8fb19f1b92dff191bd6cfc1312ffbafb810addd1132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66c6bf9a8e6a94d86793cad07ada62f0fad8d7f548d3f10e7a93d0d2026c0ff`

```dockerfile
```

-	Layers:
	-	`sha256:dce29bc8aae5fca558fc50c3302d0741a1db75bbec1be28579854bcf470c6492`  
		Last Modified: Tue, 29 Apr 2025 06:21:46 GMT  
		Size: 7.8 MB (7752016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:672cd97b7d31061f4478d0e783a1b3a7f5717610a19d4032a7b7161de25221b6`  
		Last Modified: Tue, 29 Apr 2025 06:21:45 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:73314cc9721898fea2141a981fb84dfcbd96da69fa1d2e20a4cbd9e2384b0c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125755670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3d7638f5b0129a6bad7c8bd1647325baf0096c4c50d68ed440f7d66d6f4fd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2126ac08f70d6f2cd0dcb27b01ad6eb66c85736b6636348960ed838f8953d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125ed5967c9376a454d33db163bd0ebe0c2b1e9b478f003382f51db4e1d3a050`

```dockerfile
```

-	Layers:
	-	`sha256:1edb6c3840728fb652219d591682f2fb7821aaa52df76f81199090e77035cc29`  
		Last Modified: Tue, 29 Apr 2025 13:22:54 GMT  
		Size: 7.8 MB (7751743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed5e710feffef480f30e6bd8b65034c1cb33fdf1c11d2bfa4abc3be75abdc8d`  
		Last Modified: Tue, 29 Apr 2025 13:22:54 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:15477468c556b9dbf126151a7e0a79a4dec22a0a1e449ca4ae4983569c1c5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136227589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6927a4c74950f9f2e51ca1f920267408f8c6724b422dca81d7d300c8bc24e272`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9c8f100c2f394fbf54c3349152e737fcc6d593daff214fcf0570a2d755ab56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc6b251324586f2f5b7a8118e24cbab60254ff996181dfc6975fe71632eb04a`

```dockerfile
```

-	Layers:
	-	`sha256:f4548ff33a5a44572b98773be94e9e5d10618fbfb9489f6266f5d6c97b3c48f9`  
		Last Modified: Tue, 29 Apr 2025 18:37:09 GMT  
		Size: 7.8 MB (7756863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac5f2ae17f73666193e85757cc47c7f05020578cca56b605cd4923fd35dbc9d`  
		Last Modified: Tue, 29 Apr 2025 18:37:08 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

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
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae36afb73c702b5e9e35169078a3954dabd81fd464a225b1067148de112a9c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135679320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a737554187d76d32cd628d680236822b6f941bb403281f814bdba5a6111bf28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Tue, 29 Apr 2025 21:16:09 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d4d16e04f179d4f6798f1128b86f558294912d1aa53a7bc0f88d9c65977052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8abaa35753093b6741640d9833a424151640e0569c21e18ca06846b07538d56`

```dockerfile
```

-	Layers:
	-	`sha256:dec7b46bba9b4d04435844992c58ba8f4b05994a8113afb0aeb06d6fdccca89d`  
		Last Modified: Tue, 29 Apr 2025 21:16:02 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9c79230a5eb9dcbc109a2113c2425837233029c69c10ba67a67775c658dde49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147822666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f371660b6b23abb5f3aa9412bb621545348e66093a563efc4b107e6f6b413e43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c86cca3bf8e519f071635b70d3398e0906c6aaed3c4fcdb55750f02b5d9b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47b424d7ff8b04002320389e8b83affbf4316981e928346006b500031452b9e`

```dockerfile
```

-	Layers:
	-	`sha256:1f1d97552c062670cae1965cc7f73feeaee4d22a251c9873940cee3ee07c444b`  
		Last Modified: Tue, 29 Apr 2025 08:28:58 GMT  
		Size: 7.8 MB (7758159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:955c7f154c65d6453c4fa06da666a64b400089a91bb6a5b94922a0beae6233d5`  
		Last Modified: Tue, 29 Apr 2025 08:28:57 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:42d3b590b427310d4e636340178da6ea58dcfc4748013ddf0bedc351ca0bf002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134656520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155c77ef2e6073c2b42b52f71dfc988a7a9f4383ad3698274b2f3f7d9884a702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:21aeb81bfcf6482640cfe8aa8fe38ae13af3d33f5dceec298f344e38f00a356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7757318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1660d2d43878757739726bb9c477581f30bfd4716c50219742bf65dc236026ee`

```dockerfile
```

-	Layers:
	-	`sha256:2a2c3e161bb32eddd981af71a0bdfdbe1452c148c764ed524a7272f206cab294`  
		Last Modified: Tue, 29 Apr 2025 02:58:47 GMT  
		Size: 7.7 MB (7749663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2267cd230f22468225b25b29277b125db7b9db8bec4e14db54ac75f3ca452461`  
		Last Modified: Tue, 29 Apr 2025 02:58:46 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
