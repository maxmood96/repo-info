## `debian:experimental-20210927`

```console
$ docker pull debian@sha256:36c69773d24dce42b8a5f0badf9e36d65bb53603b4dd6ea4787efe9563cf513f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20210927` - linux; amd64

```console
$ docker pull debian@sha256:b279cc9c72c9fa3cf7e544f2ce727bb9bf8ce1038c85bc59f14788529aee7a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55702303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fdaa2dc57071f1e17bda59e7fd5c9bd4575b5f15f22339a6ac7b84f5289f91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:26:13 GMT
ADD file:d9d629780e76b855e899e172dd9c2c5af25041582089ee1b21e93ff0203a3521 in / 
# Tue, 28 Sep 2021 01:26:14 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:26:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f2a8c55f290b62847a927b026f135fd01ab2550c4deb33fa1781c18f90374632`  
		Last Modified: Tue, 28 Sep 2021 01:33:49 GMT  
		Size: 55.7 MB (55702085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6618546fc27afaf845d3034394cc0f15d38e1045cac3ae34bcce417a6ae678`  
		Last Modified: Tue, 28 Sep 2021 01:34:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20210927` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ffa74a7edf8c16771aa3e1e8af3d5eed4d24c30294faef70447e4b33931dd550
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54725540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b42c7c97535bf9e53241809cc92cc2ee42df0f24ab42d1f7bed7824a66e8740`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:44:06 GMT
ADD file:c6c834163255512247f4299caa0071f4b3fe9392b02ab3867c05508f08da5a03 in / 
# Tue, 28 Sep 2021 01:44:07 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:44:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2d3594ced7745eb15a2b7007358597197a2ed8197194eae33fc3ea0db03f123f`  
		Last Modified: Tue, 28 Sep 2021 01:53:59 GMT  
		Size: 54.7 MB (54725321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b3a15a5395971b6741d18737f616db4b8eebb644c0e355d1c2d22f4c81821`  
		Last Modified: Tue, 28 Sep 2021 01:54:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20210927` - linux; 386

```console
$ docker pull debian@sha256:c74b9a5b86929bf602240b6eb825c153181d6439af544dd0785bf56566f88012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56733439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5410856927dbddda32c12d7806b55a3f365832967069630f6bb160dd032c0c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:44:32 GMT
ADD file:6b060b0698e864f6ef8a07c3a6a71205dca18a95b9b8c95d64d2a2fdee7d7846 in / 
# Tue, 28 Sep 2021 01:44:33 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:44:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9b5dc80bbd482cc8a27c804eb711f6f3216dcd2c0e78e2cdb9b847151d747ea9`  
		Last Modified: Tue, 28 Sep 2021 01:55:19 GMT  
		Size: 56.7 MB (56733217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2cc89fbb9e27513abfcf28343eefd536efaa49cd6b001560ae862aa0b02a23`  
		Last Modified: Tue, 28 Sep 2021 01:55:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20210927` - linux; s390x

```console
$ docker pull debian@sha256:76a9aec81cbf2ff1cf52171e5a57fd696d2bc9a2601dfbbce0e85cce3d17ba2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53954079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173c91a279f8fddd18831e4eda741ba964397b1fb423c6b4738a69715f8b3be1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:45:37 GMT
ADD file:8209381c87e3a9b971b314c7cb23655d9eaddd1cad08b612f6f6d0c97fa2fdc8 in / 
# Tue, 28 Sep 2021 01:45:40 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:45:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:95d1bea7bb30019c440a4a51393275efc64a586b9a0f916a69c27a386c444240`  
		Last Modified: Tue, 28 Sep 2021 01:51:40 GMT  
		Size: 54.0 MB (53953860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ea63ed6a7e4e213858f4021cd6e8ae74db5bd9ad85c27ff53f739d566aa1a`  
		Last Modified: Tue, 28 Sep 2021 01:51:58 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
