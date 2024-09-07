## `amazoncorretto:21-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:6a98c4402708fe8d16e946b4b5bac396379ec5104c1661e2a27b2b45cf9e2d16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e070ca9444b6ddd8ea180f0bff948f0f3b6712ca0b08ddfb86d3db2b9e980f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163349406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d63633bedc97029fbd8a6ef08e8f405d19d826f7454659fdd0222941f17348`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:596b7d3d38938a1506676ff708391a887187876abe376b0f227b4812787db642`  
		Last Modified: Fri, 06 Sep 2024 23:17:57 GMT  
		Size: 159.7 MB (159725599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bf0ffeb8d9fe7c11c5c8447d324d6193f06606ccd7b96f1f99359b0a276ad53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073c045deb653b2be474fd555531391dce246a66bffad005526603cdd8102295`

```dockerfile
```

-	Layers:
	-	`sha256:b5848fbe58ae67a7bc2fc076807d1705718a7f97d54ea05b4bbc8e567d736426`  
		Last Modified: Fri, 06 Sep 2024 23:17:54 GMT  
		Size: 378.4 KB (378384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9572d18e4781fa284bf183d6ff1ae69a7d7c5df78e1ba73991f29ef2264a847c`  
		Last Modified: Fri, 06 Sep 2024 23:17:54 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c490e42db0a5e9ba057b374efb0fd2df7957456aa129e87ededd61e8ac60f62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161569510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4355cf2a628fdcdae797524274197a85faf3143681534634d0c79f45999011f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:8519df6027afc977d341bcd49760a87be52c29fc18a660b2d36a8f9a845aa2c8`  
		Last Modified: Sat, 07 Sep 2024 12:15:32 GMT  
		Size: 157.5 MB (157481864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:885e48406439d8ac91ea5365ec70a80c5cf6c8f898ac6a95e966e01e2dc2c5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939734c7c38719ecfd15285d071cddc7e8a3c34ebc9c05728e81fc85c7e7aada`

```dockerfile
```

-	Layers:
	-	`sha256:4ad0cb338a8ed37bddc7127e1d758dacea7777efa97009fbd29875a463942cd5`  
		Last Modified: Sat, 07 Sep 2024 12:15:28 GMT  
		Size: 377.9 KB (377850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84cf704b797d9f12a9f44485ef6fc87e7bf128ba69125a1dce2e1efbf1db71cd`  
		Last Modified: Sat, 07 Sep 2024 12:15:28 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
