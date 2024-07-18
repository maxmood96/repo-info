## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:3101030cf2aeb63b944be01e6de2295ee1490d82727582ca52f82a217f621912
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b7ba99674c1b1ef79265578bb28f26ff43b046387dd3f0db3b910249220028de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145433303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4336a73dce8d73a0d697702f5c7d08610022bb640909d8e84cb4ed2939119e4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754cfd406645f101760bd1f62f5fc83e8d8e00447558e34127e5dd9fe83966a9`  
		Last Modified: Thu, 18 Jul 2024 00:55:47 GMT  
		Size: 141.8 MB (141809459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:29e44d1cfc9d2d5db62eec9f1e753e15fe3fa8adf5b0dadc297ad5327dee8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ceebc8d6a41d6f64ff7b7a0b20e86553d21b5d30a4793a55028de357e465f7`

```dockerfile
```

-	Layers:
	-	`sha256:087f6f3230192627837aaf63714e82ae81f3815b729d7ded233490cd34385028`  
		Last Modified: Thu, 18 Jul 2024 00:55:46 GMT  
		Size: 385.3 KB (385297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00edbe47a4a17aa44c39c50d4c4056b14a7d715c2b1682ac83d78362b7312250`  
		Last Modified: Thu, 18 Jul 2024 00:55:46 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9b8cf9616307a0e55d4e97702c094f844cce870ee66e852b66750a887a9d7e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144048563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8581aa95eb3842aab16f64b7e74cd1bdeb46c508eb5e0123032933114993b6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7f671662efdec07e12943e980d93c7cee9250d19994bcd3624da20d98633ae`  
		Last Modified: Thu, 18 Jul 2024 02:14:35 GMT  
		Size: 140.0 MB (139959763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e74b9065b5631d206dd733047f067e070b5fdfb2ca3379b7bf5a9f4e3fc5f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 KB (396227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895bb56e69cfd9e0efc55137297fdee80eb6108438e781f4ea42df5906aff5a5`

```dockerfile
```

-	Layers:
	-	`sha256:9ff6c00cae50fc3e071b8f5ae0eeaba70d48bacc1b1a9b74ffde7cdff54c3135`  
		Last Modified: Thu, 18 Jul 2024 02:14:31 GMT  
		Size: 385.4 KB (385401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba023f75922b48fdd9fe5d04ab7a81f5675ba70289ac2e9835ee8032355e2c`  
		Last Modified: Thu, 18 Jul 2024 02:14:31 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.in-toto+json
