## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:5f1a85a235b5ef5d5ed3db8925d387c3f2e86701eedf32320c27564eb7c92e74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:277af38969d21bedb7feb99f9710c5a2183f024dc5b1ac8f7f9f8d4cca9be913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145522802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d91c0128dc3a6ecae3128a558e334a86b4bbccfda29e5ddc19a20d45deb8e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3d61b036c68cde5a4b4c7e2dc2137e79239753379b059c10333a96688321d2`  
		Size: 141.9 MB (141908803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:615c0f50f4c22a4e68478c749c539b7a6293277b15dd10ec3d9025ce908281db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.5 KB (395496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa1f19726eb8d4b2b74de30a759fb5776745cdd839af3c9a18a7859bcf70253`

```dockerfile
```

-	Layers:
	-	`sha256:16710e5030c038be5ede291b706cb80289e52471663cbca0a5443792e810a227`  
		Last Modified: Tue, 07 Jan 2025 03:29:58 GMT  
		Size: 384.8 KB (384771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75849f457da846a165ee33523256c77d3ba9a29e438601d17ae065a8b787f7c`  
		Last Modified: Tue, 07 Jan 2025 03:29:58 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0cb9f15f31c81301a8a601c898a465d75df5f4d27e8eac12accafd6b02519ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144118439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af176dd956b30b6e62ac0252be4d76c6d41f5e9c5e3a22c14e06fc86beaffcf7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feef5f54761e4ac1e35370a37a80317ad13c13520a484a79788aab6fb52a56f5`  
		Size: 140.0 MB (140030713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:132398796a08101675598aed6fab7d5e9718b15be9297dcff63a34cf2087ab50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 KB (396384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f5e941b36d89e77d81645cc383b960c888e1992f9bf3b9dda171fcd0491cb8`

```dockerfile
```

-	Layers:
	-	`sha256:91c733bb0e8a7d9c6caa3c595c168dd17c9d6ae28c72ef26dec663fb20f28ad0`  
		Last Modified: Tue, 12 Nov 2024 11:08:09 GMT  
		Size: 385.5 KB (385507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43762d29cdc1935bd4056994bc85765b6435703986dcf220e12acdee0549d06b`  
		Last Modified: Tue, 12 Nov 2024 11:08:09 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
