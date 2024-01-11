## `debian:testing-backports`

```console
$ docker pull debian@sha256:01286ca11e2a05cbb1cf4a1e6ef4260edb3bacb4f4012aeec7f2e72af2a12214
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:2d5e815b5ab12f5c11284f9560b7ba17ec4977421694298ad21e798c36b34413
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49562258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303f5e686e302d8fff8451e6e8b8ccea5cc5dd078634d51b54f89b082fb504cc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:16 GMT
ADD file:c2de988c5ebcbdd35e966e0b0df2b51f873da4fd6cfad69b544a880adea9febf in / 
# Thu, 11 Jan 2024 02:40:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:40:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca79a0e7616dab713d72010635cd337f89dbec0d613bd32a7723ad7bb86142d3`  
		Last Modified: Thu, 11 Jan 2024 02:46:13 GMT  
		Size: 49.6 MB (49562036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddfb142b7d6a1238eb39678133918d42fdefb067244a82f654c320ee54d174c`  
		Last Modified: Thu, 11 Jan 2024 02:46:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9acad769afd509d9f6bd1b4904695176cd73ffe87b03ce40656c091b5fd26d0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47275500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16af9428460dd0d00bbde4ce2b840dd642a67301583d0ba0a5a3f5c66f34fe6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:51:06 GMT
ADD file:5eb10a8acef322c94c6dace0bdaba1b4bc884b27c602474329ca2b61bec5a3dc in / 
# Thu, 11 Jan 2024 01:51:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:51:12 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01a68d485460a970e7f49c6721919a7dfe414f253859efd4de6ceed92d434ba2`  
		Last Modified: Thu, 11 Jan 2024 01:57:03 GMT  
		Size: 47.3 MB (47275277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e46ee7d6105d23aefe946d0fd5907bc51494e4b61a75003b1198bce51d969d`  
		Last Modified: Thu, 11 Jan 2024 01:57:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6a5a8f45c0986ba972d1a646ef7840e7304e2bd046135ae1362fda419efb8d79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45063689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17439c1bf0591a245445b79e071210ebdab824791e26d2d196752273a8fd4d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:14 GMT
ADD file:280e422ab65a24b8e657a1c853d4fe0f2156a02ca6f47d53d599f1937c038325 in / 
# Thu, 11 Jan 2024 02:45:14 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:45:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5457e06e1e16d62235b640137875b482b03bff1069f2010fab43f7a0d0609f24`  
		Last Modified: Thu, 11 Jan 2024 02:52:53 GMT  
		Size: 45.1 MB (45063466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f4fe8309a78171722c4340f58a53728ac1876297d92a73f06d19c208f9c18e`  
		Last Modified: Thu, 11 Jan 2024 02:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:23045c0ddd4af908360b80d5e4e5c5aa3bd77dcca8249f1243b9fedf014a7c17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49594385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed62e707e4f8c6353a9390fb9c10d82a79b233e77dbc6b02611ae8d2c674c9be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:16 GMT
ADD file:ef74fbd95a42ea9067fb58e0cb214318f25e01383dbaf8bd4f65c491328da115 in / 
# Thu, 11 Jan 2024 02:42:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:42:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45c62a2271fe4658739419a2d2f31eed9a7af320ff25f51d28c9961d6625d27b`  
		Last Modified: Thu, 11 Jan 2024 02:48:04 GMT  
		Size: 49.6 MB (49594165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9526bac3050a9c7e584f22bb97ea069f81ea37c30ed80fde5afea511011783ba`  
		Last Modified: Thu, 11 Jan 2024 02:48:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ed366f22e1dff2c299b329ce6b31c8c4cafd5db4c122ee6e7c649227fad4ca02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50527290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d604b8fe3467058a1ede627f2a2f0903c2cab56b8a26d8eb0652168067d02`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:02 GMT
ADD file:c626f1d2fb5f841d8bfe93637e77041a0cae5735dd6fc5e228829a4e79576052 in / 
# Thu, 11 Jan 2024 02:41:02 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:301b8853942493af4d453e790be5762833d544568485f2b61ac326c85670bddc`  
		Last Modified: Thu, 11 Jan 2024 02:48:12 GMT  
		Size: 50.5 MB (50527069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33b0d5400f4fce2514dedec8dcbebe0a70f15ca296f477915aa9d84d623fe41`  
		Last Modified: Thu, 11 Jan 2024 02:48:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cd6a897b429468cf943c0c46fba862bb41a9dbdfb304ae47ceac8b78582ddabe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49333505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfce58c50827674dcabcbcf4840bcd7cbbdffcb0fdc6ec9ef9eef8e13ae709f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:17:09 GMT
ADD file:54729da3e7fd950b26c0e2982165bb31cb3bec3154991b69ca5548a86e107186 in / 
# Thu, 11 Jan 2024 02:17:14 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:17:28 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6cfd039d0ce3d0545f76a805a0b508b4a0d2272adf3de69c759f8c63576de2ec`  
		Last Modified: Thu, 11 Jan 2024 02:28:48 GMT  
		Size: 49.3 MB (49333283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddbd1355888132b7b69567403ec85df82075e4ebc143d12f93feb880681d414`  
		Last Modified: Thu, 11 Jan 2024 02:28:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ba423fe339e06ac25fb51cc3998ef3b5e910001c660accb1ea382910a8ed9570
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53435969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481ba4ecb6184eb2e38a618a52ad18cfa62c5363724ad1db84fcc26e1d2bd219`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:36:44 GMT
ADD file:7bbfdd0ef6929b558d9177e8e25da2b51a5fc03501fe368eee680082fe61b5af in / 
# Thu, 11 Jan 2024 02:36:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:36:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:906621e89c1664a87130a19b59bad8b965ec51ec0ccda6544080841d92cc4105`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 53.4 MB (53435747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeeae28ad2018597255b2fb0666b304fe65bbc58c1be19de55bb02df72b6095`  
		Last Modified: Thu, 11 Jan 2024 02:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:3892e81fa17e3876a5d61b9b8ee40a9991abae35dd9cac9568fb5aa6368b72d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49092089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27964535e93289bbc0223cc83ada59d4e8f4e8fc3082c1da74db94ce5ec212`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:47:47 GMT
ADD file:99f7dceada5a4de4b63b031da99463b28215d60590eab63420c2d31adc558936 in / 
# Thu, 11 Jan 2024 01:47:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:48:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f29a37bb4112320796c8c57ad72bde831042b4c9adba3e230ca29fb2c897ee05`  
		Last Modified: Thu, 11 Jan 2024 01:52:41 GMT  
		Size: 49.1 MB (49091868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4ce678baf9c5473d03de36c74618d9175b473f822e499899d55111dde7425a`  
		Last Modified: Thu, 11 Jan 2024 01:52:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
