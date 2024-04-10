## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:e5db10723100475338ed397d4dec94a221253fcd489926807b06a33c16c87eee
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
$ docker pull buildpack-deps@sha256:a8a2311234c1c18e31ab0b23d6f6da08b9b205efe0fad6da745a1b924dbdee98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143000432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898afa8f00f636706e6847193dd6d9f607a64385754ad3dfd1749c9793e57f86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:36 GMT
ADD file:99b2f09b38f37e8fb43da4af7e905a316ef0ae5d1372e182af7a4467ef8d7d73 in / 
# Wed, 10 Apr 2024 01:53:37 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:32:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e95c2810bf71ea304ff068100fda778bbde84d0612d720b0cab3e6069e85fa0`  
		Last Modified: Wed, 10 Apr 2024 01:59:53 GMT  
		Size: 52.3 MB (52332312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b66a844a336d24bd3d65fb1c2fa52cd05dba564c7d3c1a7655648d2891df776`  
		Last Modified: Wed, 10 Apr 2024 05:39:03 GMT  
		Size: 24.2 MB (24160926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614b95f18c1108db17cec7a97089473d2212ca808e2961450b05f7c8a9b8df4`  
		Last Modified: Wed, 10 Apr 2024 05:39:20 GMT  
		Size: 66.5 MB (66507194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2a2a99dde82d5792a4270021d6c09a2311de06ef022d9acfb0e963fd340e2e20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136610529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c610be905ba59b1c8c3256c24b5d28fc6eb0a98a979bca3c1d78ee82f6b48260`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:52:01 GMT
ADD file:0476c16083d61e234237e2ef7156b893d991ebc8124b8bc6710b73ef2fe671d0 in / 
# Wed, 10 Apr 2024 00:52:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c8c28d868d5d3991cbf017b63d5fac41114aa7d2eac7b1224fcb86c76b143f4`  
		Last Modified: Wed, 10 Apr 2024 00:58:20 GMT  
		Size: 49.4 MB (49422136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3293a18c8b358e708c54799a531104a9ddde33e702e4608e103d0b33b15cb3a9`  
		Last Modified: Wed, 10 Apr 2024 04:58:50 GMT  
		Size: 23.0 MB (23041769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f2f7b0c3bd000167dd0d210fe7cfeb3c2d1dc31c6b0e387868179dfae14c44`  
		Last Modified: Wed, 10 Apr 2024 04:59:12 GMT  
		Size: 64.1 MB (64146624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c3dabb148d66024ed98c2e318f20e9f78dacbb024ceeed40a44899944960d12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130788117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1b94b1a0f2f69feff248c86ee0629c9c5ee76783538aecf1df6c8397a84b07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:01:55 GMT
ADD file:656b365d8d9314f1217c95cc1d4d7cfb6bec38e30aea70bfb00983db7de41d64 in / 
# Wed, 10 Apr 2024 01:01:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:55:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2733bd62bd4d649c9ab65374a55302ef287fbb5318c00121743e3223bf33e52`  
		Last Modified: Wed, 10 Apr 2024 01:09:16 GMT  
		Size: 46.9 MB (46920080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02643c0d13132e32e3d948fe0f9e603b1f3bc4e4dab635e89566aabcd733d1d4`  
		Last Modified: Wed, 10 Apr 2024 07:04:59 GMT  
		Size: 22.4 MB (22355167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1919d5931d6716bea45e42bed91785de5a79886b5964c4c66b4d9c8a6032e2`  
		Last Modified: Wed, 10 Apr 2024 07:05:20 GMT  
		Size: 61.5 MB (61512870 bytes)  
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
$ docker pull buildpack-deps@sha256:eed184f7c0a8d3c5614a63902094e8b29d82dbaea4e9710e2591b9c3cfad513d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146751747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e487430056e803e7f442fafda3fb9030b67eca8226babf68a2a3e8ca55ed5ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:073778b7037e665c7deb59a4f06a254c6be933587f8fb58d705794a27a93e25d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141333448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db4c0353943ea80b7ba5e735727b8a5c912807d88ac7d1804205b190897140`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:db4ff030fc8fcafd5bb33964020119008316595a4a8d6e470c84c604eea7680c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154508161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133efac2ae0b90eb9ade939586fd5b7b2be1bbb8a0f8e6f3e52a282adab11d3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:55 GMT
ADD file:f2e3cbd5cfb4aff8ec6395d52d929fd664d9648429ab4d9e1153ee9f8459da76 in / 
# Wed, 10 Apr 2024 01:28:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c75969f9d1cfa02f8bb4ac9be57d10b36fc89340facd55e8f3ee886024860d42`  
		Last Modified: Wed, 10 Apr 2024 01:34:52 GMT  
		Size: 56.3 MB (56250111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c594ec063ba0274cc2cf2f1cfb2f564c330c348dec7ab928f2424a30b4f1bee`  
		Last Modified: Wed, 10 Apr 2024 07:20:14 GMT  
		Size: 26.3 MB (26256738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038140cbd597a5abde48b6e2e138b1f52f404b75dc59349b57feeff15b2c6e42`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 72.0 MB (72001312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aa05026047d17c73bd438c9e8d0fec6375b011e4f1b6a23b1c99dcb1e30521bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144647478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f89cc5430550b3dab76fc3d9da91459aad0a7df5426c1cddcbbaec353931aa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:38:00 GMT
ADD file:a05ac36ba0a9e12dfdf53ad56de60918b6f7f530f4b32b570bdbbce0a7bc514d in / 
# Wed, 10 Apr 2024 01:38:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a7403c42a27ad5d5ea9a8c3224d14c269f7cb3da9339e45b20c533dcbe911289`  
		Last Modified: Wed, 10 Apr 2024 01:50:55 GMT  
		Size: 51.8 MB (51761790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c24ff3eb07a21f2639bb7d99f5c6a035571ca068e5457d79f063f14100f020`  
		Last Modified: Wed, 10 Apr 2024 07:33:51 GMT  
		Size: 25.3 MB (25297536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ec7f7c2fddd776232182d05cb2a896283dac486022dfe898eacb7640fe1e5c`  
		Last Modified: Wed, 10 Apr 2024 07:34:07 GMT  
		Size: 67.6 MB (67588152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
