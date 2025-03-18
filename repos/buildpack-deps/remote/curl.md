## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b59beed764615daa96c9cacb06bf55c97a657994603991cfc7d6217cfc6528cf
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:333ba289c859bc57d408574b988b31ca7bf9777b365c8da64727f68715518ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72478974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91801a68eb85de45a01bc36d92280721736a7c5addac6e78d6ff05e8863273d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1423d97832283b5e2ed67f50a74444591d141c6e67b38f6e74c4694f6cd33d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b745e7c43332a1de3470761d50c97fdd44a58e8664ae8126a8a2f460e71e45`

```dockerfile
```

-	Layers:
	-	`sha256:cadc62ac2ff74e0b0dcdb09f35881911d51a9b56d6fa9e01d3fb8bbf884b4bf1`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 4.4 MB (4358719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7bd7d08515975ecfc9ab42446b6b307e7b9f12fad7ab1a29fc84288afe0886`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:412a7858d5d2b13cd0cabb32ac273d9d4d6a8a8a33edf4973834011e6c10e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e201fa2120f6eba36dc73ea0a23a04c148cb1833e9795ed6999f1044fec2893e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e0a2dd0a028ee7f43adadc6c0243fddd3c703276a18e7f6301dd144d3567f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b1cfae99e9094a505d09ae33a13e40f85d367b71d17521a1737b58343665c`

```dockerfile
```

-	Layers:
	-	`sha256:1b38b60175baeea066a33aca4fe7b41cfd46c5baaafc26d52e148a9b565d4257`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 4.4 MB (4362843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc8ba87420f080d009d7ce34eec7a3661c5d6104ef08301a75ec178718f0efa`  
		Last Modified: Tue, 25 Feb 2025 05:15:58 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fedf677819399a4890675c080321b90777145ff180f1bc5e898e08f90a5edc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66140264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306115598a20b03b481cbfa53bfed30439d9081b3b1375178e8faa774626ea29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b9c68c614a4c1f964afe9a02e198e5347d8dbdf78f7f27b4837ff62df20b7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca217b092fa607ec7caafc4624772ad5487594f01bed66087730ef3f48144d`

```dockerfile
```

-	Layers:
	-	`sha256:6ea2228bc6a164dff1000cd503782edc90c75465167cd7bc802972cea0e20b88`  
		Last Modified: Tue, 25 Feb 2025 07:16:40 GMT  
		Size: 4.4 MB (4361624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88db7765a141e0f0d5d0f08695e6933b109a96c3e6d97b7410923ba391968eaf`  
		Last Modified: Tue, 25 Feb 2025 07:16:40 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a4ef43b568706d91b533aeb28acf2c15661b6c9d1b332c6b37dcd7d00a617815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71906283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af06db0784df741a129793e7649834bf226f75267ca9a13fb1f7d778acbe53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a57e0bcf173d3b353fa426debbd70cea1ab1c8bb888258912fc6341cb655b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496c3d74367b4b2ec8ce6f126f251d40c10384380f59bde82c4ce9e57ff1f07`

```dockerfile
```

-	Layers:
	-	`sha256:9e8867348647a6bae854812be326d7979077790bec5cf7f1213b6d02f74a2c70`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 4.4 MB (4359600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf94d50991dd56e8e28e665c9bf6d429cd456ae48d74153e45e0833d753304e`  
		Last Modified: Tue, 25 Feb 2025 05:41:43 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3a141c1432df22e29e37a42f4f6a1a60774084f91c8ba65a516998b18e8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74301460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220fd3a6b367a2c721642b722d19ee3bbaaad040b003f9b5e717d9f7ed9c02ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e191898e03a9782c13272045f7c55ec3abba0174528b7c635be75c551b3666f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4362914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1a93929ace3d5733d664f48003ce09b2db814956b8e6216c85d333c7064ea`

```dockerfile
```

-	Layers:
	-	`sha256:c1bbbab70569adc06d7f1bf40195f8fa2bd794936bbbfa4620c4a86e6960adac`  
		Last Modified: Mon, 17 Mar 2025 23:32:44 GMT  
		Size: 4.4 MB (4355777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ce43ffd9f989625a81736199dd41bedfe80e8130176685aa757d25de4db1d6`  
		Last Modified: Mon, 17 Mar 2025 23:32:44 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4492593db5b2f8e7f63c2d231fac0fb4f7a016b9632fcd32fd1727d1c0abbc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72411228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f00d52ae6489c5983fe113e4856c858040228d832aeef87e6290c4161d70be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc8b0d2c1cd2c1e69321c8754130d87eb745727f395a5bdd21269faaa9028653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4966027f91ba6c5a99246844583b24c07f2a7ec2a026d74692a6738394106247`

```dockerfile
```

-	Layers:
	-	`sha256:837e8dcf97e3764dedfbe87eeb376a92a0c7ba8355c755872923a19d8ea31b87`  
		Last Modified: Tue, 25 Feb 2025 14:48:24 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:077a34637a749b3a43099c51c786c607832092ac323697d123eab7114ca58f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78025725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e2b28a6c13dfde19c69f4c01304280791a8b51790c658c2ea64ac0126a13c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:15c60896edbdad9a10030d589bf85bcf3fb1c0802becc396e2fd0f7f928e0229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce4f8aede9958fdd2a5370299126de5bd6b9635e2ee49ed994b766196e247c7`

```dockerfile
```

-	Layers:
	-	`sha256:5300fe4fb6e4fea4577d8f9e0b1f50a94d878ee9db340d9cfccf7560cfbdf638`  
		Last Modified: Tue, 25 Feb 2025 04:32:33 GMT  
		Size: 4.4 MB (4363821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb736f27de1f13f3da09799b86227266509c85e37d0d9bc6e6148d3318f3034`  
		Last Modified: Tue, 25 Feb 2025 04:32:33 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53ea1f604f83a98e6b818095fc926631c7fc1463aceb13f81d1ed725eed59725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71187731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dbcd045e2ced314d65e9122112e5912e50ca3ddbca7accf720dade201c7b4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f17e6d44962cf75a1f49524e69d8f90a37aacd08a9b881e6d35bc9991524cd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c98e27105a35f40832f09c1317b88642562f618bfa3c64709c66f28885d10`

```dockerfile
```

-	Layers:
	-	`sha256:f3139b8c795033539ae18c779681f4298ea316807f277e0a22283ec327841060`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 4.4 MB (4359023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bff308ba27084c9be8a478673ad8b387758198fb246b1bded1c69816c74c44`  
		Last Modified: Tue, 25 Feb 2025 04:04:14 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
