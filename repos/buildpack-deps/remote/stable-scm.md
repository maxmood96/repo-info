## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:15bf0c525f81fcc72e16ed423c4551b2cb67946998a3e85c722de41bee251ca6
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cf237fd6ee95be040699c45feb2072d097fc1ca22d2f178a410926b98c6dad8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142677879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df7c749befcff293af40b1d6b60f0a79c26e976efe9a1394d8764a9c2d051c6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52ed5a22eac12afa8d7df5ed09c17eef4992ad052c10cbc90b384cd6b1602c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4004af6c07523083552fcc661a9a91c028ff4099b473fa8cf9920d148960782`

```dockerfile
```

-	Layers:
	-	`sha256:8351ca0b60d4248cc546d3ebe18e690efd3a090f5e9826b6f65f2f9499431cc4`  
		Last Modified: Tue, 04 Nov 2025 11:22:34 GMT  
		Size: 7.8 MB (7767050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cfeb791d2ca9b11b12db579be227f5721ead4bcafdefbb6bc285d25ce8514ac`  
		Last Modified: Tue, 04 Nov 2025 11:22:35 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e54c2a8c14465f5d90d2fa87d651064daaec88db92db0be57b7f81a433f63774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137117335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334cf64fbb74b2efb4f75728f5e228e6760edad152e4b0d5e4036d6b1cf8503`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:51:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e91b819b99c2c8690acb5b01465ae84356bc40a50656db0ab817eb28337198`  
		Last Modified: Tue, 04 Nov 2025 02:51:11 GMT  
		Size: 24.3 MB (24343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6dc99f3137f9645c516987d6a868e6cc6233f36d0a984e9553daeb02a012e2`  
		Last Modified: Tue, 04 Nov 2025 02:52:04 GMT  
		Size: 65.3 MB (65324780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0571a236fd0a7de67791f4667e9b214e2b2f0515d7cf3bc1970fb6d3df48978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3553686243d81cf8baa9751ca1aba679f0160c10e73ebd5d048c9e85dfc2989`

```dockerfile
```

-	Layers:
	-	`sha256:d082f964b79484e8e04dde95ecf02b2f1434567ae737602375976d07f202f447`  
		Last Modified: Tue, 04 Nov 2025 08:20:50 GMT  
		Size: 7.8 MB (7768088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e33df14938f67da1f5c9e77d887a2a864aabd2093e1f13f36e04aff8b12fd52b`  
		Last Modified: Tue, 04 Nov 2025 08:20:50 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f684ceee0b600c8d0a4aa9ae731f77a6159641ccb378e67a5eba1d3646883998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132055845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8457f02d5a79f8f413fd422ae6d74f3d2db377c59cd8e3f57bc3ee9d9848c54`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:caaccdf8fb49cd124dc4c23baaca3be5aad18c1263c8afe3356d15af000e612d`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 45.7 MB (45717135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368971cf52e52bedcc9c34f098c9d72d70d67b7064ef11faefe431b570e27f9`  
		Last Modified: Tue, 04 Nov 2025 00:40:16 GMT  
		Size: 23.6 MB (23617115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5622b4d13fac6a61fac2dedf72d7cec257ecd1acee5ddbdff6f27c4b9ebc7331`  
		Last Modified: Tue, 04 Nov 2025 03:07:13 GMT  
		Size: 62.7 MB (62721595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb17c9ac5160ef19e1e2f45ae074116dda1381899d88ae9b57f9d2e3077c51b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a33bfd77ecd847d5022de5adfc69eb87b1d6577fc81795228970a65cbc803`

```dockerfile
```

-	Layers:
	-	`sha256:b7511ccc27711f1d2cc59074ad80c2404aff7e35d5e250bcee738a16566bf838`  
		Last Modified: Tue, 04 Nov 2025 11:08:32 GMT  
		Size: 7.8 MB (7767557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6072412cc60ac914835631a3ff7fabf839cab4ed060e0ccb27e4359066fdac4`  
		Last Modified: Tue, 04 Nov 2025 11:08:32 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6888758e8e23b46c767f59852368b0d4b816cb68d1eb511e4525b9f8da831104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142251881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b4a2b5256fc68fad9b2076240ec6aa5cace3afe0a4b82d0f1e1916f590cc6e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b99212e6800832d3b05434ff618127ce534bafed71269bc1d97a823422ac6644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62e1438fe9c9f87d2735b8485d138878cda29f645d1579021f152019bd017c3`

```dockerfile
```

-	Layers:
	-	`sha256:c9f18dc9f7faf70db1cb3de5e6e6fd1b2533467978f092a421f3160d6b7b5c5f`  
		Last Modified: Tue, 04 Nov 2025 10:25:17 GMT  
		Size: 7.8 MB (7774725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac33ad1a40d6b7ab6618774db26b57a05a0c812a57db240398158bb94c9ec45`  
		Last Modified: Tue, 04 Nov 2025 10:25:18 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:723bd4d2f849b47dfeedd721635b268d44edd55e509115451553f93c15db499b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147371187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4145ec8857885f88a585f7ac3774707f23f6eba72aa22c9fff03d65dde51a039`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac49d94324079b69237b0b1612a8d78112618ce6800066877fb7d7a38ff9e74`  
		Last Modified: Tue, 04 Nov 2025 01:32:28 GMT  
		Size: 26.8 MB (26775967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1318169541c4f79fbdfc20cc98993bc7ba60d45d8f2235f647857ce150c6f7`  
		Last Modified: Tue, 04 Nov 2025 02:20:45 GMT  
		Size: 69.8 MB (69793982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ced20556833fda75475b61fc2b7c3b88a184439faccbf60f1e882e40ce0fa80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3842b7fc3561224a4b8ee84cc06f4648a809bc5a208cfc37a5ec2457aea51a0c`

```dockerfile
```

-	Layers:
	-	`sha256:31f0c9ad90132e59767cc031c83891577ca7c3fb52879de18bdb248465b9448c`  
		Last Modified: Tue, 04 Nov 2025 09:26:26 GMT  
		Size: 7.8 MB (7763185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60550f3091b185a5f9d17ed8411de98bbf3f3826f340a1ed1cb8cdea9e13aaeb`  
		Last Modified: Tue, 04 Nov 2025 09:26:26 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3d843c5b054d86b0ae2072a0aa7c5624f86e382eb266fe475c40260884c74d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153135368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b80614c8fa45528e2cc004b84225c8d1dcec0d63266288b03d438bcbdeb3c3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4871597e9e7cfecf8469d9bbc320ddffdc2fc43dc51f60b3296ba13960231bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e89b9495c6adffdefeb4751b3bbd1df704544002c979e27c58c0727b0790881`

```dockerfile
```

-	Layers:
	-	`sha256:589c03069d1d6372edbd1ea4950d57d0a3a57ba1cedb31411d690907f1e5be05`  
		Last Modified: Tue, 21 Oct 2025 19:20:46 GMT  
		Size: 7.8 MB (7774173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60412275fa31a71dfd01f825081c5e7ca04a36d18dc9a4a37c4a27103aad052e`  
		Last Modified: Tue, 21 Oct 2025 19:20:47 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d87a89f3ec977e572d06f6eba37a10c57497e51eb1bd363b741b1df36943a0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139386544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e594ff0d18dafbf92e81e01f41215158ab4e080333c11e2be34ba851f9702b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05bd658b6b88b72fcd0763d85f85d239e81655e6c5f5a33d4ae006af111afd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df2880ffedd1abdc9ea47b20067e8694d5c31dba96421fd891a621ad0eeff04`

```dockerfile
```

-	Layers:
	-	`sha256:c8fd5ff1f15beb51785c747c08ffc42fd59040a82f92f7b4f3ef8a6d1cd9b455`  
		Last Modified: Fri, 24 Oct 2025 22:20:26 GMT  
		Size: 7.8 MB (7756886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235bbb0d6fce496d9ae15f82e4d71956ea60990fce41397054289fde8911e24f`  
		Last Modified: Fri, 24 Oct 2025 22:20:27 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dd97f751d26f0fc8aea4751840ef6165faa9363addb66199bd426fbc8176f4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144765648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a379e2d580c1490ae60224d3655a00c49494cead0bca8ce4cbf923ea0b64fccd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7363509bdabaee507d788486430a67895cc266ce0b808959842f46de0bc92e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44a253cb1c6d35994addbd4b8eb06403a3982f0f2bd18ea3fef26efaf0ddd91`

```dockerfile
```

-	Layers:
	-	`sha256:9e782feec5ef538338ac3d315b9a647df87a78a854099dcd03263a6d7e0616cf`  
		Last Modified: Wed, 22 Oct 2025 01:21:11 GMT  
		Size: 7.8 MB (7767963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6430bd306930583d68f6d1a189ebe242a4be4f1a77c9656a4e6f77886413dfe0`  
		Last Modified: Wed, 22 Oct 2025 01:21:12 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json
