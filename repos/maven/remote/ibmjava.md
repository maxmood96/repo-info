## `maven:ibmjava`

```console
$ docker pull maven@sha256:05e7873ee92ab1de09eee9ceae94acc5c4be799a0edf085761feebb3f8416df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:ffe7e6ca75cd9c8edbb4964212c79a86b83f0d4fc0e14ac8bdb3cd2600124fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215278611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc01aae98005c23fd760a2fa0286ce4aa09469b8d114e68fcc621334ca70a1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:28:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 04:29:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Mar 2024 19:52:50 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 19 Mar 2024 19:53:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7055a291305403c09d9248ba93ba748db390c38de46b38bc4153c1f07731cb75';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2aad67a7340e93c4830e04901191d41082329a9390d40ecded124458f6990b95';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a6e64697f4d1524444eee27eceaa6d8ce0e26879f8a656148c31661a75f67b4b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='53816ed6e12f44a7466c0e06a2ea9fbee363574febe3747ec612166a0676da1b';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 19 Mar 2024 19:53:31 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 11 Dec 2023 11:12:11 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba89721884a18e231a2358fec4f8d2aa4e12399d5170f30d637f3cc1e9edc12`  
		Last Modified: Wed, 06 Mar 2024 04:30:07 GMT  
		Size: 1.5 MB (1469281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ebde281b5130ddba8112c1ef2aa19d288314fcbe8c24044d0fe50934e26023`  
		Last Modified: Tue, 19 Mar 2024 19:54:27 GMT  
		Size: 172.2 MB (172179929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd1fabf808caee2000c2467e6a7b569651d2afb43dfe8859043743d8d4658c7`  
		Last Modified: Tue, 19 Mar 2024 20:16:39 GMT  
		Size: 1.7 MB (1696783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58e3399cc5d4a9ac2f74645a0b3a1e5efe7b7f9ecf9922bedef2014d553f0c4`  
		Last Modified: Tue, 19 Mar 2024 20:16:40 GMT  
		Size: 9.5 MB (9479940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884dcbf3264eb963226193dc3d3fa1c34190c15e6c0b944b6f00feb2b1e4b5cb`  
		Last Modified: Tue, 19 Mar 2024 20:16:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d456eb90b5281ce12856fea50621ebcb8c339a08af66a82523fc683a96182f37`  
		Last Modified: Tue, 19 Mar 2024 20:16:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92562edccb88f07c110931a0896dfa27b83ebf4db30737b7e0c53537606535d`  
		Last Modified: Tue, 19 Mar 2024 20:16:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:4e83ef250e0d5066cb84cf94c4e236baa1d5f1ca3672f2bda55242b21c11af47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221482616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f3f89db1a9c28d88b50003bb3d13ef90d776a8f17e431a71e104e9c6f38302`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:50:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 01:50:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Mar 2024 19:25:39 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 19 Mar 2024 19:26:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7055a291305403c09d9248ba93ba748db390c38de46b38bc4153c1f07731cb75';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2aad67a7340e93c4830e04901191d41082329a9390d40ecded124458f6990b95';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a6e64697f4d1524444eee27eceaa6d8ce0e26879f8a656148c31661a75f67b4b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='53816ed6e12f44a7466c0e06a2ea9fbee363574febe3747ec612166a0676da1b';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 19 Mar 2024 19:26:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 11 Dec 2023 11:12:11 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140a853d05db5896b4301801c8f248e4544bc9cbe992489bc58fdbf0a2147cf8`  
		Last Modified: Wed, 06 Mar 2024 01:51:25 GMT  
		Size: 1.6 MB (1574416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d677810f9418ca8f987721efdbe6984eaeea93ce037137c1f42db0d6276ea5d4`  
		Last Modified: Tue, 19 Mar 2024 19:27:32 GMT  
		Size: 172.8 MB (172756367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb41390c84807e965e82f979e0cb202d7c4163b84b7e82066ad29d59d4c37cd`  
		Last Modified: Tue, 19 Mar 2024 20:24:45 GMT  
		Size: 2.0 MB (2047782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ce9766f10c607d925e592c6b7f635a09d290db16d8d85855da368a8ddeaa7`  
		Last Modified: Tue, 19 Mar 2024 20:24:45 GMT  
		Size: 9.5 MB (9479937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e9ba79f2bc3c45bdec9d838f09350b06148160b53ddc9782969667f613757`  
		Last Modified: Tue, 19 Mar 2024 20:24:44 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e761a46c2c55533a404921ca6b6a0292dd5a95bc7e3f46a4b5360142a7099d69`  
		Last Modified: Tue, 19 Mar 2024 20:24:44 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b82287687a4be6d9874fce4e9c733af2643bf7d8e27d63b7bd235d398015e96`  
		Last Modified: Tue, 19 Mar 2024 20:24:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:e8fd74ebe220f20f002ed1b5aab2faa367058ff3177a0666e46e93cd603e957a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203514650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a75fea836e6900da2aa13db26dd13116a910ac861ec537bb3125b8ace56574`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:53:10 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 04:53:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:53:17 GMT
ENV JAVA_VERSION=8.0.8.20
# Wed, 06 Mar 2024 04:55:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1f62bdb0a919da6b5a8db56d6dc6df4c019e7d099df59ea6b35df4b3e7b21ab';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eb3b880f1b6a19bd418b9e8cefefc13455c9e205f17c78a0169b0d376d1e594e';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='645eac2657371e4cb55e437a5835e80a29be66e64603698a4db0c8c92558c753';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='bebd9e9f5334339a32b69e1293368afee2c606ec01dcafeccb3a18c5667236bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 06 Mar 2024 04:55:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 11 Dec 2023 11:12:11 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bdb96287595f0898b0f731954aac1bc39f56c6377e3b5474bfd5d2f48b5c8`  
		Last Modified: Wed, 06 Mar 2024 04:57:08 GMT  
		Size: 1.5 MB (1477377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd86019c1fba7566660567c2373ccef50e11cd40033c667a199e68a7a06b31`  
		Last Modified: Wed, 06 Mar 2024 04:57:47 GMT  
		Size: 162.2 MB (162227327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c82ee33a600af50dafdc38caaded42935c0e0becddb4ea204a7550ee208a4e`  
		Last Modified: Wed, 06 Mar 2024 08:11:49 GMT  
		Size: 1.7 MB (1691872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a866b4c47ecc39fccdd3f547712b3b9898177d327705539975c454b605b3504`  
		Last Modified: Wed, 06 Mar 2024 08:11:49 GMT  
		Size: 9.5 MB (9479946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a58f569e5ba018c72908021e2c4a627a319969fa75ba1d7407652ad377c207e`  
		Last Modified: Wed, 06 Mar 2024 08:11:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227eeeab82b1ba5c89cca4bbd651f6a57b159a924153e66ee12ee5105149eb27`  
		Last Modified: Wed, 06 Mar 2024 08:11:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faba30fc38bd5f5e36876e5910038135b21e4b32c560aa55b5ed60a677a07699`  
		Last Modified: Wed, 06 Mar 2024 08:11:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
