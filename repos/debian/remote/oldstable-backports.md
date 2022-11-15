## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d7c5a2406c19f622b7faafd09feae34e01c1721bd6e97e694ea9bc20838a1c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:057e9eff1c92feadba85e7d88bec7a60417901ba7ec44584f290fce1d43f0217
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76816c13da3cce6caa08d2fa7ff424c4f5c8fdadea5dcd3b5f27038d22cbc385`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:23 GMT
ADD file:e92fd2d35ba2034fae69a1dde36a900d2f3ff610d7142b6c98e8c4ba59736154 in / 
# Tue, 15 Nov 2022 04:05:23 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:05:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0142f67c7bc40943fd7ae8671cec8033ce1cb876952964e4a4fa80524e77b6a1`  
		Last Modified: Tue, 15 Nov 2022 04:09:44 GMT  
		Size: 50.4 MB (50448833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c88dca9b7a841ff10476c0e2449a74cd75c8cfc75047a3360b29d329404ce`  
		Last Modified: Tue, 15 Nov 2022 04:09:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f9bc25fa59b0b4289d31af1e8f9c3f25f539198ede7aea75b89cbdfdfb6529b8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349be398c494be0b06b930c449915d4a8ef8c25018b51f205ebd327d2cde3fb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:44:11 GMT
ADD file:58250dd35fcb126e447a12812f45680e2e95fac075e850dc17ac2821fe2f1c43 in / 
# Tue, 15 Nov 2022 03:44:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:44:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e11b927848aab53099ca5c99f29ed145bcd14b943d018f4282a9d0b44014b394`  
		Last Modified: Tue, 15 Nov 2022 03:51:26 GMT  
		Size: 45.9 MB (45915531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98529a7d2344cac73e6f3443d10489a121f1a197d75932f733a80a19aa86818b`  
		Last Modified: Tue, 15 Nov 2022 03:51:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a351d47332030d49527e8170983affe37c35d425e8af861c80323968cabe9bb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeca687c40bbbfee9d7b13a258b895ac1bace795451bf8b5164f69bc94a638c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:40 GMT
ADD file:d3e305927856691817f0b321e3ca76a6ddbdd557f62aa4e25e2501b5c4aae4d2 in / 
# Tue, 15 Nov 2022 01:41:41 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9aca4dab0ca9af54fb0bc3c53006adc1874be641f15371a314b9643b230a590e`  
		Last Modified: Tue, 15 Nov 2022 01:45:30 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106419bd0732254a61c54c6eff9ef3004e8f1f13dbfdc2cf6f7b411254998bd`  
		Last Modified: Tue, 15 Nov 2022 01:45:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:09be35b01c99441cfbd29dfcbafb8a8926b6a1512318dad5d45da9606cf61aa4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac201fd4e11ef094042d56e75957ed5e7a0758865ed41a1f8459b99bed26cc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:05 GMT
ADD file:a38f163ea2aa00d0da6d41e110886005a371094cb39fda5e247f506153001319 in / 
# Tue, 15 Nov 2022 01:42:06 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f617ec91bcf39f4f673f082643fb6396395615449fd76a6a24183c93350e610f`  
		Last Modified: Tue, 15 Nov 2022 01:48:13 GMT  
		Size: 51.2 MB (51207659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614e41d38cbde638aed57b5183515cf7283c2ee42066945d996186323fcab649`  
		Last Modified: Tue, 15 Nov 2022 01:48:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
