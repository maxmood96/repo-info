## `tomee:11-Semeru-ubuntu-webprofile`

```console
$ docker pull tomee@sha256:2470ce88df230bfcb06cb0e7b676c4bdf49c302c8585840e816c3b0cbf3613d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:11-Semeru-ubuntu-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:12bd5139acd455b3c7e7a4ce776882c95ea604dec9a71d8a4948a74a280880a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172393215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d636f2645894b4f1d62c232f629915a76f67c3f0365a79c1e5fba3cc4dbb920f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:18:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:18:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:18:21 GMT
ENV JAVA_VERSION=25.0.3.0
# Fri, 15 May 2026 21:18:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='191941c4353c703daae0111c676dcc9335519bd4cecd72ed8709badf16e35708';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_aarch64_linux_25.0.3.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ed82541c3a9f0b45b0e15fcd54ceb62ec970dffc9309d0c27d6fc70ce5d60bbc';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_x64_linux_25.0.3.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='78ac845aee34b34a8c9acba89e40cda02b2671e967745e604d4a8d33cdc9ee36';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_ppc64le_linux_25.0.3.0.tar.gz';          ;;        s390x)          ESUM='5f24293d1352355c1c77bd373a7fcf68a0f9dd986cc575f208cc72978c4ada53';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_s390x_linux_25.0.3.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 15 May 2026 21:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:18:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 15 May 2026 21:19:28 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 15 May 2026 21:19:28 GMT
CMD ["jshell"]
# Thu, 18 Jun 2026 20:44:14 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:44:14 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:44:14 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:44:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jun 2026 20:44:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:29 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:29 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 18 Jun 2026 20:44:31 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:31 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8d1e08fdf0b634d5a5704da4bbaf8301d6b3219afaae1648cf4895de7ac03f`  
		Last Modified: Fri, 15 May 2026 21:19:41 GMT  
		Size: 12.2 MB (12173229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314563d86adc877cbdd672404454b99e775b4e6407a0d515bc5a5f9b64eec7bb`  
		Last Modified: Fri, 15 May 2026 21:19:42 GMT  
		Size: 60.6 MB (60571206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621daeea923a69c30e67d88d644d2f9423b5dc08e853b56528698033ce790d1`  
		Last Modified: Fri, 15 May 2026 21:19:41 GMT  
		Size: 5.5 MB (5453065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902c0867a6d661c4340f304bc7a2703101cdbf09098ba3515a5c597622676a88`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d17e1669d7bb38ead094898e0e0a55b54f26555f3536c4a5ee8b5b4b7b377c`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 2.4 MB (2357736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6acf59d63c841b8b2eaab1184d751f95be49bac5ffdbb92ea499a4fd70a51b7`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 75.7 KB (75667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58396959e7e8c71e7eed46da5b44f8c2611cfe58bc4849628d316d501ebfb2d`  
		Last Modified: Thu, 18 Jun 2026 20:44:44 GMT  
		Size: 62.0 MB (62025423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:224366c9eb2c45de678a45c1e31c138dc41ae8808c074f89c7eefe9044518b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81df5187b9d341c0bcf56599aa0274d67d90d558e3b4d00e4d02f6a30053501`

```dockerfile
```

-	Layers:
	-	`sha256:17017b5fd9ca81354033f3d4e93514648b3def2cb51511520ab037253c5aadf1`  
		Last Modified: Thu, 18 Jun 2026 20:44:43 GMT  
		Size: 4.1 MB (4110268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d965239fab1ec1afb41c204a145c28d6fabee91d281a48bafbd34002cef69cb`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 29.2 KB (29162 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:11-Semeru-ubuntu-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:36ea85d4213cc0ec9582dd626f1e6337159aee6c90b0e93f385b25f97ba42a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167887446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829dec8b8c3741819f89d30a8cd954021c96b33e304a0b27b68292d966690b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:18:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:18:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:18:59 GMT
ENV JAVA_VERSION=25.0.3.0
# Fri, 15 May 2026 21:19:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='191941c4353c703daae0111c676dcc9335519bd4cecd72ed8709badf16e35708';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_aarch64_linux_25.0.3.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ed82541c3a9f0b45b0e15fcd54ceb62ec970dffc9309d0c27d6fc70ce5d60bbc';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_x64_linux_25.0.3.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='78ac845aee34b34a8c9acba89e40cda02b2671e967745e604d4a8d33cdc9ee36';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_ppc64le_linux_25.0.3.0.tar.gz';          ;;        s390x)          ESUM='5f24293d1352355c1c77bd373a7fcf68a0f9dd986cc575f208cc72978c4ada53';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.3.0/ibm-semeru-open-jre_s390x_linux_25.0.3.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 15 May 2026 21:19:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:19:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 15 May 2026 21:20:07 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 15 May 2026 21:20:07 GMT
CMD ["jshell"]
# Thu, 18 Jun 2026 20:44:13 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jun 2026 20:44:13 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Thu, 18 Jun 2026 20:44:13 GMT
WORKDIR /usr/local/tomee
# Thu, 18 Jun 2026 20:44:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jun 2026 20:44:29 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   85FBBE98D6C37CDA8A7D8FF9F9FF83A48D339D37   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Thu, 18 Jun 2026 20:44:29 GMT
ENV TOMEE_VER=11.0.0-M1
# Thu, 18 Jun 2026 20:44:29 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 18 Jun 2026 20:44:31 GMT
RUN set -eux; 	ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if curl -fSL "$distUrl$distFile" -o "$f" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	};   ddist tomee.tar.gz.asc tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc   && ddist tomee.tar.gz.sha512 tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512   && ddist apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Thu, 18 Jun 2026 20:44:31 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Jun 2026 20:44:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5436112ffecd1dac709b2fa55d7f5f1182ff40bb99440207f0b60b05eac3536`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 12.1 MB (12144656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abd7187f7b67865791a8cc60920f7e595d2ff74bde49a524e6f4ce32b5fd910`  
		Last Modified: Fri, 15 May 2026 21:20:22 GMT  
		Size: 58.4 MB (58427275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f013a9666a75234afbfeb57bec30c3e0a5b723b9139e3ac795e54689a3602a4`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 5.3 MB (5260427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca389081b7040c4226ccc54418eb44d423c9e3d941849855e4b7d0b85bb7df8`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078fd14db641581bdaf3c4fcdb16d6e1d1fbd04af18e8c3d2dfe41c1ebaeba83`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 2.3 MB (2347186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124c3c1ea41a04d7e44d68ba6049b92c39e954a855d0887a5177af04c64a593`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 75.7 KB (75651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ab1ab928ed80f6c662031d2d2d096c0131b97ecabea9e6870d1494700f535e`  
		Last Modified: Thu, 18 Jun 2026 20:44:44 GMT  
		Size: 62.0 MB (62025423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:11-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:8c0d7b39a0731ec4536424e37c8ed85ed9986dd85a0bd07f79e2765e378ff9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca6f824b7f3a95ed2a94eec5c8e566e9be071b4858a8cea9641f9883b76d29d`

```dockerfile
```

-	Layers:
	-	`sha256:506f6b26ac125da103eb2812348e387e4f80742e80e74d3ce34b70ee86947811`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 4.1 MB (4108143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f2137e046aa314c1cd4830c7b1bb35b448208698528e2991caadc972d70c22`  
		Last Modified: Thu, 18 Jun 2026 20:44:42 GMT  
		Size: 29.4 KB (29407 bytes)  
		MIME: application/vnd.in-toto+json
