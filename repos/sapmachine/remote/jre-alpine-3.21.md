## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:9f157d530146c33e0dcf2e2d5c274c604ab4c9fc43d5f075aa3aa1d8023b23a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:257f11e71ed558702af59285d454307bae965a67e802edcf8629947609128070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71606208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6756913e01bb4625c5b67b0e63095a533e25b8046daf3cc3acdccee9dc2aff3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jre=24.0.2-r0 # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jre
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a2c66feb82ecd8b241b3d114e17e67ffb63d29bc2101f0c698a61eeebb4fa2`  
		Last Modified: Tue, 15 Jul 2025 20:45:59 GMT  
		Size: 68.0 MB (67968638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:283810e27666aedeb3bcd3ffcfa086e2b5783cf7d020b50614b3f4f83864db7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 KB (438513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c259ff743003670c9e5c0ab5a5d98e6fbebb6924ebbada4135299616217324`

```dockerfile
```

-	Layers:
	-	`sha256:3dd66b48c45cf569a10f86bc7ce9037fa50d559b651b3d0020053451c2f60f99`  
		Last Modified: Wed, 16 Jul 2025 00:10:11 GMT  
		Size: 431.2 KB (431185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00a53480858ddae6f45cd43408d4d2295934f81ab649411931b890872bb90248`  
		Last Modified: Wed, 16 Jul 2025 00:10:12 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json
