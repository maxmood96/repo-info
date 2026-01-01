## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:74384d01cc8d74de7e92499776a926145a64d22b848c9cb600ec61647a37ac49
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
$ docker pull buildpack-deps@sha256:63f8cc622484d4919c8efa1a709873c3a4b7efa45c49397b808982c998314b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b00b7c6f2392505f8719a98ff2f6ef8bd616ae75ef7033bfcb8442dcccb6a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:021dadb2adf7f142f52a3b87e9527c6ae5410bbfc99709f18919770f7bcce486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12102b232575087daec3456b81415b1010576ac0e45300cd0a5421d63f6121a8`

```dockerfile
```

-	Layers:
	-	`sha256:e6766b0f7138d64adf4ff5cb6023cbcf5e681d5c7c60f094212fbdcf9052261a`  
		Last Modified: Tue, 30 Dec 2025 04:25:42 GMT  
		Size: 7.8 MB (7767098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facd45e8947218a737261140ebddca5599bdc71412a292dae28b67ce6a7c77b5`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:00f4339ae846dc8d72349295bf5ebe475fe5bd855a7ba521bda76aea8d09c870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137112408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fb1df76de89cd9d8c3f44a56de61ddda6148e31fb84ffc9bc01a46dcb63214`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a515687a5a3da2827aa6a3b8071d1f515ed0d5cba1dbfad9af02797c060c18`  
		Last Modified: Tue, 30 Dec 2025 01:51:10 GMT  
		Size: 65.3 MB (65317909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:57d68bcb77bbe9f10bdd6d8bb08f52cb153996c2af0d30138374fc84ca2c0add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e53e0f95ee2532231410d1abd27bb07089be41314f4d7fc54e208fecdad9892`

```dockerfile
```

-	Layers:
	-	`sha256:95665755aba303d45b66107b450547aef680d875aa0739a2b4889e4018b5f828`  
		Last Modified: Tue, 30 Dec 2025 02:21:54 GMT  
		Size: 7.8 MB (7768136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e726e8b358215e37277138c929245d328fab46fcba9a13cbc3d63c54f57ac2a0`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9173e66cc789c7d22b9a1203b233727450f7816db16bb0118a25aa55d18a0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4635ff2f59f4de314c6b4d7614ca540da6c28b13053ddc26f4766e6b624797`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce4edf7172b6f99521524b3967911df3792316257e84ddc2f1282a3ed31e94df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3943b7627c8906d99e3b3e003f021d91de0e15b2839154e134d941d0ff3d9b`

```dockerfile
```

-	Layers:
	-	`sha256:bd8cb70fc0a8410f3677b42aa093100885acc69ff04cb1a7b2d191e3016fa37f`  
		Last Modified: Tue, 30 Dec 2025 03:27:58 GMT  
		Size: 7.8 MB (7767605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69ef4cf4ac1e60509823cc3b831649961c8444c37bedfce99218c60b267d492`  
		Last Modified: Tue, 30 Dec 2025 03:27:58 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8119ab350578420190116327ce38e9226fed560a819b506976d4916c4361e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e276557c308bf61abcfc36346ee60d4addef22f06f34c33aee4f54a5759ab9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07bd2f4efc761637e2a36f2786027888067b46db13bb374246ba54834b251371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937eb4e9195af3fc59a307e4faaba355a986702a5b78ec703e955c1363cc9a52`

```dockerfile
```

-	Layers:
	-	`sha256:239e86fac866c26929a9222835aea5e9d8d3f3cb912d715f30daeb41398f01ee`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ad4db7e7e58aba8a75a580c9daff8586372d78e7d220f430868c4128b3f265`  
		Last Modified: Tue, 30 Dec 2025 04:25:44 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f2b6283001cd4d5d581129ece1ba4da31e84f747dde66300eb1c2b93aa7706d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147372851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7fde892580f2257f3ce88107d9793fdc6fa7c2e32cced7a52a6a7cae5d717b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db57e4717828025dd65b68e8f5180e596cc4b38ee18d81541377db5e13f7ff99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66d0796a8dd250a8f4f572c99ddbba377c7976ba390790b485e49c22e2703b8`

```dockerfile
```

-	Layers:
	-	`sha256:9217446bb82851e3a4c4fbf55177d6fe76e985e6ac89e23db290f46fc2b1d74c`  
		Last Modified: Tue, 30 Dec 2025 03:26:46 GMT  
		Size: 7.8 MB (7763233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70802c911e7cacd168c279a1630587d04e0e6a1137e5cd58e637debb4fc7d01`  
		Last Modified: Tue, 30 Dec 2025 03:26:49 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:57b78503a128eab88ffafcacdfea874711f665346aa9f3a27be8a02c53ecaa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153136310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aab931c9f8f7cab2e208d53a5402a44c33c5581cefcdcd46ba891b57d1c08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91d81fca5e6c748002000a619bf74adb52e958764c3c6f71a567585a73e8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069a58fb1a0b5869260344405479b130ca91ac90f5a24e7ddf5db615d11db55`

```dockerfile
```

-	Layers:
	-	`sha256:8e2fb6cda59c55f063358b415517bbff8afa47db03b6af15bb6ed5b65628b658`  
		Last Modified: Tue, 30 Dec 2025 11:20:48 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1359f5f7767a35fe07f597baf1ef10e3ce7654d9ae7b45ae33320516456727d3`  
		Last Modified: Tue, 30 Dec 2025 11:20:49 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:47f0d7bf4589499bf86ae079371541221d2a24c51a3e91a8f9264d0d2ab97319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139385592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05506de782b06c88c810945b6b4226d362d98d59bc47d8e5b414983cac14730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd2dbde918ebc895841fc4434fa07a707f13b9827f60e711f81ea8f9a40b5c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5b684b68309cc1b7a987d1d3029a7ec75401629fef4eef065cb8ad28b1c621`

```dockerfile
```

-	Layers:
	-	`sha256:a438c4d29c04cb19c729472faf5d7c3ca350310f9ae7ffc14da9402993db8ec1`  
		Last Modified: Thu, 01 Jan 2026 14:20:43 GMT  
		Size: 7.8 MB (7756934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cb7e8aa876eab1b676c86c992bb4bcb023509797d46fa4c30ac11d06561536`  
		Last Modified: Thu, 01 Jan 2026 14:20:44 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2f3056e8a07632fb8634fd67d352cad811bab0a37468c5e9d702d6b5e2a5c0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144762759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76813b4737563fa6882b66f0fd63d66866086332b200884fff05e3da29ca49c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1493de138e251ebeb34a45b9e9af5089a743b7d2fcd0fa86b24c2b2bdb7a2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25feb2ffb614cf0a2b2c7c98ccb782aaf70d774c6080b80f842c586db74f112`

```dockerfile
```

-	Layers:
	-	`sha256:ce7094420676644a509bc861d0af1399d3f1714a8bdaca0957c6e055efe6d589`  
		Last Modified: Tue, 30 Dec 2025 08:20:56 GMT  
		Size: 7.8 MB (7768011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2689f7685533adfc17bb6a19378eb879f278d2922b8c75d53d8ef1abb826a8`  
		Last Modified: Tue, 30 Dec 2025 08:20:58 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
