## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:316f2812cc18506a1477d41fe38bb9c493e05cf4ef97f0820f32085bbe2680ff
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
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
$ docker pull buildpack-deps@sha256:1135d2b8a5003fc4c194caf24d0876991738191ab92c0e819133c305eaaa44e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63922507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12093ca040c4d920dadb5eca090038728d8dc7cc434935165023accc33cbcdb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5053ce02008332f5d21c8078e9333bd265abf67e1c9fc7795ef38fef0e7ee2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29111f0461b7afe2a4c13e858af6b5ad3ad65f1567f77ad94eb85318b15efd8b`

```dockerfile
```

-	Layers:
	-	`sha256:f4081543aee1e1039ba9786fdd6dd357c97ab1fe2649851fbbf8569ee87857f3`  
		Last Modified: Thu, 22 May 2025 02:28:36 GMT  
		Size: 4.5 MB (4514945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e6b4a71881cc4768b18353f0d952a4026c71ecfe3d8af27c82f3b7bdf1c89db`  
		Last Modified: Thu, 22 May 2025 02:28:35 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:badb1e8c71ac4a0430d0edf9510da28e86b8493834d7edd59181b6143c14a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67998137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f0637b612281cd2b99945c5d2f6d4a70542ff4d2106a431ae51f461db5535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c284d1fb20a7202e4a179c37fe99325b9e47f527f59ca18bcff30295bd115fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f274ef3e6d0b3fd24f2b4a6d2093b1ad71a14ac3f039cdd845637aa217b47f0`

```dockerfile
```

-	Layers:
	-	`sha256:526e8bd3fa862aa29174553e2dd977c0171ddba81ab2e083128d7794f0be0a12`  
		Last Modified: Thu, 22 May 2025 02:47:51 GMT  
		Size: 4.5 MB (4512923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9760dab3c3fd222f5421db90e412905059c82b79acde4f7d858acadbfeec3e26`  
		Last Modified: Thu, 22 May 2025 02:47:51 GMT  
		Size: 6.9 KB (6879 bytes)  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
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
