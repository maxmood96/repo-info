## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:77ceb58ced2ac1c9a53cd9d682d91964173a37044c60fb200861e722e8659fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:1270213fdc4f1111e4c5886c7fc4855157472f4e6ecd7385db395f5fa76c0e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94f48d9ecc00eb33253a17aec4875bd0fbcf10abfe2c93b9cff504f96a3fa6a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c1fe4088fbbb049c51655abeadbf9a8ffa173bf595c0ec46c4f3813dafcb7`  
		Last Modified: Wed, 08 Oct 2025 23:50:54 GMT  
		Size: 178.5 MB (178521094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a7028fe28f0a1eacce3a38867534643ae234eba2239e0dcdc4cbb4eb8221cf`  
		Last Modified: Thu, 09 Oct 2025 22:54:03 GMT  
		Size: 2.4 MB (2364422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ce4dd7127d4745f9f2a93c8c067be7a799a28c308b4aded335cb44a2233cb3`  
		Last Modified: Thu, 09 Oct 2025 22:54:04 GMT  
		Size: 9.2 MB (9242589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23a6f45f787e0b057b27f584cbdcad067292c3cfbc910bf74381663da572caf`  
		Last Modified: Thu, 09 Oct 2025 22:54:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0688f3f33f4851a63d5fb166c5598ee7636753f788a86d084541c99f01024902`  
		Last Modified: Thu, 09 Oct 2025 22:54:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:42b05c1412b02205539c013f05d5acfdd6ccc4c1c7b6e3c82e118e80aefe754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 KB (549436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c568ae4d292392fd25ea1358c64ee93c55b3cf27743f1c17e7814fd2c3b4a7`

```dockerfile
```

-	Layers:
	-	`sha256:230d2f4de530addb8a206f949d85e9384e68f22447c19a331effd75467742917`  
		Last Modified: Fri, 10 Oct 2025 05:30:17 GMT  
		Size: 533.0 KB (533032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbab9aefe8b16002b95917ea121690216ccd3bb8da252a5e14db4d4674b1d23c`  
		Last Modified: Fri, 10 Oct 2025 05:30:18 GMT  
		Size: 16.4 KB (16404 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f1e8737e21903ee5d53e2dcdb12c0c8f2f4eec7013e4b6c33c4e8328a8749e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194157670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1afa7c8aa051b535c10a5b327be8ae336dc25861b1689b1f6502260a72940d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 12:56:50 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
ARG version=25.0.1.8.1
# Fri, 19 Sep 2025 12:56:50 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 12:56:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 19 Sep 2025 12:56:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c5f3bb4876c6aad498a033c9c1187005a2710a104690543fede50be55452bb`  
		Last Modified: Tue, 21 Oct 2025 22:16:34 GMT  
		Size: 178.4 MB (178369790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d168351fa97372c801eaa1333af8dcc9f80bd8211754b5a3e6dfa5b3947bbcf1`  
		Last Modified: Tue, 21 Oct 2025 23:02:02 GMT  
		Size: 2.4 MB (2406191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe9e060864f249b4713b0705b92e44e43ceec22f611e29124db47bf38d7536`  
		Last Modified: Tue, 21 Oct 2025 23:02:03 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ed928a34b47b49449031ad8f822aa4500f068b8f80f661b7f6865d3b2ee93e`  
		Last Modified: Tue, 21 Oct 2025 23:02:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d946413992f2592dce73ad9253f1c3be53e7a707f4babe2ee0ad7d2cdddc9`  
		Last Modified: Tue, 21 Oct 2025 23:02:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:93af4d5813073ff9a4613779c87b15b05cf1ac75b17adfdff2a62fcb81ded172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.6 KB (751557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416b2a2a7a42edce642d43a7eb5c4bd8d072b30d54225852e53efa46316a29b2`

```dockerfile
```

-	Layers:
	-	`sha256:2dee5e6b273bfd01ccb327ddb5968fe4fbc95e4e32ceec49b385531968a71bcf`  
		Last Modified: Tue, 21 Oct 2025 23:28:45 GMT  
		Size: 735.0 KB (735019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e5a63d1891876973f454740e0994dc8c7c564ffd5743ea4c1a8b309137967e`  
		Last Modified: Tue, 21 Oct 2025 23:28:46 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json
