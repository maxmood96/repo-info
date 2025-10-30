## `tomee:10-jre25-Semeru`

```console
$ docker pull tomee@sha256:a3b8041a7a360d2c4cb1c8b543187c15cfe1cd63ee712efbde51e25262a173ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-jre25-Semeru` - linux; amd64

```console
$ docker pull tomee@sha256:a069e512d66a5fc29d26de91b9907dbad9e23a94f8a56103457869ee0794ed86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179907561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a793800765292a436acfb6bb3b9c606edba1cff9c0efa3f20177a44bfdf70247`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:58:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:58:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:58:43 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 18:58:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f917271612b0a29dac208bcbed1544008223ab96e0a000c6c8ca59d58cecd83e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3f3a6e3e1f0f29cebb7b8a0e8661b4e59cba99aae3752f5c7c131eca3ab4ca57';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='386ac1e3ef8560b6c86896e70f27978629f4805e924eb2eea68278c28eed14fb';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='2bdbc0dabb35d4bdcbc7235a60f3249f651b0970c9225d1355885ef4896de623';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:58:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:58:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:59:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 18:59:17 GMT
CMD ["jshell"]
# Thu, 30 Oct 2025 19:15:35 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:15:35 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Oct 2025 19:15:35 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Oct 2025 19:15:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 19:15:54 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Oct 2025 19:15:54 GMT
ENV TOMEE_VER=10.1.2
# Thu, 30 Oct 2025 19:15:54 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 30 Oct 2025 19:16:11 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Oct 2025 19:16:11 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Oct 2025 19:16:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52668bae106c3a2c744bee4b95333514ac52fd6888903d78b32d37cb168a59e`  
		Last Modified: Thu, 30 Oct 2025 18:59:39 GMT  
		Size: 12.2 MB (12171677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d358bbdfdc8f1e53e89cbf059bf7a697e8a13b65ac97d5bb334a9adf8023e15d`  
		Last Modified: Thu, 30 Oct 2025 18:59:47 GMT  
		Size: 59.7 MB (59660176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e4c842092d769f4ab54465de7294f70c09d9d67220b01ee61b17b0d57bea37`  
		Last Modified: Thu, 30 Oct 2025 18:59:38 GMT  
		Size: 5.7 MB (5659922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ab4b3cefd3db983aadeab1b845aed5cee6afb02950f7a96913c38a681591e6`  
		Last Modified: Thu, 30 Oct 2025 19:16:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d70dd1b2cdc31b216b46e1078283d8ffd6e60303ddbed5c0866286ff7bd464`  
		Last Modified: Thu, 30 Oct 2025 19:16:30 GMT  
		Size: 2.4 MB (2357834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555536bfb7f919fd1cc249dc96280a162f81d703a9be7abaf36fee984b7496af`  
		Last Modified: Thu, 30 Oct 2025 19:16:29 GMT  
		Size: 75.7 KB (75682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c2f869fe9b58cc92397a2b3d9836610ea4e8f450554e53d29c1a1f5be3510`  
		Last Modified: Thu, 30 Oct 2025 19:16:40 GMT  
		Size: 70.4 MB (70445249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-Semeru` - unknown; unknown

```console
$ docker pull tomee@sha256:2424d96dbfae32dee0967d80a80e60901e39045ad5034632e32996b44bb18cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d354e128474c1712e3f4dd9a5a793ddb3850348e0e370eac7c85693ba825910f`

```dockerfile
```

-	Layers:
	-	`sha256:798ec988114251488e1d6e5a52319b318e6d62f4c47ad968d55525dd6c937461`  
		Last Modified: Thu, 30 Oct 2025 22:11:22 GMT  
		Size: 4.2 MB (4230613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dacd23d55c8132139bb9069dd9389dd8ef705e49a4387d4e5dfd8ef490ca9e2`  
		Last Modified: Thu, 30 Oct 2025 22:11:23 GMT  
		Size: 35.7 KB (35653 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-jre25-Semeru` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:df3445eac43a9b8dc7b98f46e5f09f799306711ad82f158e3d4e7d359090413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175554963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b7e39d12fd4d4f8245352fc1d47a5e7cd933513438e5e431c38edacb038e41`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:55:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:55:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:55:14 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 18:56:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f917271612b0a29dac208bcbed1544008223ab96e0a000c6c8ca59d58cecd83e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3f3a6e3e1f0f29cebb7b8a0e8661b4e59cba99aae3752f5c7c131eca3ab4ca57';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='386ac1e3ef8560b6c86896e70f27978629f4805e924eb2eea68278c28eed14fb';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='2bdbc0dabb35d4bdcbc7235a60f3249f651b0970c9225d1355885ef4896de623';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:56:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:56:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:57:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 18:57:11 GMT
CMD ["jshell"]
# Thu, 30 Oct 2025 19:56:41 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:56:41 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 30 Oct 2025 19:56:41 GMT
WORKDIR /usr/local/tomee
# Thu, 30 Oct 2025 19:56:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 19:57:01 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 30 Oct 2025 19:57:01 GMT
ENV TOMEE_VER=10.1.2
# Thu, 30 Oct 2025 19:57:01 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 30 Oct 2025 19:57:13 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 30 Oct 2025 19:57:13 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 30 Oct 2025 19:57:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5fe7e1d5c811a3b4e2a42a2401d7ecb2b15e487c6c1e9e89554211fecf1ee1`  
		Last Modified: Thu, 30 Oct 2025 18:56:33 GMT  
		Size: 12.1 MB (12129982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674b66540ebf7b192cf18c12f8443e2e69644b04f3806b0ef25bd7543879aa4c`  
		Last Modified: Thu, 30 Oct 2025 18:57:32 GMT  
		Size: 57.9 MB (57900957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb51acf6ce5c6517fea8590e187b8407a4467197e2842b2497f407326c87dadb`  
		Last Modified: Thu, 30 Oct 2025 18:57:32 GMT  
		Size: 5.3 MB (5277864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d109e437949970d56e0c8bf00c4fb948171dab667d9c1ae702585f7d932f2`  
		Last Modified: Thu, 30 Oct 2025 19:57:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65340d2d53c70f3a9e00f24882af9979cd763eb2652d96ea0fc336020278fa5b`  
		Last Modified: Thu, 30 Oct 2025 19:57:33 GMT  
		Size: 2.3 MB (2341921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2847d5828f453b206560b2e3d01f39710259fb527b0ad4e025418abb3a09b`  
		Last Modified: Thu, 30 Oct 2025 19:57:32 GMT  
		Size: 75.7 KB (75664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec4cb9bb3e8b3ff80ef87b713e54b3aaec2c148641df675dc7c7fe79f1078e8`  
		Last Modified: Thu, 30 Oct 2025 19:57:38 GMT  
		Size: 70.4 MB (70445264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-jre25-Semeru` - unknown; unknown

```console
$ docker pull tomee@sha256:4b681b3f3f9a518b09a70a65e8fbd526ef75436d7e751187a637621c54b37e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4265489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec28c8ef8a1c66f03df3e480e88136498ef8fca3c4e0ddc09bebc79233fc1ff5`

```dockerfile
```

-	Layers:
	-	`sha256:01f9a6e9712eb2a61e5a0f5519464434388c377a77c2e10a5338875cac211d8b`  
		Last Modified: Thu, 30 Oct 2025 22:11:28 GMT  
		Size: 4.2 MB (4229351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d272e99c67de004bad710aec926f6cba4138f122409e4eb5c79614c9ced0dc`  
		Last Modified: Thu, 30 Oct 2025 22:11:29 GMT  
		Size: 36.1 KB (36138 bytes)  
		MIME: application/vnd.in-toto+json
