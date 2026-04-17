## `amazoncorretto:8-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:bd92eb9bc3db9e929fb717afad1825cf4c68eef7e078b62021667ef0e25fc904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e9214ee97fbeb84aa8fc06218f890c5ee5dd59b4a32a9876b609454b4da93ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104405211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9040cd647ef40735b4581adf3b90e6e196314339f247dc212eefbda760e47b1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:02 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:02 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:02 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11ce49f10c3de980c66a9b7e90420f346f7c09a2317c108161578be153081a`  
		Last Modified: Fri, 17 Apr 2026 00:22:16 GMT  
		Size: 100.8 MB (100774890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:09e3b2a398022d36165dc84edbed6b0a24c854cef1059fcabcc6411c149cf685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8bf2d734ffb38e3a85836c583896b39aba65a4c00119d08c0e9587fca1f172`

```dockerfile
```

-	Layers:
	-	`sha256:2a40b288dbf4ea60d0ec32180a0cc350c7fa83e1634ef343e38875db2097395d`  
		Last Modified: Fri, 17 Apr 2026 00:22:13 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5a419c891e6529abc9c87cbbf2a9a15112900960bad2a1ee9186160bb17a34`  
		Last Modified: Fri, 17 Apr 2026 00:22:13 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e95709303e143e049a43a7282a92545e845e8253af3bcab621958895ad9e8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104653321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460020f6cdb6c198e4627c53fe333b0552bac397fd43bcc99065f62838b28bce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:58 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:23:58 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:23:58 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:23:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:23:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e558bd1e2733a049f46faeb44d0ba533800617b74490bbd1a6c9f6c6644c3d`  
		Last Modified: Fri, 17 Apr 2026 00:24:13 GMT  
		Size: 100.6 MB (100561002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db688c933a5e3b3ba884e2aedcf18ec354d56e77d16940f079a29cbc4aac9691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d761216df3c50871dec11b0da4e842b7de94bf4728cc62ed6f088e27ebe299`

```dockerfile
```

-	Layers:
	-	`sha256:76fd13ea9dad69e4d4352cd618464361e82e8b2c7d6d2b6e251b9e9134df971b`  
		Last Modified: Fri, 17 Apr 2026 00:24:09 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86adf21638f56795a2d2dca7457bc0d6d4e21e604479c0e4e31315aa63384d5b`  
		Last Modified: Fri, 17 Apr 2026 00:24:09 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json
