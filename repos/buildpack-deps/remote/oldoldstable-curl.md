## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:ee1416924756640319d0192db5c3beb52dad6dcc3ca953c029f2c276309e5855
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

### `buildpack-deps:oldoldstable-curl` - linux; amd64

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

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

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

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8c226d8482cd4116684fc284172431affb779c2c645dc27f28e29a650f8cccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68028044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce33f7d8e6aa3719c56930b119851055b9f54200e68626b3ccb76ff8fe45ca1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d20a72a3ae72af0f6239652b45dcc6f5eda87bb797e4c05972c586c32afca3f`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 15.8 MB (15774834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:992b3d6330dcd43af0ef3b5c351de937dd4b704d3d4f87f05d6150f5d37d2798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c129b228dd57bbb5f0fa98b9093e66e28661020d73a47ad60a7601cced03a18c`

```dockerfile
```

-	Layers:
	-	`sha256:aa73aea84017ee42d0521e2e41899558f5e43b9e0ae5b3ae5ae1af28fc0af7ad`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d341aab8e205eafc8124bb4a0eb76602588e4e5fbc839b5a36292dba05233e`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 6.8 KB (6843 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8a4731252c0b2089d66b842a5dbd381239474f7b13d30618750d41f2794b5b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71000777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c1247f770f724ee456b4f8fcdf9214c9cfb2a97d2463e2d137bd8da8ab26ad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f313e1ea7e09266848088c3a09b07b715bfc6a8bb9980dc9b80da0fb20132694`  
		Last Modified: Wed, 22 Apr 2026 01:43:07 GMT  
		Size: 16.3 MB (16295616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:78024333cd52f507691097100dcd9b76a8f6d1d4095953ddeede643952dae2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8e7985302483187c92a68a440b6ad6fc10198e24bc2562518c113b7bde94d`

```dockerfile
```

-	Layers:
	-	`sha256:05cb6d9c0c0921703d421c832df36f6bcca253def0ad494f2ca052bd88ed96ce`  
		Last Modified: Wed, 22 Apr 2026 01:43:04 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934485b578366b0d798eeafd44fca4a847f2a8eec2aff421205ef9394d33a3e1`  
		Last Modified: Wed, 22 Apr 2026 01:43:02 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
