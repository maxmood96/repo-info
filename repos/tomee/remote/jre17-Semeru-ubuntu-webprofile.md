## `tomee:jre17-Semeru-ubuntu-webprofile`

```console
$ docker pull tomee@sha256:626161190f18006ec34dbd7520b7047136b1aeb5c3b758df267c68c210c01704
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:jre17-Semeru-ubuntu-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:2d2fa88817052a4a2814fb7e72939b8a9e044c64484f74abb87617ff34e27b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160455655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0210339084908f45595006178b51e142b634ad5b1085e34ca575ab7535856d79`
-	Default Command: `["catalina.sh","run"]`

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
# Wed, 16 Oct 2024 23:15:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 23:15:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
WORKDIR /usr/local/tomee
# Wed, 16 Oct 2024 23:15:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_VER=9.1.3
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 16 Oct 2024 23:15:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6414d03c2b0485d19a9eedadfa3506c7d6b3aa2fd7f92ca5cc9b0dfbf42c3`  
		Last Modified: Mon, 18 Nov 2024 21:06:16 GMT  
		Size: 12.2 MB (12175060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe6084c4786be715649408fbe05daf01251ad3ab08ebc3193d3c830d482d56b`  
		Last Modified: Mon, 18 Nov 2024 21:06:17 GMT  
		Size: 51.5 MB (51533608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f79bbc470e2639578fb88cd2c9e6f368b8c37ab13c89e06e0ba5d8d954686b`  
		Last Modified: Mon, 18 Nov 2024 21:06:16 GMT  
		Size: 5.0 MB (4965093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017d6bd9c1e9b58a9446bef6acadb6e64053b0568d415b86a60b594633f5b20a`  
		Last Modified: Mon, 18 Nov 2024 22:05:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4c3761cb6acb262ba245cca8da9e1e605f0beb8a37d3f33f1f2d4ff2f33b5d`  
		Last Modified: Mon, 18 Nov 2024 22:05:35 GMT  
		Size: 2.4 MB (2356440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f867835ca2aed695ee0b4e7a2dab63f49962a86404a771abb4bbf24c3c9dec`  
		Last Modified: Mon, 18 Nov 2024 22:05:35 GMT  
		Size: 75.6 KB (75649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51fc676a08b098324fd98d316e7739c3223d4f586496a78f7782631160a77b`  
		Last Modified: Mon, 18 Nov 2024 22:05:36 GMT  
		Size: 59.8 MB (59813911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:e701942a6a27ab51558925f8ed6ea76185568f88d343b56e3dfc0ff1bb4bc740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccd0364c2c5ef7ed539a1c803930d9e59bd9bfd84f5f0763f15d51f630408ff`

```dockerfile
```

-	Layers:
	-	`sha256:2f05275fbe58f2ea5b72ea00a72fc0a43b18651ff0a98d6fdd4d6c12063c3d82`  
		Last Modified: Mon, 18 Nov 2024 22:05:35 GMT  
		Size: 3.9 MB (3949752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90fbf0d685f7aef5d3d90fb2954139360d66d923c891b96f72617017693cdc5`  
		Last Modified: Mon, 18 Nov 2024 22:05:35 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:jre17-Semeru-ubuntu-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:6a1e4ace8922788a6abb4be3e0bd36600ef366ee5f5c479ecb13cfd6c0080811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153913078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6303e7fa63a8c14cd75fb2e1d894560804753175e36751705035699b6dadf34e`
-	Default Command: `["catalina.sh","run"]`

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
# Wed, 16 Oct 2024 23:15:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 23:15:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 23:15:53 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
WORKDIR /usr/local/tomee
# Wed, 16 Oct 2024 23:15:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_VER=9.1.3
# Wed, 16 Oct 2024 23:15:53 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 16 Oct 2024 23:15:53 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Wed, 16 Oct 2024 23:15:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 16 Oct 2024 23:15:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Last Modified: Mon, 18 Nov 2024 19:12:40 GMT  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf2d4b2e2296540c2e5d354b52aeaddcb98a98da98203357f0e3a1528ad0ab7`  
		Last Modified: Mon, 18 Nov 2024 19:24:53 GMT  
		Size: 47.6 MB (47553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823a239827a007e8948393395137942949dc3dcd27f4476004f4179771e99a8`  
		Last Modified: Mon, 18 Nov 2024 19:24:51 GMT  
		Size: 4.6 MB (4641171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20278f2de5d62372c69b60ae3a41411cd929981a8b0f9b2aaea6d2d3648f1e`  
		Last Modified: Mon, 18 Nov 2024 21:23:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bda535b7140bd7804b7907dcf00b0eb1f1433821d0a3c57cb2f0b1786881d`  
		Last Modified: Mon, 18 Nov 2024 21:23:13 GMT  
		Size: 2.3 MB (2341681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27f2539656187cdd47a0bbbfde704e92a5b2d79992702878022ebf95a06b79f`  
		Last Modified: Mon, 18 Nov 2024 21:23:13 GMT  
		Size: 75.6 KB (75622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca36d39740f3da6c95f69b5775615ae320cdaabbe7971d8cfd064465dc9340c`  
		Last Modified: Mon, 18 Nov 2024 21:27:04 GMT  
		Size: 59.8 MB (59813904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:jre17-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:8680e0dfb7c2d16148876213a7b1f30ef3f7f5ca24cb5ef5a30ce2230034dae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb91c5769d79d058c60b62ddbfb895674183da3e0e074a9bba048d9b0154b66`

```dockerfile
```

-	Layers:
	-	`sha256:e64857118cece0da07b4bebde44db2befa50e210f37af55b096a69132f00c135`  
		Last Modified: Mon, 18 Nov 2024 21:27:02 GMT  
		Size: 3.9 MB (3941307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42004c4fee9058670e5138bb0bf4653a1bca4755ade9ff6f476f0c48be93796f`  
		Last Modified: Mon, 18 Nov 2024 21:27:01 GMT  
		Size: 27.0 KB (26968 bytes)  
		MIME: application/vnd.in-toto+json
