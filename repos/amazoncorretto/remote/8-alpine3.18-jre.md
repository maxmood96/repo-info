## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:b3eda7a53936bc4268ea96afa2081f8991c1d85cb350a90817b7c0a0e10dad29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eddddb43054c1b334b7e8c27f0e2a65f379dd7303c2b8b65281bd1d878a969c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45073905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9ea8aa2c07e598d1d563666e247fcfea82155b1754bb60c49d4bdbf4ab0cb7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068ec254366c93ac680a0ec78689c76498a8c202b06a73f82e8e9f4b6c3f44c`  
		Last Modified: Wed, 08 Jan 2025 18:09:11 GMT  
		Size: 41.7 MB (41655931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ed673d18e7a748509a7e06f59ced8306c3eb64ddcf10bf3905b16db8287c4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 KB (193371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e198273a17510240e11c01357cb5645c58e3762ef92798f83672014c14302b3`

```dockerfile
```

-	Layers:
	-	`sha256:0794d4919e95c4ae6ce12bcafe7b9383c3ded31c9e8824225a51888c20d93543`  
		Last Modified: Wed, 08 Jan 2025 18:09:10 GMT  
		Size: 184.7 KB (184672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c47461838e817c6d454974e4d1f407790cecb316d569c0e9c2b510a344b70e7`  
		Last Modified: Wed, 08 Jan 2025 18:09:10 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ec82fcf94f240dbf0f4177cb2fd8c49f7d178f22f10fa3cad9d9001aabd0a932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44703954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b347e9f912c43c61eca73d7654474cd34a0de17927b73163f4782aae423b95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80107f328542d43844ab4a5b84f1b0d25d241cb8e57916de80c9446f5443c529`  
		Last Modified: Thu, 23 Jan 2025 18:32:15 GMT  
		Size: 41.4 MB (41362093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fad32e6e281bf70b478aaac903f505d97894f148e2951497c248726f0f758622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ea1dcb0087eba19c30d16b0d8ae59b2d83e8f2608c71ca3ada3e3da2247b13`

```dockerfile
```

-	Layers:
	-	`sha256:1705609fafcb811a140d8d17164bcc5c36ea2d864d2d53a628db8fb4923cf9bc`  
		Last Modified: Thu, 23 Jan 2025 18:32:13 GMT  
		Size: 184.8 KB (184780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee492cbebe94cc4a0d932a0d576e2036401f15d224c4e37b7a4090d63b0352c2`  
		Last Modified: Thu, 23 Jan 2025 18:32:13 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
