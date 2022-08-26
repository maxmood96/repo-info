## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:21b5c144b6663ea5ef5d3a1961a85ca271969754f8b9edb236a93de867163df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c91344e903d6bea0fb98c8df86886491a013958ab957eb55a08e4a898727543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487998330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a9a6ede56b90857d5d422629dfecd2d2153eb3bf752bb71ae038541217232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 00:39:53 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-44ee790ea60c4090ba6e215c0d148c239e7806623b75f6f14930ce7e2f6b07f8.tar.gz"     && echo "8b5abb84b1d279d3c26a9c2721b1daa1317ca4109f56f84b032d756c3fab7368  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd6532db54d15f6c38e8c6535dea038b0e4354712e588e1424d2f035a863896`  
		Last Modified: Fri, 26 Aug 2022 00:41:14 GMT  
		Size: 424.1 MB (424059565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
