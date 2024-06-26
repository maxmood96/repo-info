## `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7`

```console
$ docker pull ibm-semeru-runtimes@sha256:22db8e240052c512992b27a95a1b97e8dedf02b4067833540c7d1bf821446dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:4292870b8b8512a3958f6a98dfa251367516bfb763e190e33cb038b1c8c47857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147498644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9472224a36f59f2c543b6bad20f2fa899ee3fe7cff7dbd4c45d02c495126c5b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7fb241b2de7227851a294b1612f83c10be940d5c4c92354b83dbb353db0009`  
		Last Modified: Tue, 25 Jun 2024 22:58:00 GMT  
		Size: 14.6 MB (14642469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb61be05ebc02cb10f224ed68d119427990f5d5e544ae024a7f0ffff57298683`  
		Last Modified: Tue, 25 Jun 2024 22:58:00 GMT  
		Size: 51.8 MB (51801659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61830f4d27d13346a859e1e113d013c8cd211c3e0b58a3f4e4964290163cdb0e`  
		Last Modified: Tue, 25 Jun 2024 22:57:59 GMT  
		Size: 5.0 MB (4957359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3e96856f9f854412d9d8b67e99e958084c370d598dd5f609c21c41c9505db6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5183195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6843096ea2da6c31175c7f7158572fa4ab0e12c7ad12a5d69550a3b95bd34a`

```dockerfile
```

-	Layers:
	-	`sha256:4d627a6781165e428b7d946f74fda2c7eebb35e9e2addfa5026bdfdbf3fc1651`  
		Last Modified: Tue, 25 Jun 2024 22:57:59 GMT  
		Size: 5.2 MB (5160053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612a2d2edd22623bab4bd5d0cbd0acccf296986ac4abba334b92dd0b1faefa46`  
		Last Modified: Tue, 25 Jun 2024 22:57:58 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:49da97a0cdd9388d43a23d33039aa02bf5ef7aaee007f870a4db6a43948d041c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175001900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da415566d63102ee3bb44bffbc5a6a838f1d5212317538abcb6427292b618a33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d618285429c2bf62e795cf4222667658ce0dc51d7560e205d38445dbbd56a0e8`  
		Last Modified: Tue, 25 Jun 2024 23:04:41 GMT  
		Size: 14.2 MB (14167828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff8c9147128d38f28f1445b6210029377cd9eeac98ea173f187ff9a0bc622bf`  
		Last Modified: Tue, 25 Jun 2024 23:22:38 GMT  
		Size: 47.8 MB (47819168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae403548eaf380367c50b14d49c8c8572fcc46646a27ea6a62e9abc10590128e`  
		Last Modified: Tue, 25 Jun 2024 23:22:36 GMT  
		Size: 4.6 MB (4639959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:f60f0de3b38b07d58659887f431567094c081947cb23307f074aef0601d14c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6365062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edd97bd553b107fb9caa7eed5202ae91fe124e6a2c4c780cfcce6489b42d989`

```dockerfile
```

-	Layers:
	-	`sha256:4c52b138773791b153225d321aefbbda91786e2606cd6c929f374b6a53ea4cf9`  
		Last Modified: Tue, 25 Jun 2024 23:22:36 GMT  
		Size: 6.3 MB (6341643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0030eeffbf6272ec8200d971dbcb0b5dadbbc6dcb932a9b75c5042e93f87673f`  
		Last Modified: Tue, 25 Jun 2024 23:22:36 GMT  
		Size: 23.4 KB (23419 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:6d5c536d03facd0ce768a044457c9d74e0a5bf61552b893fcda2b0bf46d6af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151888833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442ac9fc3fb410596916f3fdab95313c02f0bc773766ccb4d88482f5fcfb4350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991a61d82e75ea7116e8f0546b27c479f7364c780fcd07cd3ccc01bebb7f5dbb`  
		Last Modified: Tue, 25 Jun 2024 23:06:48 GMT  
		Size: 14.5 MB (14546231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc3d2b9bda02dc9473691976c5b4001687286088bd3f5247f1c3159de784865`  
		Last Modified: Tue, 25 Jun 2024 23:30:07 GMT  
		Size: 53.1 MB (53050194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2187879256c3059482ca6ddb8a6d0194b2628c62a2e9c25c1bd37551ac1c0c79`  
		Last Modified: Tue, 25 Jun 2024 23:30:05 GMT  
		Size: 3.8 MB (3775948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jre-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:862b002a98736e721cc34e48358cb79a5fabae6e30789259512d816066da1ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dec400dc935004e737069979d63f19f82e52194eb63b0ca8650a48d16f71ae6`

```dockerfile
```

-	Layers:
	-	`sha256:eaab92439899b5cc9874c1ac60bb8f8a468b84f535d15a4000dfdc0818e0d919`  
		Last Modified: Tue, 25 Jun 2024 23:30:05 GMT  
		Size: 5.2 MB (5167022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73788b479bcfc1681afa2d97f9574d099d0b1a25aabf573d3faafe74f06aec61`  
		Last Modified: Tue, 25 Jun 2024 23:30:05 GMT  
		Size: 23.2 KB (23172 bytes)  
		MIME: application/vnd.in-toto+json
