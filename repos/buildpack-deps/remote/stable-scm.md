## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:e830d5fb2fc908e2e3fb6c4477071940eedf83f07b6fcd05df91def754f0d86d
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:06f191eff803ad2e91e6da35baf08f715c791b05d42c9b0b639d4c18a4008afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136914855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6e3ef7d762499cda27d0ba3c0e6e386e095faa430667ccada53029da4cf183`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94335992e3d60e078488cff7e63b3a3cd0d4ecb66aceece2034b16fd4c01d9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9588933ab1cc32be8141a06a74d626e1d5167be3091a19c932e8460e1561fe7c`

```dockerfile
```

-	Layers:
	-	`sha256:bc88903454509e8359e55c3e5214f609103c915da61f6e606cf97197531a6f9c`  
		Last Modified: Tue, 01 Jul 2025 04:19:51 GMT  
		Size: 8.0 MB (7958934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbbd76a94589b2a371b4ab788835cd233b916f3d5d851f2fb9a677e752026c18`  
		Last Modified: Tue, 01 Jul 2025 04:19:52 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4bf0949fe07315995529d92f35fb9fafbd34c190a314d1383af31173bddb7012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130721459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6327b50f52d0bf5fcffa82e23f4204eb2f653baf74d47b571eef2703696d130a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d208698d30e75c289cb2ee99e5f2a75a42e11f8e1b4145f8fb1a881298b833`  
		Last Modified: Tue, 01 Jul 2025 01:14:18 GMT  
		Size: 46.0 MB (46026558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3fc3e72f0d51d8e4d2ef852051b722d30ab0273006822b4317029f0c2f0082`  
		Last Modified: Tue, 01 Jul 2025 06:07:13 GMT  
		Size: 22.7 MB (22696790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a0d5b45d8acba98ba50bdd9aa910689d51522b56b3a703832038000177fd5c`  
		Last Modified: Tue, 01 Jul 2025 09:28:16 GMT  
		Size: 62.0 MB (61998111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:891eb5b1c29d47765d61d4a4c433b10a3e1fbb389c2c664f6f4569c443291643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282e7505c90ce3c0df912dd4312f941e8899959efc556bd0a9493811a1876ca3`

```dockerfile
```

-	Layers:
	-	`sha256:1c6b04825244d7509f78087b11a2fe405107e0cabc08b81796fbcdd324b95cdd`  
		Last Modified: Tue, 01 Jul 2025 13:20:02 GMT  
		Size: 8.0 MB (7960800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6f796087060df7c791e270443d7a49814cdf1e730a7472394cd2fe8d9da845`  
		Last Modified: Tue, 01 Jul 2025 13:20:03 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b2cfbee32d8d7dea6c5bdb4f82504a987cd1aac61c6ccc6e72a45ee044a738c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125793007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3865f5d9135f5d161d8fc8d23cd3dd97386449ead7ff04900d5ae4d53cbd6aa7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:820c5e18cf9e4ab05490df676ac715c7cf48761d79b8041b26a3c9d84ee780f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7967942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edec2d9787b47c26c939ddaca6abd981adace35173a85391317cef02cdd5d6a`

```dockerfile
```

-	Layers:
	-	`sha256:334b6946ef2c471007de0a3edca715a61a7a2a3ee170a72a6c672957b3267f37`  
		Last Modified: Tue, 01 Jul 2025 19:20:00 GMT  
		Size: 8.0 MB (7960219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34fd43ecf35770aea63deaa92d3261c52204c3d96bd0c8fc3f63fa37b6dae20`  
		Last Modified: Tue, 01 Jul 2025 19:20:00 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:60c0dbbabcb2b123f4ed403d8888471d4ec05d6ce00456e47ddd9968352c1b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136260087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae254ff59eac5f8ad67140eb429e54245f37a7cc9169878cf9ea7e6c7bd5cd64`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b39fa27303b3fd2eb3a8c7ab5fbc8636f2e01e28267e2cd1098d7e450e848b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bf7d2c289be9e2f4b9e1ba4cb797184004cd8c6f274c5a79503a183bb8c612`

```dockerfile
```

-	Layers:
	-	`sha256:4d5f8d8258275b1ae7aa7bfbe9c5ea4b301f9b73c118b72fec90fa8abacf563b`  
		Last Modified: Tue, 01 Jul 2025 16:19:58 GMT  
		Size: 8.0 MB (7965339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e328b7e0951160fbb49271e6a54cca1498ccf588d80c72c896bd2c668ac3a1`  
		Last Modified: Tue, 01 Jul 2025 16:19:59 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7440bffa3edfe318d5b5272ae65e72c9e0409c758eece13e667eaac1b9d8d0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140559671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4486d446a9af6b6b4fb571faaca94c06d6decc7f6444c49c009e0b05145f52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83e054b03e5a5d9ff20dd3290749a077812d71baa3f314f2bfdcd83ae6182fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981fba1870d9fd3220ffcf022fb36b7c1e6e56f6c5d97217d29eb2b24b4af10`

```dockerfile
```

-	Layers:
	-	`sha256:cde02496da231e6ac29718044c3cfa791e4dd425cdeeb814faf539c40a9c12c5`  
		Last Modified: Tue, 01 Jul 2025 04:20:11 GMT  
		Size: 8.0 MB (7955093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e57414e82f867152f2876c6d4a1a8f41be7b69b31077265d5af4e5580f8210`  
		Last Modified: Tue, 01 Jul 2025 04:20:12 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c5fa8aa15c9d9b6d8a8231fdc3bd876bb4cd3ae156165aa0012717d09d5d8b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135682904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beedefecdfca808792d43e8ed0999fa21f700419443b0e4207a8c23b12433573`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6206653cbd2aef53c06e2d9a0e2a3c484f1a46ec5abdfd9eae047797fc380aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985218f874530b5d6fb2a079b9c1603e2f0228173b95fc9ddc7c3f0406ed13`

```dockerfile
```

-	Layers:
	-	`sha256:c8859a87661d317ba7efcac029bcd846de7f4ed57b5780bd3d2bf6626194da60`  
		Last Modified: Wed, 11 Jun 2025 22:20:04 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2b7a6a8365eae7cb84eaef545e9e535253b4e18d59dab48cbe7abb836a2b6dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147840924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a72684b98e0ce1c9adda8eb4061532a51c1a48b86864c1811058d048bf70eab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85d7351b117bf2eead92efa7bc23b24eaa6c30eb148d6d1ddf4b344c3f870e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54417a3b3858eb20d4be3b405a46b0d18285faffb284b5267b25b7f336c6460`

```dockerfile
```

-	Layers:
	-	`sha256:0214569cf36d3bf6390b9ceccd417f6e15a1dacbdcba6e0c916afe17bf17e5bd`  
		Last Modified: Tue, 01 Jul 2025 13:20:24 GMT  
		Size: 8.0 MB (7966801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db99413cbcc3de0205cb045334a53959607d21ffca60d5835ce35c96fa269c6`  
		Last Modified: Tue, 01 Jul 2025 13:20:25 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ec2c0b1fcfd242d8e47ea14056ef51248dac763925c891fec157b6864cfb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134667792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ef3c9e8faf1aafc458b4a19ccb1cc5b5a76a1cca5b6f726c5bdde6ef24d96c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:633076af373671ac439e1661db1e5c0724f79cf2ff53a16cac4d0578be4891ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749bdee2495b60249c0a479d3d6cb891e80a844877b0b1c011ed7372ba55727e`

```dockerfile
```

-	Layers:
	-	`sha256:54b1f686b06595c3970c3df3d3f22033614b9e6555fa0097cdf719dfb9594084`  
		Last Modified: Tue, 01 Jul 2025 10:20:15 GMT  
		Size: 8.0 MB (7955247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c708440b09ec17bcfe1583bab83fac03c69d16c70093be8d6223734fc537a46`  
		Last Modified: Tue, 01 Jul 2025 10:20:15 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
