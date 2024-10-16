## `amazoncorretto:23-alpine`

```console
$ docker pull amazoncorretto@sha256:f390e458a05dba29ec4d21a39a782720f96da6ddfcd6639bbf37cd8dddec42f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6b4911a53f098803d2ea9796aabaf111b8bae5c9dac0b00de98335e426275bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170282508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c5aa4ad4b4fbf6805ae68d3e68e8f277520dff976bbde2385090af8a1575f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e41c6c5ffedd5f7487980ee0dd96f3ecf403baa45baa1cb36ab53e3dde586f`  
		Last Modified: Wed, 16 Oct 2024 17:57:23 GMT  
		Size: 166.7 MB (166658701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a66be7b23cc53c7a11cef61b1b3626d1ae56a16d87c6cdfe9af52cb9d75b3574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 KB (390859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938f9a9e424e0e271c71d8f88e07a174aedb21aaaf188bba86524d8a32f5d58b`

```dockerfile
```

-	Layers:
	-	`sha256:a0f78fb550882c12f801d050bc50b2159319bd6f4dbbb893e7330a46fadeb94c`  
		Last Modified: Wed, 16 Oct 2024 17:57:21 GMT  
		Size: 380.3 KB (380347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bedeb234ff12c6b5b9f7f3da8f327cf700711b19e195356aaa286391bcc3ba5`  
		Last Modified: Wed, 16 Oct 2024 17:57:21 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:696bb0383ecd9f82db2b5cb415d978c70eaa8f845358951a8e51cf7958943b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168439867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4c884bc36f5df12ac6b640c9f72e21d878b7a4242544ac7a6e90af8f7a25d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec1ef0065c454eb9ae29eae0899d2f45f39e4e6a82929f0c88e27dd992af1ac`  
		Last Modified: Wed, 16 Oct 2024 18:46:10 GMT  
		Size: 164.4 MB (164352221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79f9d55025d13ce62afbb9be0cfdd7d3148fc62820842493b4409cae8ce5c6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fd82f35c7cfe1e47ec72f61252fe343f76bc2a206df2c837874d74c51d82ea`

```dockerfile
```

-	Layers:
	-	`sha256:c777163501bb7f393deae75b3789497da0095f3c75e3485a50e569840c2c3074`  
		Last Modified: Wed, 16 Oct 2024 18:46:07 GMT  
		Size: 379.2 KB (379172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623a1ebd53661d19bf8a5f789fa21e9e81861e33d2fabac06e24841e3c2e1bc7`  
		Last Modified: Wed, 16 Oct 2024 18:46:07 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.in-toto+json
