## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:ef58de48c98b6c354912ffdfa61302bda7c7d0e676d38c686a5c21eb153931cc
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2c9e1f04f2efc5e43cb4d4dfa874460e4b309cbdc9a857112f1e1a77aa70d5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69515069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27383dbfb9fa1f9ab19021b6c6a89f97f0d2ce96465f3d712d45e09659fdd9ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:806b730332a971ab3bc219f4a362748aa1fabf7434344b41f2fda1b9e5bbc32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d144f38e99e86275c4e511d87bc3959ad716bb67378a583d1a6029059982f436`

```dockerfile
```

-	Layers:
	-	`sha256:61cc2ae18839c218d7505e92e3c3072cae17c848614613f936a818305a6977ca`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 4.5 MB (4513309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:063335964d518ff4557a9546ebafaddf626a0677e22018e96ed07690484f9a12`  
		Last Modified: Wed, 21 May 2025 23:20:28 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d14988f7c7c894c48c7da779a89f8c532b8e4395080c747d17ba604cc8d927a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63919074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637d5ab9034b7391a56654eef6653d91512dbb54aa6f9197788c3a43c2eb0955`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2846922343e82f242ebb6628c32238c38d795f3b40aeb0b0b490c7150df09e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da6fd7296d29d283b2551f15de22985b4b530782a2feb549941a4bff940000c`

```dockerfile
```

-	Layers:
	-	`sha256:2965beefe878e8f2c79404960ba551f702afe9f0e596bffe23aed63686109875`  
		Last Modified: Tue, 29 Apr 2025 03:37:43 GMT  
		Size: 4.5 MB (4489231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2885fabfad51fa6993820e91f78f0b7a19758d41981f55ae32fedcd1c53f0a`  
		Last Modified: Tue, 29 Apr 2025 03:37:43 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e1bebc1a7c7f1a71aab7f1ae5ac7899cab503b2fa6112f4e930552529c4ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67995087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4563a8350604a04af5600b62b1d16edccb28d5c97ea5a4395705e324029d47`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73edacd89346f748ca631980c7d87e425867813036f412fcdd0da331cd7c94fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66432a7d5d046912f35f417488f45297790fe1e6c2a6a3f760efca30a0bb5f8`

```dockerfile
```

-	Layers:
	-	`sha256:36e35f94cc356568286cf0a10f2d3fdb834e31300b5cb9ba2afd931318c3f36a`  
		Last Modified: Tue, 29 Apr 2025 01:47:12 GMT  
		Size: 4.5 MB (4487209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815b01e92dafaa107d8ec9c574a418507eb81d537f13bce19f109fafd38ab9ba`  
		Last Modified: Tue, 29 Apr 2025 01:47:12 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:73beb323532ca4d5d9962261efbe8144c3cd88257e5b12be71631d0cbe58c7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70954269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5365658063035e909459c632b716c88625c7aeea421956baafb5c3ef28e7216d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2850d1b21703d900244f8864bdb41f4035c7d24e7431a82a89682a22e202df15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46256d7763d40c8964f663b2cf00403e337c1836b9ea5f4a2e2868d6900a48`

```dockerfile
```

-	Layers:
	-	`sha256:45da473173583802c80b3b8c6c9d0a4625c68a12d96f5e81a01ec193968f2a1e`  
		Last Modified: Wed, 21 May 2025 23:19:37 GMT  
		Size: 4.5 MB (4509812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097f9f0736f261eb216076af101273215ce99571b12546280131001317a3b01b`  
		Last Modified: Wed, 21 May 2025 23:19:37 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
