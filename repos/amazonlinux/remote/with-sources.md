## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:150721a0226b49f11ccd47ff3af21495abed1ac0e53f835222330565ae55d84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:983d3e4de81b1c27d66e23dcaa8a16c475d5c5b495aa385604ccb648a8058788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.9 MB (542850367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e352e313d08efc3970e6993a06e67920b041e2e9e87622b5a62639aee5437d5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-020afd68ea87fb6a4b381a6874ce0c38c6f291f66d9f9d9fda853a9bc76a954d.tar.gz"  && echo "c74f4742eb862e351271e7bceff838061332d4bba919f1944568ed779351fceb  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332009c39171868832b64d8784eba0fb853d50be1faf582791d991cf57a9210f`  
		Last Modified: Wed, 27 Jan 2021 22:21:53 GMT  
		Size: 480.9 MB (480853791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:9c7588150eff1d7928416c7fafd35edaa4f1d03d663f0c7fdac8ac62de67c8a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.6 MB (544552541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d28578129bba32d0a61dcb4c5ce73ca3365c60abcae712f3c4d2edd3009ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 19:40:28 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-826e231a97252a5034e63006e69224de2364211252782ce0d9eab6a50c799006.tar.gz"  && echo "3d237536b5aa360bd744e30abd284cdd42eb182e390f3d4c2abc4655f7a048a2  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3431b17c8d2c281dfa9b3b9f9880a6159a978452bed73137b8af89f04586250c`  
		Last Modified: Wed, 23 Dec 2020 19:41:41 GMT  
		Size: 480.8 MB (480844627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
