## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:0355d8376375216ea245aba2f9e281693ce6d06ebd2f1de9ba51b82bd30b21c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibmjava-8` - linux; amd64

```console
$ docker pull maven@sha256:c9da9a28e3268eeaae092f7797cf5ba924446724dd63b7d501da5749d5d55db6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234861779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4b89269ff36b46fb6735deba4ad589806b0e0aa2ad907c0ccdac3b29b8ad0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:22:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 26 Jul 2021 23:23:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Aug 2021 17:20:00 GMT
ENV JAVA_VERSION=8.0.6.35
# Fri, 13 Aug 2021 17:23:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7dfc22f7c3ba656e33af1728d2f87e854cfc2616f153b3c8310a9d3ed89cd484';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='2c1363167aa22f6b20f7c5d5a10bef06563a8405835b9e894eaf2fc2c966eca0';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f8a837860f8a3142c95b78eb1d9cf36bcb4c633ebde3293dca453ab2cdbd0dc2';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='421e69d2307c0c8ab0f75fc0a32332f083286f46d4c4ac1742aaf12d7ae0dd99';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='0dd9fbfe0aa12167d1ad6a482ba1493058440d379bcd0c7d1a18d3b44bcecca5';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Aug 2021 17:23:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Aug 2021 17:58:34 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 13 Aug 2021 17:58:35 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Aug 2021 17:58:35 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 13 Aug 2021 17:58:35 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 13 Aug 2021 17:59:01 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Aug 2021 17:59:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Aug 2021 17:59:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Aug 2021 17:59:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Aug 2021 17:59:01 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 13 Aug 2021 17:59:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcc8b59a59a15868e1ba8f0176e149949b7fa1f2c69f90ad72eb7270fdc65f7`  
		Last Modified: Mon, 26 Jul 2021 23:26:50 GMT  
		Size: 3.0 MB (2958819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0374f1d5f6233b9fb95ad96e7bb99ee0c7ae1c2b461cd128654daeb782bbadcf`  
		Last Modified: Fri, 13 Aug 2021 17:25:42 GMT  
		Size: 165.6 MB (165624558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd30c15e497a5c2e14165c4acf9d41841b4e37c9756e878472f36dff860eb513`  
		Last Modified: Fri, 13 Aug 2021 18:01:41 GMT  
		Size: 39.6 MB (39568149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dce2c2134cfe453abb65cc136aea2f4377fbe018903c0b5cbebb86fc4e2f75`  
		Last Modified: Fri, 13 Aug 2021 18:01:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd4845367906e73646e98f74eafc29b07de673a8ac0ae16a15c582c7d8f1a03`  
		Last Modified: Fri, 13 Aug 2021 18:01:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; 386

```console
$ docker pull maven@sha256:ecf60e78c7c8b62e15d57866f6ad7601d99c2105ce3a706a83a02af55278c5ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221068851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44bc7b8de15186cb07a34157c34ae4dc7c48b9b306f818f5a887d2832cc6a7a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 26 Jul 2021 21:18:53 GMT
ADD file:45b15f7ce91c2c05cc5e273dee6b36fade4217c3da1d407a6dc8e108f50e2b66 in / 
# Mon, 26 Jul 2021 21:18:53 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:51:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 26 Jul 2021 21:51:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Aug 2021 17:38:56 GMT
ENV JAVA_VERSION=8.0.6.35
# Fri, 13 Aug 2021 17:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7dfc22f7c3ba656e33af1728d2f87e854cfc2616f153b3c8310a9d3ed89cd484';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='2c1363167aa22f6b20f7c5d5a10bef06563a8405835b9e894eaf2fc2c966eca0';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f8a837860f8a3142c95b78eb1d9cf36bcb4c633ebde3293dca453ab2cdbd0dc2';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='421e69d2307c0c8ab0f75fc0a32332f083286f46d4c4ac1742aaf12d7ae0dd99';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='0dd9fbfe0aa12167d1ad6a482ba1493058440d379bcd0c7d1a18d3b44bcecca5';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Aug 2021 17:41:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Aug 2021 17:57:58 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 13 Aug 2021 17:57:59 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Aug 2021 17:57:59 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 13 Aug 2021 17:57:59 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 13 Aug 2021 17:58:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Aug 2021 17:58:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Aug 2021 17:58:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Aug 2021 17:58:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Aug 2021 17:58:24 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 13 Aug 2021 17:58:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Aug 2021 17:58:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bc0a67b78038e09ba1732c1a7c63e6c8e924aca7029364acd54d64dd669b151f`  
		Last Modified: Mon, 26 Jul 2021 21:19:48 GMT  
		Size: 27.2 MB (27162925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e868994170abe61785da91631677200dcc7cec9fc1feeb71f3c5aaa31d6cf`  
		Last Modified: Mon, 26 Jul 2021 21:54:40 GMT  
		Size: 3.0 MB (2988058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ddce3cc7da01f2e4024c23637f51df9816a8461a5836890a1a357d4dcc29e7`  
		Last Modified: Fri, 13 Aug 2021 17:42:36 GMT  
		Size: 153.8 MB (153762766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62663b359e1a25e10fed63f1f0471d8f3a85e018cac1901ec54a766792b1b384`  
		Last Modified: Fri, 13 Aug 2021 17:58:55 GMT  
		Size: 37.2 MB (37153889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a47818d08c2a814597befa5dc763eee3ad51dddc40e0106fd579636dc734b78`  
		Last Modified: Fri, 13 Aug 2021 17:58:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce3cabf587ed9ecb8c11c45942a163d8ab1c0b2bb85ee22eaa68a76ec7c143f`  
		Last Modified: Fri, 13 Aug 2021 17:58:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:8af08b61b832f4b43824f8a93576c1141883f22661dbea08171793e6c9556008
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233286589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8459856ed9326f1249c006b64d1bee7405f4c6004920ab60eadd9a1fd04ad712`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 27 Jul 2021 01:56:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Aug 2021 17:16:48 GMT
ENV JAVA_VERSION=8.0.6.35
# Fri, 13 Aug 2021 17:20:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7dfc22f7c3ba656e33af1728d2f87e854cfc2616f153b3c8310a9d3ed89cd484';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='2c1363167aa22f6b20f7c5d5a10bef06563a8405835b9e894eaf2fc2c966eca0';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f8a837860f8a3142c95b78eb1d9cf36bcb4c633ebde3293dca453ab2cdbd0dc2';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='421e69d2307c0c8ab0f75fc0a32332f083286f46d4c4ac1742aaf12d7ae0dd99';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='0dd9fbfe0aa12167d1ad6a482ba1493058440d379bcd0c7d1a18d3b44bcecca5';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Aug 2021 17:20:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Aug 2021 18:07:37 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 13 Aug 2021 18:07:40 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Aug 2021 18:07:43 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 13 Aug 2021 18:07:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 13 Aug 2021 18:08:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Aug 2021 18:08:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Aug 2021 18:08:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Aug 2021 18:08:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Aug 2021 18:08:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 13 Aug 2021 18:08:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Aug 2021 18:08:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274a7ceecd631ec4df912a3b0382831ab0f4d2796b455732587f4678f12dc8d8`  
		Last Modified: Tue, 27 Jul 2021 02:03:19 GMT  
		Size: 3.1 MB (3083057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59db1bc347dc1c514aa697f4458ad7bbc9a6937ffde23bc2510f3ce26b137d45`  
		Last Modified: Fri, 13 Aug 2021 17:22:23 GMT  
		Size: 165.2 MB (165225235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688c88ec779ec4b61a10d03416c5f558d7f4543015a1c8c872ac3c5b5a2c66c3`  
		Last Modified: Fri, 13 Aug 2021 18:10:58 GMT  
		Size: 34.5 MB (34539125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063726f2ba1f0bc32c01e314b676579c7413da782493ab5d604ce95561b61aff`  
		Last Modified: Fri, 13 Aug 2021 18:10:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af01e17208614bd67fb2403b23e26aa6d152976f5dad1dd09cecba5ee6f80e4`  
		Last Modified: Fri, 13 Aug 2021 18:10:54 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:9359fe9839932a5fa8d4a1a105eb678aa1faf349061b1c8e43b3371b486e6833
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216346859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1302604fe53cf26276b93771e2505838bfdaaa24ecaf5acc92c4bbbb5fc7e291`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:03 GMT
ADD file:edb1df135699bb6ca591e6493c0df55d2030d8990c3e0a3afa80442036f92e16 in / 
# Mon, 26 Jul 2021 20:55:05 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 21:13:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 26 Jul 2021 21:13:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Aug 2021 17:41:46 GMT
ENV JAVA_VERSION=8.0.6.35
# Fri, 13 Aug 2021 17:45:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7dfc22f7c3ba656e33af1728d2f87e854cfc2616f153b3c8310a9d3ed89cd484';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='2c1363167aa22f6b20f7c5d5a10bef06563a8405835b9e894eaf2fc2c966eca0';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f8a837860f8a3142c95b78eb1d9cf36bcb4c633ebde3293dca453ab2cdbd0dc2';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='421e69d2307c0c8ab0f75fc0a32332f083286f46d4c4ac1742aaf12d7ae0dd99';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='0dd9fbfe0aa12167d1ad6a482ba1493058440d379bcd0c7d1a18d3b44bcecca5';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Aug 2021 17:45:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Aug 2021 18:29:45 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 13 Aug 2021 18:29:46 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Aug 2021 18:29:46 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 13 Aug 2021 18:29:47 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 13 Aug 2021 18:30:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Aug 2021 18:30:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Aug 2021 18:30:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Aug 2021 18:30:17 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Aug 2021 18:30:18 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 13 Aug 2021 18:30:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Aug 2021 18:30:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cb0153f85b121ce88ea3f3bebbb54c31f8547bed022bd201416974cd40c61f59`  
		Last Modified: Mon, 26 Jul 2021 20:56:50 GMT  
		Size: 25.4 MB (25367016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beff8b50da678c028627d9aa04a27cce09ff57f8baf2b9c79420f9f2e076484`  
		Last Modified: Mon, 26 Jul 2021 21:17:51 GMT  
		Size: 2.7 MB (2676858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddcd70367bff0f8365074de2f2a0345a632ea67ad5908a82e798cd797b1026e`  
		Last Modified: Fri, 13 Aug 2021 17:47:45 GMT  
		Size: 155.7 MB (155741941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260c0ab5df69cd7f66c6b29f86cf69e71edeb1d948394f616dd1ddb6e27cf87`  
		Last Modified: Fri, 13 Aug 2021 18:33:00 GMT  
		Size: 32.6 MB (32559828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ef6845cc8bb427ae150ff4f1de0a61a50874fa657d23fbe6d232e23e8cc6`  
		Last Modified: Fri, 13 Aug 2021 18:32:57 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fef7e9c023276ff1bb4ee39c30ff60bac4e96def52df5685549703aaaf0b2b`  
		Last Modified: Fri, 13 Aug 2021 18:32:57 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
