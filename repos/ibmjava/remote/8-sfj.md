## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:d4779fe0093a80e4e067d15324b65a987eeb409676539fc5f4697068b1b50041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:1252fefc95619fb06cf1f8bda335a2528b94421b5cf49c6e36e9fe10efcf6d18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94517110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a09af8867a8c8484ed4ce06dbf6fb50e1af4c157a18bca21c69815283de8daa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 01:06:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 30 Apr 2022 01:06:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 17:02:18 GMT
ENV JAVA_VERSION=8.0.7.10
# Wed, 01 Jun 2022 17:03:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c1fb549eed0be5462a9a52099fcb46bb451654b1815f27d1a71ae799daabb527';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='415565deb6b0fa26d84ccad928d91c22274dc23f50f10d11d1e7ee686da1588d';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b37ac95d0e91bf04dce30139abfe49c9054fefc89c7d47227d579912cd2843c6';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8a719a3e5b9e0648c5d309701fbe4d4583aacaef0b3a01c6d29bb6d7cfef328a';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='de4fbb36bd46cffd88bdc6bd5734aaa4ad4c09f4adefdf66fb8bb9e58ca47639';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 01 Jun 2022 17:03:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9274cc4ee93edf7c6c542860e9243251f72535f23aa9365dc6f25072d40216`  
		Last Modified: Sat, 30 Apr 2022 01:08:49 GMT  
		Size: 3.0 MB (2959981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7c18ac03e125dda80179d7efc73ffcdd78419174347898bb4946a175d2baca`  
		Last Modified: Wed, 01 Jun 2022 17:05:02 GMT  
		Size: 64.8 MB (64848021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:08facdd3af99354f17adcdeadeb6564bdc80bb0478fa3c3291d19410831236e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94385713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8813b4a8da1ea73677945d5e92fa22bb788f3bd6c0bc260a2c82f2861cdc6436`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:46:47 GMT
ADD file:bcce1e9e400660e474d54b70b67bc484a7976aff4e980b58d10ddcb4daa58a7f in / 
# Fri, 29 Apr 2022 22:46:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:10:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 29 Apr 2022 23:10:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 15:38:41 GMT
ENV JAVA_VERSION=8.0.7.10
# Wed, 01 Jun 2022 15:39:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c1fb549eed0be5462a9a52099fcb46bb451654b1815f27d1a71ae799daabb527';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='415565deb6b0fa26d84ccad928d91c22274dc23f50f10d11d1e7ee686da1588d';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b37ac95d0e91bf04dce30139abfe49c9054fefc89c7d47227d579912cd2843c6';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8a719a3e5b9e0648c5d309701fbe4d4583aacaef0b3a01c6d29bb6d7cfef328a';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='de4fbb36bd46cffd88bdc6bd5734aaa4ad4c09f4adefdf66fb8bb9e58ca47639';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 01 Jun 2022 15:39:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:14c49d5e021ef38e29480c34c86df22d89b9b63fe1a57ec4dd970f56497edf9a`  
		Last Modified: Fri, 29 Apr 2022 22:47:32 GMT  
		Size: 27.2 MB (27164138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08de056e8ffee8045cf535785282f3b64d4f5516108a6e75d5024df24973f981`  
		Last Modified: Fri, 29 Apr 2022 23:12:51 GMT  
		Size: 3.0 MB (2988554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef49d109952c74ce2804d02acfa5c09edf47d814e3e1e5b6fd96b43bb832af`  
		Last Modified: Wed, 01 Jun 2022 15:42:44 GMT  
		Size: 64.2 MB (64233021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6cfa2d4a879aefa85bc143d8a00d71693ee7136c4ddaf7edfe60bf8458737000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98583875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685099966dfa7bbf6e92a545f4fdb6f04edfc71f3aa4cf4946471d7ee14441f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 01:49:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 30 Apr 2022 01:50:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 18:17:09 GMT
ENV JAVA_VERSION=8.0.7.10
# Wed, 01 Jun 2022 18:19:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c1fb549eed0be5462a9a52099fcb46bb451654b1815f27d1a71ae799daabb527';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='415565deb6b0fa26d84ccad928d91c22274dc23f50f10d11d1e7ee686da1588d';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b37ac95d0e91bf04dce30139abfe49c9054fefc89c7d47227d579912cd2843c6';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8a719a3e5b9e0648c5d309701fbe4d4583aacaef0b3a01c6d29bb6d7cfef328a';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='de4fbb36bd46cffd88bdc6bd5734aaa4ad4c09f4adefdf66fb8bb9e58ca47639';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 01 Jun 2022 18:19:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b9fc7dc4c2bad9d9f7db0ffd5b499212f90be1d458552dba4bd7e526ede046`  
		Last Modified: Sat, 30 Apr 2022 01:54:24 GMT  
		Size: 3.1 MB (3082255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5044c1118da702ce6228c445ba6030e22ff1de9748f3611f9cd369772b8d`  
		Last Modified: Wed, 01 Jun 2022 18:21:58 GMT  
		Size: 65.1 MB (65058437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:57f34290d8177eb96f3e9c4b3786a000795cc1379649678951defc139a4accc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93938170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7480b5e6a5a4fb65fbdacfc7cae9356dee7530d5418fe4a27806f53e98550a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:50 GMT
ADD file:9b5ddd45fc485b5c5ea3d28339d1768fa5d8f60059022a971897d51d94ad5847 in / 
# Fri, 29 Apr 2022 22:49:54 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:27:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 29 Apr 2022 23:27:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 15:41:55 GMT
ENV JAVA_VERSION=8.0.7.10
# Wed, 01 Jun 2022 15:43:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c1fb549eed0be5462a9a52099fcb46bb451654b1815f27d1a71ae799daabb527';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='415565deb6b0fa26d84ccad928d91c22274dc23f50f10d11d1e7ee686da1588d';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b37ac95d0e91bf04dce30139abfe49c9054fefc89c7d47227d579912cd2843c6';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8a719a3e5b9e0648c5d309701fbe4d4583aacaef0b3a01c6d29bb6d7cfef328a';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='de4fbb36bd46cffd88bdc6bd5734aaa4ad4c09f4adefdf66fb8bb9e58ca47639';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 01 Jun 2022 15:44:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1347a7b069ceb0e131b6f229b7b96bae189f8e4c594c1933170e278d0ed928b2`  
		Last Modified: Fri, 29 Apr 2022 22:51:49 GMT  
		Size: 25.4 MB (25365828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f94c1c13b8b89cf54909fe9580987f60938a39e09f8c39697300c3a17a3ec1`  
		Last Modified: Fri, 29 Apr 2022 23:30:09 GMT  
		Size: 2.7 MB (2677016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b9e7dfa7de385f42f71c6982d6724d743bd12c3718b249adf0788b1247cb76`  
		Last Modified: Wed, 01 Jun 2022 15:46:38 GMT  
		Size: 65.9 MB (65895326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
