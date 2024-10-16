## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:7ab62108b2a065f6fb42636aaf6d0b408b551d3c31c9c8a8734410abb09064ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:90533eaf55d4ef4456319967c5dcb387c35ddf750a508ae3bfc96c679bd9bc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162553998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283e09a50b7aa9753215d44aafe20c551476de2e6e278bd47d5f0e0bb3625d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:bfb2972ecae7a9dd2f51282c368df744040af6055effeff6fe1f6c73abf3a003`  
		Last Modified: Wed, 16 Oct 2024 17:57:22 GMT  
		Size: 158.9 MB (158930191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd7078ee435abdc9c0fbdcc2c7ba61ba82056f014ce493ef2dbc1f1097574444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745d65d425eeb26da9e9b5baa40be789f80a33b97ac6626fe8b287ca473f7ce7`

```dockerfile
```

-	Layers:
	-	`sha256:eb93ca53eb8b5da0e492535d68e59b7480f997d06cb94ba3b5f2fffcdedb3160`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 378.4 KB (378399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e03aee9382f383338cf6bc66f189a035a6b5ff82dd61f7f29af9733940e053`  
		Last Modified: Wed, 16 Oct 2024 17:57:20 GMT  
		Size: 10.5 KB (10514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2d3fe4a361e5fa38b2ae3e326d52e23b402b8d32e34378e874e6a6e5b07ffee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160967656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3553bbada4ff6ce37a2535f7299c9c6c814843d32586a09682e2a02bda5241e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5caf0a1ffd86bb63189c72afc5447c3e4d36fe0f610c98f82c31d967535a4628`  
		Last Modified: Wed, 16 Oct 2024 18:38:39 GMT  
		Size: 156.9 MB (156880010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f1ef3e202a5b5bb42b002cf939dc1fc50559d9f50393d25d285dc644343aad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 KB (388524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5c81b4b775f29a6e4d75af3268aab18406df7ecd8e44673fe84726926a9c64`

```dockerfile
```

-	Layers:
	-	`sha256:54813018254face0db4d101b5d626415e10b8e6f3b04eda9081494613f9d7e81`  
		Last Modified: Wed, 16 Oct 2024 18:38:34 GMT  
		Size: 377.9 KB (377865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e6cda40d6cce8ea80ff064abbe0070d6e1953691b7c5506dd0789a4c000c8`  
		Last Modified: Wed, 16 Oct 2024 18:38:34 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.in-toto+json
