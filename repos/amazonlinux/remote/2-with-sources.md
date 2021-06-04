## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:92a93194e51ae2b7bca16cc13d23ed8d24f1ff654292721a95ef2fd4a794d8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:54a81a819385e5ba38b4586b3c960265d106ef7c3924e123dc6848a5b4c8c797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542818467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4415525a0de6b386eda3d2e8e55c3530698cf3846bd4fda077e8e21743635d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:26:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aa16be21b849cedc18925697d377825ff62903ab864293be050e3af75e2de4`  
		Last Modified: Thu, 29 Apr 2021 22:28:00 GMT  
		Size: 480.9 MB (480871335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:22ae10d8afcfbc828545f5925e7b7fb66201f45664b4def51f22b9c64b6481ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544531395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cdc6f6ea121d17b21f32bcfa7f650c13201914dc60ca0e269e86adbffd7134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 21:39:22 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 03 Jun 2021 21:39:22 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 21:39:42 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d13694054fd2292bc82935f30053f08860d9c7daaaa74d8f5f585dc5be3cc9df.tar.gz"  && echo "532d92b76391e5f08e90ddaac93c1dbf341a2a34550c32e357fdaae61a727917  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1d087798acb0c72603bd5a19518ad85996bbcc1faa1951c260238b894cec0b`  
		Last Modified: Thu, 03 Jun 2021 21:40:41 GMT  
		Size: 480.9 MB (480871327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
