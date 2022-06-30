## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:b508b3907eebc5582c595592a3921ebd879867eede29f497f0cab77a1b21ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:674bb59511e82c8a1c2d258fdcfc7a53a179669a9ebc795d480cb9a4bf8b6168
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (483963823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ea24a33c3438f88cbb312990d340600fcc8d3cc9e09e8a6b1f4f4bfc3bc4a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Jun 2022 22:19:29 GMT
ADD file:3cc0d880def73a3d39f2ec8da9923e1d9311fbb286f57f0354ee67812655e9cc in / 
# Thu, 30 Jun 2022 22:19:30 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 22:19:52 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ed69c9a13dd98aac57da3e991b6dba1e11b4436b0fb28daca9344392622a25bc.tar.gz"     && echo "a952c3af116216571c43cf213c443310c15a0687256336904b5d98f9d7fe393d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:67cf6ceed7a460575d469086894c81433cddb3fe8a258514d0619c8d7a1f1ec6`  
		Last Modified: Sat, 25 Jun 2022 04:14:50 GMT  
		Size: 68.8 MB (68790038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92b5f39cc6d3846d4fd81cba740c98bef113e094ecb3de3798b0f03411997e2`  
		Last Modified: Thu, 30 Jun 2022 22:21:01 GMT  
		Size: 415.2 MB (415173785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:39e4598fdabf667f3bfc9a7b0582e2d3146defe878d9b19d1ba4fa9036644e7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.6 MB (482645042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efad68787d41d9985e9f2bbb76c4f6a542f53aa5905a4bbc025559c18f6e774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Jun 2022 22:47:54 GMT
ADD file:926e57673a5a19362689efbfce0973de6fbc4ad7bc237d8962bc7cc64a631402 in / 
# Thu, 30 Jun 2022 22:47:56 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 22:48:16 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ed69c9a13dd98aac57da3e991b6dba1e11b4436b0fb28daca9344392622a25bc.tar.gz"     && echo "a952c3af116216571c43cf213c443310c15a0687256336904b5d98f9d7fe393d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:1f01c3b9181adee87be273b076d739f40845af3c16a7f2187d34f0628ef1d1fe`  
		Last Modified: Wed, 29 Jun 2022 19:57:56 GMT  
		Size: 67.5 MB (67471292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e701220f7372405534d76372c2859f143bbdca7e6022077bb65c516d6bbbea0`  
		Last Modified: Thu, 30 Jun 2022 22:49:42 GMT  
		Size: 415.2 MB (415173750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
