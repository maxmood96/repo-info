## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:4c783009560a5f08a4d623c73eaeda37fe1ee471eadedd3367134b2312a1c253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0d9f1e0225df93bd2bba70f617f89179a127521cad15e17a6dbcde76dbfdc843
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.6 MB (476630585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf287040157831d59644400a2ebe9282a4a2958806dd9aaec89f45a4b60676`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2020 00:19:43 GMT
ADD file:21f17d9ead4aa13446f2144c5042f6f83bc7dc26163bdc2ea6de306b67154747 in / 
# Fri, 10 Jan 2020 00:19:44 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2020 00:20:07 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:67e0556e0c29917bdaa234432962153167e628b99444a27333976b499590d8c9`  
		Last Modified: Fri, 10 Jan 2020 00:20:43 GMT  
		Size: 61.6 MB (61552853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46f1f3757b9b441219f29d7c37d98f714a2d5d0043cc2a6b4151e4041bfb47c`  
		Last Modified: Fri, 10 Jan 2020 00:21:18 GMT  
		Size: 415.1 MB (415077732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:333ab3c09fcd688afb8ff5c72ae49a75124e92f75a06905dba9f762aeaaf8de9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.9 MB (477874498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0c7fbcfbe94cabe2f0115ee5fc3f669abb53d528cf8dd34fe81e7a893f8f3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2020 23:45:53 GMT
ADD file:add3cf2f51e227816df93be763f4c623b743cf37786e5c11118149dbfaa4ad67 in / 
# Thu, 09 Jan 2020 23:45:57 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2020 23:46:21 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ecb5177bc6769961844d6bbc8632ca9f4326737db8dba1aae6875d6021507dfa.tar.gz"  && echo "5bc97d65c81fdc544a92c8b1bd8ccc56b730c4354e0fc9b4529e147056eef82d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9606ab06f949f5879fcb558b6c4a487afd285954e409f8741df95b27c6e0c5b2`  
		Last Modified: Thu, 09 Jan 2020 23:46:50 GMT  
		Size: 62.8 MB (62796733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34e86703318f8a60930cd62ad26d01ef97a89085a74d36f8924c8584468424`  
		Last Modified: Thu, 09 Jan 2020 23:48:04 GMT  
		Size: 415.1 MB (415077765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
