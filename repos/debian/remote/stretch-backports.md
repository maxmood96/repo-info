## `debian:stretch-backports`

```console
$ docker pull debian@sha256:3c08a2240db20598d831f8293f3954310e1820459703aee0810daf2270288999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:d9a64d561a6dcf1de97a78537047d7f3d63e9a443b54a19bda0a5f6c142591ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45430245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa615e99255efa8b09be1abe27e17bb93a79ce49fcedc420eeccf727585ff0b6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:22:14 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c2c583c653f37dfd5c24a19a969b744bdcb3209716087ef4067bf934d0ddc`  
		Last Modified: Thu, 23 Jun 2022 00:29:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dfdd5b5b69b7dba4bd7340a99ae496a72bbec5c311318d0e1cd7e4b37896162c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44124878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2bae701f2f546cd2eeaccd041b15535af24721981bd4c0be1abb167e8528d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:55:37 GMT
ADD file:4fd9afff1465319b24ccf87076562babe87771f9c1251684705a3896e673aa09 in / 
# Thu, 23 Jun 2022 00:55:38 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:55:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad86940bdd4f85f3b8d536255a8263fa6320c5075402f2a29b22648c59285219`  
		Last Modified: Thu, 23 Jun 2022 01:12:52 GMT  
		Size: 44.1 MB (44124653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42767fcc75ef3806641ed857fa28fcf409f8ad36dbef2924654e0776f7ac855`  
		Last Modified: Thu, 23 Jun 2022 01:13:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9e7fa538dd6e7159df38a14d4605d43dd37aec9abefa680b8a2b00cd0617b628
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0770c300e06e44ea384bf758a6ab1d3ea36481c312de3867f6718e314dd100a8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:05:16 GMT
ADD file:f859825c79355490a08b5fd55799cc3eb1643e21abfeebe59a3a4b08e54e3f7f in / 
# Sat, 28 May 2022 01:05:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:05:32 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ae3d55ab33f9bf9aa2c47629e66da1c4e679da10d83c29941f39b04140996e4b`  
		Last Modified: Sat, 28 May 2022 01:21:38 GMT  
		Size: 42.2 MB (42150781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34e492b50671ebe5997ea3a6d53fcc53fc84f71d310916f9df435e0db9ab3ba`  
		Last Modified: Sat, 28 May 2022 01:21:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7dbac5675768e03f4dbcd479dfd56e060df653a6acf74fac1f7b2bdbb2874126
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f7c39f2cf353a9f6e7375d074aee9a2426e58ba997fd4272c619bc55d16a73`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:45 GMT
ADD file:3d8b1da94fcec5d068e3e6465fac70cce404c331bb52e30a5bf7cbd950baa5fe in / 
# Thu, 23 Jun 2022 00:42:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d8ccec8a513f896fedd1d9765f3f2abf98bc8264f61cecf17919c80c9aa7ddbc`  
		Last Modified: Thu, 23 Jun 2022 00:51:18 GMT  
		Size: 43.2 MB (43213121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d460f028f56489890a42a3781f2b6a37f537c3b13e02800a37e92fbe140b3`  
		Last Modified: Thu, 23 Jun 2022 00:51:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:70292b5dfa8079f930fff5c17422d2f99fff1d737e6ce9822716b5236029c57c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46150823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ce43e3c3c25d7d8ee2796f7dce6d0957327c96238a11f0ab385022616db043`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:44 GMT
ADD file:ec3ab24d5698ffb1c2c01f4cf088854df8d14de655c3ea1235b3ca4c06864be4 in / 
# Thu, 23 Jun 2022 00:41:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:41:51 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:198ad075a14b0fdef3454be69cd94a50c01a286b210867ddfc0a62404bdf34b1`  
		Last Modified: Thu, 23 Jun 2022 00:50:47 GMT  
		Size: 46.2 MB (46150601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89386d6540cb273140ff7df1034688ce0f7969a5be4cf486cdba8a5afdcc181e`  
		Last Modified: Thu, 23 Jun 2022 00:51:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
