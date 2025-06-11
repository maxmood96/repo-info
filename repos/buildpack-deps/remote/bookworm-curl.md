## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:b408f4b91b9d5c695d0eb888ac9e1fce29ab00039202b195f8ce3ec0ab57fc1f
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a402fd948d62e1f1ae75d8a6a0559296213443a90f29500f23d9c6d729c510e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72509980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83445ea8dc0a615caddd520325738d8331e4b1e65aaee7d3a8c0959fe0d0342`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bba18db24014ba5bfcf65486d97507ea1dcd897186714dabdded994f639dc9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4513030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14e184c90dda6f9defee457af07d3556dba25ce1875f8e5d584800fd3696575`

```dockerfile
```

-	Layers:
	-	`sha256:9a6b0d8a0d8881e7182dca2ee0b5d64c57786b106ddcae2d501523044b62677e`  
		Last Modified: Wed, 11 Jun 2025 00:07:16 GMT  
		Size: 4.5 MB (4505866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f960db62a55ce9ce278a0c9f609ff6a0d4c80e22ce1877609039295afeed7247`  
		Last Modified: Wed, 11 Jun 2025 00:07:15 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7cbad7a9ffc6a8484c45f0baf74e249db60b52314c5fffa93eefef7f48d09a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68715669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f75ab7ac04fd49e705b10f41505e5049afbf4d7bdf725a7d70aa4a131ff38b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b51cc5977be0e2fae0a0314b991e4f90fafc6823a929775d09884dc18bcd7`  
		Last Modified: Tue, 03 Jun 2025 14:43:54 GMT  
		Size: 22.7 MB (22694185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ad6ab4db9d0e46e95e95d909e4236ff260487e6e399fa8212617f84800b5c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4394774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f625a91de2549a9a5da6bf452f89853827ca701f89d14da25a7c7774c9301d`

```dockerfile
```

-	Layers:
	-	`sha256:5d62cc7ec17b7c3146d38f1b1843a920d5f722b50fc8c6b28841574480f95e2b`  
		Last Modified: Thu, 05 Jun 2025 13:07:23 GMT  
		Size: 4.4 MB (4387542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9febb84fea7b4982d7295ed81b767124923f206c161ab4684ae85a217f4ad54a`  
		Last Modified: Thu, 05 Jun 2025 13:07:25 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:febaf867189f9e8f0f5cfb6b09c8ec232e8e38f1def3e5071c32685773e5680d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66127406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767fbfd5efeb8c1758f00290ec1da9ba76e465d10dbf2465e9b1cf3af839e305`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70cbd5c4a00799f7b89e8635110c4e93c7982206d48ff6902aab07e010376398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4393246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca1e86bb29c224db06f08e715626d66193ee8818c5dbccb7b39f055d01c8098`

```dockerfile
```

-	Layers:
	-	`sha256:86b141f8243215d55a1958ae7ad3976a4eedaa5ae52612dac7b5beb2059794bc`  
		Last Modified: Thu, 05 Jun 2025 13:07:28 GMT  
		Size: 4.4 MB (4386015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8527f7ed9a14260daefce28a6c6517590a705e98ffaa4b2674c0db07515c23c7`  
		Last Modified: Thu, 05 Jun 2025 13:07:30 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b548321d9e1abe839dabfb56eb21104d5a176fba6feb7697b226430144be3dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71878579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c887e4316a568557e928bf1b9000e944a303c2e12ca62e60347ae914547c6be1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96a611779207a9c05359d8f8342f67870ce51bd9cb40819e2282fa39cf7cc02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b309c3cc1029c5317675d83f1bda0d3b8e98e5dd0d37c85ef008e9a207250a`

```dockerfile
```

-	Layers:
	-	`sha256:14e47119ede993a31135b049ef3f05dd2c5ff62ed409c94d316cbb3d0cb67a58`  
		Last Modified: Thu, 05 Jun 2025 13:07:34 GMT  
		Size: 4.4 MB (4383991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe160ab997f00248adfe85e7b5c2601e8ddbdc14b8acd536fd4ab6dbf3994bdb`  
		Last Modified: Thu, 05 Jun 2025 13:07:36 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e0c8bbd81831c468bd34e8895d75caf2bd3d7d1753526ebc05dd7b27901b0fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74333180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e3de12fb61ab63fc1aa8a4fcc5977bda270874ee09a2512cf11a51d2e453`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c75f4bec42d705c7461dafeca15f760baded20b8c9c51e46af0486bae92b6d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee2c18a14e2247535ad23558ffa27b90b3532c7b650247fb85ab76a48693b1`

```dockerfile
```

-	Layers:
	-	`sha256:229d236f7698edca5239178dfc367ac38618184e5685384c0b493b69b268f474`  
		Last Modified: Wed, 11 Jun 2025 01:20:13 GMT  
		Size: 4.5 MB (4502986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff30beb93213cb3822b0d65631703fbea63d5ca2bdbd9f9c65439fcd8e52b171`  
		Last Modified: Wed, 11 Jun 2025 01:20:14 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bde0b234b62790a825c929bacf4e4fefe0fb0f3e16fa5db0663767f401068f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72368366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eb836e49d6dd33e836fd0f277f58571c7e846c70521629bbec375c959e9085`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5969b50970c631564ddd670b0af2622f135fc52a0d7582e9980f536935283e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70de946090286097339c2692af0397f80ccd82314d0fe296bcd6cbe48fa09ba`

```dockerfile
```

-	Layers:
	-	`sha256:36fc14c9036ed037ab3d98c089ec73aee8ae37da2618d6ce536435277d59201f`  
		Last Modified: Thu, 05 Jun 2025 13:07:44 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2ed85b76397ecc3c35352ae354419a4a63cb6d200e90f55b4a33c43461e01cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77988916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884bbe6ff02f91883d58b5a423fdd84683a14829c57a44b7f578397a299cb4a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b76f20b7a6db2e5b39870d22db6b0bb21da6e4ec39811f3802a8cc5a1afde93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4395540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda24d2f55caaa586123f573e42802b100e75c86198ebc758f125b215bf7002`

```dockerfile
```

-	Layers:
	-	`sha256:0d4bc0f9d7ae33da9fdb29b5ac68a4657327916008a8fea9ea00353cd8e2b452`  
		Last Modified: Thu, 05 Jun 2025 13:07:50 GMT  
		Size: 4.4 MB (4388338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b23babb05ffbbb217827ff8f988748256c3be4259614a786aac7bd35e4ca041`  
		Last Modified: Thu, 05 Jun 2025 13:07:52 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9f3b41f02ab360de65902e326908ac8a7e5a71789ee102ab377b36e4def63723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71158698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8504d40974c221d20e9ae117c3e9ee41c2ead70dda2f9e23d33e84b56b52dc9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ca0532c045354fc9114cb4fe202274e477bdd9c8fa8f696b3b1237e3c19b166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4390578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce000f6b82d6c43621635313ae3ff9915997b423183bf297d1b2a90921c27c84`

```dockerfile
```

-	Layers:
	-	`sha256:dd82f7d8b79d27e9d4a03982373372d633092b8b7ebc71b8f1d6c27a981a348a`  
		Last Modified: Thu, 05 Jun 2025 13:07:55 GMT  
		Size: 4.4 MB (4383414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda9c842d794f54ee63f1dbfa35205fefc38a1fb84dc369ed1847dd004c0db22`  
		Last Modified: Thu, 05 Jun 2025 13:07:57 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
