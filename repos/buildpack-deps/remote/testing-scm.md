## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:4b1ac8cab774a4b2e672328dd8b4f8fa2d282967fee8a60fb439fb2f94c209d0
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
$ docker pull buildpack-deps@sha256:51092cbec226f662a97ab8f224f1c6a22c784015b39ebbc06812a0828a22b0ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137682711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86552ccbf7feeef5f1324e901fcc4b77049d31af9ced94638b9fbd1fe3fa7fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:19:36 GMT
ADD file:aea4560c39a3a877086fc63afdf218ba3600a05abef7c44563f788e8b60c04ef in / 
# Tue, 23 May 2023 01:19:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:45:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c98dda1b0e97e7fa61fa33cea43f85bb1a36a4f6f65c7b8430cae442b76ece09`  
		Last Modified: Tue, 23 May 2023 01:23:14 GMT  
		Size: 49.3 MB (49301275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a463ac54ed3eeee295443fb87b28643b95d7975e83bd214bc93db462b1b59de`  
		Last Modified: Tue, 23 May 2023 01:55:08 GMT  
		Size: 24.3 MB (24274092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7076663891554c4b6516ec84fd2d5459502966e94b4d794796b086aea4f4ca2`  
		Last Modified: Tue, 23 May 2023 01:55:24 GMT  
		Size: 64.1 MB (64107344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:58ef84833f6f40d5c9265613e25ac370ea2377a4bb6de1ee4a641d5b87735cae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129944093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d440eaeb8ebe37f5bd260a4ce5361d5a8ad9890f8dfe4e266e6d886b82f1479`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 01:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 01:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f867d323ed66972b6c492120ce3fa78d7e1d63e0279362a9a55229db8e7127`  
		Last Modified: Sat, 26 Aug 2023 02:00:38 GMT  
		Size: 20.3 MB (20250269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dfbc5e6b18e516ad072378c62dcfa42e9981f0925b16c44303b5c7f6424eca`  
		Last Modified: Sat, 26 Aug 2023 02:00:57 GMT  
		Size: 62.3 MB (62298697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:331db16e2b01d1927b127fda6bee4baaf1afe723687ad2f28537e9ccccdf534a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126423598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd030fb412ac7e3dd0bb5fdab07c73d829d6a214545a719a34f87de4e32bf5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:57:23 GMT
ADD file:76738dad56d76cef0c57f5c574260e6494d397ba6ea95f5ea14ceeda292e8a0d in / 
# Tue, 23 May 2023 00:57:23 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:51:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b62ba7ac5fd70caec3910c292af59431036e6a2f6a4fc4266b3c04d3f6f7febd`  
		Last Modified: Tue, 23 May 2023 01:00:49 GMT  
		Size: 45.0 MB (44989913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5316b360a91afe489f52f8edacb51535faca57922a648164ceab10593e7842`  
		Last Modified: Tue, 23 May 2023 10:03:35 GMT  
		Size: 22.2 MB (22176633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d1443969900c81509f08727255738a226e326b2e78357a9f564ed1a40e0de`  
		Last Modified: Tue, 23 May 2023 10:03:56 GMT  
		Size: 59.3 MB (59257052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1099c74a36aa3e7994816236eaafd33977cee3e8856f0c7489006a4113204ef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134198876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690f08e5887bba5afdddc9f0866feaa0fed5ee90a92507fde699e7721764e317`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:42 GMT
ADD file:16621389c05de9ece6b8d40e6c62ca81465940296cc58f7f1c56571fac05b33e in / 
# Tue, 15 Aug 2023 23:41:43 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5fc9f67522f8eb1fc65844ccc91e1d93595f85d410842d334c85f7e0a15d841`  
		Last Modified: Tue, 15 Aug 2023 23:47:22 GMT  
		Size: 49.5 MB (49521978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c849b78c27f87cf11f7bfc3a6c274880955ddcf718ceae8fe425a331d69fb`  
		Last Modified: Sat, 26 Aug 2023 02:59:50 GMT  
		Size: 20.0 MB (20038140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d90315047ca31a048692ffac9ca9412c3013153dff0ae8d9d7fa6d3dc5fc787`  
		Last Modified: Sat, 26 Aug 2023 03:00:07 GMT  
		Size: 64.6 MB (64638758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7285ecb58abaacd425e46a8f49f8848527e92124aca75931d3946c1485e6553f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141403547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829e40641db120e27b6767c9d5834e7a3fa2066af32effc700c78a83725e9393`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:38:43 GMT
ADD file:4d14207b5cf935fa2b9de70132f41a0eb90a8b5200ed3d27e60b766fc6131e13 in / 
# Tue, 23 May 2023 00:38:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:54:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22e40771358829b6817b47cb2d682b51257385478c18bb1ec96251a68a9c75e4`  
		Last Modified: Tue, 23 May 2023 00:43:23 GMT  
		Size: 50.3 MB (50323189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008bf109a603c637e9a80a5a8fe46353089a5fb8c6333eced350af89d7298576`  
		Last Modified: Tue, 23 May 2023 02:03:46 GMT  
		Size: 25.1 MB (25110482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39204aa4c310e5b428093f5182d87e2f302dabb686c85507aed2372505156242`  
		Last Modified: Tue, 23 May 2023 02:04:08 GMT  
		Size: 66.0 MB (65969876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d6809556d02b5b488d34cd28e2ef5aabca701e4beeec3929b4166bdc34c2b1f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132598884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361130f6e6031db81ae018a108c6664eebe1dade2ea82462af9e54693e69e991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:15:24 GMT
ADD file:21a0349f8818b8dfb23d9795ca922c9828660ac081ba9db3e4fe08efddeef0dc in / 
# Wed, 16 Aug 2023 00:15:29 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:39:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b01e2a8b457425ca543dc2e5fd0920c4c1baf753962560010906ca5d157fb3dc`  
		Last Modified: Wed, 16 Aug 2023 00:26:31 GMT  
		Size: 49.4 MB (49449783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b7568185112b7ae667741ad45f90e22219bb33f27fe4b15461aea0fc1766e`  
		Last Modified: Sat, 26 Aug 2023 02:46:44 GMT  
		Size: 19.6 MB (19559201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3389ac306ca24c2ea9675ac7442b509e039a22dfb231109ea46f541dc045bc66`  
		Last Modified: Sat, 26 Aug 2023 02:47:35 GMT  
		Size: 63.6 MB (63589900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a70fee0093fc78a9ced3f519cb0f01aee68baedc6ac1f6a1afa1cc11103d3ff1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148803187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e212d4fafe68f0c10626374ccb6d62ba1b8d22f76d5b5913300ed6cfe2ba0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:16:38 GMT
ADD file:28e774b3554d274fc742feac48f78a3bf6f120cb729e2824007dd94d5c414156 in / 
# Tue, 23 May 2023 01:16:40 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:46:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e109feef3fc6307cd9a880958cef6624de9c2c6f054987e479461a1ae51c7503`  
		Last Modified: Tue, 23 May 2023 01:20:49 GMT  
		Size: 53.3 MB (53312324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab84a55cc084469df8b38ab6a01658bfba2b29b7410a970ba6d9d2864846672`  
		Last Modified: Tue, 23 May 2023 01:59:19 GMT  
		Size: 25.9 MB (25923867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfbe0bc6dc85168e7da83a7be20c9913921338417e0c639a93ff1cdc5664403`  
		Last Modified: Tue, 23 May 2023 01:59:46 GMT  
		Size: 69.6 MB (69566996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:86eba8d0ed60b48b529ddd1fa9a42ba9dc1e84552405d3cd7dd12bcd3cc025be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132378845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8069752d63fd4ffba7fda3c5fb1f7e844eab399da974735bc3c1809fb328a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:45:32 GMT
ADD file:d99fe1ff201690fcb871123822de04002451af1e06ae75e1a18fd80ef531de86 in / 
# Tue, 15 Aug 2023 23:45:38 GMT
CMD ["bash"]
# Sat, 26 Aug 2023 02:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 02:52:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:73c53ccb564b87caad8f214df94d16496ce4754e4b20ee558b3c8f3ac938e41a`  
		Last Modified: Tue, 15 Aug 2023 23:50:14 GMT  
		Size: 48.5 MB (48539809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a53bb03e6b4b7d81815de0b07a64fcbe6daba956f76e89e89d7b363f2792c8`  
		Last Modified: Sat, 26 Aug 2023 02:55:22 GMT  
		Size: 19.9 MB (19924635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e76065e4595f9d0768d5101fdd6a014761c6b1ebb18d266a2d788cc3e717e`  
		Last Modified: Sat, 26 Aug 2023 02:55:36 GMT  
		Size: 63.9 MB (63914401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
