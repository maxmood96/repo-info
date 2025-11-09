## `maven:ibmjava`

```console
$ docker pull maven@sha256:90f6fd5b7e031ba1203fd919ad2bf48257e46fe0ab71f61092de131a8669f484
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
$ docker pull maven@sha256:c885540c180f10c9bdfbf7397c24835e444164fb2c4d5b46764eaf331e4b5157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216128877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447f243eea5b00fa48172aa0e24c502c96f21551d973238c49e7cb75481d9937`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 23:53:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 23:53:22 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 23:53:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 23:53:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 08 Nov 2025 19:22:05 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:22:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:22:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:22:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:22:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:22:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:22:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:22:05 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:22:05 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:22:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:22:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9258735a9e6d43d87267ea87f6837e9802319a364eb65924efa3a2c13c7bf4`  
		Last Modified: Thu, 30 Oct 2025 23:54:03 GMT  
		Size: 1.5 MB (1450028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1616394b14baed2fef4dbefd3f12b0dd0aaa8ecc2ac9933fd4332efb6138d2`  
		Last Modified: Fri, 31 Oct 2025 00:14:29 GMT  
		Size: 172.8 MB (172785546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3efa6dae703e5001d05cd5e33f964d562c5d90f2448b878a781c7b2e296b5b0`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 3.1 MB (3112878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bd44862b33305ff010558598c9a8c93d641f8efc8ffaee5546e0b259dd902d`  
		Last Modified: Sat, 08 Nov 2025 19:22:20 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11131dd9cd75d527830999aef231071bb722d8ccee86988a0d498de287ea80df`  
		Last Modified: Sat, 08 Nov 2025 19:22:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2410675d0190220d3b122e34b5a057a94a312c480b709a7d9e8b03b8bd1634`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:c77ef3f7585e6ee78ea7f335af19f84d838bd32d278d8aab29768346d13ddf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b418b25657c7d7bffec8919fe68798ff6dd91025488540650f9a10bc33055cd`

```dockerfile
```

-	Layers:
	-	`sha256:5e75035003b20f3d417c2c97ab0d527c3746cb3bc4d8810cedcf9651c6eb7907`  
		Last Modified: Sat, 08 Nov 2025 21:33:03 GMT  
		Size: 3.3 MB (3276870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca818d1487d74f4b1a822c9a76defdb809cf4a48d8c9366729eb377b47c37eba`  
		Last Modified: Sat, 08 Nov 2025 21:33:04 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:cbb1647b21e602d4761478e943f32f96c463d4104ec8eedc0cedec2506f507e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223094448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b17914ca2cc65b75b591e8394ec62538f9e3986895ec3360eaf2da818d6091`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:46:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Oct 2025 00:46:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 00:46:30 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 31 Oct 2025 00:48:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 31 Oct 2025 00:48:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 08 Nov 2025 22:30:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:30:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 22:30:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:30:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:30:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 22:30:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 22:30:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 22:30:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 22:30:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 22:30:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 22:30:53 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 22:30:53 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 22:30:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 22:30:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 22:30:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2c2c5b1d0021029ccc4064df99950687160117bc008ac4bce5618b2dd9154`  
		Last Modified: Fri, 31 Oct 2025 00:47:22 GMT  
		Size: 1.5 MB (1536224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81f58f0a0c63dcb89d788cdb4cb2f68180856d6a496930378a62e02c7df9e68`  
		Last Modified: Fri, 31 Oct 2025 02:17:38 GMT  
		Size: 173.9 MB (173942708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03153a24467c4d7c753c86aab43a78a30fe903393900050d190c5f78c3942322`  
		Last Modified: Sat, 08 Nov 2025 22:31:30 GMT  
		Size: 3.9 MB (3925116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72db299afabe7d189d77dbf6515c25ed3dbb0ad2f5b6b0761ad5f4bb47b897df`  
		Last Modified: Sat, 08 Nov 2025 22:31:30 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05f9ffa036a5ba137c7b6d745a78a5ca6f0c721cac657f1df7cb5e2f07d617a`  
		Last Modified: Sat, 08 Nov 2025 22:31:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1856e5478b1adfc62eabb998eacbd95801c293e30e64870913a6c2663dd032cd`  
		Last Modified: Sat, 08 Nov 2025 22:31:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:62c48c77814a70919c4b8e5636708b129f9c7843a7ae89c3ea529785514fc31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8cb04f190bb06db626f1d1a84888c77586ce5b2c2fb03c194c896ca501fa0`

```dockerfile
```

-	Layers:
	-	`sha256:b7cfecfda4b7182cc3b06c04c95c24f342e430f4bb96419a85b2892851d7e630`  
		Last Modified: Sun, 09 Nov 2025 00:29:09 GMT  
		Size: 3.3 MB (3262981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac48f73eaa12fedb605a9eb4b2cb91f808ab29c6b64b2ac28a7d43e651c30a91`  
		Last Modified: Sun, 09 Nov 2025 00:29:10 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:c113a995b2ce218c4dd7498250860c8bcd89fdc9f8c78b39b745661136464973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205059604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0328c47b3901ffdf145b4fde21f69b8a22fae6d1c0e2f753e485a4ad1c09e914`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 22:32:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 22:32:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:32:22 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 22:37:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dab5d799a225e64f6ae3979e701f52ad6add23d80aa3c4d1325759cc944f3ffd';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85ff4b0e689b46e2e76e27b40a019072872afa7ef79901ebd84c2d5975d3c218';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='e53d487be3ea6fbe6c4eb5a40050642a92894c5056aa24e142b3ace848076163';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 22:37:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 08 Nov 2025 21:08:19 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:08:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 21:08:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:08:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:08:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 21:08:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 21:08:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 21:08:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 21:08:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 21:08:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 21:08:20 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 21:08:20 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 21:08:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 21:08:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 21:08:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a741b67c0dbf6d2e66e6ffe23e30ec9031bce057ebe9e2cb812bbb79480aa2d`  
		Last Modified: Thu, 30 Oct 2025 22:33:02 GMT  
		Size: 1.5 MB (1455880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87264c6379c67bfaa8d13c8c061c27a900beba7c0aa4f4e67e14894e9502ac2`  
		Last Modified: Fri, 31 Oct 2025 02:17:52 GMT  
		Size: 163.3 MB (163302980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e7e57372a71bfe54072621317bfaa0dbba9bcaa87f38bc0399aca5536d602f`  
		Last Modified: Sat, 08 Nov 2025 21:08:47 GMT  
		Size: 3.1 MB (3053722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90982c912e8ccda8cd6cb4e2ce5f4b5ce274b0be7cad3b83b4a5840836ec36e8`  
		Last Modified: Sat, 08 Nov 2025 21:08:47 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8892e7e38d6344f8b72cc711af377ad5aedabd6a175ca77d6175c83bb159fd71`  
		Last Modified: Sat, 08 Nov 2025 21:08:46 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caecd42913abf8bd2fe601297edd29f2849fc3f034b41822d22a753c7effdf2f`  
		Last Modified: Sat, 08 Nov 2025 21:08:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:5df0d92eedf897534d3571d940657e98a40a0c9a753d8509bbc8456030e3e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21890918f17b52fe0aedc20181225329e55a5f50797bc9b8658112010c5a276a`

```dockerfile
```

-	Layers:
	-	`sha256:8e7b0c8fb3956cdcf50cbcf85c7dd4dc1cda83c95d91e2c221a171e613fb760b`  
		Last Modified: Sun, 09 Nov 2025 00:29:14 GMT  
		Size: 3.0 MB (2950170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6546dc195695bc189b2566b2ed778737af47285b5585cab85e1e2e816f555dfb`  
		Last Modified: Sun, 09 Nov 2025 00:29:15 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json
