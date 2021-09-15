## `centos:centos6`

```console
$ docker pull centos@sha256:f1121f50a287e3743101d8498bdb09046f91b5d3a3fd5297e40e4b88ad834c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; 386

### `centos:centos6` - linux; amd64

```console
$ docker pull centos@sha256:9aae95c8043f4e401178d68006756dc68982ae6d0693b71a714754227ce0abc6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69835815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0957ffdf8a2ea8c8925903862b65a1b6850dbb019f88d45e927d3d5a3fa0c31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Oct 2018 18:20:03 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 14 Mar 2019 21:20:10 GMT
ADD file:0065316a41144e95bcb133567cc86816b8368a823cc067d741e06ded59849fd8 in / 
# Thu, 14 Mar 2019 21:20:11 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20181006
# Thu, 14 Mar 2019 21:20:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff50d722b38227ec8f2bbf0cdbce428b66745077c173d8117d91376128fa532e`  
		Last Modified: Wed, 30 Jan 2019 15:06:57 GMT  
		Size: 69.8 MB (69835815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `centos:centos6` - linux; 386

```console
$ docker pull centos@sha256:498c1320b2574fc5bbf897768ffd2c510edf0af3bc4c561aa1836f64845c1c27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70074539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259a2295d192482447eb64d2bb5d1f6b02268de8dd8d9aa0403ae9a34b0d74a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:00 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Wed, 15 Sep 2021 17:39:09 GMT
ADD file:a37e74347ae6032b793c87e5c46a27c0d8c24ca0ee4700f3eb1851c834b3ce19 in / 
# Wed, 15 Sep 2021 17:39:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20181006
# Wed, 15 Sep 2021 17:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c3945419b531b5672104afd31d137de0c2226d41118e983353be7d4fadb3a34`  
		Last Modified: Fri, 15 Mar 2019 10:39:49 GMT  
		Size: 70.1 MB (70074539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
