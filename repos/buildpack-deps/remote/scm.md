## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:60e9b140ec467cb4f56902bd488233f0a14da7a537ff6d46d46993c1b2d03e6a
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a3ad5da8566863beb50f90f3c15694ddda7d88626be20c351f54fac6edac7d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142700219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38e225ca45f2512204278b0204883a2a1127ba8b31e816621c902c5bc3ef5e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:927a43c16a038260d0bada9cd06edfb2c3703acf7f72d851741ea98c29a2cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a27ef448fc956985a2207d4ecd334d404c56840466d782cc0c37d3588e174f`

```dockerfile
```

-	Layers:
	-	`sha256:ff6c54eb35b94cb57992c180e6ccf391d1370003cc30fcb71977b3a618ad8e22`  
		Last Modified: Tue, 07 Apr 2026 02:43:38 GMT  
		Size: 7.8 MB (7768211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e888f83801c3f7a7cb6295fd9af40f9ef8d47de035bfddfc63ad845b985d9f`  
		Last Modified: Tue, 07 Apr 2026 02:43:37 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:33eeae37b7407d6681ae07cc8944940b269a517d15c58e07f67eea2713ef9e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137141433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4458330fbcb8a6f3f3853776f12469d5a720f4c1a9c320a694498b90b1b26b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c635b73b8a91f67dcb5ba2db26dcc3f74099816e3c14bb345601bfa9d19e569`  
		Last Modified: Tue, 07 Apr 2026 02:46:09 GMT  
		Size: 24.4 MB (24364186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84775a808bc27f08b75800bf67edb5ac5e643d59d96e408a2ce3807f82ca1ee`  
		Last Modified: Tue, 07 Apr 2026 04:15:26 GMT  
		Size: 65.3 MB (65316355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d916616788be61bb3f24a417794262c968417ac8b7b0fa2596ff3cf89e6979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3bf44d5b213ed4bfc4972b1a486d2be9fbc084a8208a00b4eff62c1eae991a`

```dockerfile
```

-	Layers:
	-	`sha256:e578b6fd3439312015ce648481e4746e82f2ec4336b4a20aae282f0aa9aca89c`  
		Last Modified: Tue, 07 Apr 2026 04:15:24 GMT  
		Size: 7.8 MB (7769249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4a568b266f8ffde183a4a30f73857176320400974791107e6edfd92c48624b`  
		Last Modified: Tue, 07 Apr 2026 04:15:24 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d8dc2a525e220e926cdf3e85df006e42d714932c9406a960d00918782010db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132092674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f6b6162059e07e9991176ed12865c1c9a63a2d253cb849dd1c52a553679b77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868f799858ac0f14507e60a2ff0757894394681e874e60066914254664b5431`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 62.7 MB (62722704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8da39a3830c55f10489584f2194635f3a520109849830488d6c147879582030f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e9ae0105b17ac8488b448f5a11a8e5157e8f57623cdee94e36a5662482547b`

```dockerfile
```

-	Layers:
	-	`sha256:65ad02a833646a003c7b973a5a277bbd48cb93fa8962383d1f25fa7c24169a4b`  
		Last Modified: Tue, 07 Apr 2026 03:50:04 GMT  
		Size: 7.8 MB (7768718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d17cb2ea9b621d85d477a1a208ed217156c973fe31f87ce26216a2869d42b66`  
		Last Modified: Tue, 07 Apr 2026 03:50:03 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4965849bd2a20ae50681c7b088f8e8e5adf7321f29510ce11da58dab266321b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142280825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74de749170fab0664a4332dde7c6d976249bebe60375bf513560de45bddd96bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f990eca824ff493cf405f75d56e0c4c4fe0aafa6336a32a0730768007656a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8530a1e21e5a9c753ab65fd0447c9c7d43aa3a8ac20dae71daa67eff60f43115`

```dockerfile
```

-	Layers:
	-	`sha256:27256a533743cd799c92cbffd0dfdbeb15f6513eab1010d4af475b06f21f688c`  
		Last Modified: Tue, 07 Apr 2026 02:54:13 GMT  
		Size: 7.8 MB (7775886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9daa2e1d487a23b0733f18928567ec27ac036be9e05d82d5081f02613b1da915`  
		Last Modified: Tue, 07 Apr 2026 02:54:13 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:624d7ccad5782ec2fb8150f4d88e4b87436e6d17fd2c766d09776911f182fbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147397769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9221ace121fcd078a4a901a21cfacf8f437d77baa74bd0ee479e4aeff11f9d25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da593751d4ac5330362be2da2c6b0a17a5769b721979ff3214f729c53b720f`  
		Last Modified: Tue, 07 Apr 2026 02:41:41 GMT  
		Size: 69.8 MB (69795302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb34af5c0bf9ec5910df9997f0162e7667f80157f58717001d0db5b101b5ee64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83df99200c4afe7d030f41e1cf62f6c84bc08bb64a7ec84cf4bd7501086b7de`

```dockerfile
```

-	Layers:
	-	`sha256:b19643620f5704428d427b4e198eac315af59e3ee148358988825879cfa00377`  
		Last Modified: Tue, 07 Apr 2026 02:41:39 GMT  
		Size: 7.8 MB (7764345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b187dd5e54709c488b1e8a2420ec4ba1b86330b122b08fa0c7bcbe8a7be6be5a`  
		Last Modified: Tue, 07 Apr 2026 02:41:39 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bf7cc788651012a3444337354341092221642b943326518f02e5a26419dd56e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153166506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8babb85c18528d4146e4b5cc1a6070afded2b9999a888d99418ad8a8917338`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169353b9ab6307e2b065964fc878588895f32907dd884c905868bc86f58edd0`  
		Last Modified: Tue, 07 Apr 2026 09:55:34 GMT  
		Size: 73.0 MB (73033989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:359f6895030f521697388a4059609133e709af8ff6ec40ca3cfa39d9047d161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2990afcc579568222a51970f58c8751c077ce7bc4fa04fb7bef4e6e3d6af9522`

```dockerfile
```

-	Layers:
	-	`sha256:4c5463200b6741960ea0432fe8a6df3899e2f00d4bdd65a93563eaf37423d911`  
		Last Modified: Tue, 07 Apr 2026 09:55:33 GMT  
		Size: 7.8 MB (7775336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd7a13c838c7cfa6f747aca2bd1bcd978a8e27f471881e424847c542d4c441e`  
		Last Modified: Tue, 07 Apr 2026 09:55:32 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:eccfb123734ba577321022ea2c5750986010ccb0c170ca59053aab7df665f52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142574368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592a20bae16261cfca099ab1d165a593561497f5d5ffa23aa28760fb427a7250`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacec47fc648b6d60a98d7ff6fd4e23039ac63553f44613cd15e968e674616e6`  
		Last Modified: Sat, 11 Apr 2026 03:02:36 GMT  
		Size: 66.7 MB (66662977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88e92e6f6d98fc6b3c197fe3a400bb12b7de9571ae2d3e0033975c1cd5e0642e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724f7bb7552bcb36c9e52e478dc4c4b0537cab41970b8b63777ace7c7a56984`

```dockerfile
```

-	Layers:
	-	`sha256:ab418656e6f4278b21c7e8e1d365c13798ec14538273bdac46ec4ba43dc7b8a4`  
		Last Modified: Sat, 11 Apr 2026 03:02:27 GMT  
		Size: 7.8 MB (7758049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c130b63d3e6fa450895311d90b905055412dbf993d89d11dfc4c89ae96574d2c`  
		Last Modified: Sat, 11 Apr 2026 03:02:25 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:605bcb00b47c442f0c985fb0380e7fd89d28068d3901f541bbbf677b520102c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144795355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e583ba671ec14401cec1c84f64bc10e2cf5186a92a27f47dab1d7b06222341b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b42c01b5de7637ae2e011d2f9775f913b01f72b9797773d410bb0d8b437e3`  
		Last Modified: Tue, 07 Apr 2026 04:55:14 GMT  
		Size: 68.6 MB (68627207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8072fed7c1978d89c85afe002e50569d981518707b796b9fe98d5e1349d55d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a0969c2f8ce6b46bae95146516d67ca15685987e497a419105bd28c01ea67`

```dockerfile
```

-	Layers:
	-	`sha256:7cf663da3be41b58d4a5a08fe67eea479be9d23b30193821c8711eee547d656f`  
		Last Modified: Tue, 07 Apr 2026 04:55:13 GMT  
		Size: 7.8 MB (7769124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8a1fd236861e576533896f379f2a0516963813c2e0afc528ca192737c95a24`  
		Last Modified: Tue, 07 Apr 2026 04:55:13 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
