## `ibm-semeru-runtimes:open-8u422-b05-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:fef77bcc979bb9a2536ef735eb0d9446590810bb1cc7e2f61bb03723f7834276
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-8u422-b05-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:37f60fcfd03ce08492be141cf36e1ce417d0031aece0f26071592e9bd1740817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96289286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae0cb705b359557fcaf16777614613e10a9574cb99b341d4484d0b4bfec9a42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='1b19a927beb900790dfac47f324d232b86ba5219ed065a33a77eb15c240595c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7cc60ce639b5ee2139db03578ceae944cb41ca1f7e3233275abc311cf87a8339';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='4e737653e890c4c8a38588c887fa4081fe70b8370a46e94b0fb4121178f2f352';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='ff17b03a374b4b4c1184cebebe67d06db46b9bb63e1c99d4ab69c80f16c73e58';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacdaab3ff52884212496b6468f62bcf0f345ad8303b3a7b1e96ee116f02ca63`  
		Last Modified: Mon, 04 Nov 2024 22:04:42 GMT  
		Size: 12.2 MB (12175022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b47be1263d871fd0ba909cc3c2dbd9592a9367bf43a1ec8b30cd7b860dae4b0`  
		Last Modified: Mon, 04 Nov 2024 22:04:42 GMT  
		Size: 50.3 MB (50317873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e4554c734737e3820764a3dc19ec0bde84bec5b6b65af576117600841f95e0`  
		Last Modified: Mon, 04 Nov 2024 22:04:41 GMT  
		Size: 4.3 MB (4260703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:aa157587b2eadee1f2d32077af1d27d252af3744df480f02996df527cdc7d5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3639966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c63b89f6213a858530496ecb27eed217701b644b749f5defd3598f345f6ade`

```dockerfile
```

-	Layers:
	-	`sha256:dcba8b8ab6e3ef802614a1ccbfe60bafc2bdd2425f26fe9a7fadcdf8b52e7a34`  
		Last Modified: Mon, 04 Nov 2024 22:04:42 GMT  
		Size: 3.6 MB (3615341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49232b4a9c0dbbebf3e2b362bb280ab63b126b90ee29d2eb0108cafe44762f03`  
		Last Modified: Mon, 04 Nov 2024 22:04:41 GMT  
		Size: 24.6 KB (24625 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:539ad656d495934db90bb7bac773467d335c2e10c97ff6675d6ead29aa3010d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93263634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d3a8ec69d94d9880640e009eef72884353d7eda3a125974abb0e950b708427`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='1b19a927beb900790dfac47f324d232b86ba5219ed065a33a77eb15c240595c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7cc60ce639b5ee2139db03578ceae944cb41ca1f7e3233275abc311cf87a8339';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='4e737653e890c4c8a38588c887fa4081fe70b8370a46e94b0fb4121178f2f352';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='ff17b03a374b4b4c1184cebebe67d06db46b9bb63e1c99d4ab69c80f16c73e58';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8db97a9b46a080a285ae7eb265ed5e64db7de26df73e85dcb3512fae3446d`  
		Last Modified: Mon, 04 Nov 2024 22:08:00 GMT  
		Size: 12.1 MB (12128492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f39ca169c5ccd0d8605c97df867edcd2b0f1120c5b08d47104c5baef037d78`  
		Last Modified: Mon, 04 Nov 2024 22:10:19 GMT  
		Size: 49.8 MB (49750994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5837faa6861766e268afface6d829cbae32ca532ed4a61ed182a07f9508db9`  
		Last Modified: Mon, 04 Nov 2024 22:10:18 GMT  
		Size: 4.0 MB (4025819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b3f89abbe09bdfd762ff3f254db8be4e90ca35f3c8df06cde5ba20991e14a9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3639926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59ec429e8b9f34776cb76699dc854db3e095e3a76751b7665f3bd099dfbb428`

```dockerfile
```

-	Layers:
	-	`sha256:f65c99ea7bd6c085ca92fea44e86fee2571174d153920f8d99bb7a9540f9eba1`  
		Last Modified: Mon, 04 Nov 2024 22:10:18 GMT  
		Size: 3.6 MB (3615167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2437e451d2e2e97b8f2a17b3121c419f775588d2dfd4c035065236b2795a23b2`  
		Last Modified: Mon, 04 Nov 2024 22:10:18 GMT  
		Size: 24.8 KB (24759 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:613b8a1398cf82e36fd0b700d2e933a5402c34fbbf0b4b69bbe2f604b846e3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102519149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b26c2aa371f7034b08d64274c0c6ae607b258a85b62d4aea20013d613d92f6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='1b19a927beb900790dfac47f324d232b86ba5219ed065a33a77eb15c240595c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7cc60ce639b5ee2139db03578ceae944cb41ca1f7e3233275abc311cf87a8339';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='4e737653e890c4c8a38588c887fa4081fe70b8370a46e94b0fb4121178f2f352';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='ff17b03a374b4b4c1184cebebe67d06db46b9bb63e1c99d4ab69c80f16c73e58';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402b95c89192f7e12642ee48a9555e3f966f8c0de4c4b2a758b247e8dbb0991`  
		Last Modified: Mon, 04 Nov 2024 22:10:30 GMT  
		Size: 51.7 MB (51747196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b1241292475af9fb66183fdbcb178546c21dec7208ca995279748d1d75cf62`  
		Last Modified: Mon, 04 Nov 2024 22:10:29 GMT  
		Size: 3.4 MB (3435579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:dba73985e7c527a4c7816aae2df6b5b2abaf705b9db2d8b17a9ca63b8675550e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3638790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573d6f3a2e0c8d31b48677a50142c7fb7661bc40d6d821943f145e0f9098a1df`

```dockerfile
```

-	Layers:
	-	`sha256:9c14f4acbbf0003fba8fe592df5d084157e2f30ecf537a7e32f58bf4fb19ac32`  
		Last Modified: Mon, 04 Nov 2024 22:10:29 GMT  
		Size: 3.6 MB (3614117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87ffa29bfbc2986eac6401631ffc19dee7b3a8b264775ac56cfca792a4a7675`  
		Last Modified: Mon, 04 Nov 2024 22:10:29 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:9fc65131206965121e9964fd31ed9d347aaf0690c0ea7a892f569c95321d39fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94839276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982651d56ef6102887e400399e0ffe6072ade6d27f859e8cfda47a0fbe049fb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='1b19a927beb900790dfac47f324d232b86ba5219ed065a33a77eb15c240595c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7cc60ce639b5ee2139db03578ceae944cb41ca1f7e3233275abc311cf87a8339';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='4e737653e890c4c8a38588c887fa4081fe70b8370a46e94b0fb4121178f2f352';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='ff17b03a374b4b4c1184cebebe67d06db46b9bb63e1c99d4ab69c80f16c73e58';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f72f8b473e0d914be656e69a64248605b7fd83fca25f92643c1c1092d99e0`  
		Last Modified: Mon, 04 Nov 2024 22:12:36 GMT  
		Size: 50.3 MB (50289187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0d33e85d3cddcb89ae3742feac06db2af546f22e46c1cfdb4f103771aca740`  
		Last Modified: Mon, 04 Nov 2024 22:12:35 GMT  
		Size: 4.3 MB (4344855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c484fb1d2915755d4d38f3e522ae37b5588cfdf177de0cee930d429005441c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9f465327bc7a806f7ec86b8dd4d6c2634e19f15c3b141e1497372a0da88ac2`

```dockerfile
```

-	Layers:
	-	`sha256:231760774ef927bdca03d2b486ce1e68261f1c7f0fa1991c1661ce2b999ac460`  
		Last Modified: Mon, 04 Nov 2024 22:12:35 GMT  
		Size: 3.6 MB (3611673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7592134c2864587d2474f9899574dd9edadc887036eb2110b1bbe3fc3b23fb9`  
		Last Modified: Mon, 04 Nov 2024 22:12:35 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json
