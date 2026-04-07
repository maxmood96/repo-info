## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:971e6db7a8468254b3f9bb66b146457d8ecce38fa1ed7977a49a1c5570eb4491
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:81913788bc787a2cc69074c89767027d02f175efbdb42bb68670aa06f63a7fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72527092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f41750a49a6013c0f93c595d7ba1e7c48f2e3dc79095af86b81886373c426eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41c6958192069208c9ec8c42290b76d62f5ffe0a30138651c37f45c8fd43f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee97e4422b180cd410fcce88fab0be43237ba4afc99aacf256c06b18f3fd0457`

```dockerfile
```

-	Layers:
	-	`sha256:f5fde9e1961f6d6dd8c587758167b4d7de62388fd2c4fdfb8876842c75c3d02b`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851d2cd8a185160a15e9beeafc15af921c55602a7a6d71cdc848ea38d94e4cf1`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bfb30825cd6f321ea1506388e2d9d974343ad4dac9f6e5fc290cd5a43d80187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68735522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2789e5895d93a7397da9c83cecab079256a15c0329ea35a9b56a841d4ba7f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:45:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa35eb02005428c4a86f22e10592a31c9665a2c6271b47a76c82cbbd92be8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1748625dc80131d70ff6175bce0d4865c49ad28d01480d4d4e97521d25c42f4`

```dockerfile
```

-	Layers:
	-	`sha256:641be05edeead0a8d65283f30505d49d8bf78d2cb4681d369a8f9190c6d199c9`  
		Last Modified: Tue, 07 Apr 2026 02:45:20 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a736332894c431cbdef8058a77543be067d15a2ce5d0d208258c8c7eb142923`  
		Last Modified: Tue, 07 Apr 2026 02:45:20 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:271cf490dcb7abcd097c98a0cccc4cd10f2fa1c760ac065fe42c5bf14bafd3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66149900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1854f1e50a412eccf8dc9b0f38b14b7453a132e90c561d21e8ab1e79c6c74892`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2824c024a6b0fed117f200c6592c644995c5b2395b3eb4f5d2c3669be4209c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbe2ddaac1d0c61c98ea9c8e76f2184fcbfc29a764ea72f77119a4f636c5c7c`

```dockerfile
```

-	Layers:
	-	`sha256:517109260cb42d09e1de78426ae1cabde06230f7344c4da4d75c0dbb729710d6`  
		Last Modified: Tue, 07 Apr 2026 02:00:46 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17abe87e6cea727e38ab806a872beb165428487a0b4cee8dffa7496d8c723237`  
		Last Modified: Tue, 07 Apr 2026 02:00:46 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b371c6547e6df20396ac3b89d12b11c9ebe9dd909253daad245bf00475ac2d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71977967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9915db06900b69f94664c8d8c83c25b278e97534baabce6c1869dc1383f71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1267f6d777ec4034b1f46b1b8d06bb3cb3995844618640ded74d383631728cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992451b84214e2aeaec01fd5149c7b68d9ecd6f800c86358493a42fdd828ea33`

```dockerfile
```

-	Layers:
	-	`sha256:9bcf5df7c9851162d4c81c6bbf28d5082131351b6a5863958c0b654a44558d88`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baac774a141dc83d4e9c753bbf342cb4ac56e9fae1d032b2f9bece6090fd3606`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c33c8cd14082f90636d0f0f946200a32a63a8639ee0c4ebb694d06f4f1690502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74349888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4bfc5bfc80bda6f0e9dd944ab5714a205727b729022527ce121baef45b5f3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:170ad219e0cdb2f888e214482dbbe76e20c3d88e6b4d1ca738be363c63dd6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559672e0390f8677ca79c8a985a8267fd684258da8783bd74216522834afd76c`

```dockerfile
```

-	Layers:
	-	`sha256:0cb7087cd5727c9c1b746b598b153bba31640a3c5b07a17a3c58001e22c82ab7`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1268bd3fec73488cc30b510a28861c45d182780a17825243cda55dcba9df61e5`  
		Last Modified: Tue, 07 Apr 2026 01:45:48 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ada7d57a75b29b6ea3e0518ca428802f8fff749f4e06ae8b102bae809eaee888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72397441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea1b4f3bb2effe3b75e25a21e6ff5808fd4fbef88c8fffbe8c4a61222b71ee5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 09:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:55bd01c42402ce77937fae9abfba9b351fd4b3fab7f1f58eccf5b2fcf0ac8978`  
		Last Modified: Mon, 16 Mar 2026 21:51:11 GMT  
		Size: 48.8 MB (48782288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a46874b19723e755d13ba2292477f479fd221937f5480b97990afd32f94b3d6`  
		Last Modified: Tue, 17 Mar 2026 09:32:54 GMT  
		Size: 23.6 MB (23615153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3f902aafa44ff7e39051ea4d6b0e9a85631803dc5dbc74ca879d60fd7d0b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15a409c697ca98640110eddb854d96ebc6d6203be152de55966a3314ef19720`

```dockerfile
```

-	Layers:
	-	`sha256:a36bde0ed2a64b4c270c2cfae3a0a8f22c64b946ab8b9792e2a6a088ab049e76`  
		Last Modified: Tue, 17 Mar 2026 09:32:51 GMT  
		Size: 6.6 KB (6648 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:04a6bc7e75f14374ce8e2aaade7772d143ad2877e219b6079d3fd052e2aa0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78008515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c354d89ba22d3a9b6e2c44efbae0efb8a5f977551ee11b76d8f04421dca7f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3998bb20ab515ebdb115aa358a4fb6b284588d063c00f576551abdd57bc35768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4064c8a05050600b2799319bd0efaada4a72658264e2089c7d7b7f27e50de5`

```dockerfile
```

-	Layers:
	-	`sha256:8c050707dff502b9d779ca56bb19f45ae6520868d420ea384d0cb21bbf4d14b9`  
		Last Modified: Tue, 07 Apr 2026 04:21:53 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe25b575a62a170708e763dab6b93874a984408f2fedc75b6a91df1b64dae72`  
		Last Modified: Tue, 07 Apr 2026 04:21:53 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:06d6fa28968cf653afd38c145887b285348696d86bb5e6dec772bbc70070f37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71181719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c597e91719dd0bfc6f609906e5b8794bf8be23274dc43fd00fd18bd2dc2ef5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05de50f03f5b8266842829dcad025f88b9820481a8dea9cd0fb7cea381de1741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c74b680987c07e465680a57206e80ceb5f08cd779381381b474a645c13891f`

```dockerfile
```

-	Layers:
	-	`sha256:929dc215bcb631649d91bd1147fadd77b92800f2dca462693de8d32c95628ff9`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca598d8ba5004d339ff8cc04e677b8719578b316865df61bb74ac1ed0a6ddd61`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
