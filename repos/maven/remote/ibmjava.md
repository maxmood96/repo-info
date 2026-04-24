## `maven:ibmjava`

```console
$ docker pull maven@sha256:83b2f8e707cfa400a4f5ed52693915a947cdb0206a886fb3af72d436522411eb
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
$ docker pull maven@sha256:23c8f35885f182c7a30945681892de7c6e6dc3be309d3f2396b9c68bb0f89571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217135955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2401b9049db33843f38f54d60b25a76b026dfdde2081a43cbc8af6b45473ad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:26:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:26:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:26:54 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 24 Apr 2026 17:33:52 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:33:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 17:33:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:33:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:33:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 17:33:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 17:33:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 17:33:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 17:33:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 17:33:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 17:33:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 17:33:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 17:33:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd87c806116a3327741f8989fb20f94e5b7e156ca698501e1e0b0514c15176cc`  
		Last Modified: Fri, 24 Apr 2026 17:27:49 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da11bf882625bc0731870fe51d67be8846835897063fdf7fbe2617b1a03e93`  
		Last Modified: Fri, 24 Apr 2026 17:29:10 GMT  
		Size: 173.5 MB (173521349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd90500c68443c315b7a2a3ebb7cc028fdf2b95111b927074813bb3dc966284`  
		Last Modified: Fri, 24 Apr 2026 17:34:01 GMT  
		Size: 3.1 MB (3114826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c926380c65217d1b8dc780ec1208192da30df6f4e790c8276aaae00eded3197`  
		Last Modified: Fri, 24 Apr 2026 17:34:01 GMT  
		Size: 9.3 MB (9312204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc110a39b8c5d1e55e65a6de94d58b4921d5c694b39f2515ff097482717aeec9`  
		Last Modified: Fri, 24 Apr 2026 17:34:00 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b2181a836347d3efc43c69e621b0e8642278edc9afdd98dcded85c342f818`  
		Last Modified: Fri, 24 Apr 2026 17:34:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:e4ba85de760cf00f241e919d2ccc3a4f1d9e348a4941260b7a114ad33d6b58ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98d5821906998f67bd4cd650f32e7cb9586a056924b92cd3d804cd9afc09104`

```dockerfile
```

-	Layers:
	-	`sha256:50f19b31c71138c7e6e5901d624497415b94dc128de6b1b2b1c04da87108801f`  
		Last Modified: Fri, 24 Apr 2026 17:34:01 GMT  
		Size: 3.3 MB (3277480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a1264264438678d9e40823d9de835bd7e52a35106679fbc1c9f2994cc511fb`  
		Last Modified: Fri, 24 Apr 2026 17:34:00 GMT  
		Size: 16.8 KB (16779 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:63fe7b77aa06c005b156aeb2a28fd5a97308a123f89f9f748414ac2ede829540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224070904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4e449ded2c4901aef84284e49792c5c3b8bb115c727162ba665fc267628f28`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 24 Apr 2026 17:37:39 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:37:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 17:37:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:37:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:37:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 17:37:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 17:37:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 17:37:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 17:37:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 17:37:40 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 17:37:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 17:37:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 17:37:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132eaca12df4dc2a7b0af262a8068d86a7122d98ccc02571ca194fca2fb9e83`  
		Last Modified: Fri, 24 Apr 2026 17:28:02 GMT  
		Size: 174.6 MB (174644995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3b73ffb9b11ed13539865522c18597051d555e8e1be07afb702223f198236`  
		Last Modified: Fri, 24 Apr 2026 17:37:58 GMT  
		Size: 3.9 MB (3928061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c638e968f478b6d83f469216620960dbebe4315aa2d0562fcb25e9a3f4265e6d`  
		Last Modified: Fri, 24 Apr 2026 17:37:58 GMT  
		Size: 9.3 MB (9312259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383dd44900ef19a1863f630b870cba910f35893ded63f0685e7af057aa40baaa`  
		Last Modified: Fri, 24 Apr 2026 17:37:57 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63b299beb945c9f395f8a410f1d672aa0157831a01f74fd5503e8902dee0b50`  
		Last Modified: Fri, 24 Apr 2026 17:37:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:7f1765590cd1273fbd22fb396d2bf0488dd44005b6fc6886b5d0fb8686c54174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0bba71190d6c029c7121108addc7062997d8a10d4d5f7a5bcf9d88c6e991a7`

```dockerfile
```

-	Layers:
	-	`sha256:47c2fcbe9c6bf98f49858e6289c9647b9b3daabe8854edcd573cac1c3f0a63df`  
		Last Modified: Fri, 24 Apr 2026 17:37:58 GMT  
		Size: 3.3 MB (3263591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efda3596836fdfa25e811ac0fe5e71c05bdc002862a4d98ad420fec567ba61e0`  
		Last Modified: Fri, 24 Apr 2026 17:37:57 GMT  
		Size: 16.9 KB (16853 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:5a10b2bd1f3d73c0e530ede459d5409ef97a643c4c1c9a060ee33cc126c188e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207197873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fec4b50b7368c92741920c8f7cb29a72f3ba340822b8d1a752108a0348057d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 24 Apr 2026 17:56:10 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:56:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 17:56:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:56:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 17:56:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 17:56:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 17:56:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 17:56:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 17:56:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 17:56:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 17:56:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 17:56:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 17:56:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d965b2264e89cbb2ca1fd752191cb709cc08ea307b3d630dd92092bcc30f153b`  
		Last Modified: Fri, 24 Apr 2026 17:30:11 GMT  
		Size: 165.2 MB (165169474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97278e3f4d1e392564acd5a6c04a951f06358e36bda1cbb012beb8fc7377422`  
		Last Modified: Fri, 24 Apr 2026 17:58:22 GMT  
		Size: 3.1 MB (3056965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4018525cdf5e6dffef7980507f77c0367a1d095ab56a0c83a9d927c9e702c330`  
		Last Modified: Fri, 24 Apr 2026 17:58:24 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46385f75cccfe1a505fca0250cff8fc528e47eb190eb6fc3c8fa4942f83df054`  
		Last Modified: Fri, 24 Apr 2026 17:58:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482d65700f0d93295d25ff03dc568231977e799da9998aff2d328a09c672bc1`  
		Last Modified: Fri, 24 Apr 2026 17:58:23 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:ac94e89cc135be269f51f4a8750b18ec1afa7bd3bd1ab4adca572391a1341a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2591c886c8a26951e919428e9ddab4a92693d0dd0af943c3b9847d5e243f90`

```dockerfile
```

-	Layers:
	-	`sha256:22845e894253454ddcd8c95a43c00873062e7b0dd2e5db1223269725ceaf88b5`  
		Last Modified: Fri, 24 Apr 2026 17:58:23 GMT  
		Size: 3.0 MB (2950766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04bd64646f948bcdc46983512adb4769f36a65e3d16545bf399324c020a5dd3`  
		Last Modified: Fri, 24 Apr 2026 17:58:18 GMT  
		Size: 16.8 KB (16779 bytes)  
		MIME: application/vnd.in-toto+json
