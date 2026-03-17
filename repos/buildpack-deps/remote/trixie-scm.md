## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:4d516f559f6b843e771843db30d25b9502b33d42a122c99d502e938af5f342a8
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8fa75851d950e798bf713fc586f9b8b2c81867e896cc158d65f6bb945b70033b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142700003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475fa5515c86efb1a506dfdcd396422c7f2a13c3e93f8270322ea374ad817af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f100349c860d9e43c43477b657a8bbd2118dadde8cce6ea7b7dd0d464943ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a43e52bc30aeff029e5ab8171529537f206bb3ca7421688784b025cd6915b8`

```dockerfile
```

-	Layers:
	-	`sha256:216d2bb16d3264697ab5c799ab4baa77adf62dfe6ba34315084fd8ade48707e8`  
		Last Modified: Mon, 16 Mar 2026 23:25:56 GMT  
		Size: 7.8 MB (7768211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81298b5cf03750a07deb482d2f2fe3937413ea3964825274332f3e3fe3c3f50a`  
		Last Modified: Mon, 16 Mar 2026 23:25:55 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f1105d568d4f508f1f434c4a637d156ea423d75c3cf1249b9011847deaae1ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137140874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79c83b4750b69074067c33157adf70dad0f0308b9873d44f69501a8d63b1c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a10acd8de7c2ea5feeb4bbe7b5147fdee10ce64d8ad5f6db26957ab6ab82a0`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 24.4 MB (24364203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043762e26fc507e51d741404184de0ffa48c048233f8091ab9a9f0a36a848703`  
		Last Modified: Tue, 17 Mar 2026 01:08:51 GMT  
		Size: 65.3 MB (65316059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53524971a04ce4896c2708c345f7e1d7b13192825fd86a12c49809d27a5a6e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa89be7c1e7134daf99f835692636833229c4d0a78b77eb418f3cada1540cc5`

```dockerfile
```

-	Layers:
	-	`sha256:dc2b643e9e92425cb38c93b1f5c619275f1ea8f726857e8d098f32e7af045f9f`  
		Last Modified: Tue, 17 Mar 2026 01:08:50 GMT  
		Size: 7.8 MB (7769249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc21b4a22f664b564d3615b461a6c307109b8e4b50b63ebda4120bfbc7325f9`  
		Last Modified: Tue, 17 Mar 2026 01:08:49 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c29884a12842bbf40a0f161d53711f19465dd35882f13a2dcbc345571dd81e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132083561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1654c3cae64bec4f63eabbe65b45db542134adafe30f7cd5b1e1a78adb7e3b52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:743dd6eade64d9b372335d09236f70aad7544f3483022e3ae85a1207edceeba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec908eadb640b0cf8b8c6704ff8c7e449b22114ca5d30e4fc6d4f3d306c361f1`

```dockerfile
```

-	Layers:
	-	`sha256:55db8356c37f4edf2401c4c9ff6f78a07b5bacad9d68681d8fed5144dd918415`  
		Last Modified: Tue, 17 Mar 2026 01:15:27 GMT  
		Size: 7.8 MB (7768718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c0d66e68f41ccfb3165414ab86dc753d6a6c4f12aee929d61a6a8a87ce9471`  
		Last Modified: Tue, 17 Mar 2026 01:15:26 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aa5d3b513466c24c78df06a736821ec25a5420925f55e08dc583fe8c237f495e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142273249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0cc0e2bb642e883b44319887dcb1a0903cf817f93a76c56f570c0b0d08e059`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cacc4315e9ede49677902ea5112bb65cbdc40246d7e0d5e4c701ca9b455485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9a4aed8143c4c4058c3f9c6e92e4c8a1767dd93b43f75325cb9158013a6b88`

```dockerfile
```

-	Layers:
	-	`sha256:6fc033ca8e2bf15c99648317b8554fe2d73cc951e7caac2f87129cd8dee10cf3`  
		Last Modified: Mon, 16 Mar 2026 23:30:58 GMT  
		Size: 7.8 MB (7775886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ec307835ba5ef67efb7a12422d99d916cfb90918a3920d7e752b6a05c1e182`  
		Last Modified: Mon, 16 Mar 2026 23:30:58 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d138ad8b4b3ff8b1b75c8a069e79031c3f6020e9f32badb8da6296005daef5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147397647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5e1917ef7d208dab1bcf0f8be86e0bf376d0c1b023156b54c32dd5b512e126`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fdf4fef02040e0be6707273b6ad7a68301962c7f54bcea4e0249619c98a88746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae613962dd03a5fcfd176d95fa8dfed2786ea28e17fe8cfc831dfd5804c0ca7`

```dockerfile
```

-	Layers:
	-	`sha256:1aa2d22eddae191876d89fe3010f10279a91c83c4d539b195422fe1642ba59ed`  
		Last Modified: Mon, 16 Mar 2026 23:42:20 GMT  
		Size: 7.8 MB (7764345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3652cd3b2ec6395daa9a5410c5a65e5f8cd25de50795c1fd4525324b25f65299`  
		Last Modified: Mon, 16 Mar 2026 23:42:19 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5f3998f8fe1cdc81525e0a04814a2ea96e8accaca7d7cff9ee7b1865a9fb4920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153165025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80adb4345f0e345df905733ba83be5af120a8b5e269043cb5ea7f150249952c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9636d9d3b5fbd7442148c521d9a6fcb4eff747b6d5a4fa8e55afa5a590ac08bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963b49b6e40a8bb018737e4436a8da9094aaf262d09eca35f0e34d4b8aaa6f2d`

```dockerfile
```

-	Layers:
	-	`sha256:539b0ecbdcda0f9eabcc104c7076b8812d4082053449b551914f5e07a182b6e4`  
		Last Modified: Tue, 17 Mar 2026 06:06:07 GMT  
		Size: 7.8 MB (7775336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdbaa20945c699203fbfb1e99a71ca957fc595dc85a260467c50697c33203dbc`  
		Last Modified: Tue, 17 Mar 2026 06:06:07 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0b90891e67a0ae5c9741a27d9cb38d496c0150dee9509ae48cbe210c952644f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139391128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0368adf4a211d51ccbfde501ba4790c597ee8201f9994fcbb803473f44f08407`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f13107c4da5dfb26999e015bc0a6ba56a7d7277ab422c18e50a0196ab4ba1b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c7ce93bfeda397cf9ab8bd8631b2e118c051386d2d1675a7442bb17f206ead`

```dockerfile
```

-	Layers:
	-	`sha256:6aa36d0aff359d76287eb9604b6f49ac7a30cd44b0808d54b904bbedf19189f9`  
		Last Modified: Sat, 28 Feb 2026 20:02:07 GMT  
		Size: 7.8 MB (7757975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cbbbe97afd462b6ad86611ab1f142d104f9ea9fffad69ed6bb83823de9e3511`  
		Last Modified: Sat, 28 Feb 2026 20:02:05 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cdcb322dcfbee0d9e38a8f8011e4c091e10ca184ae7544e8b2184e1957802559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144796410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969edff921d9d0084de3c8403248bc3e51c5aeac3c3feb2b2312bf0d94d552e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72a3fe3dd486af0c534e22724734a886b8c652e5b4bf6aa6e62cdaf79ce1dbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac60d44b325fcda011aafe466ff2d48b8a024cb0eac081800d33bfae1059629`

```dockerfile
```

-	Layers:
	-	`sha256:4e51ec1067b15647c7b8437f51573dc512c1b8b7c39080c835e90e5af4d431ef`  
		Last Modified: Tue, 17 Mar 2026 01:34:58 GMT  
		Size: 7.8 MB (7769124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e68a32b9d4c2ef5e7938f21cd0697b90713c508aa1c67fc3ecc380007270ce`  
		Last Modified: Tue, 17 Mar 2026 01:34:57 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
