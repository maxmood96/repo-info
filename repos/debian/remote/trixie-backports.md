## `debian:trixie-backports`

```console
$ docker pull debian@sha256:132a1383b864e8073f9b414445a536c49ed6fa5e5590605c6c6759ee31423b94
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:7cd92d5096988f313b05a8d9b42b7e50cb5804a66737fe33b9eecca37248aab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49604376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d569e5bc2b52eb1fd1928375ea4473ecafd6e19595bf0232c3b082fcfd05442c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:02:32 GMT
ADD file:1170cd4ff0eb634606742ce298b7bef45db4b76df3573e41853850f4bb1fab87 in / 
# Wed, 16 Aug 2023 01:02:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:02:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c74a9d7ecb9b51b7ca655015e97fe63c4c4643adaf35c9af51956deead7d037`  
		Last Modified: Wed, 16 Aug 2023 01:08:58 GMT  
		Size: 49.6 MB (49604152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc0d9cd13ec14b05ee1894d7450c1411bdcccca560e40280c03c90948a06926`  
		Last Modified: Wed, 16 Aug 2023 01:09:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:629317e1f5b90fadb1fb92a23a209f22e7c40dc97e29b18b016d279ccf28b40d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47395349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f67327679440f0036887b5d460b6838f89e8581f17c7afa8b01578a922c8def`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:56 GMT
ADD file:d0da838ea8ff64a44e445dfb0001a4f6a2442085f0c0f942d0129b6f8054c7fa in / 
# Tue, 15 Aug 2023 23:49:56 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:49:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6d8f24fa9802404161e1d0ef0d1db6d5f4c20cb1f0e5884dd191e1d77f2373c`  
		Last Modified: Tue, 15 Aug 2023 23:54:43 GMT  
		Size: 47.4 MB (47395127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595fc3b761ab0750256a3059eb3a81984b876b3d315e76592af11a4b592c5640`  
		Last Modified: Tue, 15 Aug 2023 23:54:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a01f9fa4ea856ae31be0070715ef1fd339f25262ed0687c129df0d65e1a48b9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b546a1d0f2916ff8c98eaffad039a888ddbad401dea58296df0f5e5aba405c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:19:37 GMT
ADD file:fcc6e87e54bebf4c148573f42bb67ddfe40bbb89b37b0c88d5a5ac8074852e50 in / 
# Wed, 16 Aug 2023 00:19:38 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:19:41 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:00b7ed9deba9ea7ab64452a4e5dfd73f0f68e2784fb8cd589dc15932edf9a46b`  
		Last Modified: Wed, 16 Aug 2023 00:25:41 GMT  
		Size: 45.2 MB (45176042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466b6c570fd3c2713beb3209c055978e1d002d943d009d373b2a76ebfffe332`  
		Last Modified: Wed, 16 Aug 2023 00:25:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c27b6c2a1965658833ec27edc0d3401202f109503eb1c81ce92a8f49a45f48f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49522202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d781dfed58f60b08e68e76fe17ec9922b573125dfddf4a7b53cebac07613559e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:42 GMT
ADD file:16621389c05de9ece6b8d40e6c62ca81465940296cc58f7f1c56571fac05b33e in / 
# Tue, 15 Aug 2023 23:41:43 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:41:45 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c5fc9f67522f8eb1fc65844ccc91e1d93595f85d410842d334c85f7e0a15d841`  
		Last Modified: Tue, 15 Aug 2023 23:47:22 GMT  
		Size: 49.5 MB (49521978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cf68cfe6022db91f0314621a18fe9ff3f478f6830df4e9bc27b45115d85891`  
		Last Modified: Tue, 15 Aug 2023 23:47:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d7aa4808a28c9c7ab4265dd27868b589ce9db8b65b8791f6e012d880765d72d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50618757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c001c00d8feb25926c94108161d32246aa67965e488752513f7f988d7a5af228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:32 GMT
ADD file:4d14eb57255656e664c93bdd44713aab3556f53199d3002e8b099b8a4f99ee66 in / 
# Tue, 15 Aug 2023 23:41:33 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:41:35 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:92cb61533d6d73bc90b946ae69c5db6942d13512056cb4f565d14697cd7aa909`  
		Last Modified: Tue, 15 Aug 2023 23:48:22 GMT  
		Size: 50.6 MB (50618535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cb415975c46926f754f627525c5e557c0e3cb8667d931f9d29e549ca6f0540`  
		Last Modified: Tue, 15 Aug 2023 23:48:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3642af36404b260a93ecc46032baac5b82e1902a6d57c4b8b15a2e6c17db94c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49450010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dd49c1bdb4b5c335f9e40ba2e12421625cd8d553c100071c0e5e2fec5d1a7e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:15:24 GMT
ADD file:21a0349f8818b8dfb23d9795ca922c9828660ac081ba9db3e4fe08efddeef0dc in / 
# Wed, 16 Aug 2023 00:15:29 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:15:39 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b01e2a8b457425ca543dc2e5fd0920c4c1baf753962560010906ca5d157fb3dc`  
		Last Modified: Wed, 16 Aug 2023 00:26:31 GMT  
		Size: 49.4 MB (49449783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09fc033cc8929f0d28b76100c69e45a647595af1afb242664634cd820c9a245`  
		Last Modified: Wed, 16 Aug 2023 00:26:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b3a4ab1147f91550966324ba98ef23217bd85a82716a28d1d45f9b7c32e265c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53544269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0a737526ebac2e7f14f556aa1d5d80bbbc9487d6bbeae52f5d692a213d7fc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:12:56 GMT
ADD file:121000b06bc7b1fdd1e3c87b4b93debc6d4ff153c7e305f8fb9fe076a52c4ccc in / 
# Wed, 16 Aug 2023 01:12:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:13:03 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa279ce1030b6b03f549d223eeb76ece36944bfb3a79e0a2758b54fcadc346bc`  
		Last Modified: Wed, 16 Aug 2023 01:20:59 GMT  
		Size: 53.5 MB (53544042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1c689df414a3eee38fe4e6076fbebae69cfdc9514a556f1755d623f70ecbf3`  
		Last Modified: Wed, 16 Aug 2023 01:21:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:ee76d8178ddfb5eca74c7971a0c36146a98b06d22671259da3db82e0bd826374
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48540033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738b5c61b570b03f4404f6bc446db1cb3a56a48546e80058d531356a1b21d721`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:45:32 GMT
ADD file:d99fe1ff201690fcb871123822de04002451af1e06ae75e1a18fd80ef531de86 in / 
# Tue, 15 Aug 2023 23:45:38 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:45:43 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73c53ccb564b87caad8f214df94d16496ce4754e4b20ee558b3c8f3ac938e41a`  
		Last Modified: Tue, 15 Aug 2023 23:50:14 GMT  
		Size: 48.5 MB (48539809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd900779cc19e5cd930fab5f49a837be66dbdb8d98eaf247522a3ffb039e622`  
		Last Modified: Tue, 15 Aug 2023 23:50:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
