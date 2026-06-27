## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:29d6dfb5905c150d4d1bf4bf59cdf14eb08b7525e42756f37e3403080f6b9e37
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ceb2d76b9fcbd9258f676552f502fca5c2881676a6a8eac3335d3684499ae5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74952193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832f40bf47d41fe2a4de398aa8175737c221b1557ccd8fba64cfe68b4897469d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c834518a49045cad5b3e493572abed2a8604ab45cc9cb25688e8cb9531f84bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59ce6de8a81e9e25971476047b74827c233cc3d52c61bb63456d566fb79990`

```dockerfile
```

-	Layers:
	-	`sha256:17c4ba7d3317689b932692d233be8a8395cbdc5e8c54192c06199d9edeeb08ae`  
		Last Modified: Wed, 24 Jun 2026 01:41:49 GMT  
		Size: 4.1 MB (4120137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699836a8109e7f8be93b800d6f8c95f8ce0ec9234500f020c164d3496cca197f`  
		Last Modified: Wed, 24 Jun 2026 01:41:49 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ba4d5a4e2160345b211ae5aa10dd16b0827ec0310743a9d31bc87c11aa56d230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71859333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725e028f73933c26e77eee2748d0d13db11aa629b5fb774ea81115b6f363cd09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0904cce1afe0c8a47ab4491cfda145d253ca2ea73dc133ce8c90a1475215fe54`  
		Last Modified: Wed, 24 Jun 2026 00:28:15 GMT  
		Size: 47.5 MB (47494964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eaea8159712ba25c96ef93db0fc4f7d8dc3d1df2aeb2cfbb90861e303446027`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 24.4 MB (24364369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec7071a8a5b7c30204707ef654e8907d52c65eab9066cd63a6bf5a6ee03de2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c64856888c92dac5f803e6d03ce31c2245067a641bee1ea9a0c999b221339f`

```dockerfile
```

-	Layers:
	-	`sha256:0f4ce58556a01c271053df1b4c329866776c287393e10474654cf19b60db73ab`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 4.1 MB (4123127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c53bc3653d86ea3096ee4c994fd8bb6a520ee7b0ed4435702c0664df4381d09`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:716e7999e82deca537ef5c24ad02d65e2afbf91bf827158a46f9e262ec5c4146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69384589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5ddf2fbe301815782d27bd9ebfcdc4dde6e42747b9d19691b90e06c0655bdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ec13525e08787ad79558c5631e8f1a1fa24a87872974d31cec094e902b73822`  
		Last Modified: Wed, 24 Jun 2026 00:28:39 GMT  
		Size: 45.7 MB (45748717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5391dda58327007b323e3f3d892147e59e5e36215f08b370a235cf10aaf0a`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 23.6 MB (23635872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9464e40e694b52e0301b7a2cd7e049fd292bf0826158ee4ca357cc01b05764c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da900e9dd381c962fcd0404fed327d87172d8c00e9d6fc8078c8a8e46da8b023`

```dockerfile
```

-	Layers:
	-	`sha256:054306fa85f4bfed94c791c58c32574f9149cac0744a21a9ed9577b09da6180e`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 4.1 MB (4121638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1be8f6bf675c463844264b851239b92ee568dccd471a94359c2e33aadfe586d`  
		Last Modified: Wed, 24 Jun 2026 02:25:19 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce1c5994300b708ab1704d11b4a16505d0d38ae034290baa1e8a449faa54c294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3418489b3b1bb78ffbff67964352c327d230d2fabab5d866692900f9ecfa0fc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c5db37e38a17339e815947e2c667196d88fa0b9756fa4c4b5b0af6b4d776de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5823ebe368905880ae52aeebc02b580e4628cead96c454c517d686b29da4b8`

```dockerfile
```

-	Layers:
	-	`sha256:5f84623c76f14b406675a0d140176e3d58ad2cebf9531e9602a4f400be667f67`  
		Last Modified: Wed, 24 Jun 2026 01:45:25 GMT  
		Size: 4.1 MB (4121042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b1389da88e4d374548e0a44ff9c328b02e57eccbc21a5820623e7f37db559e`  
		Last Modified: Wed, 24 Jun 2026 01:45:25 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b5874b11c8cc76eaf8894deff697389de54c5c66270baac995748777e056d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77633059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962dfd1c988258c43606ba6005dd0ec5a16df29dd09b2260b681b7ae1e100373`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ae12c2ff3fb5df23b854f2a97ab858f54bb2f71491a9276fddf8be7e76d3182a`  
		Last Modified: Wed, 24 Jun 2026 00:28:34 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429f3d50e84943497f0eadc90e14107210f6f5e2fba29257d54a1c7858400bdf`  
		Last Modified: Wed, 24 Jun 2026 01:44:16 GMT  
		Size: 26.8 MB (26797404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f220d6807ad67c642890266da8975f1fc401b17a884e6bc969a61d703d281ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f584064f44d68ddd3c05698e06fa0ec56c6d30056d3022ba9131afbdec991f`

```dockerfile
```

-	Layers:
	-	`sha256:e44d43909d0b65bb6062b829a08fa71379011f239e9961be692005b3a7eacd7e`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 4.1 MB (4117244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c354c21414166eba7b44e24da885fb46a33d353d01989d0d439796286e15496`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f752d9ac135bb6d787e6ff54b52e5df60c920121db82e933c41ca23f4bb8bd50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80160096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c7c298949555a06b9f9e33419e2dd975ecc753299ed84ea30f2be60784cece`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f80d2a3204cde8ea1e7cf5156c0b0e385216cbdcc894bd75c3d81ec51271e`  
		Last Modified: Wed, 24 Jun 2026 03:26:58 GMT  
		Size: 27.0 MB (27022027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12ad38aab3ef5e2549ab13b78a4a00ff05e8285533ba9f92b2fdc73debca8073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7045674054c02eed8e48440adf59d03f9c39ae36e3e7c67fb0fb09f39dd85266`

```dockerfile
```

-	Layers:
	-	`sha256:af693b82a32da41a551c74070d35701873506efb6ff1f12055838898f075bc57`  
		Last Modified: Wed, 24 Jun 2026 03:26:57 GMT  
		Size: 4.1 MB (4123985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564bca34edcc1c6bfe6ae8a3219a9c29f611a4f9146a9238761d4abac53a8d2f`  
		Last Modified: Wed, 24 Jun 2026 03:26:56 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1998c7c27325653fdbf188577efd1e97f724854a82a185594fc73590267e9506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72771707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72329d0a94dbebfa07705b782ffac4c028e3fbc906417313e623b34fc26704c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Sat, 27 Jun 2026 16:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:68b05b25f9ac1e0d14e55abeddcd8bd010c0b74e64761b736e55e1ae65501399`  
		Last Modified: Wed, 24 Jun 2026 03:40:06 GMT  
		Size: 47.8 MB (47802658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38215cc1fb71b3f12158a195db4a3a178efcb8a54e7878031484fca1958c3ed9`  
		Last Modified: Sat, 27 Jun 2026 16:21:47 GMT  
		Size: 25.0 MB (24969049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da5dae7657f9bba0334aeb98df0592b7595589180fa53f14f09d4f49b089c1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f89ecd82ac5d264144112d43d363f323310c2aa27a943d177777591272320`

```dockerfile
```

-	Layers:
	-	`sha256:84317d632cf20ee913cfec0855ffbeb87b31e66d38004cc4698c232d7e0c29f0`  
		Last Modified: Sat, 27 Jun 2026 16:21:44 GMT  
		Size: 4.1 MB (4112685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58639ad38e980f2202a8d07ededa15563cac7e6fb65d3f1e47ce76ddf79901ab`  
		Last Modified: Sat, 27 Jun 2026 16:21:42 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:de4d16b3a9f3ee7ca01deb2e3230f1e5bc339257f7f3c06f8d91c0524eb2ce6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76190005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bca96160c6f746f66e3eacac06c4c64ae36313ac4165664b781b4ccfc09056`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ad8b668881e5b88baa7f13010c93f1bce4021cd7e873db608fc3d64c83f78`  
		Last Modified: Wed, 24 Jun 2026 02:46:45 GMT  
		Size: 26.8 MB (26803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f514ae6e70e898d094db15f81c9948fc7e4ae7354d79db2ba146aff12393d631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffc84893c41d8bcf2e10089a871de5bde9c3caa5c442ffc9b5d8b4a925ec2e2`

```dockerfile
```

-	Layers:
	-	`sha256:7ca84fa567e81e33a6da09913cb83500c1cc1c44ea229b334852e74c9832a7c6`  
		Last Modified: Wed, 24 Jun 2026 02:46:45 GMT  
		Size: 4.1 MB (4121547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cac083c66bdc7a624a16e62d3ec52b1cabffdc8b2130801c0d2c160ca8bf84`  
		Last Modified: Wed, 24 Jun 2026 02:46:44 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
