## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:0b38cda763e96edb3fd591315a17560b9f82c76f7183028751f089e204621178
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine` - linux; amd64

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
		Last Modified: Tue, 07 Jan 2025 03:30:02 GMT  
		Size: 141.9 MB (141908803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

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

### `amazoncorretto:11-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2ed040e50c37ed1509d661e6e9bcc9d178c54fda97546001769292623e4acb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144117390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597ed559fed6c3dc32691512be2fc57fc839294c150d631982f2bebb4add8efb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd1e94f93e82ff452f6f5fd5f1b62cccec7538ed7612a8b68ba53b2677913d`  
		Last Modified: Tue, 07 Jan 2025 07:22:34 GMT  
		Size: 140.0 MB (140030704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ac15118ac251a52c1bcff7f43fdc42e98cdee62a93a7db53892b428330c11739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 KB (395752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c0a5eec24c903d9a6dd0c4475d4703932b405797e4b248c3f51404243b1ceb`

```dockerfile
```

-	Layers:
	-	`sha256:9a9ef33ac7ae6a3c42d8590cbf0f8918a1286ecbd5c39a9e7041c0145764d5a4`  
		Size: 384.9 KB (384875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2d95acbd54e4171c33ce4b3c0c2a248a60eda6c2bedb8e9e8833e421e9c4b0`  
		Last Modified: Tue, 07 Jan 2025 07:22:30 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
