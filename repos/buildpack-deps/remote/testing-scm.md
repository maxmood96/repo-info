## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:08c8bd0bd94fad0723db88f1d47c9dad5d9c933bf50b313002f1e714d6156ac1
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
$ docker pull buildpack-deps@sha256:a34da2b9118ef97f6957c2679ef49fd464dba77f4ff6f319cc368a0208a8ccdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143152753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3a9948b9349fa7522fbdb1e093bc0e8f4c4f6e20eace5e7c5395e54a21e697`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d4eddc317c1626d430512efcd56711fbeb6b052430bf0eab58eaa6e7e09d3e1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131194434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd44a7db20e0827c98eedb880f842606707f49427f01dbda60a98f6b7a74535`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:58 GMT
ADD file:67cf4d8ec08d8be721c8b3c00d573d157c1ced0941182f1bc4963de79d90968e in / 
# Thu, 13 Jun 2024 00:49:59 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:1ec46f726aad0ec6492a2d4365f522b616a315262eae058ddae31bc48bb54536`  
		Last Modified: Thu, 13 Jun 2024 01:28:04 GMT  
		Size: 63.9 MB (63869461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:218a78aa3747a001e7c44441197a0a9d951a5b61585a84fd2aba91ab38181f29
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125492407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e378133afaa75a5369d8bd2945c131aa46ad892500eba410f3dac977d2b4fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:59:47 GMT
ADD file:d796d27ece53d8f1990a8b90cf835997d1cb9520f76b3476f3fb834465a282f4 in / 
# Thu, 13 Jun 2024 00:59:48 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:7e1f736e76daaf801ffe0f5e18f4941fe63aa2a69c8cd6d41e58a0f35a8fbe86`  
		Last Modified: Thu, 13 Jun 2024 01:37:54 GMT  
		Size: 61.3 MB (61268135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b41fff0b75cc30507ac62f4ac9a2880de7d734cc4cef4bb8a447d18e9edbe0cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c68243ec8ee65021f1ce3872499d665227b48543c6f16b5ed66449518f1da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c4d4ebe4bfc568fd3648582fa49f610039786dea8e8bdb2e80252e5d22aa701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141088795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38566c60b6918b26840a47ec9109fdc647f311582ecc206134b5ce6688c8d08c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:04fdde644c2537c8f96a9ec7f170c8d7998434f50a9cfebb6ede9ab2fbd6bbee`  
		Last Modified: Thu, 13 Jun 2024 01:24:27 GMT  
		Size: 67.9 MB (67907988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:99dc76b40f79ccaa33318997c9e623e8ef9cc23adaa7716aa548909884a2a543
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135837548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00577513e6b233addc239e18e08c0368b6371f3d49128cf77c570f74c6e88ae7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:26 GMT
ADD file:4f8e64cb73f0bac5394470bb779521bb9b544dd7513205d8a870b13ebce84cf0 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:2b8a3cfbc2aeda20ac68a789ca74022fd826e3d1aa98a47c8a0e8597cce2c4e5`  
		Last Modified: Thu, 13 Jun 2024 02:47:06 GMT  
		Size: 65.2 MB (65188152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7a46e3cdadcac60026f7675e71a7a9868d2db93b178a4902982396212a405f7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148851164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd79633e0facfdddf2456675d11fcd6868c3cc93f0935e945b09a3bbf9e2b25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:19:22 GMT
ADD file:7f11aeb3b831c3c6b30678c3d7984daa533d1db8a095121fa83cd6eccfd45947 in / 
# Thu, 13 Jun 2024 01:19:25 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:4c51ee1c602a71ed936afa619f5837e429c4674c5827c404f2f25b4bbaed28f9`  
		Last Modified: Thu, 13 Jun 2024 02:03:43 GMT  
		Size: 71.7 MB (71707938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e5c1a3992746e6832041bee53a8c59e76b89adf2545474dbc4535c28314d24d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145292706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e09e7693ba380c030f007b4b0993daa21b667a828f32c97efc09b9770fa9f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
