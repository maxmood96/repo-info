## `tomee:10-jre21-Semeru-ubuntu-microprofile`

```console
$ docker pull tomee@sha256:727b26b003ea0e00893d81f4d39b14d070dba108a29882778453581f4cd14b3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre21-Semeru-ubuntu-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:220255d70d5866de4e7bbe54db83b55b4c21b3a884c3e67b12aeccdfa78dc5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179656121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f095aa843b327d622493337870dfe4b724f16d8d7b441f777507dddbc52ac0fa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 Sep 2025 09:00:25 GMT
ARG RELEASE
# Mon, 22 Sep 2025 09:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 Sep 2025 09:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 Sep 2025 09:00:25 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 Sep 2025 09:00:25 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 22 Sep 2025 09:00:25 GMT
CMD ["/bin/bash"]
# Mon, 22 Sep 2025 09:00:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Sep 2025 09:00:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c611717d51b2adf67e3bc676870d000ad28153b2b7c4057f6dc353be10a67e6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='90a72e4413917a89a825ee973215db7c1a50f61f46ae1609eb52945999f85ddb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1f952d4b0a7c5e59286a5b7c4cd5e8b841a888c19b21fb02b8620eb0b5109366';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='0204bb84c5cfd705298f482cbed9687bd2cb324306f505cee80a4b684a4fbf22';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 09:00:25 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
WORKDIR /usr/local/tomee
# Mon, 22 Sep 2025 09:00:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV TOMEE_VER=10.1.2
# Mon, 22 Sep 2025 09:00:25 GMT
ENV TOMEE_BUILD=microprofile
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Sep 2025 09:00:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a2cebed03b67a6d1201db0d1f1760142ae172d4730f5c35fed5f9d50fb10f9`  
		Last Modified: Thu, 02 Oct 2025 05:05:59 GMT  
		Size: 12.2 MB (12171669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22da3257cd3e21d9db9d1bb052d4c5e366fbfaf947f1d40eda7a72f10c90bd3`  
		Last Modified: Thu, 02 Oct 2025 05:08:01 GMT  
		Size: 59.8 MB (59787029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1848f3de3cec4f46dec5bcfdfc96961ad55d566dd35138f2591962813cb5a39`  
		Last Modified: Thu, 02 Oct 2025 05:07:57 GMT  
		Size: 5.3 MB (5281752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0935ac9cd1363cad195fdee774abe671897f5e590eb551167fd51c083a7105ca`  
		Last Modified: Thu, 02 Oct 2025 08:51:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28798564f1bf8ff5f66d819558866bd12f066af79d2620dd4a8823cfb88cbf62`  
		Last Modified: Thu, 02 Oct 2025 08:51:02 GMT  
		Size: 2.4 MB (2357776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efbba4c76db4cbb6d5ee2962b900cb389baeb22e30834e14eb105b80194c88d`  
		Last Modified: Thu, 02 Oct 2025 08:51:01 GMT  
		Size: 75.6 KB (75634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab54cdb7cb1ce75f00261c8b6adecc9f6e6271f3b4cb744502169f17ee273f`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 70.4 MB (70445239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-Semeru-ubuntu-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:3655ed4a6b7306c94eadfe5b68023ea96af872c1d72d9e1d605ddb8432866f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4261894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eada0089df24592ca5f0f3acd368374d377392b49a4320b308d115b09a01e1dc`

```dockerfile
```

-	Layers:
	-	`sha256:ecb4edf2eb985a43afb13bb944c63dc014b5b439320f3f7a5926a2052cdeb5a4`  
		Last Modified: Thu, 02 Oct 2025 10:11:23 GMT  
		Size: 4.2 MB (4226186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc1f099f4a1b2dcfdc6e1078615194b27f4d297456d48ce74ea50822aeb9f4a`  
		Last Modified: Thu, 02 Oct 2025 10:11:24 GMT  
		Size: 35.7 KB (35708 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre21-Semeru-ubuntu-microprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:19f1b2b4dfecddc8693e1f52947f3f1c7e1f32e5ae7cfe62be0de2277ae4c4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175401092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015fdb0d67b0947f55645fdc17d2e7a0ba6c877eb9318aa7a4e142d19dd7d8ab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 Sep 2025 09:00:25 GMT
ARG RELEASE
# Mon, 22 Sep 2025 09:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 Sep 2025 09:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 Sep 2025 09:00:25 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 Sep 2025 09:00:25 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 22 Sep 2025 09:00:25 GMT
CMD ["/bin/bash"]
# Mon, 22 Sep 2025 09:00:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Sep 2025 09:00:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3c611717d51b2adf67e3bc676870d000ad28153b2b7c4057f6dc353be10a67e6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='90a72e4413917a89a825ee973215db7c1a50f61f46ae1609eb52945999f85ddb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1f952d4b0a7c5e59286a5b7c4cd5e8b841a888c19b21fb02b8620eb0b5109366';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='0204bb84c5cfd705298f482cbed9687bd2cb324306f505cee80a4b684a4fbf22';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 09:00:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 09:00:25 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
WORKDIR /usr/local/tomee
# Mon, 22 Sep 2025 09:00:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
ENV TOMEE_VER=10.1.2
# Mon, 22 Sep 2025 09:00:25 GMT
ENV TOMEE_BUILD=microprofile
# Mon, 22 Sep 2025 09:00:25 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Mon, 22 Sep 2025 09:00:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Sep 2025 09:00:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53cb56ac0ce292961a2ca963800fcba758e1f4af2710cd5cdb3fafb219df4b1`  
		Last Modified: Thu, 02 Oct 2025 01:22:07 GMT  
		Size: 12.1 MB (12129376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d53afd02b251376d573c33532c796cf077f257de399cc3427055b3ae38ced`  
		Last Modified: Thu, 02 Oct 2025 01:23:12 GMT  
		Size: 58.0 MB (58041325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62f3c94da0ecc3d9c22fe6ebb1157a5d181390dbc578d76de84f92e6594c48`  
		Last Modified: Thu, 02 Oct 2025 01:23:00 GMT  
		Size: 5.0 MB (4984248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecd56810605e97fd7fbd74213adab7a8f6306a881f952a8d9488d96e2895abd`  
		Last Modified: Thu, 02 Oct 2025 02:36:22 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7def2d69c6b427d535da5a02c5f14b124e317fa465c599744f4ea117c3b377fb`  
		Last Modified: Thu, 02 Oct 2025 02:36:22 GMT  
		Size: 2.3 MB (2341982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be3b00556eed7fd45d80af40b3d4dedc00053ccd6332e6bcdd0ad2984a0a4c8`  
		Last Modified: Thu, 02 Oct 2025 02:36:22 GMT  
		Size: 75.6 KB (75632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dd13f6fcf48247e5b5beb79fb40b5fa2f7a5c457dbc486a6fe288dc99ca03`  
		Last Modified: Thu, 02 Oct 2025 02:36:28 GMT  
		Size: 70.4 MB (70445220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre21-Semeru-ubuntu-microprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:76c4a46824d7804514f66653b30449e62595f8c4295f2f6b53077e2e1da49f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4261117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfee67bdb8397cafb7883a44bce6f6fdb590ee08eeec1a187ec755403d2871cf`

```dockerfile
```

-	Layers:
	-	`sha256:d1ddbf80a5fe6836e22270d9e4c7535ea13042ea54e66f9403d62d02550e9f6d`  
		Last Modified: Thu, 02 Oct 2025 04:11:35 GMT  
		Size: 4.2 MB (4224924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afd14670be57a624fbf80fa783cf5e7a4b92d6f2cf8633d68853972d25e47ed`  
		Last Modified: Thu, 02 Oct 2025 04:11:36 GMT  
		Size: 36.2 KB (36193 bytes)  
		MIME: application/vnd.in-toto+json
