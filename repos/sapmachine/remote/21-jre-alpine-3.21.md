## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:2ef98ed76102778ca5e3ca85a1d37e0f01a3e5f7dd9f31123d2e46d029abb643
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:d32aaaf1fb98f84c57b1a31f9615ab60f5bbea9d9524a85ed952e2e52414b0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63771211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc983509e0766f46d6e1769c733f28555b4019ebcd809873484e3bc72a22915d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.8-r0 # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98642ca852c3012611726fbb52f82e6cd372961f49e615f927a59961baa1a3a4`  
		Last Modified: Tue, 15 Jul 2025 20:46:03 GMT  
		Size: 60.1 MB (60133641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:93fc51e8a0309126e54f7b3a59ff92a96dca62ff7d4f84a0ab1fe3530909ed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 KB (431378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1c5603125a411e420d084dd342eae641fb368385abbc27b9ad816ec22e24e4`

```dockerfile
```

-	Layers:
	-	`sha256:48fb7a754ccb4ef5dfd865e059b9c3ef8a739aee127eba6ca9cae97972864985`  
		Last Modified: Wed, 16 Jul 2025 00:08:16 GMT  
		Size: 424.0 KB (424042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dded686d676d4f892ed4a1d68c31e3a29d03bb824de275a487d428f6a1e2db6`  
		Last Modified: Wed, 16 Jul 2025 00:08:16 GMT  
		Size: 7.3 KB (7336 bytes)  
		MIME: application/vnd.in-toto+json
