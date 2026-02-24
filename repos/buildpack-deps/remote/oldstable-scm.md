## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:82b253992d84168372cd737a37a9edc9196e71bb0527fa14d1255ea97a8bf876
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:45655e802c96cc2cea34b911ef66b769f1c37cd34a5a5ec78d3b56dd3f25b4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136923080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2c35f2ef975b98fec39c19fb49e1d7f095041902b367786e104fb94653368f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e99e22cd442fce918372ae0672abc187f10d1c419b06624a99e7de4399db800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8243332ecf3f21237c93d31131902e9869c9273a54083e2e81940d72180de6`

```dockerfile
```

-	Layers:
	-	`sha256:2fad9f513a8a2846afa2e29b18ed5de72ccd766ee69f9b2bc6ba1d642ee42e13`  
		Last Modified: Tue, 24 Feb 2026 20:03:47 GMT  
		Size: 8.0 MB (7966048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5015bbc8d768c9ddb27d90417a72a7843eaa26a68df2a9ac8b5f9a3ac40ccc04`  
		Last Modified: Tue, 24 Feb 2026 20:03:47 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1e77683fd6494b50e1ad1899b060d649c71422f68d6f0a7564486c3bdce6c642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130739375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c57ccb190748ef26d32c983a8909f70764eb425e13eb35e2304ccf83904d87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c031851c0852eda9cc103afa92ccd1ccefa07dd936a71f291d45de349d70b`  
		Last Modified: Tue, 03 Feb 2026 03:26:08 GMT  
		Size: 22.7 MB (22713907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2787358314b0b690e6368b20e1faf8551e6eaee19cdf0cf05d8e0a7e3fd0707`  
		Last Modified: Tue, 03 Feb 2026 05:17:27 GMT  
		Size: 62.0 MB (62008804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:071c718d4cc4f92cd5ffe292cf7b3d6ba99bba526e88aca7ed68d925f03a92c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f52043c605ee639e66f92e29ebccb6b62ce8a52c6463a8247b8883b5e80401`

```dockerfile
```

-	Layers:
	-	`sha256:8bbf21d96e702aaa79cbbd07e750bd80c2ac8a36458129d580527992b35ddf39`  
		Last Modified: Tue, 03 Feb 2026 05:17:26 GMT  
		Size: 8.0 MB (7967906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a61e724931bf00c300195508df2bc5471d323dcdf3c199092220de9f6caca3c`  
		Last Modified: Tue, 03 Feb 2026 05:17:25 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e6fae156bcb3c0274277d65b3d4df820ee140f4a029ac5869e040f1c6dac3f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125792740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e57ecbbfb94918fc1febb684b447b2afe6bedee2595aea7a8f7690090d17c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc85f3c50fed0bdb934cfb613c0b9993dc7d11efbc5fa0e6603e774332fda614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261ada7f281d60463b0990b2a4fe7ee887ffc87506964b509fc1d096907f0e34`

```dockerfile
```

-	Layers:
	-	`sha256:5cb9f823d3f3f20006368806335bdbe2bd946dc062250e283d810bd5e991f4b6`  
		Last Modified: Tue, 03 Feb 2026 05:00:08 GMT  
		Size: 8.0 MB (7967325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f673e4acf83b18de624e2abe21d1e389afecc7267aea42cb849732e5687ee3`  
		Last Modified: Tue, 03 Feb 2026 05:00:09 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:eaa4cc0d5212baae6cf6ca0f138b69132620f1631c2f025a3183fa39cf2d0b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136457352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f1c9426a86be484f114945c17ce21c27f35853e3d3dc88e13cfc0b2ac8e8dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c39c531b66f3f6ea78e256ed7460183a593ce258b0fcb0cd4701a751bb847c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34010e4679f5c5e70ca8a5581d26ec253f9ccbdaac13b4f56b9720dc3f28a300`

```dockerfile
```

-	Layers:
	-	`sha256:bc7481c804221f6d06cf56e2384bddc197128afa9ac507bfeb2f89ecf806142f`  
		Last Modified: Tue, 24 Feb 2026 20:14:45 GMT  
		Size: 8.0 MB (7972441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1ad9ef023c28ce8dd4f6dd1b527356a26323a701dcb4d15c973193f5d32e73`  
		Last Modified: Tue, 24 Feb 2026 20:14:45 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:046e2e3a969f690870ec5dc71e258b26e53edb44a573462268680afa4fc62493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140584293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2822edf2db0b4597235414de18776f21df5d0e57d30ba9999515c9a81c400c56`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04fe9c72d7fa8d2bd1d4f2b2c4e0ee114d0eea8ab54b1678d69f3b09b792de0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45349b218340753f2bdaede2715a79e09f2be53c9062dc86c3eb930e6ca37c1e`

```dockerfile
```

-	Layers:
	-	`sha256:3097d6195a57fe23464b759b274ed1264f5cbcff12d5dc086becc382fb78f1c0`  
		Last Modified: Tue, 24 Feb 2026 19:56:52 GMT  
		Size: 8.0 MB (7962206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f49d38d5e8778cd2cf75ece98d48d895fa3060bc67312f0209b6064c11e10bd`  
		Last Modified: Tue, 24 Feb 2026 19:56:51 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7a32433cd56f1f31eb109dfd82d4c327949c05b22c99c61767451a6ce893c678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135688763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08758f28469338dadbdf1ed32baa80fb05f77a65cb4806c65e361066ffe6bc6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3311450b458a6185e8fb0e80f3a9e961ca2a9d92737c05b66ae73aaeee4045dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79506d16b61b0e5a7fd99bbf0c88a10b1dad5ddc3d031061cd0fe41e16701066`

```dockerfile
```

-	Layers:
	-	`sha256:85dba8d5df2ee0b6d6efba7370d977b78d7810e08c666e5f10492e6b26015328`  
		Last Modified: Tue, 03 Feb 2026 21:29:52 GMT  
		Size: 7.1 KB (7142 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:874a19c2546d1d1878efb4063a91b147af018a2183c0dbab55de16d37ed27c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5ed6dccca7776cdc0be44c1c3fbcfd4cc026ed02d8e6893297183e21b53fee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a51ced8d571f3701d95b4933306e6eddba8a91934a22cc15e6712a21500c098f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776e4f099f35459e64f77982e19fdd6aff5e14fec3a57327f11945e2df50d0f9`

```dockerfile
```

-	Layers:
	-	`sha256:cd0c8fa1d6bbc8863de13045ba046335a021cf75fcb71c39dc92a6549a14bab5`  
		Last Modified: Tue, 03 Feb 2026 10:36:18 GMT  
		Size: 8.0 MB (7973921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bd81d8a82a340569994e29562f8f0fb68a2bf7a82b975addbf5d3fee839f5c`  
		Last Modified: Tue, 03 Feb 2026 10:36:18 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3f5d7f7711b70f8436ecdca206c32c8830c63eee2ff3d51b00c3ce73823b24d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134673296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2194c9c37c4f210263a6b9ddd00dcea2c974d027ad219e3e4e6a9c1245d3c03d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dff4055e76a9684e3c207d34e4d974f19698bc50ea5cb5a641815dbe3a68458d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49de26c5c65e684080e7a79a6ea77e687bd1276379e30730da88345b7a55ffc1`

```dockerfile
```

-	Layers:
	-	`sha256:b456ee3158088962f210826487e6fd56e6def69ef609a0f91473508b8bb2e40a`  
		Last Modified: Tue, 03 Feb 2026 05:29:10 GMT  
		Size: 8.0 MB (7962361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abf999e9d9b9caeb9f6a2aead2e5a1d4fb0589e510667ee588e327d1a61ec58`  
		Last Modified: Tue, 03 Feb 2026 05:29:09 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
