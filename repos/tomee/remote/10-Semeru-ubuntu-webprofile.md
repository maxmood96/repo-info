## `tomee:10-Semeru-ubuntu-webprofile`

```console
$ docker pull tomee@sha256:dc709a3ed758803dddc971495aa6773e26ce2bb51fa6d5f67f553597bbaf3a7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomee:10-Semeru-ubuntu-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:18239dd76c3af58d04386e679ecf5e241e3da0797aecf552ea226123764b1fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161588536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a0faba39b170a73017cf912541272f0ba883dd560e76e40a382c7f243694b3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 18:18:20 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
WORKDIR /usr/local/tomee
# Tue, 23 Jul 2024 18:18:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_VER=10.0.0-M2
# Tue, 23 Jul 2024 18:18:20 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 23 Jul 2024 18:18:20 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 23 Jul 2024 18:18:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 23 Jul 2024 18:18:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cdd08645bf75b4a165cf353b8ee5e3b6030df892d333fda68f3a2ef7d08e57`  
		Last Modified: Wed, 17 Jul 2024 17:56:03 GMT  
		Size: 12.2 MB (12156533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2799fae833a91bf66a37eb1b4282c2059f25e18679967ac847d040eca6d3fcf7`  
		Last Modified: Wed, 17 Jul 2024 17:56:04 GMT  
		Size: 51.8 MB (51801964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d2ca882a4ea3eac23d98066c79e6779e03b6dd8a7563c81c3eacec986f5f41`  
		Last Modified: Wed, 17 Jul 2024 17:56:03 GMT  
		Size: 4.9 MB (4925828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742871068545aa8e6d8b8be54511333021f39c41ea8978ac7b5be3fb4b24bc81`  
		Last Modified: Tue, 23 Jul 2024 19:12:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a31b1cb174cfb7252989d15fb736ce67c558e233c624b21a2c9ddacb8e6b92`  
		Last Modified: Tue, 23 Jul 2024 19:12:34 GMT  
		Size: 2.4 MB (2356383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597822c523bd155f78d09d9e9d2ace521e94e049c5c9c4e9dda5717d6b48a89b`  
		Last Modified: Tue, 23 Jul 2024 19:12:33 GMT  
		Size: 69.2 KB (69204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9221c6c2207dbc5551e62c8a103204411a47ec4538cf419c1c08d994506f4f`  
		Last Modified: Tue, 23 Jul 2024 19:12:34 GMT  
		Size: 60.7 MB (60744367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:54c98addc76ac80c5e11a0c89fef81d831abdc1f74eacfc34bdf0cdcbb4585e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed108fadd73e4abe7e385e22f3eb2af3eb255bbc403b5db0e82f2d8c03fed1`

```dockerfile
```

-	Layers:
	-	`sha256:add1b3ab6ca98d118c894fbc882029050ff0fec84c8127abcc22a8d5a2fccaaa`  
		Last Modified: Tue, 23 Jul 2024 19:12:34 GMT  
		Size: 3.8 MB (3802293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25956011bf7600df4c19e1cc1ff7dee67042bb690797bdb9618b3003920407a`  
		Last Modified: Tue, 23 Jul 2024 19:12:33 GMT  
		Size: 27.9 KB (27864 bytes)  
		MIME: application/vnd.in-toto+json

### `tomee:10-Semeru-ubuntu-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:e9c4b3d939dae92b8f781e3483cc029adae073cf8db2760260918e2dc1856983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153990147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a938094d91e9f945c20865f05d2584fed7b092dd28a43fde142565c5545c4d2b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 16 Apr 2024 02:54:00 GMT
ARG RELEASE
# Tue, 16 Apr 2024 02:54:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 02:54:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 16 Apr 2024 02:54:00 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:54:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 02:54:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:54:00 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
WORKDIR /usr/local/tomee
# Tue, 16 Apr 2024 02:54:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_VER=10.0.0-M1
# Tue, 16 Apr 2024 02:54:00 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 16 Apr 2024 02:54:00 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz* # buildkit
# Tue, 16 Apr 2024 02:54:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Apr 2024 02:54:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a73c992d8ae249d8805479ac497dac9fa0b1b48ab385b7d65a1b68d7dd3f7e`  
		Last Modified: Wed, 17 Jul 2024 17:58:36 GMT  
		Size: 12.1 MB (12114226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db374f73c52ab08440f55d862929f19e0099fc10512477644151d0b9cf9a0ff`  
		Last Modified: Wed, 17 Jul 2024 18:05:14 GMT  
		Size: 48.3 MB (48326042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b53ae9469bc737cc8f50f8d21d0daf2e815f0d8ada06498b257a3dc1419492b`  
		Last Modified: Wed, 17 Jul 2024 18:05:12 GMT  
		Size: 4.2 MB (4188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c605c8f4ce436005737a39d237e6d643b564e6c3c506d56aa13a32563f4070`  
		Last Modified: Wed, 17 Jul 2024 19:11:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850e3cc20f6201d2fc37f9ee4246e2b7d7cd6c30c3e81a27b52db30a429c5764`  
		Last Modified: Wed, 17 Jul 2024 19:11:20 GMT  
		Size: 2.3 MB (2341685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af61db54af3200cd5a6a675b896f797c7594b512af9fcbc5e53420d83891f186`  
		Last Modified: Wed, 17 Jul 2024 19:11:19 GMT  
		Size: 69.2 KB (69244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2463f8c0858b026a45856a509ff5a30ca4b81e46069f9c8d8447ee28381c1f88`  
		Last Modified: Wed, 17 Jul 2024 19:17:49 GMT  
		Size: 59.6 MB (59590054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomee:10-Semeru-ubuntu-webprofile` - unknown; unknown

```console
$ docker pull tomee@sha256:ae4782a9d932e400f624c30856c902e46cc023e4014ff93f54832d427f5b60ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7d6d0f556d34988c9a4187f3223af4f1070de5924c14da3d3261c6936b274e`

```dockerfile
```

-	Layers:
	-	`sha256:44428c1d1a29b6ad2e4ffbd055ee8e2e082d9980a2b6f96e05c88d0459a547a7`  
		Last Modified: Wed, 17 Jul 2024 19:17:47 GMT  
		Size: 3.8 MB (3799287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1bb9cbc4f22ac958c812133725ce7959c31c3e76ab338399093ea3c30987154`  
		Last Modified: Wed, 17 Jul 2024 19:17:46 GMT  
		Size: 28.3 KB (28345 bytes)  
		MIME: application/vnd.in-toto+json
