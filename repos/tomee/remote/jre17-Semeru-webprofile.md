## `tomee:jre17-Semeru-webprofile`

```console
$ docker pull tomee@sha256:853cc0b2d9b28fde9bf6035dc0f72313b7eb1203b3300c864c9d51a9ff9f7d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomee:jre17-Semeru-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:200683aa3e6419ee352a318cdb7a7ee53acbcd7298c5529ba253480b16fb8e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148719670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1816f72f535b8dcfb0109a02ca4123eedd7862071f576f8f7549efccc0b63c31`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 05:44:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 05:45:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 05:53:27 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Fri, 09 Dec 2022 05:55:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8f934ce1745f52a067bdeb56b3b9e9192f51e674ff2956a1e53b33e44ea5ca42';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d54972fb938f655a3665512c7181c2c5813e3bfe742650d6081e2f480388ef2f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='759f9c507e0faf53b260ee9f492bab8fdeb8091bdecad904134861714e4d913b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='64ffeaff0ea4915fb66d3356ef5de65e884172b031e0c268bdeb4d2aa6be1c91';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 09 Dec 2022 05:55:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 05:55:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 09 Dec 2022 05:56:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Dec 2022 09:10:53 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 09:10:54 GMT
RUN mkdir -p /usr/local/tomee
# Fri, 09 Dec 2022 09:10:54 GMT
WORKDIR /usr/local/tomee
# Fri, 09 Dec 2022 09:11:00 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 09:11:09 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 24 Jan 2023 02:38:26 GMT
ENV TOMEE_VER=8.0.14
# Tue, 24 Jan 2023 02:38:26 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 24 Jan 2023 02:38:32 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 24 Jan 2023 02:38:32 GMT
EXPOSE 8080
# Tue, 24 Jan 2023 02:38:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbc191ace5f8a149991701d080d201686bc4dd0bb3dde552a9ff623d58dfd15`  
		Last Modified: Fri, 09 Dec 2022 06:02:33 GMT  
		Size: 16.0 MB (15995452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865195e08e4adf61d4127cbd251ee8cfd4d2441224b8ab63a48824ec3daacc29`  
		Last Modified: Fri, 09 Dec 2022 06:05:54 GMT  
		Size: 48.1 MB (48096883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b59fb9ea8ea53e0d684187ffb910930c352fe6368c5cbfdc44da865945c093`  
		Last Modified: Fri, 09 Dec 2022 06:05:48 GMT  
		Size: 4.8 MB (4842754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9858a92c73e18db40803829ebe4bdaf678dfce6da3a07fe5d9aaefbe6824de3f`  
		Last Modified: Fri, 09 Dec 2022 09:43:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e1fdf2982eabaa2bdc1253442265e1e16db5780763d7f8feac643b3a74ef7e`  
		Last Modified: Fri, 09 Dec 2022 09:43:56 GMT  
		Size: 3.7 MB (3660747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd28460d4c0058e8271fb1aebbfe77305857f1306bcc403b4e8362ff454f32c3`  
		Last Modified: Fri, 09 Dec 2022 09:43:55 GMT  
		Size: 62.9 KB (62922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0837141096044c5749d6265ac7e17776c5b2e2048f4b6ad60ba63efacc966a`  
		Last Modified: Tue, 24 Jan 2023 03:22:02 GMT  
		Size: 47.5 MB (47483858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:jre17-Semeru-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:6cdb50aa113e754b0bc9e2392cf506f090937bfb24c96c8c449a3a8f17be411e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145150483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddea55febf980fafc8146aee97745975c33a39820ed0d5b729f055575d09f96`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:37:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:37:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:36 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Tue, 31 Jan 2023 18:46:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8f934ce1745f52a067bdeb56b3b9e9192f51e674ff2956a1e53b33e44ea5ca42';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d54972fb938f655a3665512c7181c2c5813e3bfe742650d6081e2f480388ef2f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='759f9c507e0faf53b260ee9f492bab8fdeb8091bdecad904134861714e4d913b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='64ffeaff0ea4915fb66d3356ef5de65e884172b031e0c268bdeb4d2aa6be1c91';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Jan 2023 18:46:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:46:28 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 31 Jan 2023 18:47:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 31 Jan 2023 22:54:44 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:54:44 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 31 Jan 2023 22:54:44 GMT
WORKDIR /usr/local/tomee
# Tue, 31 Jan 2023 22:54:49 GMT
RUN apt-get update   && apt-get install -y  gpg   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:54:58 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 31 Jan 2023 22:54:58 GMT
ENV TOMEE_VER=8.0.14
# Tue, 31 Jan 2023 22:54:58 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 31 Jan 2023 22:55:03 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 31 Jan 2023 22:55:03 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:55:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdbed22b0a8a0e7be353c90eedf03945efc6451043f2f84c4b81d21cdf90ff8`  
		Last Modified: Tue, 31 Jan 2023 18:53:46 GMT  
		Size: 15.9 MB (15860320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbba699bbe69efcff34e79fa9be240b8071ad4a363b561acb1a1d8f6c410fc7`  
		Last Modified: Tue, 31 Jan 2023 18:56:38 GMT  
		Size: 46.3 MB (46320143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802cb3d6ac6bbbee7bb619a08db2d82159f9575897c9b9320599b71cdba4705f`  
		Last Modified: Tue, 31 Jan 2023 18:56:34 GMT  
		Size: 4.6 MB (4580745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96782faa760b7dedd95ab3768c60a03f86232a3f07ab020471d3ad27d84652b1`  
		Last Modified: Tue, 31 Jan 2023 23:23:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94802e86ea685011d9909e93903bbd7d66446f832afd8902aaa5a207b76d38fa`  
		Last Modified: Tue, 31 Jan 2023 23:23:21 GMT  
		Size: 3.6 MB (3648606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a297ee657d8cf3fd5428b6e9a8aa6d69da923f6c0650d3a203097ba7a837e57b`  
		Last Modified: Tue, 31 Jan 2023 23:23:21 GMT  
		Size: 62.9 KB (62912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a54060ff7a3646f04320fba28708bebd87bc2f0091b6363529d09de9fb461a`  
		Last Modified: Tue, 31 Jan 2023 23:23:23 GMT  
		Size: 47.5 MB (47483849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
