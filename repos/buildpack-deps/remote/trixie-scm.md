## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:d4f68908b2a98a3932b8f533c241b1dd2045c6c19922bea1d0f9059199df71b9
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:81fcd0e947272f6fccaa58f908cb0efea8c3b9dc0b1f5e49e3e13af5b581c641
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140186501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b52da353361f003e3a3f9fa4bd2fe5f8d5fbd0da5ca59e4191d93131026bbea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:22 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Thu, 17 Oct 2024 00:22:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:08:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3af942d5f32a53d271e49824c635bd83b9f44545e34efa1a534acbcd19cf8c`  
		Last Modified: Thu, 17 Oct 2024 01:12:47 GMT  
		Size: 20.6 MB (20646136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631e0c8c5d1c8cd92a1b3ac1bedbfcfae442b261c1dd65bb2161aa4ce066fbfa`  
		Last Modified: Thu, 17 Oct 2024 01:13:04 GMT  
		Size: 66.3 MB (66301624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0df3a0cfc9bb93c117f8ebc0b4596b0196f02bb9988c15fd3650ed88d7b4d1cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133532073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47b282ce6c59bbb85d5398351c90ac974718987e6cd518ef318dba4b83121f7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:50 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Thu, 17 Oct 2024 00:55:51 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:33:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881241cc914c17be2c506105e054bfcf46ca5dc3a2c61b399fb49563a725f97c`  
		Last Modified: Thu, 17 Oct 2024 01:37:57 GMT  
		Size: 19.6 MB (19644443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cc8728e864cc21d996b1238d79456f457c2d6f8c5d26d74916564e44abbe5b`  
		Last Modified: Thu, 17 Oct 2024 01:38:20 GMT  
		Size: 63.7 MB (63741533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:053ee781c68e0d80fbcad4bb1fc6ef24f20705f8a43c45be1e9ede6bb990e7be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127423556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526062e2e04d2ddd719664f3e5b2a4dc4611137832180752268433ca2ae0913f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37dd52fd002bb99bd49c9bed7893185cc0dba9fb61e6876b290d76592b7648bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139904889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd83450b181a65930ccb9e202233c0b03c9eb558bb321fe45618331e73373d36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c4123449797e112c0b2efe2e4ec0f29db8f28e2423c93dcb7f2f89172384afe1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143939177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2932abfe80f042ec585ba3e310ec244018c675b65559b0fd9da458c26553d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:55 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Thu, 17 Oct 2024 00:40:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:08:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8bca6b1029fb346ac8c3fd8fd0242c8617b39ff467401ae5be38d72823e794`  
		Last Modified: Thu, 17 Oct 2024 01:13:34 GMT  
		Size: 21.8 MB (21756980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a074313195f31eafdde1ef7f85c59bf5ee3996435610f09e54f50d51a3f12d`  
		Last Modified: Thu, 17 Oct 2024 01:13:55 GMT  
		Size: 68.1 MB (68104739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e2c795dcaafebbff8af22ca3f2efb1994821c14f413815e403f5e7a575aa8595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138169419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7b2030d7cab94531502664095beaf1ae1ad9f15ef5cd89f5deb2857f698d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:13:57 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Thu, 17 Oct 2024 01:14:04 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 02:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3136c2a952f0ce80aeca2b6928afe3f03863f57c7fa1a03ebd2f7c0be5923c8`  
		Last Modified: Thu, 17 Oct 2024 02:15:26 GMT  
		Size: 21.0 MB (20965665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8f48a50ba530f6de6ffd4fea12c7a1881ea25592c7713fae880299f80511d7`  
		Last Modified: Thu, 17 Oct 2024 02:16:17 GMT  
		Size: 65.1 MB (65075286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:416d68c7a6ea996450091adfc2ad7659fe479b8592d3deb58962a40a976088ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152071022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a632aee26b4b1f0c77d9eea17429ff8bd4d62ccfc6a7c47e2034dda6e1ffa5f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:20:15 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Thu, 17 Oct 2024 01:20:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcab475561b983c55c4a069685bc4edb3857233ed2831996472141939c0d16`  
		Last Modified: Thu, 17 Oct 2024 01:53:43 GMT  
		Size: 23.3 MB (23316051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ae8e30c2b54262517c9a764062e90b5c337fd1a1089c9cbf94ea5050e659bb`  
		Last Modified: Thu, 17 Oct 2024 01:54:02 GMT  
		Size: 71.6 MB (71628326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4737253869238b730cc24ce2a1c76597f79bd78f9e3d303b975e12b3f058c433
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141422388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fdc194f0364e41cbd14b2f7c0f6922ee0c388c0f15df6c99eee1ea6933947`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
