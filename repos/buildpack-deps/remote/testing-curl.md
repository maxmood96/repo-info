## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:08240df5acd7e463bbaf108e1bc4cc51a16969249f1fc690e3451c6d8edb3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c660f96bdf8acb785cfbfd6ac0d68c7d8dd63a88884ba6eccf9db036c0875ebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77003837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313b5c46af83b08eeb74bf2683448dd049aea441d36a91cf66a8d67ea47de56f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:aeaf3f55b0e3a664abd6eec84e6c644234348a7f2af073d8b95966eb24931726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67324973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad76d64c3f4feb07e9e39361d872341106a4384b2bcffcc96718868496b3848`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29844d0657d8dd02a9b897db6c4c33e6651c566ad1edc4743031852caa791e09`  
		Last Modified: Thu, 13 Jun 2024 00:54:51 GMT  
		Size: 49.4 MB (49352422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976f0704ead6a05e2196815bfd922b0200c7e1d9d811bce36e0f05410767a26`  
		Last Modified: Thu, 13 Jun 2024 01:27:45 GMT  
		Size: 18.0 MB (17972551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c3c2d0172c1f96bb3f6fe6642ad60b077f1bd60837a4961442f434075218d9af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64224272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0240b158ca01de67a1d7cd35d53ff9a5f4b7b4029fa4e95f0f5836d83298803`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16fb7fece780cd7b9bbf82b2be73b9d8d6a4780cdebb977a5f734fcc541dae72`  
		Last Modified: Thu, 13 Jun 2024 01:05:53 GMT  
		Size: 46.9 MB (46856182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac0e55eae13d71ea5456f237608139f23b587604a5260254327df6d47fc68c5`  
		Last Modified: Thu, 13 Jun 2024 01:37:34 GMT  
		Size: 17.4 MB (17368090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a34c050a2acdfb8a3bb258beca9a4a587cb01039d379e95b4102451cbcd4f851
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71284731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4c9de2ca2a1fa682bcdd1352400587b9e254e9bffb1d3373dc43dd1db586c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cdbe30a0f3e833bc1134cf05690590b077194401ff05bd209f7dc5d16ca2369
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73180807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806f59aead0ee5dd5fae5e79c8102ba25a8a0627fed536080bee6a58ce53634`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc84062895b3dcce20539bf2d4d21bd25d8b67750b881b5f1672a4b66a436b5`  
		Last Modified: Thu, 13 Jun 2024 01:24:04 GMT  
		Size: 20.0 MB (20033337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:835dd9e9423d342fab292a646577fef93c0b50ec0a822acb33ad048e706abe1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70649396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5193091e963f59c515ed698458a829954ac17f307eab20e9b6f39a3918481c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:26 GMT
ADD file:4f8e64cb73f0bac5394470bb779521bb9b544dd7513205d8a870b13ebce84cf0 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:82cf140ea060591c60ad59c1c2af2452121c8cf77b184829ed04be1d69b176dd`  
		Last Modified: Thu, 13 Jun 2024 01:29:05 GMT  
		Size: 51.1 MB (51137261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0995f3325cb4fe9538ff2c2cb740572ccf176df40429dcb0b8a22aed9a06214`  
		Last Modified: Thu, 13 Jun 2024 02:46:15 GMT  
		Size: 19.5 MB (19512135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9d2158de3d9f268674fefe6f4cf3c734c1c2cea5c1e0a052f7d6f6fcad7b30f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77143226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6a1ff484bb59ed93a0f88586ff2a612540c2a9f423528cc0cebdf1c566c185`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:19:22 GMT
ADD file:7f11aeb3b831c3c6b30678c3d7984daa533d1db8a095121fa83cd6eccfd45947 in / 
# Thu, 13 Jun 2024 01:19:25 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c454865e432a2e42969df66627ee25256e1007a229199ac385d2d91b138f54b7`  
		Last Modified: Thu, 13 Jun 2024 01:25:21 GMT  
		Size: 56.1 MB (56146517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85603b7316d090b974eba19298c576464ba6b0ce6f58a534579b2ceabac0f9f`  
		Last Modified: Thu, 13 Jun 2024 02:03:24 GMT  
		Size: 21.0 MB (20996709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:21821cef67dbaf19dd6ab42d9b57bb10cf558b156869b3ba0f40276a3dc94ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77839233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96fad9bd52dcc2b83666a28ca8c7c4ee460c8493064bb9ec6e5b1d0d9ab825`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
