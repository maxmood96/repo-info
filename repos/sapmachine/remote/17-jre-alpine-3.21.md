## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:502270968198a16b5149900570ee42452df5c2f1ac7a49815346b0b18c83612c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:d1c19f3085df9df0739c3ae8e0809ba9de9d5ca19deb93b30e8d66bf041c03c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58609025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61519413c7fc034f8839938ebf0fda9294c41907df30978dd65ef38c278f4011`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:06:05 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.19-r0 # buildkit
# Tue, 21 Apr 2026 23:06:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Tue, 21 Apr 2026 23:06:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c48f1efdc1fd4fef2109db0e2fbb2f94bdcc67db43fc75722bba661fda2afa`  
		Last Modified: Tue, 21 Apr 2026 23:06:17 GMT  
		Size: 55.0 MB (54962150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c3dddf6c0cd66942f2ff142d5233da5f018b310802ae86d0127befc5be6ec0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.9 KB (433855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df522d167ce2237d37a865aa4fe9275f5742720ca00add8b1c1838fd5421a34f`

```dockerfile
```

-	Layers:
	-	`sha256:6565a2b89491512ae29d3e32a21d70d1d003ad755f714672e401895edb519845`  
		Last Modified: Tue, 21 Apr 2026 23:06:15 GMT  
		Size: 426.9 KB (426895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c2ed99515aecfdbd4f90c5323010eb8981d90e9c080d071811f293cf822fa1`  
		Last Modified: Tue, 21 Apr 2026 23:06:15 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
