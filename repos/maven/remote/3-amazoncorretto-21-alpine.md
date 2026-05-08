## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:be436cef1006f8399c65959e86b0294389a0b74f635e866535edd131e01a15ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:b4d651babe8f04f4ef7ed8bb7c99876c729905ad3dd323930402520245ffd417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177410752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbc171449431c88024fc994541d682390835088b0720969bf5861b75243f7d2`
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
# Fri, 08 May 2026 00:30:58 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 08 May 2026 00:30:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:58 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:58 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:58 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:58 GMT
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
	-	`sha256:9e2e98faccb42f737f14a19f57d8cebbf3e0429b5c49021782163e66c59d7aa8`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 2.4 MB (2420152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f5e5273cb0f65b5b5df2cbb912d53c7399f138b64f6c0c05fcea237349efc`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d843b62de738fd08fe93ff256f7ff8ee4e6548e0c76625ef11a76e7e563591f`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692d690d592f66065f8c92eb94b4530002ee09a827834c25861623081466b405`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:30a70d2d850f905c9e890ddbeddb1e938ef27dc402bff58127b13aad07fdb591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d9377cd0af0ed49550fe58b5b60358d84d61f535b27684242918658b971183`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b57c81bdec2d269290f3b8fe8a82982cd929e8eff5655cf8f2873ea3e6ed9`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 728.3 KB (728289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06061c823695f4d90f931f932bb971dab3911e59bbd1a5662f68b90fcd61d903`  
		Last Modified: Fri, 08 May 2026 00:31:06 GMT  
		Size: 14.7 KB (14680 bytes)  
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
