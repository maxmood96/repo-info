## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:64e7f2b5e04a170ea1a426b58aeee5e618bade53e7dd6d588899c5265183bd27
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e19947ed3a81b49cb014dba63e77e55f154311691f833c44b853ab3fd9bf0e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74891220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802453216cb3a7a9fe643f4e687e60cc05ca1fde583e2bbc48dbc8e2c78296bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27ec2b094be6ccd3d4d71b53c8a3de63de6e5f2659fce766bff0c2699ca5ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fa110237714b974bac6990dd6669a439a91c883d3be6171f5763ba56ff69a3`

```dockerfile
```

-	Layers:
	-	`sha256:7b576d696facda354a1ee5c389823cd799d3f80048e821ff72dcfe56b9c7898d`  
		Last Modified: Wed, 13 Aug 2025 01:04:42 GMT  
		Size: 4.1 MB (4117001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72eff9f3cb48e1dcf69e232a0094542a16f600ed5c19c84820449016ef2a4b85`  
		Last Modified: Wed, 13 Aug 2025 01:04:43 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5ceef679f267b1eefa6d106274bba7d1d4ef50b27dc7c39df3b1b9f946c8f9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71781193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e24cbd12f9d84633f8d613f5f979d824adbafa0e55fbab54f56a9f49882bb1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49b34b9ef926ce7ed8f011fe61446ff5495accfded522a04a8414730759ac407`  
		Last Modified: Tue, 12 Aug 2025 20:49:02 GMT  
		Size: 47.4 MB (47442425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10345871b22cfbefdba6d9f2d575fe7ebd340d456d55037a519d266903c1f87a`  
		Last Modified: Wed, 13 Aug 2025 00:01:36 GMT  
		Size: 24.3 MB (24338768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:162f47be4b224d7fe52999b37ddceda639f846fe7340f4205326e73229350ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2f5bc97c9932a9213f1c0c00ff0e8869359a593aebeb195da644de902d2ecb`

```dockerfile
```

-	Layers:
	-	`sha256:81e71119e018fbea3ddec156df6f30fe7467b99f95fee290fd478ae65d6e407a`  
		Last Modified: Wed, 13 Aug 2025 01:20:49 GMT  
		Size: 4.1 MB (4120299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e701cd096c80596843e443d8ac8344ef2890f77c8fce1d4119d851ede71dca7`  
		Last Modified: Wed, 13 Aug 2025 01:20:50 GMT  
		Size: 7.2 KB (7197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3c30cc1a13c2c43c4fd32125318d33566d64566c766e5a94b79d6e40c1b00244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69325676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d2742a4994352df325b2a31c1ba82d47d27fd95725efc38a19065b03765c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:075a5e10e16593686250d1a73e5d4cca8dfd59807b7b30be2771ef4ed929ba1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cebe130c4c5229360fc6cac020acafcac714b14910819719b0c23106a019be0`

```dockerfile
```

-	Layers:
	-	`sha256:a90f452aa96fe572f5177f5a0e555a671b2552cda9923166ffbf9d6dc882ac3e`  
		Last Modified: Wed, 13 Aug 2025 01:20:55 GMT  
		Size: 4.1 MB (4118810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f95d059fa174a3cc118f2a463fb655c091400dc7057671f92955d4c26ad571c`  
		Last Modified: Wed, 13 Aug 2025 01:20:56 GMT  
		Size: 7.2 KB (7197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2eeb98a80c0c76369abd8df39564c7f5fe8531fd68725b4262b84f5f0d9c8707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74656213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c453a6c8554ccfc17460e6310dd85affc2bb8fa7c8314a356bb0fb15f3fbeca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2a514f9d0189f8d10413fc4205057bdb49d38228220a74f0cac2407fa77d72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091e3d0b0b4532622745bb79b28035badbb18bffbb9c8a328124627b634cffe3`

```dockerfile
```

-	Layers:
	-	`sha256:bb4b313b1264098643fe3f8aca7f8020262fb04cf44f7048a61ff8bed2855dbd`  
		Last Modified: Wed, 13 Aug 2025 07:20:17 GMT  
		Size: 4.1 MB (4118851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba15833cfd452c120698ea3855b886317e18da213352bc13b5d7ecdbece7b07`  
		Last Modified: Wed, 13 Aug 2025 07:20:18 GMT  
		Size: 7.2 KB (7221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8d1807c15fa5e9f40aa048b9e44b86061a9c17e21464a0f3af69a48c70e05da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77566817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfca898199fad6597c7d86ed0a0d28d2f41341b1925484e5d2550cb0941314f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d9e7ad4bea344c3b3b7019d678378c4a5f820300461e65811ac5d9d0e87856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70307b543f8e52f21e08706fa0e86fe15226129bde9ae8e2b58e429d8b6edc`

```dockerfile
```

-	Layers:
	-	`sha256:ff4e1f3313d423744c26ce9d1bf66f4b6c887f8a92cf9331a8cfef054b9de9fb`  
		Last Modified: Tue, 12 Aug 2025 22:21:18 GMT  
		Size: 4.1 MB (4114114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6af988071106ffaa4bd4d60984e55d6f553ef42a4fa1fbbb37599a442da244`  
		Last Modified: Tue, 12 Aug 2025 22:21:19 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7c8f3512829f9222c4d09f2c9bd914779771e3afe3027f3224eb21fbb4d82d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80096252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46494f6099b80a32cd7780d37c9f40ffea66f89243cf066dd64a8ac601ebec53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32fa2a85187997e792aebc62c3cb1ee63c7df313a0b5ee3b98226a6412f167c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b041ec9b6be65819a2d3e540fe8c73b1487b87ba4f6d2a8fd98df4c005375`

```dockerfile
```

-	Layers:
	-	`sha256:4add0fcf1b66604bfe9952b4d48bb08affec242833627d09547532e0f7ef80cd`  
		Last Modified: Wed, 13 Aug 2025 13:20:21 GMT  
		Size: 4.1 MB (4121155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f195416056961775e08be59d2b32099305598ee1a82820b31d50dbbc3849e38e`  
		Last Modified: Wed, 13 Aug 2025 13:20:22 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:141e6ef170db84b282f34de405a2a82320eba1e38fcac97e5e67cf7a3be34929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72714887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3966b701501d3ee71a570e436896f6a08d3b9f322570e5f9f6ba5733746e0fa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9285e8807d5a555e1b50ed354646f54b61c2f3ee84d62a7a162c952506758746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bbd324719cd243ba8a55f39b4b7c579bbfdf8dfce2400df7ed5a0a82b18523`

```dockerfile
```

-	Layers:
	-	`sha256:ec88dddae2618ec6ce65af34101ed29f1a1844c069293561535ce03625407606`  
		Last Modified: Thu, 14 Aug 2025 16:19:59 GMT  
		Size: 4.1 MB (4109819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c64cce5699b480e61c79b11216e978fd32851e9a1da300301d9308094a60659`  
		Last Modified: Thu, 14 Aug 2025 16:20:00 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:497c16421714207732e41403a38b2380acc7c9d5ad26a49fb398ae48172436c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76124741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684163f560d89e0de6713a16b3cdec4bbfc40d72536daf5ad166c5402530be37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:415a914901fe80a38412ecfadadff85e2638af84f2481d2452e5c06552f6219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a3969f6ddc0127ce57c9f7ce99deed50c2ac52feb32866ebbf92a3c5f9919d`

```dockerfile
```

-	Layers:
	-	`sha256:ae6228e898b6c6f4917c10223f28853e056231c2a239846dc7b32d511e7be419`  
		Last Modified: Wed, 13 Aug 2025 04:20:09 GMT  
		Size: 4.1 MB (4118719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bd85b1a341eaa191f4d361905c85455e3c70bd91303b34b18e5dc1d1e0d62f`  
		Last Modified: Wed, 13 Aug 2025 04:20:10 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json
