## `amazoncorretto:11-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:0dedb0a42121e4b90f645e571f74a11ada49b15bdbe5e73910a71821402d3265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:33d48927e2c5853066ebe22b6d6af5ff891966e31a2463ff37ca33bf6de4b05c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145078391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87c6cfc772c138404f7afdf83ca74d0c18a6632791032fb8d60fce970989ccc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:52:26 GMT
ARG version=11.0.22.7.1
# Sat, 16 Mar 2024 02:52:32 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 16 Mar 2024 02:52:33 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:52:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 16 Mar 2024 02:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cbd52999d2f42beabcd40f31484f03adb7130e518e6adae96b3b27ca2c598a`  
		Last Modified: Sat, 16 Mar 2024 03:09:28 GMT  
		Size: 141.7 MB (141675849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef7945ef41e03b40ae6dc95ce34ae3d5a6497cb3f57a7de7a2d5c87e012b43f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143089858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a212bea6ad862454c353b85da254f434ab98c93fc86c9d91c6ee71caf9eccee9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:42:19 GMT
ARG version=11.0.22.7.1
# Sat, 16 Mar 2024 03:42:25 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 16 Mar 2024 03:42:26 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:42:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 16 Mar 2024 03:42:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5081e0247ffe3b315a8b270374b56b609308de77d7c4caebdb86cce82af722db`  
		Last Modified: Sat, 16 Mar 2024 03:56:03 GMT  
		Size: 139.8 MB (139756497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
