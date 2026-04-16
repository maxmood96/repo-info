## `sapmachine:25-alpine-3.23`

```console
$ docker pull sapmachine@sha256:45a18a00c5c21ab8a2a9197785ad5cd5d8afe02a9a7f05ec2576feb75782ec27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:7175c96fa6dd9e728544333240fbe443a864664a973d3709b7d8707e1bcc6441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (227019142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535760ac644e0ce315ecd5e9c25ef24b6c4d95c2e0f6961dd72d824e81bbef27`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:58:16 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Wed, 15 Apr 2026 20:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 15 Apr 2026 20:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3b5a795354e140138b1af09c7a13db6d5b41d35d6e1910503b2b91e2fb171`  
		Last Modified: Wed, 15 Apr 2026 20:58:38 GMT  
		Size: 223.2 MB (223154953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:77ee363c643ee8c59b5746408397fcd986c1b4fa56dfebad0b0b20813eb02ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.0 KB (514032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0335f00affcaf58e4f5df85f0f8030e7c236f96ea9c0620cd9fe7db92b30cc89`

```dockerfile
```

-	Layers:
	-	`sha256:79b3ab47b23dbfe1776739a7a21d239ccc0721e032551860c707b0438d0e2c39`  
		Last Modified: Wed, 15 Apr 2026 20:58:33 GMT  
		Size: 503.8 KB (503846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6e691e26dd742614146e5d12b57f3aa3394829fa76ef8d799ffe869821d4b5`  
		Last Modified: Wed, 15 Apr 2026 20:58:33 GMT  
		Size: 10.2 KB (10186 bytes)  
		MIME: application/vnd.in-toto+json
