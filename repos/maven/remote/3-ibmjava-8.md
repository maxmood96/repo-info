## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:e51e375e379fc4e2b8d6eaac9113d6aa8790ac719815bd1344d610c9f949d281
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-ibmjava-8` - linux; amd64

```console
$ docker pull maven@sha256:5eb92c21a69f205ff02b301dba9fc34bfe35d887579c8cc64b4c9b99e107f2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216235100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe179ca44f90c10f3bc23482454c03d600b0e8b06622fd675f29bc8a65154bd2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f678ce4d9a60d6c998236f3e466663b67491d0de867f033ff45f466b1f53d30`  
		Last Modified: Wed, 02 Jul 2025 04:28:31 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbef6e2a79b4a6f488821b533bbd58fc3e82c469e70b2a60b56adcdbb580e6`  
		Last Modified: Wed, 02 Jul 2025 05:05:05 GMT  
		Size: 173.2 MB (173182570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07fbfe6f273f50bc5a44a55b748eac49cac67118fe179881877bca6322ab40c`  
		Last Modified: Wed, 02 Jul 2025 09:22:11 GMT  
		Size: 3.1 MB (3112413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e90cea6dc94883dcf8a5913f47ac293f8090756c5c56142d395821eb4d7aee`  
		Last Modified: Wed, 02 Jul 2025 09:22:14 GMT  
		Size: 9.0 MB (8953386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6593a17f301911279746715787b0f3749a5286e82f0c4b527d6428df7bee4c`  
		Last Modified: Wed, 02 Jul 2025 09:22:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509d3e391c676e4c79338634bc7998fd89b3e12061924485269df8668d15bc`  
		Last Modified: Wed, 02 Jul 2025 09:22:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:1f56168d380e564bab3b6592c7e825cd9add7280d7cc7c1e3c240c06b40b2d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3292518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c48711afff5be3be475da32e361b76955a14bcd498a12c28b353a3abed655c`

```dockerfile
```

-	Layers:
	-	`sha256:e643cbc04c57aa7703b2069f8743b851b15d7344035d3bbb5521807a5d0142dd`  
		Last Modified: Wed, 02 Jul 2025 08:30:23 GMT  
		Size: 3.3 MB (3273697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e573356716aef0be6544a6ce3f56b93daebee36278b4fe5e8841cbbde3d5f15`  
		Last Modified: Wed, 02 Jul 2025 08:30:24 GMT  
		Size: 18.8 KB (18821 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:2f8a52c2ce5e45762fa4d0bac9e2bf52be6d41c63661980a46b0e31f84e6055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223096939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bc86e812956d899f4e45521c11ac4368d1a0e5e2837db6043756ba0f913918`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba99977cd9d6077fd4b307c3357787311ced4b3a091deff606c2244499c52dca`  
		Last Modified: Wed, 02 Jul 2025 05:05:40 GMT  
		Size: 174.2 MB (174238534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573bda55d50e8df368ddd72140ae6bc5edc18e194d5d003f1f6e6f88fffaf42b`  
		Last Modified: Wed, 02 Jul 2025 17:12:02 GMT  
		Size: 3.9 MB (3925123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f368088890b0693b000840ba1ffc9899c6f04c6a8a7b63d7a607d1afa040be34`  
		Last Modified: Wed, 02 Jul 2025 17:12:02 GMT  
		Size: 9.0 MB (8953390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777eaeafe18b5f169f8a831ef4d3c7c86833f452c379992bf758ce9781c7aaa`  
		Last Modified: Wed, 02 Jul 2025 17:12:01 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd930fca31e2fd294809466118f1a6a5e7e85b58fdd2f54c4086ddc327c0317`  
		Last Modified: Wed, 02 Jul 2025 17:12:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:1c72d959b96c45d6b5b6767b2e7b775c4a2976c62107e83de36c64e57e9ace8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61694622af8bf8bde2637f1fa42e07ada409d9526ee20380cd59633f062ea31`

```dockerfile
```

-	Layers:
	-	`sha256:531427c0a83b2c9b286f37f338cfb88de4d488229fbe6ca514e5d8fd0e1c57bb`  
		Last Modified: Wed, 02 Jul 2025 20:28:49 GMT  
		Size: 3.3 MB (3259808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c7dc3ed93d5f3170d1b94d3d13655448ac2b2efec4f451c5bc537585ac8618`  
		Last Modified: Wed, 02 Jul 2025 20:28:50 GMT  
		Size: 18.9 KB (18895 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:e4f7446ec63fea05ef4bf273763332961d2c7084ebe4c98d2cc6599f5e1e58a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204762897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096f1320196452381ea479b7e5c4015652c599a7038799f5aa04a745a8cfd4cf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd11fc7679c3f39efc75001dc136ca312cb4002cb5acb77acf1231f881ccd`  
		Last Modified: Wed, 02 Jul 2025 13:30:07 GMT  
		Size: 163.3 MB (163297150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628dae6b992c3fb9805581de217ec8ecc3fca5e5575fdb5e8766bfb8a42942bf`  
		Last Modified: Wed, 02 Jul 2025 09:19:18 GMT  
		Size: 3.1 MB (3053365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e502e774bc1ec1311d30065dd4c86948a1f615a936fdbf82f352983adff4bae`  
		Last Modified: Wed, 02 Jul 2025 09:19:18 GMT  
		Size: 9.0 MB (8953396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a516beb56906d24ee2166468ac86fcff180f7344f3ac95693cb0ccd8f7e2f88`  
		Last Modified: Wed, 02 Jul 2025 09:19:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18fe926c9292226ed8a1639a484a3d0540a090531530b20316827df4385f540`  
		Last Modified: Wed, 02 Jul 2025 09:19:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:416fa703eb2cf4fa1d3fbbe737570595090be856e631f02c1e08b3ff71975853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909e9d7ea007d53beb0d31e6f5d0a6568f3dc2b540ebbd8c5ecbc1d337ee24c`

```dockerfile
```

-	Layers:
	-	`sha256:6b903402276a67e05d5019d4e6388f118f250967eb04c9859dcac6eaac0f59f7`  
		Last Modified: Wed, 02 Jul 2025 11:28:45 GMT  
		Size: 2.9 MB (2946997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb4940e37af411ba5ba7214ad6c7552ca31b7dc4bb51d22d91d49375696c910`  
		Last Modified: Wed, 02 Jul 2025 11:28:46 GMT  
		Size: 18.8 KB (18821 bytes)  
		MIME: application/vnd.in-toto+json
