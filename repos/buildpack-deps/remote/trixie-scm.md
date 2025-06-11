## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:0d2a0d6dc3f124c64bbca1f29478605f6f26d8b367d33c644e58015001e119a4
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
$ docker pull buildpack-deps@sha256:79daef2071bdf2d4226f35b93b620529698a6e060a78d02da184c91bdc406880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142515221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299b1a9775e51c8e28bd2650caeab9ab907fb4f7d86fa8ff23af87a1d551b019`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f807a61ec306a45196094c9a44cffbe9d5d5a283a87c6e5c2469748ac3a19da`  
		Last Modified: Wed, 11 Jun 2025 00:01:30 GMT  
		Size: 25.6 MB (25601492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f581532859d9e82510a6be0d293f24d77d5efa5a66349c1e74f899cb0e711`  
		Last Modified: Wed, 11 Jun 2025 01:13:24 GMT  
		Size: 67.7 MB (67659870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3d1a461545dc5c1c378086a04f270851e3698f758c6dfc4b648c9d0d3c18d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245d20733dc8336784f2667d13f3c61da0b9f3bf22f32402332e0324ddc6163c`

```dockerfile
```

-	Layers:
	-	`sha256:5913cbed498151f5d344b2f20dba5ecafe0bbdc9d15cf36497ad4c0b66489637`  
		Last Modified: Wed, 11 Jun 2025 04:21:30 GMT  
		Size: 7.8 MB (7754982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f5ddde65cb3b0c7c9cfbccc817ca271753e677aa1ff575d3b36901fc180f4f`  
		Last Modified: Wed, 11 Jun 2025 04:21:31 GMT  
		Size: 7.3 KB (7312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e1c17601c7db3b428dd3852d2e5c17be23053dddf592499e3a78cdbcf87b6987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137129814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f3c27c3737f325db8b138b295556a3fef81b37a7cf7d321c9db03a4e5f8761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be3896271877b3e95aedbf07f86334bdb2f5374ed0d8dca30695208865ab49`  
		Last Modified: Wed, 11 Jun 2025 03:14:18 GMT  
		Size: 24.3 MB (24326796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1d6b386d300f718bd8ac1ab335ab4f9b2054343e637522505e1fa47faa99`  
		Last Modified: Wed, 11 Jun 2025 06:36:03 GMT  
		Size: 65.4 MB (65357608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ee00059f1b43f415905067617772efdf9e0f8d2856d414aadee506402f1e1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d836240ea01281392acc945785924a4ed4f2b2efdae191f2cd4f2c242b6e3580`

```dockerfile
```

-	Layers:
	-	`sha256:f06855ada5b5ea27e82724ca8914e72b5d33c3d8a57f75eeaa9b545f147b0d38`  
		Last Modified: Wed, 11 Jun 2025 07:20:46 GMT  
		Size: 7.8 MB (7765265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2fe1ebb81dae16d044c7c4f214096fff61028993ccc01bcb07a95d15a4e2f22`  
		Last Modified: Wed, 11 Jun 2025 07:20:47 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b3f3e837fb124193924f0574f802504ead35757d2b360a2bf227c4a67de693d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132045775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce73a1119fe69f4863e0025f2b3fa6493d972774362864b0a5b643e19547bcc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d82ad715078dca1bd38ac71d3c9c872661d1bdfae377c84300033db7bf3581fc`  
		Last Modified: Wed, 04 Jun 2025 00:32:15 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80b8be2756aeb2756ee1709c45d1af8640bfca2b89a56244b22bcddaa053da`  
		Last Modified: Thu, 22 May 2025 02:30:07 GMT  
		Size: 23.6 MB (23592590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef402b2ae65b191fb52b33f040b2eef1a8184aee8984cf58e6acc607be371f5`  
		Last Modified: Thu, 22 May 2025 12:14:20 GMT  
		Size: 62.8 MB (62762367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5269d54d7e76d71b950b27e83bb8d519ff63e3bdcf2532f02de803bb72140d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61b3143fb0210dc9642803dcbf58aa46dc325f4eafacf3a7c8494d218ed573f`

```dockerfile
```

-	Layers:
	-	`sha256:cf472439cba1e8378208727f0a358242a8ddf34544df2999268b7da5ebc17762`  
		Last Modified: Wed, 11 Jun 2025 04:21:45 GMT  
		Size: 7.6 MB (7587389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5918f227f505d8d1c3e0323451ae3c845ac6ff45bd3ccc0b4d4dcc0de63def8f`  
		Last Modified: Wed, 11 Jun 2025 04:21:46 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8dd1024cc47eef54ac579868c259f3518685ec01ab1e317226f232c50e6104ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142205347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d6e7714e16bd3c20d657422f994bf4e3fed8b8ec97fe983b2256b6d2ccdeae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925a0b1aba64c2f9934b5b752199fa927f08300fc82c456fa922c4303a06f43`  
		Last Modified: Fri, 06 Jun 2025 09:49:42 GMT  
		Size: 25.0 MB (24981840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546584c670303be4513862213cb042edd5a8f7eec9db9d6e8c5844665b49b26c`  
		Last Modified: Fri, 06 Jun 2025 09:50:14 GMT  
		Size: 67.6 MB (67605213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f223d162ebb94f86f5848b0fe365e0cafa62dfcc3a5e71ab2739dd9b62826fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7601947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5842487f069198920e41af681bf71c422040e5a222c47e842a45ce7d920bf36b`

```dockerfile
```

-	Layers:
	-	`sha256:9e9128aa631899ce2b9f9480548c02ed22fd3dbe9863b0db9d0ea89be4c65e76`  
		Last Modified: Wed, 11 Jun 2025 04:21:54 GMT  
		Size: 7.6 MB (7594553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e8ba31965af0a63045d7b26c75726057bad6ec1fb9ac52dd17673091c2a48d`  
		Last Modified: Wed, 11 Jun 2025 04:21:55 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:df6a231c26e28faa637a816a7abd5fad58e7cdc71eb7fbf788f93552bdaa7b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147194631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455297c717a923ebd1e9e6cad288bded8d34cd1f13797f10e669712545bc909`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f24aa3f80422a60637035cbe1e280f72c031e00f6d803abf75d114fc69f38e79`  
		Last Modified: Tue, 10 Jun 2025 23:26:07 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60bf3250137ff5f937387763b677cbdfc73f6e6d8cb191bcb236dadd350bc3`  
		Last Modified: Tue, 10 Jun 2025 23:59:18 GMT  
		Size: 26.8 MB (26755336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a68b17b2aedc3eec75668b4c1f6433dc6f26215d13bf5c707dfb14bb20bfb5`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 69.7 MB (69673683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:346224e44ffec5e36a54b05c29e2a7b4398a950c111689fe63b128eb991a3b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264520819891e0d8c97ad51ec7b1fa4da8180a91119b54350bd21cc21f554571`

```dockerfile
```

-	Layers:
	-	`sha256:98d28c1b00fff0d7d28acefed4ff40501053d62d84f3f19b90cc9625258bc294`  
		Last Modified: Wed, 11 Jun 2025 04:22:02 GMT  
		Size: 7.8 MB (7751128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44352474a9f40068dbc3dc8d124ca8b292ff87ec8d1974de3df18c6fc0898375`  
		Last Modified: Wed, 11 Jun 2025 04:22:03 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f21e454c4869aae765909116507b11de1d26e3af9324b63c30287f80051a1a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153091394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596f1904bd5a50f5c6231597287165266a9dda4d5220710c35a45d71c19aa4b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e139263efe3c22e2cdab37e8ebc2c1a1759b3b3d0c9c98b6becc0fbbd0bcf2`  
		Last Modified: Thu, 22 May 2025 07:33:02 GMT  
		Size: 27.0 MB (26965977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb27d293c54626589e1325f716f65d323eba25d860b81956ce153386de17da`  
		Last Modified: Thu, 22 May 2025 12:42:41 GMT  
		Size: 73.0 MB (73044873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53248fb118091869c6fefa98a638a86e2d2df26fc74c387600fe9517aa11b688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77e9665f2bad023a0d2076fe010491986544c5f4230bbc39ce90008e2c65337`

```dockerfile
```

-	Layers:
	-	`sha256:3c6837f8706b85b19ec9cd8cf507c16a52b2d2eabd00167d4639089b765de78c`  
		Last Modified: Wed, 11 Jun 2025 04:22:10 GMT  
		Size: 7.6 MB (7600367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ec6b3fadab1bf7780f7d83bd88a6413a56011c06dedcaeb41aaafbc6e387be`  
		Last Modified: Wed, 11 Jun 2025 04:22:11 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:54ba23fa8a5ffcb880b7753b6c1d7ec174d532a6e501bcb1772fc7c88d77af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139252299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca75d8af1799275f25d0e3c784397cc27370ca737823e538edc5b8f9e71c4ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eab19773c2912f0a6e7295e8a9ea585980b042ba4f201575fb17ac1763bdae3`  
		Last Modified: Thu, 22 May 2025 01:15:24 GMT  
		Size: 66.6 MB (66603294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee1c7757c6ed3dd2a6b693495f2fab7160131ce3c05646e915edb74279a9be7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7584054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfee7396a41fdd371b836ddd8a76222594ddae42f6f5820cd3dd7826b152e069`

```dockerfile
```

-	Layers:
	-	`sha256:90546302bb34affa8b1705430c3f7ee5ecb61eef8167d46ee935d988d7d17a5b`  
		Last Modified: Wed, 11 Jun 2025 04:22:19 GMT  
		Size: 7.6 MB (7576708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf209c649f27166d4bbc5c5e0d3ceba15670abd3a620960fac1f9eb2f04bd9a`  
		Last Modified: Wed, 11 Jun 2025 04:22:20 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac0d28bfa605d4559672e52a97490d6b7015997a9b71b03dd047986fd85381be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144781081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade171a934602dcded3e1be22fb5c37ed015f4a52604b8f531c87226aca855b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588affbec95a011eae8d19fbc59b872f3d6089f972f16713469d6820e2e3fe6f`  
		Last Modified: Wed, 11 Jun 2025 02:51:36 GMT  
		Size: 26.8 MB (26767425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a368896f3f74324a185b32673baa96c49954c4d84388e3238beb96d3b4ffc0`  
		Last Modified: Wed, 11 Jun 2025 07:22:09 GMT  
		Size: 68.7 MB (68683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1983480893303636c883521a9e11e920c29ef82a4da3ef905bbc7efc5837aaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317252bd68a8f6892450cbfbbb7a46008f2ef2d0fc3f7ae1dd0adc4f3304bdb`

```dockerfile
```

-	Layers:
	-	`sha256:5a0d919d8f367404d852d302f46874d7f6858ce0cabd056bc3dd893d4c3cebae`  
		Last Modified: Wed, 11 Jun 2025 10:21:07 GMT  
		Size: 7.8 MB (7765148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f60a009b23c5f810df4070dbd3bd7cc1fd94af08587a2c0bcfbfbf53fa255c00`  
		Last Modified: Wed, 11 Jun 2025 10:21:08 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
