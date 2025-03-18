## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:bb739f224698b44be027d4abcb7fa84883b66f7986c0a1b72cba121700ccd4c9
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:662b99f67e224e6ac22c92c3c0321e83258f65b966c68b571283e9af4e33b9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140827077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2149fe105e28674924fe90dab77901075742c1916efd804dc62e50fc8efc6225`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b312498eaedc471a9ee574437ddcf442ef14eadb9305c2ea1c843f2af922d473`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 47.5 MB (47513473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307579de8afb457f38a2a818765fbf595dc7bca2e9022efb29cd9a1e5c6b6b9d`  
		Last Modified: Mon, 17 Mar 2025 23:14:00 GMT  
		Size: 26.2 MB (26230971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8328f6595bc164f14568dbbd4ea22c25dd2666776b4b2c83c26194060e04be`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 67.1 MB (67082633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:977a1d6dc644e37314fc72f6c03e49927a2e5e731fa01260ce84e35e5ee4410b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7580737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175e92a6fe7126267a372721d169cacc119407c7473a8949887767f9b99cb14c`

```dockerfile
```

-	Layers:
	-	`sha256:aac6961803cd1c5aa867a2dd6d65a3c0b025cd1143d6069f29c34196f38d0bed`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 7.6 MB (7573423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193fe9e0e3d258110df44697005aa7f4de7fe3d776263d9c984195e423438299`  
		Last Modified: Tue, 18 Mar 2025 00:18:58 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:085faf4852d3a06b005f51862bbd9f0c30b0bba6db8429b8b47d9003e77fd83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136977710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a9665295970c848b018fb73a3615b492f581cb058461f3df85dcf2728f404`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:131ae520a4eaed5ef3f8bfb62695032fc5b0cf09159cb958245abf1bbddef3b8`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 45.7 MB (45706841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cfbb99d11f866136a1de25d46d555105f60a1f7b061aaf7d89155339ee129`  
		Last Modified: Tue, 25 Feb 2025 05:17:32 GMT  
		Size: 26.1 MB (26127258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7a39b0019bff7c7c84e047f3e1f583a04358b1f598c468c944216bf4311bf`  
		Last Modified: Tue, 25 Feb 2025 08:39:03 GMT  
		Size: 65.1 MB (65143611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee3132e287f680c0b455c0a40a66a1253a39128d15155a7c77fab9ac1afaf0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7615111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad935290c9f2da35cfaa49a2f395f7dcc342590c06b0de2e950bdb8e7eacd12`

```dockerfile
```

-	Layers:
	-	`sha256:7bbdccbc69c5bccfc107e5b15cfd61852285cf2076eff9dae5ef15a755e1572d`  
		Last Modified: Tue, 25 Feb 2025 08:39:01 GMT  
		Size: 7.6 MB (7607737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e1db012da70020b96ad983e6517a8bfae69bf796657e3ad0e7c1b9b4020ed2`  
		Last Modified: Tue, 25 Feb 2025 08:39:00 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9907fe2f8d7980756504e2503210d0af67b9a91074a326b4c17f53dcedd640d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131801495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f5db2ee7183bdc8266cb1e8f305cdaadf7695eeeec6341c26e9a9903559f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1268bec7b6bf92bd5fc4d4120fd51b9bde5a9c50d4b8a8decb59fbe4a53da6fb`  
		Last Modified: Tue, 25 Feb 2025 01:33:55 GMT  
		Size: 43.9 MB (43903193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe307003fac8d59260832b7e5476d782c0d94c51fc746df3d40b574a8cd73406`  
		Last Modified: Tue, 25 Feb 2025 07:18:31 GMT  
		Size: 25.3 MB (25278377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd6bd387fa259196771b277c7da226c32cee7039e9a1a5ee0456db83179c99f`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 62.6 MB (62619925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:050db9df21598fd2e9caf4e5e27b21f7940dab2aede1048c584ddda75d757fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db910e083faff089d90e623e3313f958bb72c026b8668267f260bae8623539ae`

```dockerfile
```

-	Layers:
	-	`sha256:84c6ffe7bf01eeb93a53146b662fc5c68058377d02b874c637ec16f98ee0e86a`  
		Last Modified: Tue, 25 Feb 2025 14:21:38 GMT  
		Size: 7.6 MB (7601299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83b91b0c7baa2aee20b237842b224a4a37ef33e33c7d34c11c522684efe0e9e`  
		Last Modified: Tue, 25 Feb 2025 14:21:38 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7239ed1c0cad237381738d496e98ade027fcce8ccb4c78bf9e5983a6442b05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142268923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2202c756b07b2672bd0306a805ccb34561601f77322bf561d99bdf1c337825`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4febb367456c7cd84b8043b3b3b3c93073aa9439fb54961fd46a9370758fe523`  
		Last Modified: Tue, 25 Feb 2025 01:33:49 GMT  
		Size: 47.9 MB (47858532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f249b42e8ca4f2ab0a926162c24ad19731e17ebec889633ecab6f0a37257460`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 26.9 MB (26882202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f03309824abf50aa8e904201f7f1a31ce290f54469b02ae3362c1a5c1d7b23`  
		Last Modified: Tue, 25 Feb 2025 11:56:14 GMT  
		Size: 67.5 MB (67528189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c72e2b6417dfa28512a340b185352d9ff07e1da9b4b85741fe3f1be934502e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6853bb24b562ba731ff11ff5ce1959c0aec391327aa7e9afbd8178a4c971dd7e`

```dockerfile
```

-	Layers:
	-	`sha256:7125150c9b210a65a1ed5b7b8f70ba72e317e443d776f8e554e8ba23e57fa802`  
		Last Modified: Tue, 25 Feb 2025 11:56:13 GMT  
		Size: 7.6 MB (7609090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4da627cdf587725b98e3e62d311c39e3c2da4b98b8819fb6610b5bd5b786ff2`  
		Last Modified: Tue, 25 Feb 2025 11:56:12 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7eb53031babd7fe1be6f99c85ad6011ddc763e90784cf2336f24c392d260cf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145262617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504cac4029ea96b97903fc04aebed70d1f39de4cdccc94b5bee4526f159c496b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f35c21acae2ef6b77873a46c174f1da0b28fbc4ea787b7f5bb3bd79c145883f`  
		Last Modified: Mon, 17 Mar 2025 22:18:02 GMT  
		Size: 48.8 MB (48831362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417ac61f214f6f239ee6ce6ccf4e9a29aead09dd8338aeca7ca8645adc7a0d3`  
		Last Modified: Mon, 17 Mar 2025 23:33:10 GMT  
		Size: 27.4 MB (27380417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d4e842f60fe8bed8af22c7d26bd8c640142408d7c59da73f8a94bc3c79992`  
		Last Modified: Tue, 18 Mar 2025 00:19:28 GMT  
		Size: 69.1 MB (69050838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed176c73e43ae031741d5307139f6f3edd7fe72358b0314111ee26d76582d5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7576134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4984e00b5f77503b242567b0a2254f59d18b5ccf080c1d28eb279edc6d7a39e`

```dockerfile
```

-	Layers:
	-	`sha256:e0c346fbec4d5622463fe88fb740816fd92165ccfe37d2ebe63ae1edc439b515`  
		Last Modified: Tue, 18 Mar 2025 00:19:25 GMT  
		Size: 7.6 MB (7568842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109b8cb99d24293e63787c51171d48d18a63f0255d31a0e835c226fdbc8abbd`  
		Last Modified: Tue, 18 Mar 2025 00:19:25 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:edbea362dd93e91cca5dd14b3ec7442bc7ae4c915ac18f2952a67c9184eb8940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fd5a7dc7e0f7f44463ef6b49ee46ed28ad37304fa952a7a91a2f758e1a55c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3018c8b96b9ba22f17940c42dddfbfef3058b787c07b7ccd94c52adb65aa552`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 47.7 MB (47684440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568a834d28f352d6c862c921a5a1525795a3ba966e684f287dc047fc5a62e6a`  
		Last Modified: Tue, 25 Feb 2025 20:40:18 GMT  
		Size: 27.5 MB (27466813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30dd389c4f7f75e0238dc8b5aaa6b88b1024d42ca2aa910e605d4197c6c892`  
		Last Modified: Wed, 26 Feb 2025 02:28:14 GMT  
		Size: 66.7 MB (66667275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c9fc52b92269c7d7b7aa24a07de06b692927261926512f6522fbb31a6192e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db05ff5f9d0f8862b98d1c01e2f7a7920741cf817d558d9bb98f6810c074b7a`

```dockerfile
```

-	Layers:
	-	`sha256:7ff109c6257be225cbb0af031db400e94cdb4d025f384a6017e2274ad5cc07ba`  
		Last Modified: Wed, 26 Feb 2025 02:28:07 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:489cbcc42cbb74dd81fe59bdefc2602ab482ea86e21e5ee82863081dcc9cba7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152997745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeab6381330afc1eaa6f8cf0c2f305a358c9ecae237dea7eb733b928c4392ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7bb81cdfac8e52fedda82eb71511b491bce0161320904fa9a6cf3542f360d`  
		Last Modified: Tue, 25 Feb 2025 08:22:16 GMT  
		Size: 72.8 MB (72849870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a0c5ea61bf72445ad603e3f0a919815f04bbf1ec098b1f75a6eae3e7b070b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3410f9541cb3d4948c7c851214e8ed536aa73ea920d4dce4c3e2d20932da42c`

```dockerfile
```

-	Layers:
	-	`sha256:3e79957f795f20fea9bad86264e2f07607f6ac2084ef23e267a1a58f366487dc`  
		Last Modified: Tue, 25 Feb 2025 08:22:14 GMT  
		Size: 7.6 MB (7613978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0091e9531de0f98ba4de3037729168d47136afa5c1cfeffb876dfa25074b25e0`  
		Last Modified: Tue, 25 Feb 2025 08:22:13 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c61c3dc39c2e52c72daf8ccd6c69a419c348681f81fe4cb8db8060e021d253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144614686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7896e9fabef8e8423d811aa137e1a24768d59f8329bd02dc2dd5d6de3075ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab0460cfb129d20515573ff27552b94c41a5822739be2d7bf548df5315225ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:35 GMT  
		Size: 47.5 MB (47508261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec199ac309750ebc4bdf20cce23eb64ef847d0a7c63d2075c1e80b9a8017dc`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 28.6 MB (28608136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971e21f8d766abab097575a50fb382c4f9461b5b1c49e9167693254a56cb32e`  
		Last Modified: Tue, 25 Feb 2025 07:19:01 GMT  
		Size: 68.5 MB (68498289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a46a938aa3e1e5c92281b102bed60eb977f596d1b1548f69b6e8fae05cab0e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7615201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd142dd896a56df52a2a52331c58cf7b48c3d93c4c81fbd783a8261578ef2e6b`

```dockerfile
```

-	Layers:
	-	`sha256:579c8c66ee9897cfabbeb5e9f0273feed6544126fbdffb981e284f684a5428a6`  
		Last Modified: Tue, 25 Feb 2025 07:18:59 GMT  
		Size: 7.6 MB (7607888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b6b2cbd496fc93fd247a1f9cfdeb05aa13c82157db1d5ccb3f19dfac78cc87`  
		Last Modified: Tue, 25 Feb 2025 07:18:58 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json
