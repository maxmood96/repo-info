## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:7ebf56145592aa0f9e24f0603416a9ffc7f2f8c7232785b2082ce4431908df81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:98ae8322e21402d9d1a47ae330578c281bedd95f82e7551694698c1c73d150b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140712020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff602ec12cae508a5eff7f955f1f3b4a7b0116e7f63fd95e3aede38e2531f3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f7f8c9fe198f76ea4d557014b74867442af6b19728ed19e19b5db24d2c9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7673901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9655e2d30b820946d8a9271aebee6149dad6dd472e02bd0dd2490a28bc82a1`

```dockerfile
```

-	Layers:
	-	`sha256:9b8dcc9e196bdf56ae35756553a098b57ee3322218cfe81f94b8d219dffaf1cf`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7666604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb4b8ce456f309d5ac4f45927a3297061e4c2e8acfb4c80126d9bf3ee145d25`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2966584a59d9e0b9d32e6387a215e424e5bc2afa5c60c678e1a02c0fe9157edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133449300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d6416fa362396520065273d8b095ca52c840c3f07b1a58aff7022f82309846`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:774970a968d4bd940468709784d0674f8143d9516348b45292c1efa99c37307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1bbb775be08af72d3f2b911e5d67dc53477881a4678e428606938e9329a5f1`

```dockerfile
```

-	Layers:
	-	`sha256:be2af54aca073400cedd5c0c72179622b7d427625d2e6476881c2fd812ffaa14`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.7 MB (7666879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b328f7f3ac3c501a7f6ae35a51e43d86de914bbc0bad3222005f311fcd396127`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49cc8b09571de3482143acfe7100f15f8d3a156ff6bea401ccb6279e58a7fead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128289386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d80ca6ceef7a2fb53ff08ce96ba5c1f8d2bada4782470ee227e2c258631e63`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b86dacd9090665be47b5966a673c201e9be17e12af3a6b155bc5749678a52`  
		Last Modified: Wed, 13 Nov 2024 07:40:03 GMT  
		Size: 61.6 MB (61581104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db36f314f12e690b6742c569de4a89729ea3e94e60224e1219d288df46355abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86ff9d0f3ddb306fdd03d1347b681887a9eb99cde3335aab0b077a1b74c390`

```dockerfile
```

-	Layers:
	-	`sha256:a0b51d6858aa210986bb5e9f3dcc57e6a24f20cb265918e257765d594eb56d2a`  
		Last Modified: Wed, 13 Nov 2024 07:40:01 GMT  
		Size: 7.6 MB (7614159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df37db634d787eb3c7ef7dd112ef7905a94e7a0e272ffc18fc80ff7b9b41cda1`  
		Last Modified: Wed, 13 Nov 2024 07:40:00 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ba6f42ba7aefae054d5f3f1bb2c078cc0b42154bf67985259ea51890f16e92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140512658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4bc14651d67b3d787ab2c20f60a20cd4624ada311d68df39bb40b296c58f4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa757aa7912e5aa5e678a45ae35e15003eb74a602d8da40aa9ffaf5e93f5a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ff85394930bde7b388d9d6c1cf7bab862637d3629f3cdb3e6953a2fced1b40`

```dockerfile
```

-	Layers:
	-	`sha256:035677f5fb6f054407dcea7a584fe83af8c3343ee7a4ee69e62dfb3955679e5b`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.7 MB (7677008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdd037048e81b72bd044d348d4ce9bb4e7a97b2f9ee3680fd1ae6a27f7622c9`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28aa3b92afdeceb776855973c3b211c28230c89a81b458bb7e67b11d8cefe2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144558793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc5aee69b53785c60a0927a7b5c28ef293efdde6e25767537d489ed2d6e1d2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1de5a48dfe09b9f75e84d47faa561d68418835bb76363623eb981f370a7eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91810c997ab4ca1105aac3782040f194980cc9236686d98672c7a9c1b2c8411`

```dockerfile
```

-	Layers:
	-	`sha256:c5867b09adbc4524a9ca98728702a0177022b1afc0e4e8385d9a61636c8345ae`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7661345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0640817c4ab08d0cfc6d0fb5beaa13797d1e7a88cd7885d6a37b80373ce2b256`  
		Last Modified: Tue, 03 Dec 2024 03:17:06 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:433ef6755fd51ee668442ab78797afaefe11b5c906a568bfdd7a237d0bf2585d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138580415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa27cd16bd38d59fe05330b5e6a7515ce6692065b0462890843f49aacaad3ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aac7a2dcb6a719b792ac16c19c2652ad08047befbc851b6ae687255f6838b0`  
		Last Modified: Wed, 13 Nov 2024 02:06:14 GMT  
		Size: 65.4 MB (65354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a12220edb3617bcb4abe259389b0324a33c89d2862e9e447f136530f0e9d5086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2e3fbb2de24c02ca4dfddd469bc058dff82a8fbd1c43904ca6aba92fe3e42`

```dockerfile
```

-	Layers:
	-	`sha256:aa271072ee92dab888071bdce24b99dec92fe97e837f30e2da96cc1793727ac9`  
		Last Modified: Wed, 13 Nov 2024 02:06:07 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59a6796beeb3b9d0867665f4811ee1eee275a710e6a5a458dcc6fb93f8e48524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151265275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd8aab6398f04086341d332deb43da5a6cd1a16ef1b5a5e6dc0a987ef76111`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5af9d705848c2dce3bc462b3b76df9b1b1d306e6bd09c2e26bd22bfc3f0c9876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651af8b104ea346af37805901de2cc5ba97cf50ebaaa790cf0de9c570f5583f`

```dockerfile
```

-	Layers:
	-	`sha256:1db2caa964222e7b334c9d443db179aa27f6a7916d2932972cac65ad9c1e5d72`  
		Last Modified: Tue, 03 Dec 2024 09:43:19 GMT  
		Size: 7.7 MB (7673155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b523a122ad81c64df21fce3272cb02fca3d3a9206244cbe6d869788cadee4d0`  
		Last Modified: Tue, 03 Dec 2024 09:43:18 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fc674a43ff201f8797f66dd82257b4196d80d7c095fc868cbe749cb36beeda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17059d9a1dcc6bf58ee32ba614a1fcbe226f8043520b842b184d3a9c6f28ff4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbd26b4002d80a7a7d2202c479c7daee401e8a0b0b2bc1e4e4d3dff743cc317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7664095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79590c6ba7424ad6bb084619f4ed4331d5e05aaad65648779da965666f5b52e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee9a4121ef32c4ac3a622baed8c3121fa68a4974fd0e3a4c5b2491d3285a4d59`  
		Last Modified: Tue, 03 Dec 2024 06:41:52 GMT  
		Size: 7.7 MB (7656766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d83211651559187f1abcb4d829c94f914b0ee443046ecda9f19c4daaef0296`  
		Last Modified: Tue, 03 Dec 2024 06:41:50 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a6e7b7995a1caf452b3d1632d89a67fd503bce71d349a2d66b6b3489271ff30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142907547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e646e8bc9897fc238aa02a1d8ac855f8561e8a87d9bf6b3034ff59ef5aafae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62bdb3d02e3a0d3e18eeefd51b090d298257bf08d95c74c779af75c028b32601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7679482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7371548547570d681cba1e2bec0c6958cf1f1b85b053244a30643706e814711`

```dockerfile
```

-	Layers:
	-	`sha256:baf8d91bd601ab293980e1fbe3335dc904de9a3306b89908c5075675c6676f3e`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.7 MB (7672185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9961d929cf0d31cbf6d32963cbe3e25aedaa9b59f3f87385c96f28d64519dbf`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
