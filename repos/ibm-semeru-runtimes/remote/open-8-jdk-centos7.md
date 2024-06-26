## `ibm-semeru-runtimes:open-8-jdk-centos7`

```console
$ docker pull ibm-semeru-runtimes@sha256:3c6504962d6c3d31fd17cbcfdf484ae22f098c7c297d400521a7df1dfc028ccc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-8-jdk-centos7` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:f317fb5657bdce20fb3e2794ccb4322263c05e5f4e4b3633bb99ec221b5ed9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212009198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fecdebac365db52cc4eef82ce761f169cc55b2e405a73996c3103f4f232b3f1`
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
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2baa88e7ed0ea9f72310fb4adfe99ee06fdb514cc04517b0e0be3c0646493ea3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6b4b2bca348877aaf8941f021a989d647b9575fb84b4ef001abf7182787772ff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='85af2c57078aab240ce31ba3f7a8e86696ff5bdf4c30f3c37f107986f07b23a6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='70afb4cdc8b95b1eb2c2b6cc4b0b9cec705b41ce328a7900fb72dc83e6eee01f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:ebcd6a165c8c29c068ecaf1e6cc35118ec05dc06dbf559c1ff265290b934ce7e`  
		Last Modified: Tue, 25 Jun 2024 22:57:56 GMT  
		Size: 14.6 MB (14642590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b257979964298d6408e189a6c77a945309dae4399a1a01a250336987acbbb1a`  
		Last Modified: Tue, 25 Jun 2024 22:58:00 GMT  
		Size: 117.1 MB (117076439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f000916bb55263baab96fb872c1f22ecb1061c34e562c6c756fa292c19d7feb3`  
		Last Modified: Tue, 25 Jun 2024 22:57:56 GMT  
		Size: 4.2 MB (4193012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a0c49aa4d8019516649ff2ba06e7c71c985d99c7b3d6ae054bbacb4a5fb84738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f6691b7712cde416414d77dace42ae48f9f8c49d3036959d178cfcfacfa495`

```dockerfile
```

-	Layers:
	-	`sha256:626d3887fb8d77ee4e283b89da090b826b0b4983238229af9b0dae55c3611367`  
		Last Modified: Tue, 25 Jun 2024 22:57:56 GMT  
		Size: 5.2 MB (5185479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e479a41298bf41a2d7975bf085ab836bd4740f7bd545062637d72bbc4f58e2ac`  
		Last Modified: Tue, 25 Jun 2024 22:57:55 GMT  
		Size: 23.1 KB (23090 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:f050f11e2181646d0bafac5d10c39801a812c50717aea6a2530a05b2ad2a2a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242920518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea03f1b4a9184276ac62d2204a2f2be7cdcad856ebf17959c69b1533cec0a1`
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
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2baa88e7ed0ea9f72310fb4adfe99ee06fdb514cc04517b0e0be3c0646493ea3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6b4b2bca348877aaf8941f021a989d647b9575fb84b4ef001abf7182787772ff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='85af2c57078aab240ce31ba3f7a8e86696ff5bdf4c30f3c37f107986f07b23a6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='70afb4cdc8b95b1eb2c2b6cc4b0b9cec705b41ce328a7900fb72dc83e6eee01f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:45900f1740e05ce16aa1374bebccb4900d731f22e3e76148c33af07af6fd6554`  
		Last Modified: Tue, 25 Jun 2024 23:04:45 GMT  
		Size: 116.4 MB (116372442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8998497a9f0004f2177bbbe262d3660fabbd7de66ba92625230867be52f737`  
		Last Modified: Tue, 25 Jun 2024 23:04:41 GMT  
		Size: 4.0 MB (4005303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a46c3e436fbf82a1659feb3bd2623d79b675fd31f46410bc7704e67b135b7b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6390436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11f61c7d9f939eb265bf46eb27110dd32fc920c33fee82e8568b2092d64c31b`

```dockerfile
```

-	Layers:
	-	`sha256:7df73af760a2b21c624ffdffd39b0d2971e0b0920260f2d72a6d42cfcf8af695`  
		Last Modified: Tue, 25 Jun 2024 23:04:41 GMT  
		Size: 6.4 MB (6367069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaeb32482c79ffa7b4b4f5ddc7660cc1ee674bcdc9bce2e7fbc6bcb1e39d9235`  
		Last Modified: Tue, 25 Jun 2024 23:04:40 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-centos7` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:d848fb5a7142664b953b41dc974e5426d5e90208962337bc4d5118485b634cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216507408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6c9f118d7ea830adaf79002fcba4c0bee83c1b38e45868191955b9fc269e45`
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
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2baa88e7ed0ea9f72310fb4adfe99ee06fdb514cc04517b0e0be3c0646493ea3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6b4b2bca348877aaf8941f021a989d647b9575fb84b4ef001abf7182787772ff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='85af2c57078aab240ce31ba3f7a8e86696ff5bdf4c30f3c37f107986f07b23a6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='70afb4cdc8b95b1eb2c2b6cc4b0b9cec705b41ce328a7900fb72dc83e6eee01f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:66b3e5e7f0112ef8d9d2724aa88cf966566e37fa8b5325591dccbb1634796805`  
		Last Modified: Tue, 25 Jun 2024 23:06:51 GMT  
		Size: 118.0 MB (117960290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4666ab7f6b46ca1bd19bfa17026e053df46bf0a4e54061bde8db8f06c364f1c0`  
		Last Modified: Tue, 25 Jun 2024 23:06:47 GMT  
		Size: 3.5 MB (3484427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:003f841163aa94b9c738409246118dfe90ec3dd71631a7bb1f0623374d34391d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45c8b4caacc3f08ebfa7ca30d678f9585c86dc57bdba085a40cd6fbbd4041ba`

```dockerfile
```

-	Layers:
	-	`sha256:8fd5734e1ac76b7b6188fda9999314b0e5934e0c6d05ecdf5569d519a87f48c5`  
		Last Modified: Tue, 25 Jun 2024 23:06:47 GMT  
		Size: 5.2 MB (5192448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10e371a3c55bd40cea445b206293a12eeca8dd61291dce92dde1a780c85a1ff`  
		Last Modified: Tue, 25 Jun 2024 23:06:47 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json
