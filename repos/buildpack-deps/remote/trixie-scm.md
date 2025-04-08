## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:4655c1124086e5ce533b77f19b63e0f22d33c1ca971992e272effd3f582ad274
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
$ docker pull buildpack-deps@sha256:b550bb1d31637bd3bdb80630d930ab7fa3d512ee68d06e2b34507f965abd37af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141123992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555c8dd85725f67564f77b275d8a3fc2e7ed9369872a43a75b073b9dc191d253`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b43386f4a8eea1a35e7c4f34a0bb12426fd9b88216af22d7c3ee489419eb1bab`  
		Last Modified: Tue, 08 Apr 2025 00:23:13 GMT  
		Size: 47.5 MB (47545414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf061a9daba97c5d47244462ed42ef128857bde7ddf55699ef7e9fdc7b5705bb`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 26.3 MB (26341855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8361b4078dfed2d0b312e243d8a8dda81b0432bf8ba1990bef58417d90eec6`  
		Last Modified: Tue, 08 Apr 2025 02:14:25 GMT  
		Size: 67.2 MB (67236723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65c1eb93cec0b1288827aa5409d7cb36d2f81bd2e03ea35bd4884c96498a9806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7585725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3384f240f86c9b9b5f6c57b1d907fc5a89310175bd6597c52f61bfc44292d38`

```dockerfile
```

-	Layers:
	-	`sha256:882f0c1f8079e3d7ff8d018b64ea8232d1978381a7db4ce0b7278f55b27c4b71`  
		Last Modified: Tue, 08 Apr 2025 02:14:24 GMT  
		Size: 7.6 MB (7578411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def5c0cfb8485548290eaaa6af77d6dae0228288d28e345b7c3dff4e07fc2950`  
		Last Modified: Tue, 08 Apr 2025 02:14:24 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f70301e9d6d766d5e3c2a66b235913218074b5a2644120b7dba6bc6fe9a379f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135729959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b45a53c7c545c41e03ed78cc47f6d2a09d386e8d331db3ec77aeb0aa662521`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec645b8b1764e458ae4d21700842e441d914fd80d6e0135fa393952e129298fd`  
		Last Modified: Tue, 08 Apr 2025 00:25:30 GMT  
		Size: 45.8 MB (45786687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9068871a08a0535e32e79d1a45670b225b99f46bbc4e55433b3bc2d040fea9`  
		Last Modified: Tue, 08 Apr 2025 05:13:28 GMT  
		Size: 25.0 MB (25013942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8929ef57738cef401ed1f8ab43e4013b674116ce7a1c298b5e5cdf5147046731`  
		Last Modified: Tue, 08 Apr 2025 08:39:49 GMT  
		Size: 64.9 MB (64929330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54b1135c459db2e28bcb08861f957b3e06feda4fbe93b1b9967c16ac82916a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7592094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811effbf5b63a29215ee28a087098dc5aa22e46cdad90c68c418d8d06a7ae2de`

```dockerfile
```

-	Layers:
	-	`sha256:3e1dbaaed6d2d727b29be281de0082f54d3eef6e1a43c4c7efce93071e1c9750`  
		Last Modified: Tue, 08 Apr 2025 08:39:47 GMT  
		Size: 7.6 MB (7584720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b38020d05463f0b98f3c91511bd573557c52dc56cf7a4c3387d72f6e6865bf`  
		Last Modified: Tue, 08 Apr 2025 08:39:46 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4ac891368c43dd195f9fb8ab5de5ec16d6e881855305ea3fff7943687f40e630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130607740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b09b9f84bb75491212d3945744d4841682ef429534b89cd7ca46dabdee52d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f935b3012df284a962222bcccf691a593747f69aa524b90eccdcf9bed048a7f`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 44.0 MB (43962830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705c4ef1fc9cf5c68338bdc47ec99f95384a22547d22ce9113fa1a4477154`  
		Last Modified: Tue, 08 Apr 2025 07:39:55 GMT  
		Size: 24.2 MB (24201775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9372173581cf51eee4c98494ac2b0977a2019e7d1175018467ee54556552146`  
		Last Modified: Tue, 08 Apr 2025 17:32:38 GMT  
		Size: 62.4 MB (62443135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4565ad9b7070f810010b43ecb31e74b0ed6663c7069fdf2e17d8bdfdb79a25a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7585638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a96541ef585966d927cf55ed51303a0e575ee2d6b8846e479c527009608b7`

```dockerfile
```

-	Layers:
	-	`sha256:dba3aa10b1b48408a16bc6962bef1ff7f25172bc73edf6db2d72f308b8d09c2d`  
		Last Modified: Tue, 08 Apr 2025 17:32:37 GMT  
		Size: 7.6 MB (7578264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d0e177b27c9fd6ab089338d618af046ae9ccfc1781f0c76a115769f2494cbd`  
		Last Modified: Tue, 08 Apr 2025 17:32:36 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe4a5e7bd46833ab459cfdc03f0eacfadaa8df93011e6a601b66be0caa11b784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140892958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac10438ec4afedc3a3db1b2f307698a2896201c58ab03d23f20cb54e550ccbfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60dbfae895846be1589b057802d5cd4dd276320555a3dce75612dc628209cb7e`  
		Last Modified: Tue, 08 Apr 2025 00:25:57 GMT  
		Size: 47.9 MB (47922433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7cce4b3d3d4958fcc2ffe1fbbf0181efd0f5febf1b3b140f3c5fb190e3e83`  
		Last Modified: Tue, 08 Apr 2025 06:04:42 GMT  
		Size: 25.7 MB (25728139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bcad993240040602e9e9d51c79d2c2f69a2ce32db81787fed4ac65abcc1c07`  
		Last Modified: Tue, 08 Apr 2025 12:20:12 GMT  
		Size: 67.2 MB (67242386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:67baea24716421b277affc099e6731ac7c16ba60c9713147189d4b3285ee2eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586acb64f2b3db1f5a83816fe5b519d3a69ee03afff433faad291ccea8855f8b`

```dockerfile
```

-	Layers:
	-	`sha256:6fde004f1d8240c28b9a859da3f8dcd616bf0eebece31daea980ba9d53d7ed07`  
		Last Modified: Tue, 08 Apr 2025 12:20:10 GMT  
		Size: 7.6 MB (7586073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b567220b75d1d5dcb3ee5fe2fc311ac3fe72c05e7889befb395281a69e4ae350`  
		Last Modified: Tue, 08 Apr 2025 12:20:10 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b661674bae72c856e75bf76c0dcfcea5862aaafcb53b7f96870db8266b1be8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145483546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61c3ab6a122f7c756aafa5751b3d1ef50a2cef33f46675ef4eff20fbd1ece71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:091329a1d6a6197a5d3e206472c088a0858ef7008c0ef0caa690ee6550acc80d`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 48.9 MB (48867484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fe46607c901c693e43f5e041d9582f12c310a5a19737459269da4c901faa70`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 27.5 MB (27452280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcbd919650c8b320058909af3123af41da829ccab581f2651d0f6c59ad671d6`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 69.2 MB (69163782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b53271c5ed7c1f44cc57a9c9e0055e22f4bab17fb6276f70ab5c5f14727af14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7581130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd71d6d84646ba7f9aee878b3c54db7cbc90c5e485a91ea21e0f1966951f338`

```dockerfile
```

-	Layers:
	-	`sha256:40ad0eb385bf0846b4e94bb33a624c49ca17e61ea1319c279a0baa405084fa2a`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 7.6 MB (7573838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad769b3fc01147faa253b9d81a065c59da9497621a223b6380e9e41e4b7f5d1`  
		Last Modified: Tue, 08 Apr 2025 02:13:55 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a1e2266f2570d7ed2fa9f31262c3074a017df04cbc2a0f8b4d02d2216d9c5f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140248221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7cd55e976c899654ed633c41e3fc57c54b779399b150f250aeedd8bf38bd91`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:46069a6fb0408c39827d84c4f957cdacbea0859425bc5cee1431cc570428f262`  
		Last Modified: Mon, 17 Mar 2025 22:19:48 GMT  
		Size: 47.7 MB (47726922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024e8bce62fef1bb0a0244ed9a2bd73704dfdd7237b2039638682f562d4721e`  
		Last Modified: Tue, 18 Mar 2025 16:27:50 GMT  
		Size: 26.3 MB (26278793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52953f47d605c459697759af84e7c1a91c6045ad23c5d6ccb67b71684026bb6f`  
		Last Modified: Wed, 19 Mar 2025 05:44:52 GMT  
		Size: 66.2 MB (66242506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22c8a444f5f03c4e8e3a4b6610ff9d15712896b1170b2d5004bfd71343de782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19700786eb2a4dab64fb77fcdce5e8d0a2291b14bb020cd1031d719e8a082e66`

```dockerfile
```

-	Layers:
	-	`sha256:1d8f1c400cb7481a9974389e0cf7faa203dcbb97f603f4055b0e70f92b3e8105`  
		Last Modified: Wed, 19 Mar 2025 05:44:46 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c689d9d795ae3ee0a31dc0275cfce2441b1ed131a2ecabbdf2cb96dd1bed34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151568308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5967edd461e25212aa6ef1e7c1e4569ef0e1ad5e2697c7ea7c6b372479a1c59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2152bfaf5665d7c627f661d81f1ebb038ec9b798a3becef3f95f6ec6dfa2adf5`  
		Last Modified: Tue, 08 Apr 2025 00:27:27 GMT  
		Size: 51.2 MB (51205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0924c3716841f5effee584d0edc58283639e6ed70d2000758424dcc55e8232c`  
		Last Modified: Tue, 08 Apr 2025 04:32:21 GMT  
		Size: 27.8 MB (27841786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd195c05796e75d6c49a1674778ee5cf1851af8875fdfe4f94f09464edecba`  
		Last Modified: Tue, 08 Apr 2025 08:41:06 GMT  
		Size: 72.5 MB (72521437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c9e584fd0fa8c6a76dc5a0fc19ced9e9de61138e1df18693c49b8d1699b4531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf8869e994deefaac90dc9f615cf72048324f8ea957d6755815ac4aa624a4b`

```dockerfile
```

-	Layers:
	-	`sha256:2fc332dda7c0306e039174358312798f0d3ea2574a0194c274df8b412d366663`  
		Last Modified: Tue, 08 Apr 2025 08:41:04 GMT  
		Size: 7.6 MB (7590903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad88d6c17a3b9c6d106a7e7f20cbf15b4c0be571935a0b1d9cc5d49cc314ab5`  
		Last Modified: Tue, 08 Apr 2025 08:41:03 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6afcf371a78005bb5ef196bfdff439422c5bfccddaf2000e2f7ef3bc7c7064f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143368004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6db8263c7996f52ffd0e4749f2c763439b60bdab70e8774b364066eb34c6a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:19a5a2e5eb505d0c1814e6d65469ecbbf0abf7cbe214ddd85cb24c5fb088dc02`  
		Last Modified: Tue, 08 Apr 2025 00:27:13 GMT  
		Size: 47.6 MB (47577872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a838b52d3c41c71c15b487ddc0ce4cada3e3fb6a44e40511f7176fd1633521`  
		Last Modified: Tue, 08 Apr 2025 03:45:39 GMT  
		Size: 27.6 MB (27569332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c84145d0b040e4691b868f5a57cc79bd3be75960c21092b456873daf06064e`  
		Last Modified: Tue, 08 Apr 2025 06:54:37 GMT  
		Size: 68.2 MB (68220800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:150f70f03ed192f9226d94bcdbd708b1ec678966fb6797a02403acfe4c3cf71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7592203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7648ed6e28808fcde7715456b1f8c62f25c1564e78a7ad80a45473c41ea4ef3f`

```dockerfile
```

-	Layers:
	-	`sha256:684f2f822f4774b73a2881fab1738550e1eac9fabaed50f540a4f59ae9a48ad7`  
		Last Modified: Tue, 08 Apr 2025 06:54:36 GMT  
		Size: 7.6 MB (7584889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a65a14b7eb02a6a34b49fabe641703700275a2ab45e6f5c99da6dbd78ee55`  
		Last Modified: Tue, 08 Apr 2025 06:54:36 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
