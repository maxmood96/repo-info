## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:ed9b01fbcc4e79ea3f6f1d8e81cf2d872e1850f04dfdbac458ee220ce578e8c6
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
$ docker pull buildpack-deps@sha256:aba3d709e5b90eaae9ce2b90fccf721e9b69e2f08fc6d7effbe6eceecbb040d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136927850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319a1b8fcd8d73b997545ce17e1516f1e2b3938ebc7b0c126c9dcbf4dc5819aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:221af5a22ec8cfbdc61fe0fc6aa885e9645ef4099ee116c9890953871974d320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace6848052c73ee7dcbfc6a60da115dd1566244f5df40d49878150ee90e7f1c0`

```dockerfile
```

-	Layers:
	-	`sha256:b6f8c6b44fa00a4325e715216072a034a8322932f44a6086e4a0786e71f36094`  
		Last Modified: Wed, 22 Apr 2026 05:12:26 GMT  
		Size: 8.0 MB (7966048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e991847dbdd8cc0b3a444949025554cf570b7f016d788f4b264880131f3fc04f`  
		Last Modified: Wed, 22 Apr 2026 05:12:26 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:02066cb7d99b90a7f0a0391f12fb8f13aa18ad5e611d130fefc83a5f8a6b9d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130744419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6277d3155eceb113f326ca5243e7a9680e73d7c7cf430a2e50ecce643c2a718`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:45:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c4564d3f444801f4c4ab3e01fd62e7dd3bd91054769ac22888b9bef61823a830`  
		Last Modified: Tue, 07 Apr 2026 00:10:20 GMT  
		Size: 46.0 MB (46021666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccdf893742febb0a81a70ae87b43e8f63165210f89f5c68b785189d45a2427a`  
		Last Modified: Tue, 07 Apr 2026 02:45:21 GMT  
		Size: 22.7 MB (22713856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7e146b82d88d31971dadf8a152fd100ad2ae38243df9944ef1e53be23ab7be`  
		Last Modified: Tue, 07 Apr 2026 04:15:12 GMT  
		Size: 62.0 MB (62008897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e67bbd5eb741ee420d7caf84efe9cfd9080b98b5eb00a9f6ef0f78b71ebaab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2bba69024294e12e8d00f147644a78a575e79160d6c4415bd75eb98e70f377`

```dockerfile
```

-	Layers:
	-	`sha256:6b9f32130c0e64a31b4839555be0316a8c7a2903668f2b203f1fbefc08998f80`  
		Last Modified: Tue, 07 Apr 2026 04:15:10 GMT  
		Size: 8.0 MB (7967906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6700c2af9df2c7a234ebfbedb26669694bb764e00a6289025f9c7a3f9e3707`  
		Last Modified: Tue, 07 Apr 2026 04:15:10 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8f6cfc1c602fa1e8f20d77f34b114602dc6cd6fcaeb37749a84090ef551e116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125806855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ac7b44d1e0c3699b40031db3351ca5ea69ffa63e802ddad62886c2c48abf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3960cd47ab70e092f1d1162d4a33a761e2cfa64e09c3ca3118416ced1e6f99de`  
		Last Modified: Wed, 22 Apr 2026 03:52:25 GMT  
		Size: 59.7 MB (59652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b224c68bd5057703d16683a96721c28360451587c07da5e0a80e0036e202903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab83068c4dbb132beb3dbae71f6374035b19fc95744e1b4866695048f785cda`

```dockerfile
```

-	Layers:
	-	`sha256:61aee257069413b841bef4830664b114a7e96702272fea04e91e0e64bee8566e`  
		Last Modified: Wed, 22 Apr 2026 03:52:24 GMT  
		Size: 8.0 MB (7967325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadb656e3400e666e7d2002ffa9f91c71a5ae17d05017ff19cc3eea4e54dd08d`  
		Last Modified: Wed, 22 Apr 2026 03:52:23 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bf22d87968520a1992114e033d52c04cba182eaa594ac73b9f051fe3ef5f1d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136462100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2cee1dea855eb67721b2dad6b7522ccea680add4cb1a0988a6a4517e22a8db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d679fcc31bb1e0d87255a5593c06745d865cf14d35402adb5d41a0a6857aede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f820e63a4eaab23d5ea33831435e1f1bec1bf50d5b3e719805c523ca5f628caa`

```dockerfile
```

-	Layers:
	-	`sha256:244afebc65d33d92fff34a3a29671286b9ae60c3ea470828165946a7fd34ac22`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 8.0 MB (7972441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27872742b9dec3adecf351bf4802467c348eebca4c05f212a243d0dae9f9f93c`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:01247dbc57fe28686043da6adb89b40a20aafa4d01b8c2bc2c195ba7bb94437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140584339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80b5d3e00a461875700b62fc3f4facd6e7de7c0ce95ce1022b8c67996f71796`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fefd2d4d18c0e4a1f706c31af7edb1bb87765de90f366b612fc4f713dbbfa`  
		Last Modified: Tue, 07 Apr 2026 02:40:53 GMT  
		Size: 66.2 MB (66234451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:321ca0988914e8a48dfc0025c07b985943811297dc89ca61a9e5fc510aec5e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819f57dee84bb309b84df295371bc3f27cf5852b87f4652b3df6b47b0a17e09d`

```dockerfile
```

-	Layers:
	-	`sha256:8570101d0d9885e55bd8f09c9230fb93025ec937b4745cf807eddaf71e3d73fd`  
		Last Modified: Tue, 07 Apr 2026 02:40:52 GMT  
		Size: 8.0 MB (7962206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba04063bf9868d0b09779ff77764c3967a889963f8764306951660c7062adc5`  
		Last Modified: Tue, 07 Apr 2026 02:40:51 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:73b61e07215a42a847ec7407f96ca84b74b350d3e6792adc0e347dce2b46c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135707915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01ce3cdb32424d2af694072eec6901872e59ec88b888d8dcf5228ea45b0ca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e619bc61e501434dd27f89110c66abe62b87fe084d2dd79996da2c81d2db7845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62eb03865a3ba5d604dab939e5da79123bbb7f3252f2efb99033e650760c86ac`

```dockerfile
```

-	Layers:
	-	`sha256:3b4c25d28e0a67edfdedd2916913199c314710196e1321eb9860fd2d06dc106e`  
		Last Modified: Tue, 07 Apr 2026 20:28:11 GMT  
		Size: 7.1 KB (7142 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:067d9327bf477290c7e85ea509bf99313c5ef51b31a9c35ffde57e6d9a243afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147854637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa83747acf7d2771fdfcdb1ae7ef1f0e80d3794a484588b7ebf8397995caa1c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e22f4dfe747107725f0e5baf61b9831ca21287b9bebe46aea369c7b5afb49a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c29ac808248305aa66f74df5342836d0bd35b7993717cd13ba32b495e8b29d`

```dockerfile
```

-	Layers:
	-	`sha256:64c76f1b98788b5a4027bef50a8d2589e9641dde9c045d061d8596b71ab85d3b`  
		Last Modified: Tue, 07 Apr 2026 09:51:23 GMT  
		Size: 8.0 MB (7973921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d8e6671ee917c21b319818392adf76ecf6227e248b5b3c1427af8e3408c485`  
		Last Modified: Tue, 07 Apr 2026 09:51:23 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:822ac8774a94e1812d48da668981b86e62266e9cdd0b31af8142ab69a2d6bccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134683077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a45ddcbcb43bdb082c1f494a538e791e371a78a019bb087149ffdf0bcc59e71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47976b1872c5d8fc1ceda4d073087f195be5506b083608f5c0a6767f6b55978a`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 24.0 MB (24033635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3377e46a7f95ad649f4e145572c4253ed3ebf1b9fa463b58c96cf8b20d651ac`  
		Last Modified: Tue, 07 Apr 2026 04:55:04 GMT  
		Size: 63.5 MB (63501358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c122201503879afd9fa1e4e15aa544d512495574225bf87eaef5531227960cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678246bb0ee568f398e4fd835fbe49851772dfe2700083a7ca0ae16e9f7ccb10`

```dockerfile
```

-	Layers:
	-	`sha256:5a8e980dcd4b15cfe740f3f6ddafa768caac54e3a201517b37402610976f0695`  
		Last Modified: Tue, 07 Apr 2026 04:55:02 GMT  
		Size: 8.0 MB (7962361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37376d764c9b06387abb332e896f3b966e19785cd463a4654b286dc5c907b348`  
		Last Modified: Tue, 07 Apr 2026 04:55:02 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
