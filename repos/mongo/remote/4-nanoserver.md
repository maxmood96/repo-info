## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:48f6089a6cee04ba4da8537552e1673468c4c5606e6254877a67bf18c16f51ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:27f06d9bde9a228054184a4618e2d7b6fb6ba9218cb86bf98ab849182c628139
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366459682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e297a936b89c337d262bbd0574138c19ea77b5c2900ff22f3c0c902bb904bd74`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 02:09:24 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:09:25 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:09:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:09:29 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:09:30 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:09:31 GMT
ENV MONGO_VERSION=4.4.29
# Wed, 13 Mar 2024 02:09:42 GMT
COPY dir:05c527a8cd901f69ca11856f2b42c60f8bfbb1c962d124799003a0c1b4353f7a in C:\mongodb 
# Wed, 13 Mar 2024 02:09:49 GMT
RUN mongo --version && mongod --version
# Wed, 13 Mar 2024 02:09:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:09:51 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:09:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ecfb8f4ed8e92da40b94150a237e938b027553d5a443f3f9a89874b62dc160`  
		Last Modified: Wed, 13 Mar 2024 02:10:00 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90f26cf3c65f0ec71ea9d66d865160aff1fe60a869f32d7ae3d97720be1302`  
		Last Modified: Wed, 13 Mar 2024 02:10:00 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfedcfe9ad86229be4e585a822847ea7a1dd3773b79c5701e19700c64b546a1`  
		Last Modified: Wed, 13 Mar 2024 02:09:59 GMT  
		Size: 82.2 KB (82205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c63bd07f732c5189c5cf23acdb97d565de71e84116c81852fc1fa1f46b35b9`  
		Last Modified: Wed, 13 Mar 2024 02:09:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cfb96b81e05d2e74b00e18f9e833b5908bf91396ce3d5abad68400bc3f26a5`  
		Last Modified: Wed, 13 Mar 2024 02:09:58 GMT  
		Size: 267.4 KB (267440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d0832bbc1c9d5d4155de9539ec867944bfc4b334559d8bef6aef54f4e16dff`  
		Last Modified: Wed, 13 Mar 2024 02:09:58 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5267379191b6483a6b6fc0cad52ee9f7fd42ccbf902a03e3a5657bdeb41739`  
		Last Modified: Wed, 13 Mar 2024 02:10:21 GMT  
		Size: 245.3 MB (245305545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13a0b14138f4afb4d47e715ed66dfa448b4dd4685ae1dba135caecafb6a8dec`  
		Last Modified: Wed, 13 Mar 2024 02:09:56 GMT  
		Size: 94.5 KB (94497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f36af31780ff55204277122f633e54255e38d0ed690d5e16a063fa3dc58dc6`  
		Last Modified: Wed, 13 Mar 2024 02:09:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160088262d74f3a5935be9e62b40d1fa73608044f6d03f1ac7d68896dee67f0`  
		Last Modified: Wed, 13 Mar 2024 02:09:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3fc76cb258ca3912797c5b8a75fb95f5dec7116d1a46b000b2ac4597a9834`  
		Last Modified: Wed, 13 Mar 2024 02:09:56 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:d512ce935fe777af9c71ac3279f607aea713d71021c0826ff87ab555470a4fad
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351659334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a64a3549eb75e4aac6226bebafb62169f061bd8127d61b09192f2ae3addb2b1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:06:01 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:06:01 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:06:03 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:06:04 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:06:05 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:06:06 GMT
ENV MONGO_VERSION=4.4.29
# Wed, 13 Mar 2024 02:06:18 GMT
COPY dir:05c527a8cd901f69ca11856f2b42c60f8bfbb1c962d124799003a0c1b4353f7a in C:\mongodb 
# Wed, 13 Mar 2024 02:06:27 GMT
RUN mongo --version && mongod --version
# Wed, 13 Mar 2024 02:06:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:06:28 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:06:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333178369c6bb718b4d22dc1fb083552e7aef35881bfadcd9016f6040f53c2f`  
		Last Modified: Wed, 13 Mar 2024 02:06:38 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93453cdf8d2a42fa4f15dfbcad492726c832532f7c39fe4fffc3efe56ae78f73`  
		Last Modified: Wed, 13 Mar 2024 02:06:38 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a8f2cb148203de713d24c7f28daec0782f339424393c7765dac185eb8e5085`  
		Last Modified: Wed, 13 Mar 2024 02:06:37 GMT  
		Size: 73.3 KB (73288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90fb6ad620a8d47670d50b1cd28b744fe6bf90df38e3d913027eae068ccd5c7`  
		Last Modified: Wed, 13 Mar 2024 02:06:36 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05458600b82b242dbee0db0e6898adcede4be1f4894c490b2f9662ad20e8a6d`  
		Last Modified: Wed, 13 Mar 2024 02:06:35 GMT  
		Size: 267.4 KB (267435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d40dbc7534b824e7b6f43fb2c2b7db51f5d84c5934a954fbb9868ecc8d8c544`  
		Last Modified: Wed, 13 Mar 2024 02:06:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4908e4e429a11780d5a1c353fc8886e510536ac321ed1cd0d86aeed3cce2a508`  
		Last Modified: Wed, 13 Mar 2024 02:06:58 GMT  
		Size: 245.3 MB (245305631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328173866d69cb04fe8d8a77f8d3b1010040bcbaa1cffbceac9dbd12de814e6b`  
		Last Modified: Wed, 13 Mar 2024 02:06:34 GMT  
		Size: 1.4 MB (1385599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b210891b7591789dac4d1ee1645e21a18d10e40aeba356e59a16051928581`  
		Last Modified: Wed, 13 Mar 2024 02:06:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a5295c2f69877b0f8a6a3ebd2a1b2ddc00de1383be67dd847f885b15880269`  
		Last Modified: Wed, 13 Mar 2024 02:06:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44eb352ebd0d504fa2d05f2868318d3d6630c6e243f34c65b21edd69bb0ddaf8`  
		Last Modified: Wed, 13 Mar 2024 02:06:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
