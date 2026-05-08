## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:7e93db7836f6bcf849116541e721268a48b37ea66769ba9f58a78c42692309f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:9dcf09ba5d998285f66b307fbcb4b899f508d6ddd0927dd564ed6ea34a925ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177410740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7348111282767a6df29f3a8e90402f3a1d21587b3845fee88d7a9f6bbf2434c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:52 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:52 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:15:03 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 22 Apr 2026 22:15:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:15:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:15:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:15:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:15:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:15:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:15:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:15:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:15:04 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:15:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:15:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:15:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b05a9ca5f91c177d0decf2d392d42cc189cd2cf569e6cdb0fd2b734d669bb`  
		Last Modified: Wed, 22 Apr 2026 21:35:12 GMT  
		Size: 161.8 MB (161813161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741b098a644105f40ec52ce2f8716911c5d9e1b4334e85ba5389d9b6964a03e2`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 2.4 MB (2420166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df4e9e709cd6fa85697ba10c257ae6cdc17a71772d33c54b420f03ed700b11`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 9.3 MB (9312215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a957ec7a6e790bc362db19cf1c2bb723cf9e78d954fe61bd8ab3d6515b4e4fa`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ac3cbc94b8f4d4fbc5c085568dbbcca6cac51c503baa6e374956d3b21d16b1`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:69c54bb3b93e4b3e8f8f11c9e8b4e97a6b1eaf607363966c40bff2fe4e99a918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.8 KB (742815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739725e8c9ff8d55a0792b838e4e377896fe1b6257561ec15755d387ced6fcb6`

```dockerfile
```

-	Layers:
	-	`sha256:1f80c177b0dc2ac68c7d9707612fc349ddc372f8463628df35b8b53a7c24c82c`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 728.3 KB (728289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7249a10211b584ee65e3517ccf9ec122333b5faf68003920495e282a292883cc`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:353bb0d37d450b0724e1027f3ebdd3ab8e5491fbe9f1bb0c0e8c73d4077e9e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175802789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663393af4ac6b930fdad42e0a0af464d7fd420740425f500b5023ada9955cd67`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:45 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:45 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 08 May 2026 00:29:40 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 08 May 2026 00:29:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:29:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:29:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:29:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:29:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:29:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:29:40 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:29:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:29:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:29:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ecb8ee1bb766b7846294cccb87c572391bd352b362a7867597720dd8b7df36`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 159.8 MB (159828502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa2768d7dc17cb0a5d98095aa0875b4564367bd536e806cf1ab16e73615c7c`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 2.5 MB (2461180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd28e738a1106e9d61e6e074fabbe28f31aa09642d2d426e3ccc70790b0868b`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 9.3 MB (9312231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618cf1abdb5e80aba84e52b91204fe1cb6ce6b3590403f41bfa70b6364a76304`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d774dbb5f3c20cb813a2b732cbaef89f6351c0aaa038978f4672cb885fb4bbf`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e1624af94a9fc2c98fc447e76502f5e0471ef102a3e8b0a65fd73b45f1a82009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.9 KB (741859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87ef50301aa0e4b77c5fc78a8d46e96cbc3a5016d8aaa6f811220f706b90dfa`

```dockerfile
```

-	Layers:
	-	`sha256:33847af65da19328f7f3d938f3a77d94c038625bb5d0a806ea75a54fd22523b9`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 727.0 KB (727046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea316461f2df1f92ff974478914d0afa96f3e6c4135e0a580a5657931cebe93`  
		Last Modified: Fri, 08 May 2026 00:29:49 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json
