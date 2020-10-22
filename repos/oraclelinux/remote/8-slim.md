## `oraclelinux:8-slim`

```console
$ docker pull oraclelinux@sha256:e1de1fce92f313c5fd39996c649f6ee176dd1c297b6708e09cc2f1d74096f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `oraclelinux:8-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:ea14ba76730c1a0233bcd13e2fb8145adc792756550bbed370ecb91ad110346f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54161024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65ab5165000ad5dd014c14d4bebd3329b0c61a1fdd3347e630025e5fae71248`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 22 Oct 2020 02:16:12 GMT
ADD file:dab686af43f04bdaabbdbe7703e0c2dc85868a5dbb38942747055a44e038f37f in / 
# Thu, 22 Oct 2020 02:16:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd3d5e431db632e40b1f1d5ed9a34a906447d43146906e56da1f14f07998bc28`  
		Last Modified: Thu, 22 Oct 2020 02:18:09 GMT  
		Size: 54.2 MB (54161024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `oraclelinux:8-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:0703e8b3b5cc0ba1c9573f2c9a83e55af553e4a99f964c94a8a0dd4243c97a78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54285957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f068c78e9933158db296551172fb7e8c495f6e39053ca52794702c25f74452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 22 Oct 2020 02:02:57 GMT
ADD file:91f94052d144e7fac61501c6d72e663eda67c40303d29f0b62fda4abe0e5a284 in / 
# Thu, 22 Oct 2020 02:03:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:428aa11a26cf7698a25c3ec8f290dd1667191a70a5797b7232fa597f1e52ec1b`  
		Last Modified: Thu, 22 Oct 2020 02:04:59 GMT  
		Size: 54.3 MB (54285957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
