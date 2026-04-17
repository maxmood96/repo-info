## `sapmachine:jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:e045023c77ffb3d3c38dd69c4935fb051c47a8dd025f26ca9c4221c276336b28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f8efb07d7dd0aa0e60843a422d5f1a45f457b36ca3d8d1165c06376db1720a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231282373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81884229b98376102c6d26d8de434ea8a81fe8c56ac43ca1596a0d24fe8d136d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:01 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Fri, 17 Apr 2026 00:34:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Fri, 17 Apr 2026 00:34:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da8baa77482dfd840b04d0964c843ec8987df2204a33a267c073f2831bcbd37`  
		Last Modified: Fri, 17 Apr 2026 00:34:23 GMT  
		Size: 227.6 MB (227635498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:51549ed02b6d4468593c3cd0f6d502bfb41c5cb68d76b30964542c25eb2ca249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.5 KB (509483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5da84f1199c826b3d58da6b8bbde630ffb3e11ead86df8ca3a42e3543b2e683`

```dockerfile
```

-	Layers:
	-	`sha256:db59d3dd2da61dd782e72e96f946f6cae2a4dc461b5c4c976511060c07a4031f`  
		Last Modified: Fri, 17 Apr 2026 00:34:19 GMT  
		Size: 501.9 KB (501905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4c062ac908fb3fd7da1a36e76a5e6cb7ca39e8e7a70e42159c72d866d8357d`  
		Last Modified: Fri, 17 Apr 2026 00:34:18 GMT  
		Size: 7.6 KB (7578 bytes)  
		MIME: application/vnd.in-toto+json
