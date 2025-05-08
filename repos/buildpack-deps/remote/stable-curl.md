## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:40c9814cceca9145f1afd1f1fb64e1d908508b9a6f65d4078a2a2fe0e5fc814e
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:66af74907dbbf8b0b007f1364cfb5533d82b0914d637c5301d66debd326b5bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72502380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66778ca3ecca132ae2e3be9f9a8816c3d6c40cb971e200c41a3f5290dad963f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4381a2b2cc6a99c2a4ffa943e12de2a3b440472c92260a91358a6538faabe30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c0832bdbf3d4024494f0f35041fa87e24e76195abb8517155a69f34eb7029a`

```dockerfile
```

-	Layers:
	-	`sha256:a0219f42489d77927b354aa04cb7ac25d3f22081c950ff62e02f3f036ac57664`  
		Last Modified: Mon, 28 Apr 2025 21:55:01 GMT  
		Size: 4.4 MB (4360055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10113efd0c00dc03f7ef0ab683562a3ac0b0440a3f69563911df606e74ceda3`  
		Last Modified: Mon, 28 Apr 2025 21:55:01 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fd0a9191a7eb02b6c3bccbb1b41995236b2eabffc409be8c1d722a3d5e6730d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68716403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4cb1b2ed38e032cbecaca3941967d88c0a86095d2bf1bd31ac940c62c04e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Thu, 08 May 2025 17:16:08 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Thu, 08 May 2025 17:15:59 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:742876fac13ce544d8882de3eae68884a7d2fd99ff936ecbdcde548ae756534d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f32db5199791a1f1a7dd25d001bf795a8fceedbc17a2a7d8656286e2fbb0130`

```dockerfile
```

-	Layers:
	-	`sha256:f4f25b9a4c3bdd9e99998078c4774634ffc897a49e9e4eacc1d413d039d720fb`  
		Last Modified: Tue, 29 Apr 2025 06:01:07 GMT  
		Size: 4.4 MB (4363571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4547fa1239e1de22e8bf2c80ce3697efa757edd69d0a9d87fe6d22bbae4050`  
		Last Modified: Tue, 29 Apr 2025 06:01:07 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:03be2117ca76816e60376f354f461f9ec41c9ecece12de0e912a17bcd08c750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66115459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9541b72dc9e642a552e24400d3aac522bbc6152f2a3b13f307c88796f47e79`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf56165bd6609a96fa12ae543c98671c91f9f8589ec5da06865f400bcb82b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b1c3e1c3fe5f913e5c1161a56390668f04f492b3941b7a142d2cdb7762c663`

```dockerfile
```

-	Layers:
	-	`sha256:9afe102eefb178dc1cc2e6d7d567d3f3bf5fd160ff2d64f6980b9aaff8a33cfc`  
		Last Modified: Tue, 29 Apr 2025 03:37:09 GMT  
		Size: 4.4 MB (4362352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e020a108c214db5ff60dbe30b35864032a33a7fe5a5162e50a50a5a3b9e0742`  
		Last Modified: Tue, 29 Apr 2025 03:37:09 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0683af870983173bafa168a23035a91fe23b5bf2c5ccdc71a5a1c55dc3d1d916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71871906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97df11a7fc7a751747ee399e5d51ab5c0fa0824735a501b4a14f86b4bfe4657c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a586350b4312a080d8aa2fecb652afc0964a4e8290c103034519c139558b2f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b01cda863f04fa328fbbd0f9367ed1307f66f97e8729effe1c05b67a4a2e98b`

```dockerfile
```

-	Layers:
	-	`sha256:cfa1777d560a7c0edfecc0cd59ea47c83aed7cd3ca9455f2f96ee5f027b13128`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 4.4 MB (4360328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd65370d2e06f01caca66b553116ab9d0ecbdd03bb457a9de071c97de6725d1`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e2682489f49c6b2ef640e27da40f0b455c2e0cc22643aa8a1794ce26206d52dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74325719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28bb7e701b08f2c5d0a26b3746f00c6e92c9f6d49389b2be2fa21d2d58f3e3a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:edba52975ea1a893d184f0bc466c88dda42c467bb3b1576a1e12a02d1a02b326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2539bfcce893fb91748e8637c274feb036ebbf4a60ebab7ff17c3fbca0473b54`

```dockerfile
```

-	Layers:
	-	`sha256:f5f2461f65e1ee57f8a9428de80797091ac584b96e2648cb00cf660ed78ebe6c`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 4.4 MB (4357113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718e0351d6be1e86a0f14b942d13972f8513aa01c6e4f97f00ab329a64fad225`  
		Last Modified: Mon, 28 Apr 2025 21:53:41 GMT  
		Size: 7.1 KB (7136 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cb356d116a4a104ca1f758dc5f2feed606eb32efa6462ce92999ca3aa4ded131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72371172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d8a493bd40f7ed61fd101abcc6a3eb89861f539415b6f03f5d309605aea27a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b81b39dfef5af9dc36de02aa1ed5ac9c4d2aba72eee5fad0298da6a76ea75b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17eadc4b49695cb90bb05b3daada4ab3d45ab822df17d67d2b92a001879f047`

```dockerfile
```

-	Layers:
	-	`sha256:a640a82e6746f646005a34771412d8f757bd27fd1a219bcde3ec57528a21d6e0`  
		Last Modified: Tue, 29 Apr 2025 12:43:04 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:397e3a744730470f2fc3e64dc07818c78c5eb0e2e055196071cf7436c3222191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77982242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8e20244762847dbfa5cfeca6ddd4f8eac6343b4a1a41ce79f0fc7f30e5731a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Thu, 08 May 2025 17:13:13 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5856b90bd67a9f0a17ac7095de7a195af578be87a31978bcb1d52222dac36bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220d9acb963f8af1ddcbd847918d0eb02b3399ece16240a73d837928e0931f6c`

```dockerfile
```

-	Layers:
	-	`sha256:feb2296affa42ce46c4f7a2bed3dddc92edb61703dfbff0010c848279dd7833b`  
		Last Modified: Tue, 29 Apr 2025 07:46:57 GMT  
		Size: 4.4 MB (4364547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8bd32208839f078b5ccd2fab2ea6e468d5d730d92c36b371355c027188eb50`  
		Last Modified: Tue, 29 Apr 2025 07:46:57 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:48ac7c92f1b0b6dd171159d652f5c6f36b78c70c982eb0c08e1056c180a3022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71159643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f80b2ce834ef28f5e1e0ed7b906b9f54bb71b878f93c3c93954fee621c70a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Thu, 08 May 2025 17:16:24 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45717e793366a78b4a3fa84c09c90cb3a210d3bc76381cc1f99b21596dee31c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ebbb2957bcf81b3ccc467e9b6d8eff3e482af8862b87a7c6b00fa260476ce6`

```dockerfile
```

-	Layers:
	-	`sha256:30fdc883177de49dbb75024e4f42cbc733d7a002328b317245ceb0040b4e73a8`  
		Last Modified: Tue, 29 Apr 2025 00:01:20 GMT  
		Size: 4.4 MB (4359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad7232f4813cd45c6d4470f8c447f041b60ad0a113e10cd2c92cab1b94d8ff8`  
		Last Modified: Tue, 29 Apr 2025 00:01:20 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
