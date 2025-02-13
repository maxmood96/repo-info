## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:c279def074909ec69f5dc76cf1b0ed0370a8a9dd87eb804f8ab6e6b0443aa2fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:68959dc6dfd96486566542b311124b35dba2586325d87e2c9ad892c9150bbff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162581022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec7b90730e0a741a4d7115ed6f0cf6a06c325a47d4e7f5381c6ff091467374a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf2a3ce78fa42de3fb3fd986d252aaed08f5484cecce6c954a589129534b608`  
		Last Modified: Mon, 03 Feb 2025 22:14:58 GMT  
		Size: 159.0 MB (158954762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e386597df21719a0370bc46bf51d82273a38abff9bfc486bb2c9d3b84b580512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11259e1720c3fad02d4514a215566ab8e9a1416f7455253ad704140394f18cb6`

```dockerfile
```

-	Layers:
	-	`sha256:bdfc2792275089d80badcd27add5d7523389bf889aa38a9ad6715a522531f616`  
		Last Modified: Thu, 23 Jan 2025 18:27:26 GMT  
		Size: 377.9 KB (377866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08d070f67c194bd5a544c5a320d36298ddc0b7ddd44668b82ce8a151d61069c1`  
		Last Modified: Thu, 23 Jan 2025 18:27:26 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4eb5c763bda5f89156855eddd58c9d2c006dfc07d4461ae09604a0480eb0fc`  
		Last Modified: Mon, 03 Feb 2025 21:56:50 GMT  
		Size: 156.9 MB (156934962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

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
		Last Modified: Mon, 10 Feb 2025 07:44:59 GMT  
		Size: 377.3 KB (377333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1abcb6dfa0426771739221d9b80222c8604ee7fa732911f33096f29dc6354d2`  
		Last Modified: Mon, 10 Feb 2025 07:44:59 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
