## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:5ac935a5c036738010379d35b4de557da6b237b48be3662f56ed4dd0c56c5d9e
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
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
