## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:070c7dd62d3363f12e478dd992f89992e68729d14a44fe727b1e2bd7d80fe127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:644de89cc735d3f4dbad2a9c13a7d26c7bc3f86ef322a8b1324de8cdace0d681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72059805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5435f83e92cc569265a2bc3b67ae18eb347d2aa3cf4989855873e0d52e9b0e3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Nov 2024 20:59:22 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 25 Nov 2024 20:59:22 GMT
ADD base.tar.xz / # buildkit
# Mon, 25 Nov 2024 20:59:22 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Mon, 25 Nov 2024 20:59:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7776d2549b54495308b2c33f4e28306ee1613d3797c285fd7bcf8a1b322e860`  
		Last Modified: Mon, 02 Dec 2024 20:23:43 GMT  
		Size: 72.1 MB (72059592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b395162f20f3b33924cef22bf0849a21dc8336f85c9c5912e94a5e863364663`  
		Last Modified: Mon, 02 Dec 2024 20:23:41 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:0985d50eab3c635ede1850812268dae26077485255bb044e4f1352f9c420faf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb58df6fed0f7aa52c335388ec96796975b7173de1695fd19e8fd09f26b7c9d`

```dockerfile
```

-	Layers:
	-	`sha256:51980706e0e3a4ef08486104c5d73e825608776e624c927091fbffc1fdd3a045`  
		Last Modified: Mon, 02 Dec 2024 20:23:41 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.in-toto+json
