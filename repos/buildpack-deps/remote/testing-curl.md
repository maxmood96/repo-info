## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:2cec63b75abdda05f02cf7164cf6a05723a73b3f465128c992be7786a4d26638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:daadf1decd2f26e479246d7fdc37deb03276b82e9df4a5c14769b8ed6200bb01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73642871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f5344b74da57c1aec89106c34972ab25c2c2bd7051723c6fa1c58e57ea9877`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:27fd4cfcb18cd2d5384a22a33966913ee334dc7f49ae1c7971b013aa4d6fc8c3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69595047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9aa623311f3d33935ec2c3686ead7d1eb6d7e91a9acf5f9d29f96717edff23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:59 GMT
ADD file:9818fa184cd3832d7a2e958d07cbdf6f16e481580a7abf2ca8cab41151573065 in / 
# Wed, 04 Sep 2024 21:50:00 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:59aa270c3f603e92ab2ded83e0aa06f94cd27fb99cc5c9166b81e03b32d905a6`  
		Last Modified: Wed, 04 Sep 2024 21:54:36 GMT  
		Size: 50.1 MB (50107080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297b17500c84a89078e828972b7358df29151b8ee076ff5c0ad428e3fa0ac49`  
		Last Modified: Thu, 05 Sep 2024 00:27:10 GMT  
		Size: 19.5 MB (19487967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:80599527d38f3f9a9d793aae25040dc1718bfdc2391b265842bf358dd867fb6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66434200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9618994342680a65b4bd70af330513c59f58b90b1979bcccbcd27e48a8e93b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df1b58b717328f01a3319f41400cb48c12ea81760537ed99307bdbd2b9696f7a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73829151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8952df3538af05ac37f9c33f6947b1d08bd149d5179bf1575d8ef3dc1a5270`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:962a2b0a55405632c1d31a9cdb722a85939ff23a88efcb3a64ea09282ffc137b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75536675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8d9c8231cda2fd80ea5a1192ea71afce46278e1172205d87fe873d2b38b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:46:29 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Wed, 04 Sep 2024 22:46:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb787d90d752888e985200fa402a100bb856346742b9ebb57978434abc2b1a7`  
		Last Modified: Wed, 04 Sep 2024 23:23:52 GMT  
		Size: 21.5 MB (21512389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a428e09f67360bcc8fb1a124a8fb67610b370ae9e5635bd8e2e950cad7dfb376
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73059100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb1cb53973ae99c5f3918787f88a2be6b9c77abc4f83cb919ab2afc0f5b3a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:feb6cf26df3ed5cda70540b834dde7d99fecfdb5ad2f2d05ae00be1599ad8efe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80227293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d130f96e42cfb572fbb725ebc678daae4713e3b142142a8005a9aabc9beb189f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:12 GMT
ADD file:72b28cd12b51875b02b32c08c19d9763a8b995f28917285fc8c454420a98ee23 in / 
# Wed, 04 Sep 2024 22:28:15 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8d710a2aeb72c4bf2e1980a336408edaec79dc17907bf54201076e8a3da2f3f1`  
		Last Modified: Wed, 04 Sep 2024 22:33:33 GMT  
		Size: 57.1 MB (57077783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a92c6b6a62daaba5f3c3ed033ab8a0ae0d09e12f1cca4ea61df9c1fccb67f7b`  
		Last Modified: Wed, 04 Sep 2024 23:17:01 GMT  
		Size: 23.1 MB (23149510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5dadfc5dab20e01252c673073c5eac4ce3241af71cb7241006f50516e8e5cd4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71492476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b0ab93f8da1cbebe40d02eb72e1b218f218b3fe86d8cd5595a4e1b5f27141`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:28:03 GMT
ADD file:3536049154c2250abe969642d7b35b085e3d25447b8953cc1e072b690a306aa1 in / 
# Wed, 04 Sep 2024 22:28:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38a3e7af214e5e0705f0ceebc8bef13cf31414ef0eb3f3ad8a05574549c77869`  
		Last Modified: Wed, 04 Sep 2024 22:33:47 GMT  
		Size: 51.5 MB (51475526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1754edde6597959b526e1765798c2e5f144cdf29b0cc5a933959b572039f27`  
		Last Modified: Wed, 04 Sep 2024 23:14:26 GMT  
		Size: 20.0 MB (20016950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3520d5b2d703a9ba9f15254f21ff6f525a3a0a16285036d7f46f4c330118417f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74350252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771060c6aeb4dff7b191c35a90d8acbe858592929541822e77932f256839f159`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:38 GMT
ADD file:d8c6bc2767ccd7e1cc72d27d8bcb6ae32ab902174ec47c087c8a760be26c991c in / 
# Wed, 04 Sep 2024 21:45:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:35e23b80cf3051c9b7be598388de687426f0b24d259df069449caf8431f56244`  
		Last Modified: Wed, 04 Sep 2024 21:49:53 GMT  
		Size: 52.7 MB (52746453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1734c15d36ee15d55cb541791e7387ae5b261bf0c1251adcdc83e30ec5ce1a`  
		Last Modified: Thu, 05 Sep 2024 00:02:31 GMT  
		Size: 21.6 MB (21603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
