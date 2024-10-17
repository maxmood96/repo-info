## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:8b54db63511676e1972c133151234e656edace3cb563e369fda2aba1ed55a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3b706a9072afca977d5a288be4510a9a07ed03f1241eafa0eb2697d97f807506
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d24b6c4458d7a95597518c043757b7a9730552936e4bd0353843e7414b8d2d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:04:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:04e1c3749d8bed260a9b4393eb7d449b58be45d527108d0100ead20da5f60e54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65121659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386f9bdcad9d646d39c4deb3e04411919ff352de5767fb8573a48d16423c4ee8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:34 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Thu, 17 Oct 2024 03:03:34 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:030cc80aa1ed6ee00961caf10d62dc44316392817100e4310dce478615b3ea17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69485120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd28885b2a5f0931bbb24a21a11a760e81cb0f28075fad6b94c70bddbdaead2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ed06bd743cf9cee9c8c1f1a86e7b84610eaa5083390849295aa97ff8b94e9217
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72346365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e9dc84b4e2597b8d40ce2e53cb881f2890629dfef06c94d93af53626dd908d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:07 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Thu, 17 Oct 2024 00:39:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:04:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
