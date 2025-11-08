## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:dc06a5ffb5b111c047725647b5484711b49a825cc09668b653095c582481c752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:12cfbe1c0efbe1fb241ad235c1d7dd97f461f484e7eb15e5674782f1444f968e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196146577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac40f29cfb29a67f1fe6d3bb8f419bd00cad178a5a4c90852824b72b9d1aaee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:20 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:20 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:20 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 08 Nov 2025 19:24:08 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sat, 08 Nov 2025 19:24:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:08 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:08 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39efdfa875cf11df5af65d4582d8a8c511a684ff9b183b51bad538fe768d8495`  
		Last Modified: Wed, 05 Nov 2025 04:50:28 GMT  
		Size: 180.7 MB (180725412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327ae30f259500ada3618d14424eda5aeee56e72079398625c3d9543ed7cefc`  
		Last Modified: Sat, 08 Nov 2025 19:24:27 GMT  
		Size: 2.4 MB (2375107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f8e60c46a303d5b1a4a74a9829e34ccea0fe1cbe296decf4daf174e0e444a`  
		Last Modified: Sat, 08 Nov 2025 19:24:27 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f182b652ce4b30eb9ca5757bacf3ec17e407d4d53c2fddfc4c861b4483877284`  
		Last Modified: Sat, 08 Nov 2025 19:24:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d22397fcbae9a3e772534f323e77ba129e95b0324f7859d5f55f193f5b754e`  
		Last Modified: Sat, 08 Nov 2025 19:24:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:30c4408004ffec7582d215e51f270e5f0770748ef531491ff743a463c3c4a40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3758bc277500151d92fd0c088b9a8db1b6cdccc15f6ef7c111d9ad657b393e`

```dockerfile
```

-	Layers:
	-	`sha256:8866ee268fa026c498279d7681deae05ff5d465c96593145d02a26b34d062655`  
		Last Modified: Sat, 08 Nov 2025 21:29:43 GMT  
		Size: 735.6 KB (735615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3faeb1e999cee2f138a7aa02c8a912fa450d0e1599cd9b3b379d6c4d9c96a5`  
		Last Modified: Sat, 08 Nov 2025 21:29:44 GMT  
		Size: 16.4 KB (16361 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f04bbef78d7add283a262fe4261c892e52debb93a2efe5ca9444c71cb97c32a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194159521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015ec52c5db2caf22d28dd0c0a4298a725966cf5007622bdfbe3f432963e63a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:08 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:08 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:08 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 08 Nov 2025 19:23:55 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Sat, 08 Nov 2025 19:23:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:23:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:23:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:23:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:23:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:23:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:23:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:23:55 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:23:55 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:23:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:23:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:23:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c3d1078166ba6eb65daea030105157330eb50995e58c176b24e5eb82842fb4`  
		Last Modified: Tue, 04 Nov 2025 23:27:31 GMT  
		Size: 178.4 MB (178371636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a0ffd66d71418cb4b88022b4ba466ed13c55184bd5cb031ad7db1d6bec440d`  
		Last Modified: Sat, 08 Nov 2025 19:24:07 GMT  
		Size: 2.4 MB (2406198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa80205a22ba7ac2bad86ca74e19bafcfcd243ba17bacc96fd77992d34f63178`  
		Last Modified: Sat, 08 Nov 2025 19:24:08 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c76af6ec1763440e7d7b9fc3588b6e207000b97c9195f176b354deace7297e`  
		Last Modified: Sat, 08 Nov 2025 19:24:07 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63276b6cefe7e22c6c433b98359c861ec1169361d446ef18aca59d0eb6f2b97d`  
		Last Modified: Sat, 08 Nov 2025 19:24:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c09a230f049ec42c74cc9b154e5c42fb401a556a595283aac6d8e0426980ee47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.5 KB (751514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9fba3a47fea35b9ca0b87eca9df82e6015373a96a79ce9f243058cb0782f74`

```dockerfile
```

-	Layers:
	-	`sha256:4945559ce869cdcaa1f5f0dc286419cdbdf9bd4a635e5bf5d42203e9d1a715c4`  
		Last Modified: Sat, 08 Nov 2025 21:29:47 GMT  
		Size: 735.0 KB (735019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c13089a21964e1da61ba6bf0049247238e400b779b28e38080b27b12f038cd`  
		Last Modified: Sat, 08 Nov 2025 21:29:48 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
