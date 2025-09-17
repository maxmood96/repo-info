## `sapmachine:lts-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:71496c6f43d3a6a38ad3aa00e85232c7b2a77b8d911b18afd5484a4d7eab5a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:79a7a68c25cdd2e744ff32011b8a033bc0454dba5e5e37f7e8f66accc875975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72936502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaae11a30b5f987a0ea8fe3dfc596809ee64bbe5a2290edf8f17faf1eeafe23`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b612089db17aa1a38ace746ac9fffc41581249ee231a9581c4aa7cb47f67520`  
		Last Modified: Wed, 17 Sep 2025 17:37:12 GMT  
		Size: 69.1 MB (69136813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:932a2d436c40bda1f8dcb9ab91512c425562ba9a4b73614f32aa3a70c227438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.8 KB (438840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704120d2b23d912915cc16a272bef979a1240064a3ab04da6a8cadc66eef011e`

```dockerfile
```

-	Layers:
	-	`sha256:cdf86d1f9732477c2efe2e81d4995842c944e9b27ed6101f0635103d7a23c3cf`  
		Last Modified: Wed, 17 Sep 2025 21:11:30 GMT  
		Size: 430.6 KB (430574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcab2b23db9f4fda82e3aac098388890a77279acc9d690bb0e243fd80ae26958`  
		Last Modified: Wed, 17 Sep 2025 21:11:31 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.in-toto+json
