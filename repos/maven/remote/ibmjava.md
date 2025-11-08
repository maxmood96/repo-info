## `maven:ibmjava`

```console
$ docker pull maven@sha256:8ea3f1be210e842f7c64927d685d8e27c5a25e3c35898222f1b2e226c10c5dd9
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
$ docker pull maven@sha256:31d5569d7b6b157e903ae2216619b476ab9d49a0ea8e07a46dc9ee7afc54f350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223094491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b100ffabc023e8e9a077dc6cc0ca2011662d06048738a94728a55a94ca9ada3a`
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
# Fri, 31 Oct 2025 01:14:20 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 01:14:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:21 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:21 GMT
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
	-	`sha256:1af2d52b98aed52d152adcb6b8952c708ca1474fdf121336f2832a7c105667e9`  
		Last Modified: Fri, 31 Oct 2025 01:14:45 GMT  
		Size: 3.9 MB (3925146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fe84fcc650652bc7b63ff62900f2be1d3d8737785ac4903bde373766ab7a73`  
		Last Modified: Fri, 31 Oct 2025 01:14:46 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87cd03ccf4dd069bd4130d7cc00b45c63dfeaa0f1823f7c8e88403b6dfbe998`  
		Last Modified: Fri, 31 Oct 2025 01:14:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821fac7d2b55dc8278aba954eff4d1145efb7dcdb7e66208a49a074b539d49a3`  
		Last Modified: Fri, 31 Oct 2025 01:14:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:b16f8ecdd8b4642212b78d9f5e6f5a05eeb9c9fa0238bbc84ae22f90087c9ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b691621c5eba09194460137e409a94db2e5c48b9c553e3e887746feab388d7`

```dockerfile
```

-	Layers:
	-	`sha256:5c02787a0e4fe9d86496b92192e9504abe90cb963351658bf3bd236b8f93bc4f`  
		Last Modified: Fri, 31 Oct 2025 02:29:24 GMT  
		Size: 3.3 MB (3262981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdcf3d9e3cafe2ccec3159084df6fbd12ae7d3d64b9ea5516342e3c63a2aeea`  
		Last Modified: Fri, 31 Oct 2025 02:29:25 GMT  
		Size: 18.9 KB (18852 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:b4ef19c54fb3bc5558f087cda987a6a4ac6e59f399e35da617afc828b3da3b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205059803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1081caad03bb106f90d1e882313d606524e283eb81befb5de8eba8bb0e6996a5`
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
# Thu, 30 Oct 2025 23:39:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 23:39:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 30 Oct 2025 23:39:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 30 Oct 2025 23:39:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 30 Oct 2025 23:39:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 30 Oct 2025 23:39:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 30 Oct 2025 23:39:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 30 Oct 2025 23:39:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:39:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 30 Oct 2025 23:39:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 30 Oct 2025 23:39:35 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 30 Oct 2025 23:39:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 30 Oct 2025 23:39:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 30 Oct 2025 23:39:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 30 Oct 2025 23:39:35 GMT
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
	-	`sha256:060c25e4a058a462caecf126b69027957598d8ee54ad0a363427ca5febc8224d`  
		Last Modified: Thu, 30 Oct 2025 23:40:20 GMT  
		Size: 3.1 MB (3053904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6026207dc78f39970634d124503cbb6f4993fe334e50ff3c2cacc61ffae11c`  
		Last Modified: Thu, 30 Oct 2025 23:40:22 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb458220c0c2666cb4fd8a1f95a1040a4ce43e11ba97b16a280cb0eed071492`  
		Last Modified: Thu, 30 Oct 2025 23:40:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58998c2d2dcd7aa6b38d608ee7ab3c21f26ab708fe1248bd913d3d12dcac3ea3`  
		Last Modified: Thu, 30 Oct 2025 23:40:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:e518ec458ee07d4b83d34472623eb617e99340ebff51aa64ba2ce063866df749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84fcb257c3c2d89a98c4835960910070ae6f437f09a42bb74348b8496fc697f`

```dockerfile
```

-	Layers:
	-	`sha256:d11a03583621fc25eb8d6318b2521b2ea6231e493381215cb8790af7463407f0`  
		Last Modified: Fri, 31 Oct 2025 02:29:28 GMT  
		Size: 3.0 MB (2950170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0eaf344881a320674c12532aac2ef2c7493201da494f5e2284c9136e796f07d`  
		Last Modified: Fri, 31 Oct 2025 02:29:29 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json
