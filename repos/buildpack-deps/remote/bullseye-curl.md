## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:a70900a2815acc732a8671bbb3eb583d761de18b62cee908d9c2c325d05f3cd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8fd9b6d499d820703e6a5da5b3c5f4f7ec4f7bcb01dbee6dcc3495ed66ddefb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69553827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8995f3efc4a51f2d74fc6011bf8b083040689645f4fed15d8bb8152762807c30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 05:00:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210b2030df8684a29d3d6bdd62a8d151c73a23016c72c44011c839c8d24c516`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97686c9ffadd75aa9cb138a42434bd4b25b4323cc7445461d94a93588f17ac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0334d1fdc1b7e85ee470ce311452b569f23e1efb068f19826f2fefd21e7839c8`

```dockerfile
```

-	Layers:
	-	`sha256:1e137ffd8f84353c967cf867252b7e328edffabc528ea89e7f1a94c4feff1293`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75deb7d22e409b63fb71dfd438b5bd85ac9424be4425229feb9f51166c2199e`  
		Last Modified: Wed, 22 Apr 2026 05:01:05 GMT  
		Size: 6.8 KB (6763 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88792bfee08945bf9d3f845bfd36c485db15e24a54555e1718ec09a915bc5eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63960109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba7b7e1cddc65251e75d95233043d65b95a36455567295da5fe976050239347`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b7f7b3cfb222580c94a933dbaaabd959ea960847c9aff9c5d4daa21494eea44d`  
		Last Modified: Wed, 22 Apr 2026 00:16:47 GMT  
		Size: 49.1 MB (49055006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698f04c927addec960608562122b5f1c50ad262b50810e813b3046303555106`  
		Last Modified: Wed, 22 Apr 2026 02:18:42 GMT  
		Size: 14.9 MB (14905103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f65ae5b312224edc77aab115226bec83354558cabb8447081b1aa6ef5c832877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58eba3d66e739f79b33dd2ca199c479324ce00bd5c07ec3773970b9e32f1ab3d`

```dockerfile
```

-	Layers:
	-	`sha256:e31093404921be4d1461806b364d96bbea76102d09c4c4a5bae71f1805ca993a`  
		Last Modified: Wed, 22 Apr 2026 02:18:41 GMT  
		Size: 4.6 MB (4639155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc8fb74b7e8cc96b172f35f065f4a91f86f0a1c61b2def0a1b46229476d2dde`  
		Last Modified: Wed, 22 Apr 2026 02:18:41 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dc94a7d5f3db3f3012da79e49c8ccbe4a51885ec1214c91e91a3fdbb00fae471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68027738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de5898bd2260adb289bc031a6dba65a74f504c9db026fb75d314b5565215ae3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5711adc3a36d05a8bc3715476e3933855fa726e65b89767e0db83ce72e755408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412ba69f5ca0a8ba6e5b10063bbe944114f80a8ff8acdd00a47d34294a3575b4`

```dockerfile
```

-	Layers:
	-	`sha256:4d896ace626dfe99f0458d3befac0d34024c43c0fe1b51326c54e5a897374263`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b940d273c2f68ab87dc10709d11c0a3c6668db4c15e8c13a1808a4d154f80c60`  
		Last Modified: Wed, 22 Apr 2026 01:43:07 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b880b11f35c35c60f65ee0dca15efebe9ad51b04d8d94cf60b73b5bc9355b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70998248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcda4bc8e14438b86e8181356eca7b3615d306d104f07fed3d16c80b21400e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d7ea2b68c41d012b622a11d60c4b7330f09ed012ac9774c3894afce154803`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 16.3 MB (16295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a8257eccafbbe56178a7458911c43a4ea05bbe38b19fe92cac6e33b57ffe1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837395334e162d6f955063ea7ba8e226c2899b6ba704023321456a0732d2ce0`

```dockerfile
```

-	Layers:
	-	`sha256:ad006909ff315e8695b187222dcb2a02fb0040a880e495bdf9a1601bbbbf0e68`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ad3125b07c502e0991f3600cc27cc675e566fcceae41b22b47dd4ce9b39450`  
		Last Modified: Tue, 07 Apr 2026 01:46:10 GMT  
		Size: 6.7 KB (6741 bytes)  
		MIME: application/vnd.in-toto+json
