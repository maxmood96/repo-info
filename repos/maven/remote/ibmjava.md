## `maven:ibmjava`

```console
$ docker pull maven@sha256:697c0f4ea12dac740fd34fff7fbb26f635813c6925b31bdf68c6d7a79157fa13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:5caf1004535366b5e184d15d1206365bd9c19a9c9cf0916e9985b123813dd8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (216008379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6552492fdd30be1624e02ed96a775b1337f8b7df288526d986907db072deb1a9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6501625c0bd93c3a9e7bdafec2b1df8d65ee819572e7bb6e337314ab31718ce`  
		Last Modified: Thu, 11 Sep 2025 16:55:12 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd794a5e418d61cd9f0391f9aa128310c0ef64a7a804c3fddc9453c8e60e54`  
		Last Modified: Thu, 11 Sep 2025 16:55:28 GMT  
		Size: 172.7 MB (172664633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93cec93321bbaa6f87174036b74da3f31e830d75037ea6d98ab3d09b9d7a590`  
		Last Modified: Tue, 16 Sep 2025 00:16:05 GMT  
		Size: 3.1 MB (3113150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271436757916a3912cfa90387f9079d90e0c8d76f1773644b1c690bca390dab2`  
		Last Modified: Tue, 16 Sep 2025 00:16:05 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7302dabe04e5ef5d60c1658bb51a38c52b509619fb50f73e9755f18da18342e7`  
		Last Modified: Tue, 16 Sep 2025 00:16:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b87a834f63d7d446b7d33ae5b4800b8e5ce33640ae9163e203312c718b6015`  
		Last Modified: Tue, 16 Sep 2025 00:16:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:5962ee1490f9bd1b8bcae7d99e2330af4c90231b5347bd72c48d23813d5ab06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acf9f7fae9a4c7d6fb210201da9c9065873d4fcf2ecd6e80e6c877311b13360`

```dockerfile
```

-	Layers:
	-	`sha256:43a916259e1c6447b7b841378f91ecf8d6d87f3a152ce16f1c469805e50d032f`  
		Last Modified: Tue, 16 Sep 2025 02:32:36 GMT  
		Size: 3.3 MB (3276292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98eb75abd2f1c74a991d256e7a784c2522eb9bbd865e32df8bde5b33ac848738`  
		Last Modified: Tue, 16 Sep 2025 02:32:37 GMT  
		Size: 18.8 KB (18821 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:9a26368367e74b0f5889953df1524c24a7a34629db30be1c07b0f54b0384c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222961911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225e845342bee2a04cc87243dc85509d5a3f4e05fd90eff2af0478f3c72506e9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a9f118ca1f1cbf4058ca82bc7edc4791643f5aab1e787697cb7e9c745ab8b`  
		Last Modified: Thu, 11 Sep 2025 19:08:09 GMT  
		Size: 173.8 MB (173813396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18b1f80e44791039ad6bde420fff0108664b55ae76d1085d84219ece67d6c5`  
		Last Modified: Tue, 16 Sep 2025 02:15:42 GMT  
		Size: 3.9 MB (3925445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f604eaf9a670d898b487492fd895398be1af476e864d2216b1954365a62fea`  
		Last Modified: Tue, 16 Sep 2025 02:15:42 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e91662930f2a1fda28593a3e4c1563fd89a63e893c9435633365cb0d60895`  
		Last Modified: Tue, 16 Sep 2025 02:15:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336500d0de3ebf5136f8252202544cba9eadec0c7dc42148baf5461029380f86`  
		Last Modified: Tue, 16 Sep 2025 02:15:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:1e34acbe4730e6b6bf379acd3095ae3298d57cec970a8fa203f387f4d15e20a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155c350e8b71f4f1afb3d86fe5cf05a46d7cf78a4c8104b4360a96385330ea55`

```dockerfile
```

-	Layers:
	-	`sha256:ee225af5a1c3c9b37d10c7b6ac77e598d058122d8508f3d2b559170b17a5810a`  
		Last Modified: Tue, 16 Sep 2025 05:28:38 GMT  
		Size: 3.3 MB (3262403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9462446b85cf9f4d56e5c2f6f0c097b9a05a0c8ffe3282549a556d8038073da`  
		Last Modified: Tue, 16 Sep 2025 05:28:39 GMT  
		Size: 18.9 KB (18895 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:832940428248cb75141c5443095350d548345d8339c54a91fb0c7f3d97d6f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204389477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b29eff02314a193278342fb2c786dad426fc4cce531fd182057dbaf49b766b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543bf796c5e3ca3d689f3ec6349f0c52c782a4da34026d3f7dbd32fbf895bed`  
		Last Modified: Thu, 02 Oct 2025 02:03:56 GMT  
		Size: 1.5 MB (1455749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6118c3e9d908250603547950dd912481d3165025106362693552c9147b413eab`  
		Last Modified: Thu, 02 Oct 2025 05:06:12 GMT  
		Size: 162.6 MB (162632954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54171281afd0255b1e45460c513a32d0971477661f52c3f8f8ba346c7305717f`  
		Last Modified: Thu, 02 Oct 2025 08:02:01 GMT  
		Size: 3.1 MB (3053754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7fe030e4a4e93ec056aaf4ce145fbe0a5a22c7a4b9a4f9ef89589a93f5cd67`  
		Last Modified: Thu, 02 Oct 2025 08:02:01 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedab0c2f6bd7b7f3dbee7b044b655143ceb4161595e10f47f960e6e76025a28`  
		Last Modified: Thu, 02 Oct 2025 08:02:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f69318a903b293b6211f67bf3c8ee80f34311c029905e2bc7a151af20f32f2`  
		Last Modified: Thu, 02 Oct 2025 08:02:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:4fc32758c96183c984b2a8df6e4bfed1a7164fd827254387c77a97734fa1a322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ca543a11431f1c171f7bd93c2e7a5863504de631048b32d0c9bab15ec86155`

```dockerfile
```

-	Layers:
	-	`sha256:6db432b16e7424eca6108b99ca39bc6a06fb774ac0e61b4ba43501114b17ab59`  
		Last Modified: Thu, 02 Oct 2025 08:29:12 GMT  
		Size: 2.9 MB (2949592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a807349ad5ee5ad794b85688a7f463b880b9043da878eac0a976cb4e72dcd6`  
		Last Modified: Thu, 02 Oct 2025 08:29:13 GMT  
		Size: 18.8 KB (18821 bytes)  
		MIME: application/vnd.in-toto+json
