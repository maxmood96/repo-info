## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:62789f043b2224eb1a3a2d3fedf8b67c36c0631869527698bb253a364b818b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:cec8782e7aaa5455f3a276dadc2e4297b28a62d6ecdb21cc0afc713434074829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.9 MB (474946109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823312af76af409bdda4e70151d51c4713c210d1dba1b23c9521aa73bf1c35e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:27:11 GMT
ADD file:9b89c392ab50f9fbb659519f443647dbafb7b229e63f95eae12d9cee1986ad4c in / 
# Fri, 18 Mar 2022 05:27:12 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 05:27:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:24f1509b57d4d358e2f5235efac55184007003087e2372f5f621b7c595ebdf4e`  
		Last Modified: Fri, 18 Mar 2022 05:29:18 GMT  
		Size: 67.4 MB (67426158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d72f01cba51a2f374f99aaddd4380ba43b81e13d58c8ea7d85bb58c017ecfdb`  
		Last Modified: Fri, 18 Mar 2022 05:29:56 GMT  
		Size: 407.5 MB (407519951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:efa82a440427284fb42c3bb04f8b6883d1d25256b94825dedc674a5dbd4bf666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473701235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f7a9f1488c64f9e231d75c17a96d6c7861535370a772aa719bf6f9d439a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:34 GMT
ADD file:0a3f467739b6b34c1677c74456d43d60dd73758c7cea9f5299bf964ac83a6f07 in / 
# Fri, 18 Mar 2022 00:37:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 00:37:58 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-fa0d04ab17f6ae9cb1de39ab5dad52c2e6d9fb369f43679b2f6a0c9e5d12c284.tar.gz"  && echo "35ebd0b74ac0b0422bf72c99f18fd2a38f226202adf6ee9271c52cf2ea7d3df0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8879502b9714388f162c398379c27a6290a8532d379327519640e91d05ac5b15`  
		Last Modified: Fri, 18 Mar 2022 00:39:40 GMT  
		Size: 66.2 MB (66181332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72833236772f911f636d1b918822c9a8ebd9cd41307464819b9beb9a35f16870`  
		Last Modified: Fri, 18 Mar 2022 00:40:21 GMT  
		Size: 407.5 MB (407519903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
