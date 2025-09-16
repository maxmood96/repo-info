## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:ca359c6783bcd3f4a30878f8bf2391b42cd1b2d8b146769f561fa39b6ef87870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c0a7feb29794155ba63e6ac1158fe5c0a9c4b0c913d83b8dfc5dea6bb3af2c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115701242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01389b124fa3c4f0532f53b2fb82946cb6f30cefbe1960fa86a0ae1b6e7415fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73204ee579640710093fde3a57e563aa1538477f34cc691377b3deae24a5bb61`  
		Last Modified: Fri, 18 Jul 2025 20:07:43 GMT  
		Size: 100.3 MB (100295182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75439b7bcf3582ae24275c33be54e7cb1116b829c0e585c921796299ebf958fe`  
		Last Modified: Tue, 16 Sep 2025 00:17:45 GMT  
		Size: 2.4 MB (2362759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f301ec746adb8f9508edda871b7a6a2366fa4621939c0cb4bc6e970ca925e447`  
		Last Modified: Tue, 16 Sep 2025 00:17:47 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430631708bef9b00b39aafec327364b33bc1ab28a3dc2df44b8a99c1c2e13587`  
		Last Modified: Tue, 16 Sep 2025 00:17:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10cf34b7e641adb08fc1cc740a08bbc42c565ce9ee3cc65de2c8ecf05e31f04`  
		Last Modified: Tue, 16 Sep 2025 00:17:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:6374f7746ec6bd846da5e4d4b2ad4bfac158263c141aab2d9bf5774290dde43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.6 KB (409553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3b2e58b2e657f0290531447bc5776334b9156531c4b29c981a70d02ae178ca`

```dockerfile
```

-	Layers:
	-	`sha256:333768d9bd3bffe6c544b151f4d9122ed8b3edd21c9d826b3c997c12c6bda101`  
		Last Modified: Tue, 16 Sep 2025 02:29:44 GMT  
		Size: 393.2 KB (393157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa76bcf37b47c74de6e80a9ec321597c41fb12d7a87db226a2ca2c75b0a637d9`  
		Last Modified: Tue, 16 Sep 2025 02:29:45 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cced50bb979190378125ae9e0472de36c0394b79f815292546a9613931e26d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115860884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa93b8c6289b5004c6663aa14f69b2d6873994cf294c6aed095ae2232783fc0a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac20185427f1c943ee893d60f765f6e7ef03a7b7fc6c4199d972082d5f1172b`  
		Last Modified: Fri, 18 Jul 2025 19:53:18 GMT  
		Size: 100.1 MB (100092363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fb6c61ce4fe2275e11e686083f187cd3073522b359c253c44af7eeaf9b068e`  
		Last Modified: Tue, 16 Sep 2025 00:14:34 GMT  
		Size: 2.4 MB (2394159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a6f56c4d208f9462f10d4e0e512ae5ae5037536ad2e08a5acdb98d59ce33e`  
		Last Modified: Tue, 16 Sep 2025 00:14:34 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1102286ec99857e3a80effda32864afd1abd06117e7adc6a4645aebd6decb7b9`  
		Last Modified: Tue, 16 Sep 2025 00:14:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce95e930d8b77d5ab4ee03ec31250daf6f9adf81535afe5a668eb47c63ae9da`  
		Last Modified: Tue, 16 Sep 2025 00:14:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:864a4d2e16d9c056c0aa4c590fb69125b776a9826692521ba16f0619d9496ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 KB (409806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c95394f2a7c5e19a1ddc87f746297a8ab2e3a0b9526c0e5314d7a3016cee469`

```dockerfile
```

-	Layers:
	-	`sha256:4cd3a82038d2346412107dc18dbc4ab2ba68b25b8dc8d181646e58fd71f1ca09`  
		Last Modified: Tue, 16 Sep 2025 02:29:49 GMT  
		Size: 393.3 KB (393277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978aa11f91078c6f8fc8e087e5df4489dedc64d0ea95638b8194460c154518a7`  
		Last Modified: Tue, 16 Sep 2025 02:29:49 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json
