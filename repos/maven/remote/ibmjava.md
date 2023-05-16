## `maven:ibmjava`

```console
$ docker pull maven@sha256:186786cbf7dbcc20b36091554d1364fb55475a3869100cfb6adf5d1704f3630d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:4ed2909f7c8ed6dc022d3b1e36c513696ee19cdabead3e1f11c73f70c9edae02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213681364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a9da484436ce1e5330e660ae125f9af5281ad5789a72c28d112544f932fbd8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:44:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 07:44:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:44:59 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 07:48:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 07:48:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 04 May 2023 07:48:01 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 07:48:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 07:48:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 07:48:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 07:48:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 07:48:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 07:48:01 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 07:48:01 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 07:48:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 07:48:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 07:48:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee7fd4007af244555d448c1fb80ceb220cf70203647e0705bbdd49468c13e4`  
		Last Modified: Thu, 04 May 2023 07:48:21 GMT  
		Size: 1.4 MB (1446362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a8698c9f3c3a60151b75fb922983305f67034c4e13a4cb705f014ff62dd81a`  
		Last Modified: Thu, 04 May 2023 07:49:07 GMT  
		Size: 171.0 MB (171003150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72684705a4a18624f80f74e640c589e10ff55d23d333bdde428b69c1373ec624`  
		Last Modified: Thu, 04 May 2023 14:44:40 GMT  
		Size: 1.7 MB (1694098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b904e6bc20c9343bf0b8409f8efb27bd35a22f15572d229bad85bf5b35a00`  
		Last Modified: Thu, 04 May 2023 14:44:40 GMT  
		Size: 9.1 MB (9106166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df1800613a03d418c8fdd729c3d9badd087a6e88b3da5ae0ad0e3630b6a380d`  
		Last Modified: Thu, 04 May 2023 14:44:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ceafe4871d417d68b8b5b5118a610e487719117b356fb2c949af8e2b0bd189`  
		Last Modified: Thu, 04 May 2023 14:44:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee188ae775c8132f60b58b0f14a0f0750a427a7a53d92dd2b3155d369694bc86`  
		Last Modified: Thu, 04 May 2023 14:44:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:5285abe773e043164a0e9d73c121f1afa5a344354377d1ae587743aa3733edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219475421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b06c990f04ac96f0a588bf54596d5ab4dcb6961f2e8fdf0bb7d11fb1093fae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 14:09:46 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 14:09:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 14:09:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 14:18:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 14:18:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f6a63d8cd043e76933823b18cbb7057a55bb4d66d64639c81e15a4700c101582`  
		Last Modified: Wed, 03 May 2023 17:09:07 GMT  
		Size: 35.7 MB (35712706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f8e1caab24446aefe2b3b975cf39a80aad52df873c970c64a0a65cc82be5c0`  
		Last Modified: Thu, 04 May 2023 14:18:24 GMT  
		Size: 1.6 MB (1552398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4a15149c5d74e0820570e3c38e95161247eb79cdafc8674172ced6fe03d20`  
		Last Modified: Thu, 04 May 2023 14:19:32 GMT  
		Size: 170.8 MB (170838404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3179417a3b11695195a520064dc075305ad8e449dd76d53c0a575f4df15db3`  
		Last Modified: Thu, 04 May 2023 18:59:21 GMT  
		Size: 2.1 MB (2056139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3414a11d1b4a352e42956eb85fc7ff6b0d0968dd0cae304558b2f99dc28d7d9f`  
		Last Modified: Tue, 16 May 2023 18:22:01 GMT  
		Size: 9.3 MB (9314404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4828f09a6c88f9903a05ce9928b1757df3268e0ea4265d9491cfa211d81c652a`  
		Last Modified: Tue, 16 May 2023 18:22:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476983e0a0f3c216fc724c4951eb65ae11373dd5d608e1ca053937965b837254`  
		Last Modified: Tue, 16 May 2023 18:22:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e703a8520119e4f86e0cbe1fa1093fd02ef2c7ecb0fedbd2e65e745a0d1634c7`  
		Last Modified: Tue, 16 May 2023 18:22:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:80ebd5d8c5ad3de72750f57534d3aacfc832011d66d76c262c9a6b6fd4f05e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201850573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccb25ed309ccf206dff7a32215eec3e276092b154e0c037ac27ea095f6733a7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:48:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:48:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 05 May 2023 00:05:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 May 2023 00:05:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 05 May 2023 00:05:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 05 May 2023 00:05:35 GMT
ARG MAVEN_VERSION=3.9.1
# Fri, 05 May 2023 00:05:35 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 May 2023 00:05:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 May 2023 00:05:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 May 2023 00:05:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec537f63976b3afc1a38ef002078bd6db8ec68729ad89795f237dab27ed975bc`  
		Last Modified: Thu, 04 May 2023 08:49:28 GMT  
		Size: 161.0 MB (160954583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394190a755e765f260d76b49a62fa10edd8e1a6465014d32eca355b6c10fab02`  
		Last Modified: Fri, 05 May 2023 04:05:09 GMT  
		Size: 1.7 MB (1688126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d6fa44cfd2c9f229e07f5a65e4648b48641240f4964b635ce257411efea545`  
		Last Modified: Fri, 05 May 2023 04:05:09 GMT  
		Size: 9.1 MB (9106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a981f4f9e13ebdaa194735a4ff9c11db0ab8519105cb636165104048deaeb0`  
		Last Modified: Fri, 05 May 2023 04:05:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ad731b8120a689cf2986e37af90c7e373ce9e9cd7e35618b3da032eb4ca60`  
		Last Modified: Fri, 05 May 2023 04:05:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8860ec4ccd38e0af6626df76665486ef59f34c09a8c0fcc2f873c1354f4d6a80`  
		Last Modified: Fri, 05 May 2023 04:05:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
