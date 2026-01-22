## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:2846722d69abeec6d7f95707bc8b530926330feb9be1011dfd4585ee539b9f33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:3a6de938878b3285fe681525247801c421d81541f149be03ba0abb3295e7336c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58513979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b4aec2774b3be9634e84b66e38eb2ee2737645f38762cd79366a7e930b1144`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:05:05 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.18-r0 # buildkit
# Wed, 21 Jan 2026 20:05:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 21 Jan 2026 20:05:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e268f10f2d3838ccfa2ebc8ed3e4a2da8a83c647f7c7d6adcc207479b4c9b86`  
		Last Modified: Wed, 21 Jan 2026 20:05:16 GMT  
		Size: 54.9 MB (54871410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c27fc61f40f8c2a4dea8fd0b88036057c46e9414b4c0c383a366354d84c59e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.2 KB (433207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756272064d5a49ab146d510be05514d56bf128dd907766bbbc19481ff4846d45`

```dockerfile
```

-	Layers:
	-	`sha256:e756e352dac804f38498e51778ef4a0a81c1e71a49d0e80fae3a0c23ff63f262`  
		Last Modified: Wed, 21 Jan 2026 20:05:15 GMT  
		Size: 426.2 KB (426248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2ed272593cbe91b5d2a8836d7865e4bff9e3a297d6a085394d2e5d2f122fa7`  
		Last Modified: Wed, 21 Jan 2026 20:05:15 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json
