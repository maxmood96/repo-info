## `debian:stable-backports`

```console
$ docker pull debian@sha256:2794fb5d3ac7001f26f6d9cdb74d55a56fee5eea25e27415804086e076eff518
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2d1a2e9497a537ecfdf7cdc4efeb667dd6b88a1e5039eda0f3dac0ea757d8a7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49552435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d7e0d84ee7f400d0b6e3d4502bfaa712ed692806598d23203736305a5ef149`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:57 GMT
ADD file:bb6d65c0862f4c248ab930b3add61276f66e109cfcdf8c8284670e77a5861214 in / 
# Tue, 12 Mar 2024 01:22:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:23:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c3dfc3642728e6f63a2fd74702f60e4428d03be8021aeebb6616d0c71f8ac03a`  
		Last Modified: Tue, 12 Mar 2024 01:28:50 GMT  
		Size: 49.6 MB (49552214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9dfaa8f30bf0366427d8caeefdd59c6bb8f959d2fed2b678997460a7d4ef9c`  
		Last Modified: Tue, 12 Mar 2024 01:28:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:308e9ce99392d39cc3ea06c3965f3422aa86939705bcdf37b183d9cd4901ca8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47312405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f90cc109855f5f4262198034db17f7a0425f19ca6711435a26e2fa109a5346`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:24 GMT
ADD file:a7e63b06f90acfc8e078d2d5555082dc76843a9c1c60288a4b2994516ec0b82f in / 
# Tue, 12 Mar 2024 00:49:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:49:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a48dead7d630a614258467d52cb25d28217a0784fc045aece1a5ab99f6636a42`  
		Last Modified: Tue, 12 Mar 2024 00:54:07 GMT  
		Size: 47.3 MB (47312180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629c42ee061aaf5d1ae68277c58e51427f829342ab7b0ec85e286dcb22fbbf48`  
		Last Modified: Tue, 12 Mar 2024 00:54:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:78a99f4916c8fed6ba2373bd94409c4ce8a14a65368449ef291206374fcccbf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45154064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636032eaa7ba5b3f674046038a1be3e13b3436994db64594ba79999c3de40b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:04 GMT
ADD file:d41d66f5770b55de36e7540e52c3c77e3428d0183e5f95cc2225623eafb50cb0 in / 
# Tue, 12 Mar 2024 01:01:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:01:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71bbf3d6a08ee6ee9fc74963cc39015640e7bdee4ca12e42602898aa729113b0`  
		Last Modified: Tue, 12 Mar 2024 01:07:07 GMT  
		Size: 45.2 MB (45153842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f9fdd756e7062331d8bc83f83f8fe23d88c49327304efb44a46c8b60fb489a`  
		Last Modified: Tue, 12 Mar 2024 01:07:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2d7b5a3e8bf3f3e0d376766537cd5998c4e7706e34b1c43559305612c2d472bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a3e21acb894924124fabaa361f7544e3fed130ff269e19873bcafd5a9428f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:54 GMT
ADD file:2c0e0fea2d6500c2c63ecb8028e0f9f802fcd260a94e9ea992a06ba2973c6f49 in / 
# Tue, 12 Mar 2024 00:46:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:46:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f5c6a5342f5cf4985c69c82ee31368e3fc663b24c0d25981d9907064bdbc12cc`  
		Last Modified: Tue, 12 Mar 2024 00:51:59 GMT  
		Size: 49.6 MB (49590975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4675c995d9e8c9e125942b060a8e8769e0488f890f2f81d950e1ede5a375d51d`  
		Last Modified: Tue, 12 Mar 2024 00:52:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:0a591ecfe742a99a1fd9a711914097eaa057893d3e3049dc1b7dad77912f4c5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50582108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff830a1b1f2c35858126835421c5c4e491f5d154af6c1b23bce6383537339e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:00 GMT
ADD file:812ef597450844ee897c4a099040601ed2aed20d11ae63b92bc579a3b0ea660e in / 
# Tue, 12 Mar 2024 01:00:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:62d6f4de454792b5447635bbc39fe875f68052cc42403ce14360f226375078d2`  
		Last Modified: Tue, 12 Mar 2024 01:06:28 GMT  
		Size: 50.6 MB (50581884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebebae8350f9b28931f2d899ca7839863d9acf6e2b9b844af23fb711d6ff4fdf`  
		Last Modified: Tue, 12 Mar 2024 01:06:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:d6ad0d84b383626a485595e5dd94b20fb9490b74c9e1cd758b9e0a23177661d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2420171dc51342d1cb89d46ec899e05a2651457e5148949541c8876e8822b5eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:10:26 GMT
ADD file:0a50403e22bb556f73386ed5ee0cc0e83169c5d685776b967289a89be81ac99e in / 
# Tue, 12 Mar 2024 01:10:30 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:10:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:045ec8374801042d4e05581cce3965f3d5b10eb00c78949bfb35f78b29cb21b3`  
		Last Modified: Tue, 12 Mar 2024 01:22:18 GMT  
		Size: 49.6 MB (49563159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cc2964650fb526a23a1175e1384886454402794d03b369efc8787c680fefb`  
		Last Modified: Tue, 12 Mar 2024 01:22:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2fb9bd1b49831e1c7fb577933d5c536b0b3c2bc6cfc3d5e01a6f85dd7f4be41a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7a2823b40b94a9701a38364a1ddd747eeb641f904241681aeec48b436a0c6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:32:47 GMT
ADD file:1a191b0f79d13e067ad0fd5cf7660dbdbc47e3b8c157db939f85fa4dd2ccb6ca in / 
# Tue, 12 Mar 2024 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:33:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e3e92d660782849c9cd99133bd4f657225b6d4d472a93a7152791e1606dc3d94`  
		Last Modified: Tue, 12 Mar 2024 00:40:35 GMT  
		Size: 53.6 MB (53556906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064ae5b8b3864d7563f4131fe6eccb3eebe82ce9bd330ddb1ed4eca20a7b7bf`  
		Last Modified: Tue, 12 Mar 2024 00:40:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b1c0bb027eef0f2bb601b5ffa98377b351ecee98f340fd2b9a5d1e9d0e926eb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47916933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c51b76e3b95b1743b7087afe83c94bb714308982faacb7a7a28658267b2a04e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:02 GMT
ADD file:78827d12ac2ddccae4fee843f82d04a85e6b81b8e8b00db8e2c7dfddd3c0478c in / 
# Tue, 12 Mar 2024 01:05:04 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:06:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1772641baa945237100109f18d05fd541348b00b201055484ef97c6adc7ebbf4`  
		Last Modified: Tue, 12 Mar 2024 01:22:55 GMT  
		Size: 47.9 MB (47916709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beab7a376dd2d399e12f3b71b349d77ed73e9397905db380faff8feadb30435a`  
		Last Modified: Tue, 12 Mar 2024 01:23:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
