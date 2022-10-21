## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:05f6fd7b6d314f7469cb27a20b06c44f59c33fc58486d372dedadcecaf5ce9ea
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
$ docker pull amazonlinux@sha256:9cb56adb55e362e1f0bc602fa374ee76f5c811694dd0fbb8115405ba485f9b36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487995276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c9041ba9d726678c5b01f35d67267439fb39bd34ec3c1639468508c85fdf58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Thu, 20 Oct 2022 23:39:58 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5739eed8c30abe39025fd3b2efc192206cf6c30a9ed1c856112143b6d7324455.tar.gz"     && echo "b2bcb16e488395c3f073ae7cf2cd2a3e979e50c0448777aadc746bc60348fc92  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c50b200f4b88b34f76bfe2124998da6bcab84e615337b7fe7ddd2d8ac33114e`  
		Last Modified: Thu, 20 Oct 2022 23:41:19 GMT  
		Size: 424.1 MB (424075407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
