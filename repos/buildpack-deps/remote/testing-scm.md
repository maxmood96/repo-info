## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:20279b86e143eab7fba7aab4e6d2f72eb73ef4263e6b2ddb0af163b33c080c52
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e5325ee1ecc0e63105f946e59f438340b5c38a08c72727a71a52c314ecbde743
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143009493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82c19cbfbf5e843cfcf66837147e479748886abc8cbfe3badfdf1c17e231557`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:44 GMT
ADD file:9465a54824a47fac7a8656f1a1d95dc38be8c06ce3809b905d67ff7ce345ce64 in / 
# Wed, 24 Apr 2024 03:30:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e07e2723f97d31d3cc6945b2518b9912a7301e652e09eaac68f1eec11330efa`  
		Last Modified: Wed, 24 Apr 2024 03:36:47 GMT  
		Size: 52.3 MB (52338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95ad0980b95c8ae82ca2a8d74a4757e86cf14913e53a8be04dbf6519d8fcdc3`  
		Last Modified: Wed, 24 Apr 2024 04:25:04 GMT  
		Size: 24.2 MB (24160698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f4651e17e14aecbd72058c76b8f5915f16370760bf5b7f31b11a45b7b29e6`  
		Last Modified: Wed, 24 Apr 2024 04:25:24 GMT  
		Size: 66.5 MB (66510163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7c32c4f1abad98c4076864034abe221b329b7820603910ef0dbf24b0149b5ce8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136629090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9342e492776bc56ae72c005cdf5b2d69269c6bdbb4eb0059a1a76133ef8034a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:54:47 GMT
ADD file:cc1e9468e81e521d409dd8b88fafcaaa5f105f627b1eaef62c896e916213ebc7 in / 
# Wed, 24 Apr 2024 03:54:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:65330d4a78bd6d548d7f0dc559b639551ef46dee6b7d5b6d0366a8e6d22f8ac4`  
		Last Modified: Wed, 24 Apr 2024 03:59:41 GMT  
		Size: 49.4 MB (49434297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaaad035748a99175cae78a5b89744fde3b0a273b1aaa1a736ed21b63fea6e8`  
		Last Modified: Wed, 24 Apr 2024 04:31:48 GMT  
		Size: 23.0 MB (23040802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41db2ec6222226bff823394d26463c48212fd9c5a9fbcc8944ff87735f08014`  
		Last Modified: Wed, 24 Apr 2024 04:32:08 GMT  
		Size: 64.2 MB (64153991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:071efb6556e4f6cd3841ebb41e7810aacabf3b83ccbedc4c34173e8dd3a84eac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130797011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2bd885e6030db179f8aaf19f1835e19b8f0cb83f5b90e86638b707ab966f15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:21 GMT
ADD file:68fc8102f9cd1f1d24d4c270a545146ee6a7ba7fb9d8b6f00d511cc30cae87d3 in / 
# Wed, 24 Apr 2024 04:09:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:59:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c2f00d681f2c70b358e621ba07e5f58c2068fd56d05bd0f1fac5a67972fc1624`  
		Last Modified: Wed, 24 Apr 2024 04:15:19 GMT  
		Size: 46.9 MB (46930352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9505d03d248caf9d52b35ec3ac69ec1aa253a9f5ad5518bad0ae8fd609e08b`  
		Last Modified: Wed, 24 Apr 2024 05:07:26 GMT  
		Size: 22.4 MB (22355377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3232da5efc12f2d7cabc485881605838030d4d7e9d541756495a9373f151f95c`  
		Last Modified: Wed, 24 Apr 2024 05:07:44 GMT  
		Size: 61.5 MB (61511282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3da49e295eb0a61679ba8cae3dc85919f9aaf321bb72cb0bd8b81ecb5dc0414a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142686302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9cc9713cbb5fe148e1cfa6a1844b470a959529fba4f7b35e55f80c2331902c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:42:14 GMT
ADD file:d3b8312bf9d9df431c2580a0add351c37786bf532e919d2af2638c2fb93062ff in / 
# Wed, 10 Apr 2024 00:42:15 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:782f2de9bf3353a68116b53b16ae9a2387174b31cc46b4c9b4cf99de0a6e1af4`  
		Last Modified: Wed, 10 Apr 2024 00:48:17 GMT  
		Size: 52.2 MB (52193812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae77305c2bd54ea5f2ca2a76ab1cd96f744878b54d2b45e6edd47242bfa248`  
		Last Modified: Wed, 10 Apr 2024 04:35:41 GMT  
		Size: 23.9 MB (23879162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e30f8a1b424817119b09ab00860f59903c62298e404ea6d5a47596c436e9353`  
		Last Modified: Wed, 10 Apr 2024 04:35:56 GMT  
		Size: 66.6 MB (66613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3c3f44b11e31204103b89d6ef8d801e882122960e99a075bc7bfef9d58b846e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146758855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c87c2bdf08245eccdf9899282beb9d4537e59123bd7ab8f06f40df577f1c28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:41:36 GMT
ADD file:ed473d3b605a6b0948955f74f5dca4dccb14a7d6cf9d219891c6110ba6572f94 in / 
# Wed, 24 Apr 2024 03:41:37 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:38:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:38:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d51399cd19ce178fe1bb087a7ed5b07667b07b1dd98716723177809157778ffd`  
		Last Modified: Wed, 24 Apr 2024 03:48:34 GMT  
		Size: 53.2 MB (53187646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9cbfbb03c89e50483bc6f14d5feeea6ad8da1d06153c1bb027ef0f401de94d`  
		Last Modified: Wed, 24 Apr 2024 04:46:54 GMT  
		Size: 25.3 MB (25279252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd74f5811c9b909697371e2951aac6db5673f860ba43dd4abc538cc436c4947`  
		Last Modified: Wed, 24 Apr 2024 04:47:19 GMT  
		Size: 68.3 MB (68291957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9468787065795edde7853bb1e0b0bd5200d946ba7e4cbba0929292911f08048f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141336943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc22e4dca09322e7eefae95d3e9d528a0398c34472809755754c76eb1dca1c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:02 GMT
ADD file:3528147ed2ff17c452628f4992045437579a2eb00d2eac617b8542d7706b58f9 in / 
# Wed, 24 Apr 2024 03:21:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3d9ec6cbd0472de02f68ab46797d6a2b9840ccc575c40d8562ede5007cd7622b`  
		Last Modified: Wed, 24 Apr 2024 03:32:27 GMT  
		Size: 51.4 MB (51411293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a78282402894106b7f446ef7995bf01264e8c063d4dc3f3d1cae34bb31b7f5`  
		Last Modified: Wed, 24 Apr 2024 04:40:34 GMT  
		Size: 24.6 MB (24624106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3a8c05e8087139d064ba2562c9f539168b11a8e1e618c0c8dd990ffddf0aa5`  
		Last Modified: Wed, 24 Apr 2024 04:41:26 GMT  
		Size: 65.3 MB (65301544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d1589cd3ef6546c4251b590572c0658260d7026c2bbef98c00f03cdbd085f25c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154517072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6ee6d714f510439cb13fd6adb1c7328a7d11e19b2d27d120859de4d08dc864`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:55 GMT
ADD file:49f2825f9c5b50843535acfc958249a70e087e06e06eb89df8fcaddcbf45564c in / 
# Wed, 24 Apr 2024 03:24:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:16:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5bb82112ecd21be1be5a4a97a1beabfa110a5d5eb34d4561d4a17294d7f44c6`  
		Last Modified: Wed, 24 Apr 2024 03:30:40 GMT  
		Size: 56.3 MB (56253273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d091ba74dd77c332622f47e69c38784baad91176e28aa55e464ca78ff6b4b3`  
		Last Modified: Wed, 24 Apr 2024 04:26:37 GMT  
		Size: 26.3 MB (26256543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbdc1bc67e9aaa4ea2e9acc9960c0bdca8a28b392ecaa8f1767e62f424e2f12`  
		Last Modified: Wed, 24 Apr 2024 04:26:57 GMT  
		Size: 72.0 MB (72007256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78c8afbcd1a649ba6ccb43b0245c328722ea000f46a79437164c04467dab7c76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144655680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107f9545e6af2e2cdd8b59ad5ab4ecf5c91c6428e7a9f9c398957470ac238bd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:49 GMT
ADD file:13427baa96123e72c30f8ac6ca708a7f7d3be7f0ac0833390d7414c8d1e438e2 in / 
# Wed, 24 Apr 2024 03:46:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:18:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f21e8a280ca933b265ed896c2cfa5317f05fac17b7b290b87455ee5b3f92921`  
		Last Modified: Wed, 24 Apr 2024 03:51:44 GMT  
		Size: 51.8 MB (51766843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd83a1cb8c7c3071ddfefcd98acfb1745aa44bd51fc629f0c9a3a31f182565`  
		Last Modified: Wed, 24 Apr 2024 04:25:56 GMT  
		Size: 25.3 MB (25294940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d8c2beefb38b0b74b231a920769281b4b909f949acae01f0aefd2b33aefaea`  
		Last Modified: Wed, 24 Apr 2024 04:26:12 GMT  
		Size: 67.6 MB (67593897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
