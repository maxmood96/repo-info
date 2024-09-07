## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:5e281b5d8b43740cc73b4f8256a62829dfc9550bcf4189a8bbd6a6f27431a36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3bd5ac6209e70d59953dd15f496204c3016ae23a5c671e4531183d5de5074d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103747598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de4679254064d06d1b92661b4217f06803579db1ae6790790e25582ba96e46`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37acea8028a4fbb47d620368843704b3220d4e77d3859fd1ae39012514b5d4b4`  
		Last Modified: Fri, 06 Sep 2024 23:17:08 GMT  
		Size: 100.1 MB (100123791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:544bd4ccfd438a4870a1617d98f887566f087cb91a30c4e940773216859b3fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 KB (253248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afc9c1a28ba2af3962eb97c736cbbfa8fc38e03707400a3bbfff4fb6c7d0259`

```dockerfile
```

-	Layers:
	-	`sha256:fa2c3f67497c223113795b5a847f216ed958dfc3d8d6a69000f8c968f91ad0aa`  
		Last Modified: Fri, 06 Sep 2024 23:17:05 GMT  
		Size: 242.8 KB (242798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b07c3ba4fa594b2f43ca8e804fee1ba085bed0a5d8512edeb2b27ce201fc89`  
		Last Modified: Fri, 06 Sep 2024 23:17:05 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4ed647b9ce9377c380bbe135cb8a1ae0d473ebf9b0b06552b48ceb9846a76141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca0682f220a2cbf22aca9ba9add0995262e8f7213804ceb8b8413bb39327cac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd4a1d60b593f6d1a636551f8cf49c12bfa3f4f259330619d9b4fd4e84a2da`  
		Last Modified: Sat, 07 Sep 2024 12:07:52 GMT  
		Size: 99.8 MB (99834737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a72765eaae4ee5bef7b15d8db0ff5a78a6b34f6db82bb81d50e2407dd2b44a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 KB (253775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd28d02ee23fe1f1efd43e9f85cfbd8fb7498c5f44c34929ed1746231687d05`

```dockerfile
```

-	Layers:
	-	`sha256:310c248aadfe2243e03b25b53d69b9fa28c19ed88524a86b9e70d020ebde4b1e`  
		Last Modified: Sat, 07 Sep 2024 12:07:49 GMT  
		Size: 243.0 KB (242978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bea63a782ae8532f472d6624d348060ee61e1f15b2a2907c865f73ecbf6d5f2`  
		Last Modified: Sat, 07 Sep 2024 12:07:49 GMT  
		Size: 10.8 KB (10797 bytes)  
		MIME: application/vnd.in-toto+json
