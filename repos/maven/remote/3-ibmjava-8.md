## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:c5a4f7bfe26cf7253a3edfe465de16af23c99d432bfe32b187396903d53d37a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibmjava-8` - linux; amd64

```console
$ docker pull maven@sha256:be9642d3cb64da4d1bb624e719b3f861b29f8d5d342122313a3f75aea9f84297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237159873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577c28adae06b9d34d76db53758ce6ada901b4d70e9859dfe36b0bdd742d264f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 02:52:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 07 Jun 2022 02:52:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 29 Jun 2022 18:19:40 GMT
ENV JAVA_VERSION=8.0.7.11
# Wed, 29 Jun 2022 18:23:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a5a580ae482fc1413feae44da07fe68acfbc9aafc911a781480e1752e3b4b94';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='565caead453b1b6ecec9a393cd298d407a2c07737e70db27b187cf4b4a7c1a62';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d982a09d55481738f9e2fea9375ad55a72eb6a5069a5142cd2cb99b6db836ad3';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='0bab09c4fa8cafb2cb53444ab4c7649f2ba51691e76571de953235cbeaa45137';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1795165f444421e63d8d6f6f4704c89368cf283c4984b00e29f152d823e2bf3c';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 29 Jun 2022 18:23:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 29 Jun 2022 18:43:40 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 29 Jun 2022 18:43:40 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 29 Jun 2022 18:43:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 Jun 2022 18:43:41 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 29 Jun 2022 18:43:41 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 29 Jun 2022 18:43:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 29 Jun 2022 18:43:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 Jun 2022 18:43:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 Jun 2022 18:43:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 29 Jun 2022 18:43:45 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 29 Jun 2022 18:43:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 Jun 2022 18:43:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc337ae35500f1356b4927d94eff4c5c2013592d9465313f05b0e829b69baf`  
		Last Modified: Tue, 07 Jun 2022 02:54:56 GMT  
		Size: 3.0 MB (2960220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e99de371ee7815a742532c800a087c3970169e2a1a6954c514be36dd0d760a`  
		Last Modified: Wed, 29 Jun 2022 18:24:12 GMT  
		Size: 166.3 MB (166253065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbde17c7fb0d3582c04c0399376a3f294d3e2d2f516fe40e5cbb39903dbf59b`  
		Last Modified: Wed, 29 Jun 2022 18:46:00 GMT  
		Size: 32.5 MB (32494243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bfd6d966ea6ef102b9eb94f2f5a18c59ebabebde3ce4d2f94fc4e71f8b61ea`  
		Last Modified: Wed, 29 Jun 2022 18:45:57 GMT  
		Size: 8.7 MB (8739505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8049a8d30296fe611b24a33a1b3db7b5652c5a901ec62f234b37ec7bca5138`  
		Last Modified: Wed, 29 Jun 2022 18:45:57 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe534ba47196031588f567aa9a2ce8f12a8c0d598400dec49023225076cc39d4`  
		Last Modified: Wed, 29 Jun 2022 18:45:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; 386

```console
$ docker pull maven@sha256:f2fc3292d7c61f705aa840858ca59bde56a0016fcfa9efe7bbaaf9a29d4ac16e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221319989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09d44adaa0c06b9f02b73aeeacaa70bf6cb1b49be437e8cd6c89b31cd6b8439`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:23:28 GMT
ENV JAVA_VERSION=8.0.7.11
# Tue, 02 Aug 2022 16:26:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a5a580ae482fc1413feae44da07fe68acfbc9aafc911a781480e1752e3b4b94';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='565caead453b1b6ecec9a393cd298d407a2c07737e70db27b187cf4b4a7c1a62';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d982a09d55481738f9e2fea9375ad55a72eb6a5069a5142cd2cb99b6db836ad3';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='0bab09c4fa8cafb2cb53444ab4c7649f2ba51691e76571de953235cbeaa45137';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1795165f444421e63d8d6f6f4704c89368cf283c4984b00e29f152d823e2bf3c';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 02 Aug 2022 16:26:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 02 Aug 2022 22:43:05 GMT
RUN apt-get update && apt-get install -y curl
# Tue, 02 Aug 2022 22:43:05 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 02 Aug 2022 22:43:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Aug 2022 22:43:07 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 02 Aug 2022 22:43:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 02 Aug 2022 22:43:16 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 02 Aug 2022 22:43:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Aug 2022 22:43:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Aug 2022 22:43:20 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 02 Aug 2022 22:43:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 02 Aug 2022 22:43:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Aug 2022 22:43:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b94ea674a65dbc89f3785f80ee02e2df7da6d3bec5eb25f6a994ec9b0db5259`  
		Last Modified: Tue, 02 Aug 2022 16:28:16 GMT  
		Size: 154.4 MB (154359005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1668ca6caf761cfdbd0f312bbccbc9bf93f16b860633fe82778579f0571b28b`  
		Last Modified: Tue, 02 Aug 2022 22:43:51 GMT  
		Size: 28.1 MB (28072754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4396c08b57020c7901851af34111f7965715f7758d5b856210e2d0251e23ae87`  
		Last Modified: Tue, 02 Aug 2022 22:43:48 GMT  
		Size: 8.7 MB (8739464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a9cda4b32b23d007c5f80a5a907b7502c0d6b3f87636df30be67edc943fed`  
		Last Modified: Tue, 02 Aug 2022 22:43:46 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84701d52ad9102c6ca654983e2fec12926da65270645b756bf45d4b69da8ac6`  
		Last Modified: Tue, 02 Aug 2022 22:43:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:36a26080f43917873a83ea01ae64afddac5962e6ac9cc4bb193276450fdf83fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233593884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f25855318e3cd7bac27372d4de72cb009653c725a5b531b689518afa8b895e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 08:49:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 07 Jun 2022 08:50:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 29 Jun 2022 18:31:53 GMT
ENV JAVA_VERSION=8.0.7.11
# Wed, 29 Jun 2022 18:36:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a5a580ae482fc1413feae44da07fe68acfbc9aafc911a781480e1752e3b4b94';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='565caead453b1b6ecec9a393cd298d407a2c07737e70db27b187cf4b4a7c1a62';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d982a09d55481738f9e2fea9375ad55a72eb6a5069a5142cd2cb99b6db836ad3';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='0bab09c4fa8cafb2cb53444ab4c7649f2ba51691e76571de953235cbeaa45137';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1795165f444421e63d8d6f6f4704c89368cf283c4984b00e29f152d823e2bf3c';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 29 Jun 2022 18:37:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 28 Jul 2022 07:31:21 GMT
RUN apt-get update && apt-get install -y curl
# Thu, 28 Jul 2022 07:31:22 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 28 Jul 2022 07:31:22 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Jul 2022 07:31:23 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 28 Jul 2022 07:31:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 28 Jul 2022 07:31:25 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 28 Jul 2022 07:31:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Jul 2022 07:31:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Jul 2022 07:31:26 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 28 Jul 2022 07:31:26 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 28 Jul 2022 07:31:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Jul 2022 07:31:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4a22aedc3b9f2593635b0a3f6fe64e6dd424850b9782f66e88c8c162926d6a`  
		Last Modified: Tue, 07 Jun 2022 08:54:16 GMT  
		Size: 3.1 MB (3082521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e192784dd2d0abe2db534ba604bc6b3de4a82a416cab016ea579429f30e8da2f`  
		Last Modified: Wed, 29 Jun 2022 18:38:58 GMT  
		Size: 165.9 MB (165909750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d739e426a69d7ec31e7479fcc82e4c47606deada44c7a1baef3fd958adc817`  
		Last Modified: Thu, 28 Jul 2022 07:37:34 GMT  
		Size: 25.4 MB (25418063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad7e78a48c08ac5eb48b1b7de5a3a982ef18a21c3b3bc6ec735b5a9db0cc000`  
		Last Modified: Thu, 28 Jul 2022 07:37:31 GMT  
		Size: 8.7 MB (8739479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40bd36c6c585f3bf67cfef66da65cb5e3e096e8d780e8b1baac773b6abfb46c`  
		Last Modified: Thu, 28 Jul 2022 07:37:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed00a0165ee430388596365819319871c579221253e036c8f5d49cfd5fc8c149`  
		Last Modified: Thu, 28 Jul 2022 07:37:29 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:0cb7cbab033ba4aa7622ebf67e375b605b0e4649570f592d4d678bf68daed9a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216613816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dac2ed8dea72f34ec653bf2a81577353a2192b892e0c5fc5c71b08847a11854`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:19:25 GMT
ENV JAVA_VERSION=8.0.7.11
# Tue, 02 Aug 2022 13:22:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a5a580ae482fc1413feae44da07fe68acfbc9aafc911a781480e1752e3b4b94';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='565caead453b1b6ecec9a393cd298d407a2c07737e70db27b187cf4b4a7c1a62';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d982a09d55481738f9e2fea9375ad55a72eb6a5069a5142cd2cb99b6db836ad3';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='0bab09c4fa8cafb2cb53444ab4c7649f2ba51691e76571de953235cbeaa45137';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1795165f444421e63d8d6f6f4704c89368cf283c4984b00e29f152d823e2bf3c';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 02 Aug 2022 13:22:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 03 Aug 2022 00:01:10 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 03 Aug 2022 00:01:12 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 03 Aug 2022 00:01:13 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Aug 2022 00:01:14 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 03 Aug 2022 00:01:15 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 03 Aug 2022 00:01:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 03 Aug 2022 00:01:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Aug 2022 00:01:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Aug 2022 00:01:31 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 03 Aug 2022 00:01:32 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 03 Aug 2022 00:01:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Aug 2022 00:01:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfef873240c8f213f8f5a7c6d6f8e9cbd199b8b4930bb4763c4784dec90a87a3`  
		Last Modified: Tue, 02 Aug 2022 13:23:26 GMT  
		Size: 156.4 MB (156437369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eababc8c7c81e20c686147ea76b329aa1241aea64cdbc651f4bf66b21854053`  
		Last Modified: Wed, 03 Aug 2022 00:07:12 GMT  
		Size: 23.4 MB (23394454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf81eccc910d35f336f1e02f1d6a250a4f993d1d37da878cb043600a0ed1aa0`  
		Last Modified: Wed, 03 Aug 2022 00:07:10 GMT  
		Size: 8.7 MB (8739490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3f8b7aaf22ecf6cf504bbc72c3aadc18f95e4f3b2d50d5b7e9656aef722541`  
		Last Modified: Wed, 03 Aug 2022 00:07:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5176559d6699f79b36269d3ccbc3ebea74f8d924e93366f1f600a5960315990`  
		Last Modified: Wed, 03 Aug 2022 00:07:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
