<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220912.1`](#amazonlinux20202209121)
-	[`amazonlinux:2.0.20220912.1-with-sources`](#amazonlinux20202209121-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220802.0`](#amazonlinux2018030202208020)
-	[`amazonlinux:2018.03.0.20220802.0-with-sources`](#amazonlinux2018030202208020-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20221012.0`](#amazonlinux20220202210120)
-	[`amazonlinux:2022.0.20221012.0-with-sources`](#amazonlinux20220202210120-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220912.1`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220912.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220912.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220912.1-with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220912.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220912.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:c558b4ced0c9b24345b87550fda27c590305a94e1dbc194afde1ccd220d1ec26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:60a54cb951cc133bf060ca0819e37c03a3e5451ed0f24b998e851bce36b8a397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57897158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fa8b9e37e99d124872107735426246b59a55cf190d2d1344fffcab79445a20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:19:43 GMT
ADD file:53e1223ac2577a9120a1b918a6969a2f229da88a56ceca0716f26803bee1c276 in / 
# Tue, 04 Oct 2022 23:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8064ab546d10ece855ef4e617864c1d385e149fff22821e280700a12e22a2a6`  
		Last Modified: Tue, 04 Oct 2022 23:20:36 GMT  
		Size: 57.9 MB (57897158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f83a2bbda22563cf22b595c53d7876a865673630cfbcc59eb726b85a27c7d3b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56695136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8099661b027fafe50d8b7015848df13b8b4c79824bebf31c37dc079e624b91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:3f0f875a288565f921dcdd4a86c780ed67ab0c18681ab1b97a7d646867e32c60 in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1e20b0535c285d016cc63a5a609b903e411c78071837e64ea3314a22ee2f50d`  
		Last Modified: Tue, 04 Oct 2022 23:40:39 GMT  
		Size: 56.7 MB (56695136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:5e477e5056e1f2d8396eca71c9935714fdd31a3f7ffbc67edecbec16230dfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:77dd340fdf55b940cdc52d4b060c93adcbe7e05cc3e12a09019130c7401d7931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 MB (391152213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2c8214c206b8a8e0a99b00da665da27d4cb6bb77ce01dce4765330f6ef82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:19:43 GMT
ADD file:53e1223ac2577a9120a1b918a6969a2f229da88a56ceca0716f26803bee1c276 in / 
# Tue, 04 Oct 2022 23:19:44 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a8064ab546d10ece855ef4e617864c1d385e149fff22821e280700a12e22a2a6`  
		Last Modified: Tue, 04 Oct 2022 23:20:36 GMT  
		Size: 57.9 MB (57897158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544896198d372500cc3a12d5d6b9faac3193dafb226e54cffd9593e18e8f59e4`  
		Last Modified: Tue, 04 Oct 2022 23:21:00 GMT  
		Size: 333.3 MB (333255055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:d189da355fa602d9b49f2579df6d35f38593ee96973f9659ed162f21955910dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (389950161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d5cc125d8b47dedd0059002952186a317b7ab8675fd82a9c90b8c488065822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:3f0f875a288565f921dcdd4a86c780ed67ab0c18681ab1b97a7d646867e32c60 in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:39:57 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1e20b0535c285d016cc63a5a609b903e411c78071837e64ea3314a22ee2f50d`  
		Last Modified: Tue, 04 Oct 2022 23:40:39 GMT  
		Size: 56.7 MB (56695136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00725a1a157c2e1b2b4928f94f0c78fb36b2283c6058a616036be3067167abba`  
		Last Modified: Tue, 04 Oct 2022 23:41:09 GMT  
		Size: 333.3 MB (333255025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20221012.0`

**does not exist** (yet?)

## `amazonlinux:2022.0.20221012.0-with-sources`

**does not exist** (yet?)

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:c558b4ced0c9b24345b87550fda27c590305a94e1dbc194afde1ccd220d1ec26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:60a54cb951cc133bf060ca0819e37c03a3e5451ed0f24b998e851bce36b8a397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57897158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fa8b9e37e99d124872107735426246b59a55cf190d2d1344fffcab79445a20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:19:43 GMT
ADD file:53e1223ac2577a9120a1b918a6969a2f229da88a56ceca0716f26803bee1c276 in / 
# Tue, 04 Oct 2022 23:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a8064ab546d10ece855ef4e617864c1d385e149fff22821e280700a12e22a2a6`  
		Last Modified: Tue, 04 Oct 2022 23:20:36 GMT  
		Size: 57.9 MB (57897158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f83a2bbda22563cf22b595c53d7876a865673630cfbcc59eb726b85a27c7d3b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56695136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8099661b027fafe50d8b7015848df13b8b4c79824bebf31c37dc079e624b91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:3f0f875a288565f921dcdd4a86c780ed67ab0c18681ab1b97a7d646867e32c60 in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1e20b0535c285d016cc63a5a609b903e411c78071837e64ea3314a22ee2f50d`  
		Last Modified: Tue, 04 Oct 2022 23:40:39 GMT  
		Size: 56.7 MB (56695136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:5e477e5056e1f2d8396eca71c9935714fdd31a3f7ffbc67edecbec16230dfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:77dd340fdf55b940cdc52d4b060c93adcbe7e05cc3e12a09019130c7401d7931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 MB (391152213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2c8214c206b8a8e0a99b00da665da27d4cb6bb77ce01dce4765330f6ef82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:19:43 GMT
ADD file:53e1223ac2577a9120a1b918a6969a2f229da88a56ceca0716f26803bee1c276 in / 
# Tue, 04 Oct 2022 23:19:44 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a8064ab546d10ece855ef4e617864c1d385e149fff22821e280700a12e22a2a6`  
		Last Modified: Tue, 04 Oct 2022 23:20:36 GMT  
		Size: 57.9 MB (57897158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544896198d372500cc3a12d5d6b9faac3193dafb226e54cffd9593e18e8f59e4`  
		Last Modified: Tue, 04 Oct 2022 23:21:00 GMT  
		Size: 333.3 MB (333255055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:d189da355fa602d9b49f2579df6d35f38593ee96973f9659ed162f21955910dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (389950161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d5cc125d8b47dedd0059002952186a317b7ab8675fd82a9c90b8c488065822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:3f0f875a288565f921dcdd4a86c780ed67ab0c18681ab1b97a7d646867e32c60 in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:39:57 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1e20b0535c285d016cc63a5a609b903e411c78071837e64ea3314a22ee2f50d`  
		Last Modified: Tue, 04 Oct 2022 23:40:39 GMT  
		Size: 56.7 MB (56695136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00725a1a157c2e1b2b4928f94f0c78fb36b2283c6058a616036be3067167abba`  
		Last Modified: Tue, 04 Oct 2022 23:41:09 GMT  
		Size: 333.3 MB (333255025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
