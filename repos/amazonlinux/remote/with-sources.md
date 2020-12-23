## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:e2d056f674fb1076c1a12dcb48e44fd89149054c39eb322130918721745ce458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6380e690beefb9299002207588d8355ced97807753d21577df24ebb493dcf247
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542819174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2b0c7efa71a10e9a135b04bc5f5f7c1fd4d52486d4fee73ec42db1b7b7db72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 07:05:02 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c9c4dcbe7d80a1586ec7d143bf92d28c1644fbc92b3be20b0d99e271b4c44b`  
		Last Modified: Fri, 18 Dec 2020 07:06:38 GMT  
		Size: 480.8 MB (480810655 bytes)  
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
