## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:dcb03eb40ec3dd4a0667f7778557a939e2e290f7189ac4d01be7b6c946e36fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1bd5816c21dfd482696112b2f7b1cfe409be46324c34324afd6cd78f8c1e1394
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138640409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6eb1e8ecebb5addafad2276bb23b14ac9333c39c1fcd6650fec6fcbb3c8ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d3eb244249a76a53e7b3f03c8e999bbac83be7058bc1aa1fe0eebb494baf`  
		Last Modified: Tue, 13 Aug 2024 00:52:48 GMT  
		Size: 20.4 MB (20428585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75784ed4e534b2a8c61e811f3ae902dd7265dcbdd4784c9d0a1e99630fb6e3c8`  
		Last Modified: Tue, 13 Aug 2024 00:53:05 GMT  
		Size: 65.4 MB (65370635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f0b187f8f18714df9e991a656fc0f2a80c8327ac62e2f23dd70080ef83f1c6b7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132313931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0011ffd5c1b4dcb144acdf454a18478ec58e58d0b76ef7093462465ea818eed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f13351eb581481c6d47c405a86b686fba7946e210157e87dc4b794f891102cb0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126637384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff66e7da2a73d3be42958fa9af13c46599bb0a2a8b84a5ce83aec566054d3d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:59:15 GMT
ADD file:99761e9b65792d17a2f1d115ea8ad35dbc2936acb0f636cbbbcf63ed20bf10c8 in / 
# Tue, 13 Aug 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:30:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8bfff960de1d4efc80e46f547c59070161e89055685b260aa43880326ecea728`  
		Last Modified: Tue, 13 Aug 2024 01:03:57 GMT  
		Size: 47.4 MB (47364130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd50d3da00085a24eb625c358426e1b80bf8ce08f61490cb333acadcd859662`  
		Last Modified: Tue, 13 Aug 2024 01:35:26 GMT  
		Size: 18.8 MB (18766680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe1bcf23c21ef61b6aaccf643634f53bdcc0c710ba00e3634e10fa911d0a984`  
		Last Modified: Tue, 13 Aug 2024 01:35:44 GMT  
		Size: 60.5 MB (60506574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:449767f242c02fcefd2da777a6b7572bfc25ffaba7a5dd22990868bea2b905c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140066591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ded28d1c88b687b49ff8d990c7368685ce1fd35e36a692f9ad5db9175957980`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acfc21a933b61a511a40057c2cd17da39e0b250e421dcc7aa725078e2e542d2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142347395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26dfc06fb060f82a67d251678866e3eff820033e7c7b1d4ef017858d28fb594`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ae61694adb073775cdca4573dfd33ebc664d11ca9805f83c9752262aa3e8593d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136649415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0878904dabe9eaaf284de551155f435f7591349d2dacf355819778e21f5e4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:217a265206c1665bace140bae895d8f0389cd1108784b49ae025ee581832f9ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150508897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef248ce0249576f6a1898b164e41333a4b6f5ceb2040c1a2fa58d257f7eacf48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59b4aa62accf6e07b2b7fb794fc05cacd6275d29ce1f60320c53774d3d540cb4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140464016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e510155ef48c59718ba45b79ed24018f4f20b5be7f993ced3cbc8095bcd5a348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
