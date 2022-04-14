## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:2fb42dead48615005ba5025a4fbbf78e727a109db62e2bf4983458d75df5275c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:10ab75802dd29ae735c049114c2b611129bb94ce07362f026057bc10a4b5ba0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.5 MB (485466953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627a04a8a008d782bc28123d6dbdafa6f3f8afd131c672ff0a00e23f430334a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:26:30 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a46ccefa1703a8b084ff61437d3d05b29f0a2c6eb6ec89bd30e032b170f7dd2`  
		Last Modified: Wed, 13 Apr 2022 21:27:38 GMT  
		Size: 423.2 MB (423229312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:1773bdac84c234a2f6c22851691bddccaaf1840e23b3c2b03872ef1a8cfebdac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487099537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4bdce10b7213f190095856d33f28b129c6f0858ba3ff1f73161425e84abad3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:39:50 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-0a6406ddc8f2cf6eaca89f0b86f008795cf7145cae334d41809451cd61919925.tar.gz"  && echo "d93caf88c75199c6d433f852aa108aff70e5c02d6f942a77c9572764a3bd6f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ba8c8fdc0b7272b7bef0ff89656b50b63e5b4baddfa8bda2b42d73a7ebc1d`  
		Last Modified: Wed, 13 Apr 2022 21:41:23 GMT  
		Size: 423.2 MB (423229256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
