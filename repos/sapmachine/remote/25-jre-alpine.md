## `sapmachine:25-jre-alpine`

```console
$ docker pull sapmachine@sha256:8f003a525ed1bed23238b01100c8266718ad09cdb545b2b1763feee3d1a36792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:33d71781c62e11cccf5ee77ce59d532c87d590bdc7ce658b7cd19f956e8acca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62255346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bec4512b8c65de8d7b90479ea9ac7f7e41acda27d2fb88f2dd16e721b10de4`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:58:34 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Wed, 15 Apr 2026 20:58:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 15 Apr 2026 20:58:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a5c364dbb8d06363475e5c6540aa8731e857109d26e253c2778646fdac497`  
		Last Modified: Wed, 15 Apr 2026 20:58:45 GMT  
		Size: 58.4 MB (58391157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37e3b14a39cfa729520e3d5dc456d3637f5d76d115500900a01e91413ad9446d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 KB (441393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3d84e5fa7a38d9c14930ae2da644ba57e1488e76197b350d2a123fd6fc442e`

```dockerfile
```

-	Layers:
	-	`sha256:644f03afc874ea411dc8d58cd1741696daa1049fb9490bce218571e917fef978`  
		Last Modified: Wed, 15 Apr 2026 20:58:43 GMT  
		Size: 433.1 KB (433134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6587bef1fd0592c9e88b6a6ad67772a98de20edc93c4d626a59e268122ded504`  
		Last Modified: Wed, 15 Apr 2026 20:58:43 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.in-toto+json
