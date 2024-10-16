## `amazoncorretto:23-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:0230c82bdea070c6b07edf743cc57a7df33ebcab5898997779af853c1da611ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98d9b5c8356369f1b443ffa8ce5a97f49b6f2ced588a69fc7ecbf2981bb185b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170075115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97188d0eecfa5d5b2c029967d9f3f22dd5b950ecbeab47320dffb74763556fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:19 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Fri, 06 Sep 2024 22:20:19 GMT
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
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895daa15395946881a4a7010b771823e1ec3c24eae62a7a826925f525d8b9502`  
		Last Modified: Wed, 16 Oct 2024 17:57:33 GMT  
		Size: 166.7 MB (166658802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c2b551e03a347da835341c20b02657f4722509bf177d012f049aa2cf2e37e2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 KB (391823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e785c64d031b0433f954ecd0d66528b80c1090ab4e5e930653e694eabef15b4`

```dockerfile
```

-	Layers:
	-	`sha256:8c3a9365250be0a9ddd0255f96ad9874b3391d2d078cdd6b7f4ddc6009c8552d`  
		Last Modified: Wed, 16 Oct 2024 17:57:29 GMT  
		Size: 382.6 KB (382616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784ecb43bbcc2a83bfebf905f88acbf036b521a64f04931b503b3b2e3d31f11d`  
		Last Modified: Wed, 16 Oct 2024 17:57:29 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:974ed3552715194fc35a0eed2c27848e5602c81ef7b0774a16caf4d5c8e34dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167693581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14cd9084dd086faa1d2e1cc9c18ec6d858ff8103aaeffc600c9b1acb2ddc240`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:20 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
# Fri, 06 Sep 2024 22:44:20 GMT
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555b3edbc635eb7e13c6a301daf596cbcfc4702681e4b56ffbd52b26c73bba12`  
		Last Modified: Wed, 16 Oct 2024 18:44:39 GMT  
		Size: 164.4 MB (164353234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:503b5e2ba6007ea72abdd4a7e3a62be28cd8b5b5b0d0ed533a5a68f761bf26c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 KB (390698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9bdd2fcc5d4c1bb1f67bd8786c98113778c6ab56c54ffa0f6217e2c67aae38`

```dockerfile
```

-	Layers:
	-	`sha256:5ba68b57243c1248f55052d454c97847eec85482691964f1dc72556f54e22a8a`  
		Last Modified: Wed, 16 Oct 2024 18:44:36 GMT  
		Size: 381.4 KB (381393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaaabaeb5b96837db2cb0467b10175df61b082f7bf82f8a5d608cc48439898aa`  
		Last Modified: Wed, 16 Oct 2024 18:44:35 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
