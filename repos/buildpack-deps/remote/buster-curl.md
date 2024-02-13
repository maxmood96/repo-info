## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:18eb72bb14a017124ef198933346132b4772609c65bba701d80952c84023db8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6b25066b29961e7aa16ca8406ce5ea650e3f8855c33e35ccaa115907dbfdea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85804feeac02c23fe4d8e2f956ae269dc0d6bdd4dff8a8f46ce34da5cd61d63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:53 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Tue, 13 Feb 2024 00:37:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7629bcdf769df4adb53f7f8ce490c59d26120c4db3b26afc982af6195e7caaa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aded50834613a27916572e410a2100b6802896d74f2c4b1a97cb0f38df5c335`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:51 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4f164ec5a25585f32edddf47dfab977b6f777c1087a23e5cce3b3d7389864500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66744369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6df5fb88d550a5298172a8ac8559d862d8dcab6dca910aaaaa3f9a6e07e4c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:41 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Tue, 13 Feb 2024 00:41:42 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0de08e18f1a2929dfd26d35b29bf2023e93138007d277e2b8e4ff6b7631e771d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae42ca5d891331e40f0cc8a32f83ba0912ecde69a7d2e2fabba6f37844828771`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
