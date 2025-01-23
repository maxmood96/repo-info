## `amazoncorretto:21-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:50280e848740bd8448e5cbd2c37bdf35abd13950a9746605bac70f17ac3c0530
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11b647d48718c98acde3c74c62f7474e4a0da13a72d7d350e4cc60b4898ce76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162556337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704d28523de9b3f8b1f4925c4297dc8f55787e9a4b9d3c82e5ff35ca3c8067d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae79ac77531690e0b6594d0ae10373ac91d4a1854ef04723718a0087231f14`  
		Last Modified: Wed, 08 Jan 2025 18:13:47 GMT  
		Size: 158.9 MB (158930077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:544a69709a3f8ef04ec1b39123834c2eb05799209a429ce6379107b1bc952a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5c92fe3e855c18425203a31a309ed0d62c5b91ef50ce76cca6fece9d5a1353`

```dockerfile
```

-	Layers:
	-	`sha256:ae4e08f5e9b65f6c71fff62e63dccadccd98dd45d1fa321561789df6ab25d538`  
		Last Modified: Wed, 08 Jan 2025 18:13:43 GMT  
		Size: 377.9 KB (377868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b527e7ecaa8ce356511ff964fa0f06fcfaa04159549aac6802bf158c5e8a31`  
		Last Modified: Wed, 08 Jan 2025 18:13:43 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ede67a8c9f62477d91425c823880d7597354eb163c133aa7982cb7e609e6fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161025731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b5310b9d1092ab39d21175435a28b7713d952a88ae0b1c75dfc5dc6cbabada`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4eb5c763bda5f89156855eddd58c9d2c006dfc07d4461ae09604a0480eb0fc`  
		Last Modified: Thu, 23 Jan 2025 19:07:37 GMT  
		Size: 156.9 MB (156934962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:327607e95295132bd1ca3169763c1b6abdc7adc4678b2202208abf912f720100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 KB (388205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6503bcee4ae5e901468a9af44d7cf6549832f5c4eda212a9cdde4696ad2683a1`

```dockerfile
```

-	Layers:
	-	`sha256:c0ab2d64364cf1d920fad8872b074a7f12a346ecf92483eeb3543be86c4b680d`  
		Last Modified: Thu, 23 Jan 2025 19:07:33 GMT  
		Size: 377.3 KB (377333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1abcb6dfa0426771739221d9b80222c8604ee7fa732911f33096f29dc6354d2`  
		Last Modified: Thu, 23 Jan 2025 19:07:33 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
