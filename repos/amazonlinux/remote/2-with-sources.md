## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:c82586d9cb52d1d76cf3fbb2ea919f57c4b2629d6ea200be46d808d6bd7d4cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:dce35a75aef0b93ffd23eb89ef29cbcfa8a5619afccb1aa46f14ad45608023bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543005154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b21ebc73b4f0ad426d2078d98bd125c2ca49c25d9b59e7ceb804893910eff6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:20:29 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42305a36d448792755e5af8dfbd0d1038b87bb46a0541aa94586427d6f7deb2`  
		Last Modified: Thu, 09 Sep 2021 00:21:34 GMT  
		Size: 481.0 MB (481004851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:8fc64668ec668d7b6feeda33c34f5856a7cea21f35c5e886cf23d3bfc83b8451
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544435646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f59ebcd6e79e41e62d3e8568784dfb20b42bf78cf10ea0c4ed494a7bbe1d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:39:33 GMT
ADD file:b9ba46926c70623a28a962a14eb6ff980ce1b8dbe27b764cd8fb8f90d9de260d in / 
# Thu, 09 Sep 2021 00:39:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:40:26 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-cbcef4d5e6ddf099c19df5fc2c6a347b3129084e4a887b4b3808cfbc109e7643.tar.gz"  && echo "45b6d3758896d184d4a02d1659109fb8ea2dadbe5dda04467c0ca76aabc6404d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:95c181d62dcf67412b438cf48275f91fffb0c788e3b13f41cef8dcc62842cf86`  
		Last Modified: Thu, 09 Sep 2021 00:41:06 GMT  
		Size: 63.4 MB (63430802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0eb3aed5c223e4cbf8c3710d58ea2ba788703f9f1a37ea6a2fe77ae50bdff`  
		Last Modified: Thu, 09 Sep 2021 00:41:45 GMT  
		Size: 481.0 MB (481004844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
