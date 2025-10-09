## `amazoncorretto:8-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:00b6a1e3197580bbe0a11fcfb6b5e34dd6ffeaa44f46c1048143dfc304e89341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e54f3e8725a1bbd37de551a7d9ec9abb6c1ac159c9f850a672a11984edd3856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103923583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a06d85b6008340d7daf8433508a2ef2c4af15f7af8314fe1324f9579e92b33d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee7d630342af971b68e73230404414de4a96eb663cb6b3e493b4ee825df942`  
		Last Modified: Wed, 08 Oct 2025 22:59:12 GMT  
		Size: 100.3 MB (100296527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f58643064677057c17fdb8b840ca09d037479860a28931e062cec99a57327de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 KB (252392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7f98153a445518c3938681c84a19c81bf6c9438a41dd82e59386abd8af900`

```dockerfile
```

-	Layers:
	-	`sha256:41d742dc6c90a4e39ea7d70827dd449434b217a3951d0f7629376f09af7f6974`  
		Last Modified: Thu, 09 Oct 2025 00:53:27 GMT  
		Size: 243.0 KB (242995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c406fb72645d579240ab4437cbe98e712d2f9a3aa6f19cb2ba1c835b498b87`  
		Last Modified: Thu, 09 Oct 2025 00:53:28 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:43acb34eb1f8c1894df1812d15f316186a5dbf2b07d32f908f968692d399365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104179047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24690fad30094419999d26d79f3a9f29a8b3223f17fe0e984c2d31ce9fb3420`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e19f4f5dba4f50a0ecafecf26830204b220114b56e79aa8ace8743c6b73e81`  
		Last Modified: Wed, 08 Oct 2025 21:46:23 GMT  
		Size: 100.1 MB (100089670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be32d5f792fb24f7771259f24df2615f895021099c4ac87102541234680e129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 KB (252629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69404c89a94952654d2a4291dc918a4babafbed6d8cf4b6e6e58cea162948e64`

```dockerfile
```

-	Layers:
	-	`sha256:2f90624c1a6b9a403eab39675f07f993a4de7527d53ecb0efece054e62da5963`  
		Last Modified: Thu, 09 Oct 2025 00:53:32 GMT  
		Size: 243.1 KB (243127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd6cabf8c9908a9c797b7f919824686d6019e67f20aef7c02ccc75be5fac7aa`  
		Last Modified: Thu, 09 Oct 2025 00:53:32 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
