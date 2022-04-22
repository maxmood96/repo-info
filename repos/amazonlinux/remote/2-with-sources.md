## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:c2f343c1353778866e90fba96b5b6173b255f07d302de7c0703c9c67d1c863f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:67fd44e1ca29a3c41ea875774083e64f218643232b1f5f27dfb1b1e4b6aeebf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.7 MB (485656205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c70976d4f4738c09199e01633142618f58f7bc2345948fa514aba7741d28e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:19:57 GMT
ADD file:4eb88d9d977dadb40c630d693a07ca066069b30b9751b7a421dfb4ba0b99d862 in / 
# Thu, 21 Apr 2022 22:19:58 GMT
CMD ["/bin/bash"]
# Thu, 21 Apr 2022 22:20:24 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-915f4823664b0d5efa5a9e17372f52c1e32718dcd0045d286495168c62f27bf6.tar.gz"  && echo "ddee5f71296afcb2dc85200f657f30688a3edb91a3e317592c02d9b387c62d5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ac1397dc8419bf1767b60a5cc5849b7130406030581d4542e48965801c303a70`  
		Last Modified: Thu, 21 Apr 2022 22:08:36 GMT  
		Size: 62.3 MB (62265199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf04fc591da032b75c5a1e2f399e07e93a1b66b3bc75b07fe457ede25a29d9d`  
		Last Modified: Thu, 21 Apr 2022 22:21:31 GMT  
		Size: 423.4 MB (423391006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:9ef53f86fd3105e8d6ed9465463739e3c672d0fb995722e7a7a0abf09bd2954b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 MB (487279116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a0bc6da757fa79443ed42fd5cf1b1909702466a8a507cfc78ca9f1ea291a09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Apr 2022 22:57:49 GMT
ADD file:76e1ee72575f50a75573a46483631e239d3b6afda9fdd53086883bd03db5364b in / 
# Thu, 21 Apr 2022 22:57:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Apr 2022 22:58:15 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-915f4823664b0d5efa5a9e17372f52c1e32718dcd0045d286495168c62f27bf6.tar.gz"  && echo "ddee5f71296afcb2dc85200f657f30688a3edb91a3e317592c02d9b387c62d5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:86bcd0b49e3391c117b5e27756fdf585aadc1a7b9054d19af0faa050839a6633`  
		Last Modified: Thu, 21 Apr 2022 22:59:02 GMT  
		Size: 63.9 MB (63888157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17307b92b5f720ad82dc04ee1d549790061ada9c458c29252ff0e64f85017078`  
		Last Modified: Thu, 21 Apr 2022 22:59:56 GMT  
		Size: 423.4 MB (423390959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
