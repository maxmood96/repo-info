## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:f20fdb3ceb3a1ffaf6b8c6febde34ad55e4510a53c68a18ec7fd4f996dd73aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:06237ff0de1785329f0428e83d7ee58d1430a5f0e33cbde4edcd9dddcf292d7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391374875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972d3f26f41b671359686ec38bc7ed11c9d2c6014e0da98b70e878a176bc0ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Aug 2022 12:14:13 GMT
ADD file:66d41fa1401574d2e46e90ac16b59303f71c7bf398ddb0922a8d1e901ff01a33 in / 
# Wed, 03 Aug 2022 12:14:14 GMT
CMD ["/bin/bash"]
# Wed, 03 Aug 2022 12:14:34 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-957d3ae3a19e9ce71b665e8cd92c84fbdd09ac787fc6fe6e529d2eb7dda57e9b.tar.gz"     && echo "e6514c0ba308c79d2d886e936bb17e7b6c5bc1761cc0264a8bf9c7b97d751f2d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71f53d65e46f63ed07b6ba9d631c781f35a9e3aa0c59d15d2a6b8cf540ea474c`  
		Last Modified: Wed, 03 Aug 2022 12:15:19 GMT  
		Size: 56.6 MB (56641949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61cbc02f83028ec35f5475f7de55ed612be3498de9f4689424fd826a703e17c`  
		Last Modified: Wed, 03 Aug 2022 12:16:01 GMT  
		Size: 334.7 MB (334732926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
