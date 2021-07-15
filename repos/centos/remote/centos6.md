## `centos:centos6`

```console
$ docker pull centos@sha256:dec8f471302de43f4cfcf82f56d99a5227b5ea1aa6d02fa56344986e1f4610e7
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
$ docker pull centos@sha256:7a92c5cdc090fa6917908e9dbfc080d94d2b91f86e68ac429ef6150848383a82
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70074539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fecca805e3d3918c7d296b0dcd269083169a77baea63ec1581a1b16881a0011`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Oct 2018 10:38:55 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Fri, 15 Mar 2019 10:39:01 GMT
ADD file:a37e74347ae6032b793c87e5c46a27c0d8c24ca0ee4700f3eb1851c834b3ce19 in / 
# Fri, 15 Mar 2019 10:39:02 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20181006
# Fri, 15 Mar 2019 10:39:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c3945419b531b5672104afd31d137de0c2226d41118e983353be7d4fadb3a34`  
		Last Modified: Fri, 15 Mar 2019 10:39:49 GMT  
		Size: 70.1 MB (70074539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
