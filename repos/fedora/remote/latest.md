## `fedora:latest`

```console
$ docker pull fedora@sha256:21d852dd242e8afe748c6f021a990c60e2444de583647eb52f5dc2d52e37126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:8fa60b88e2a7eac8460b9c0104b877f1aa0cea7fbc03c701b7e545dacccfb433
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66774261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0858ad3febdf45bb2e5501cb459affffacef081f79eaa436085c3b6d9bd46ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Jan 2019 21:21:55 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:21:07 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Tue, 29 Oct 2019 03:23:37 GMT
ADD file:298f828afc880ccde9205fc4418435d5e696ad165e283f0530d0b1a74326d6dc in / 
# Tue, 29 Oct 2019 03:23:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d318c91bf2a81634e0283fb7e7362efdd7c21164b60b74498360756dc82a95d9`  
		Last Modified: Tue, 29 Oct 2019 03:24:22 GMT  
		Size: 66.8 MB (66774261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:b0d24e01fbfae9b54d27ea1c56aad451d7eafd58aa0174d578dece0ec91009cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66535521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a50f9110d4e2bee94a42cfa3c8ce88ce7dd73631cf2f590dec1063aabe97c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:41:10 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Fri, 21 Feb 2020 01:00:36 GMT
ADD file:802fd23d2e88228881203b44c1e64bb1fda52436fee03fc94f0ed37f77d3bccb in / 
# Fri, 21 Feb 2020 01:00:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbad5a3d9e059ad673cb03431604f7d02d3d16a4f6bad97eab35b8db19259d0b`  
		Last Modified: Fri, 21 Feb 2020 01:03:05 GMT  
		Size: 66.5 MB (66535521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:bc2dd5a257d49cfac256072103ea72acd4bbdf83932177a08225452c58d01c5b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72597480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138251280ac297133ca4b08ab007259e5b42efb3163601c38a71612533bf0dee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 22:08:22 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Thu, 31 Oct 2019 17:09:07 GMT
ADD file:d33bb2a427734a63cebb88a46dd671f11b6aadd75cdc8d78f543aaeb3a74632f in / 
# Thu, 31 Oct 2019 17:09:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9efe76f4bce654be32bdd70fa2c193d5a094a18c2e99a1837ecfc6efc2f217eb`  
		Last Modified: Thu, 31 Oct 2019 17:10:33 GMT  
		Size: 72.6 MB (72597480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:df186480927cc4fdf9d8350b255fedb98e48cbd2a3a6dca794523f62f2097e3c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63903433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044f7646c1c935b31f40c8c3f31c5f124be36ca95e6ebaed63e5233a1caab206`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:42:39 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Thu, 20 Feb 2020 22:43:17 GMT
ADD file:c567f902e775272a4a040d6f191cda1bdb8e3589b295e8bd90535099ddfe82bf in / 
# Thu, 20 Feb 2020 22:43:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6decbeeaf87b7738a70081478c58cc225d73039e15a07e51f6d43236e23f5649`  
		Last Modified: Thu, 20 Feb 2020 22:45:16 GMT  
		Size: 63.9 MB (63903433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
