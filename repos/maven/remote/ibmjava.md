## `maven:ibmjava`

```console
$ docker pull maven@sha256:8f886e188a107c7483ae9e70bfe1dc187f704df5e7cad1f56e57159a95c8b95a
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
$ docker pull maven@sha256:f3c1cf6c79c26e95e6e2116d7b4cfa2175e37be6d9ff44ca728690de7dca41cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216671823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca290f4159b45c907f7631ffb78920a7f563bbe08e908c5c074fbd18164aa281`
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
# Wed, 15 Apr 2026 20:43:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:44:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 15 Apr 2026 22:49:37 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:49:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:49:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:49:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:49:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:49:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:49:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:49:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:49:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:49:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:49:37 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:49:37 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:49:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:49:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:49:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0869c1d8322d2c466905fc89398127e5fa8da14bf6344b72aeaebf3e4b9fa`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 1.5 MB (1450020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3970b600b7b1cd0857ebfeea7cea0eb07dad38ecf3a14c048202c18536742bd7`  
		Last Modified: Wed, 15 Apr 2026 20:44:30 GMT  
		Size: 173.1 MB (173058215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62eead9e079e254177f13505e9a99f4294673389b0f664c8c43693dba5f33a9`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 3.1 MB (3114860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d1270d3ae32fea31b943333ffc4ca73e490b992793a8e84d72c092d6cae432`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 9.3 MB (9311194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3842082c51821c7de6959cbe1e951cae40f04900b10f7cb3829955f2a797e9`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9d4f9bf911d32e80768429b456e55444c7106160c617b2a272a1420c73a95e`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:58a3f7080addcad531043d1a3c70d83f19ca559519a77963202c28ed93aed6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734238c996d0f904ec2b7a189b917643180b3af29103c9a8bcb74e8adf25daff`

```dockerfile
```

-	Layers:
	-	`sha256:0665b78bfdf7391373d761960e806858bc4dc11c6d87b21a4d0d07437c56e96b`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 3.3 MB (3276857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c0c65b93109fe482f6e5d3fc95cf04ae451f2fc9bf587219399dbb24da1952`  
		Last Modified: Wed, 15 Apr 2026 22:49:48 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:cdb4654c577c1b07536fa417e13327c1c48ba18ba8d1ab3770922b7b913164d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223639115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155757029b1d3ea02c0ad15a65b16daa9894cdeb933536fd68191cde5f5be952`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:38:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:38:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 07 Apr 2026 19:02:39 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 19:02:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 19:02:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:02:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:02:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 19:02:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 19:02:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 19:02:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 19:02:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 19:02:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 19:02:41 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 19:02:41 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 19:02:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 19:02:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 19:02:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29860e716cdf5ebc33e42e2dfa9ebfc64424bdcb33dd0e665d639d8eccb8aa8a`  
		Last Modified: Wed, 01 Apr 2026 20:38:57 GMT  
		Size: 174.2 MB (174212661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91a5c724c9cfca772b0f53bb94c651a40000b32dc41111738e266321ce4e8c4`  
		Last Modified: Tue, 07 Apr 2026 19:03:06 GMT  
		Size: 3.9 MB (3928309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac17f74a5864cb099240c1ca81564ee5e77539db7101f36fa210782c25eb5f0`  
		Last Modified: Tue, 07 Apr 2026 19:03:07 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3324845f55c3d55002d24c1a719e07ac0db51b0750a75c822161507c0ee7d`  
		Last Modified: Tue, 07 Apr 2026 19:03:06 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ecfc98eb389f1783151166f6bf66953861c0f3ba358218366e8ba3aaaa2c56`  
		Last Modified: Tue, 07 Apr 2026 19:03:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:ffcf5fa759ead321bd760dbe0e3f795561c0e308aef0a82a2f21d417afbfed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd65471c31797f8c44d9230f1c3ada60dc7b12426e9783f6ab40c2a83fd4bf2`

```dockerfile
```

-	Layers:
	-	`sha256:b389e9f4050c61582f82e4b69753aedf4dcbb2efb9f2b29072ef87b38f7cefd5`  
		Last Modified: Tue, 07 Apr 2026 19:03:06 GMT  
		Size: 3.3 MB (3262968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070036c4bbe59db8565d43f66cdb03ca2849110cf97375903f7c52cd28b43d99`  
		Last Modified: Tue, 07 Apr 2026 19:03:06 GMT  
		Size: 18.9 KB (18852 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:4ff2509b0529421b597c48c91ebf91ba80b65984cb4732e3696a5f579926ad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.7 MB (205657426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dba8139ba79fc907cb12162e812daa3e0cdca0cf06b8e3cb32f26e4c63a1f8`
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
# Wed, 15 Apr 2026 20:59:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:31 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 21:01:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 21:01:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 16 Apr 2026 01:56:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 01:56:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 01:56:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 01:56:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 01:56:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 01:56:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 01:56:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 01:56:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 01:56:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Apr 2026 01:56:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 01:56:48 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 16 Apr 2026 01:56:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 01:56:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 01:56:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 01:56:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ab3941cd71bf0d1ed95ce637baeea5969c841214c1f8546382a091a99864`  
		Last Modified: Wed, 15 Apr 2026 21:00:27 GMT  
		Size: 1.5 MB (1455827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172dfe04452112fe2a9b06fdb9d174719cb641c264b107db9241522cca0a1f19`  
		Last Modified: Wed, 15 Apr 2026 21:02:06 GMT  
		Size: 163.6 MB (163630492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a586f727d4c52ba01ea63706f214ccfc7ac4288d45210f911db56529d3345d7e`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 3.1 MB (3056586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0a9145daba591d8d2d30145b61f1422e922f16efeab43fc3189a248a42c2cd`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 9.3 MB (9311183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe3d4487a8f3d5e7d0331179b690fd9e78a4e312788f2567df474af127e74f`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e0883247a04eabf34c7daea54b06ac0e1c75d4fdc420c8e3465a9c2675bd84`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:781a3e2bb811086096ff5f74e1939f93798fdbae090a788fc7d8381de13e0cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076a3b73f453dd5c93788d681e623245d16a3dbd02bf1da703aa4ecc136a100d`

```dockerfile
```

-	Layers:
	-	`sha256:979d71e198a9051cf119eefd8193220fb2c6c23588b1f09d8605c0ad78a80c5a`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 3.0 MB (2950157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75148974c284d6ceff04447a2e13edf8ab55c266771a92f6b3238427ef6c43ec`  
		Last Modified: Thu, 16 Apr 2026 01:57:05 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.in-toto+json
