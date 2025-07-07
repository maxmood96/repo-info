## `sapmachine:17-alpine`

```console
$ docker pull sapmachine@sha256:6000c5d00b36db0eaa32a1757dc49b0446d60454d81df7cf824596cb02d15734
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:70f50dfb9742c9920fe9eb650e222447b17d17791834e6d0f27f281b33f98ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204577558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfec14db8e6cfd269146e2d13dae911c250939360a6fd38dbe081e77ce6c56c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 04 Jul 2025 15:51:10 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.15-r0 # buildkit
# Fri, 04 Jul 2025 15:51:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Fri, 04 Jul 2025 15:51:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f0105174b731c21e6f89a8f4c6e01499e6a6fc6f1c2a4ba46bbc16f231bb0`  
		Last Modified: Mon, 07 Jul 2025 20:45:39 GMT  
		Size: 200.8 MB (200780712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:238cb38e2845189580a482b9e26ce5e3cb87164828bc275d8f7ac25f9e4eac30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.7 KB (520701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a37c8e6f15adea3c94f7638225945e14123dd3fd2a367608a6d0b840bc3a1`

```dockerfile
```

-	Layers:
	-	`sha256:b4e9558df1662ada87fdd8928695332c0606cc2671230d662d764d13c5c8f5a0`  
		Last Modified: Mon, 07 Jul 2025 21:04:45 GMT  
		Size: 511.8 KB (511751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56a276613d40c4dcdfd3e94777146b9e9dd66e3d31a0a7ec2e43d81ff289751d`  
		Last Modified: Mon, 07 Jul 2025 21:04:46 GMT  
		Size: 8.9 KB (8950 bytes)  
		MIME: application/vnd.in-toto+json
