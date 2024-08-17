## `ibm-semeru-runtimes:open-22.0.2_9-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:a6cf7a2a7f0cce1402b5cde178fa00669d5d4a34f3b7999cabcd505486ddca4a
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

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:b57e15e5e63cb6ca4f257b59700b0ab0ab77db4e50a71e53c736879d9c37950f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102258869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4286cbbf982153c0912ae37926ca4a052a229015e3aca76c5c4351b5b299526`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9f445cb0b7f70e3bba62fb9fa8f6248010d17438a38ac663fed06c4d22d69c`  
		Last Modified: Sat, 17 Aug 2024 02:05:03 GMT  
		Size: 12.2 MB (12156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0de6e36b439e75579a5148b38a33c6810869b32b90aeb1e6dadaa219ab2d05`  
		Last Modified: Sat, 17 Aug 2024 02:05:04 GMT  
		Size: 55.3 MB (55324749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e81207d37a9c0a1ce6ece9bb1e25ff9f1a40fe405de6a244e10f4a316d45978`  
		Last Modified: Sat, 17 Aug 2024 02:05:03 GMT  
		Size: 5.2 MB (5241567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ed06fc5a952c8e3caf4c8da42ee274d42de7f05f3ae5a846fd0508f64e29f6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3483920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0227870961fc87d04f509f47254cbdf1f09b03662789dbe350047519f61d4416`

```dockerfile
```

-	Layers:
	-	`sha256:ab521e5830d6c78968bb889c8168183d7ab273dab6f9b56a0cb1b99f586ee8cf`  
		Last Modified: Sat, 17 Aug 2024 02:05:03 GMT  
		Size: 3.5 MB (3459522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1baac6509eb86fd8770babe0fc424a211103fc707e1d66342bc056bdb074f2`  
		Last Modified: Sat, 17 Aug 2024 02:05:03 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:6083e8fb8510b231e7bf4b94002f05e61ffa533ad38df7fb17330f38c2a9d231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96097130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71682204c6545602cbe110b27d59cdefdadd3845aa106e39fbecc3892ffd8e17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796176255eb9eadf7741e60b3298ab78bb156acff4ff0b231c1728a3fab9c654`  
		Last Modified: Sat, 17 Aug 2024 02:29:05 GMT  
		Size: 12.1 MB (12114317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd91f6c4beda4f000df785a51912a7c6f89509a66159e3e44581db499db5bb7`  
		Last Modified: Sat, 17 Aug 2024 02:50:15 GMT  
		Size: 51.7 MB (51691489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7183cae66631bbd3ca4631591eaee037f2c8780ca5186aa7c1eec86ee3418bca`  
		Last Modified: Sat, 17 Aug 2024 02:50:14 GMT  
		Size: 4.9 MB (4932641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:15fd49bee9cbce443fe8a53ace7e2d9527bad1979911bbb489d3f72d67b30d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01340a874f11e0cba49371619d4fb64f59b2ab93c8b3c0044af37b75c750d0ac`

```dockerfile
```

-	Layers:
	-	`sha256:d900b732deb52ff78c45c0f2af6b42b405eba1e74b2783ba957531107fea267c`  
		Last Modified: Sat, 17 Aug 2024 02:50:14 GMT  
		Size: 3.5 MB (3459811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2e75a8e4390f8a1cd71724a49e5e414bae4608170e96d18bc29da4db667dcb`  
		Last Modified: Sat, 17 Aug 2024 02:50:13 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:c876eb049b2059f9311749bcd05a1cb580a13b845bce8dcc6be2aa6619d39632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108287886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7440ba58a20c05135a172912043f0385fcd38b54512298f23fa842f5e3d1974`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034c9a8e8a92761eab1079b6deff5f91278bcf3719ef203182c3fda1ab19c29`  
		Last Modified: Sat, 17 Aug 2024 01:11:07 GMT  
		Size: 12.9 MB (12888375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981b5f3d687972bfdc2bfa719a5d48db4591d46d29957811f8b13fefada8231c`  
		Last Modified: Sat, 17 Aug 2024 01:37:25 GMT  
		Size: 56.9 MB (56938725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdc72fad76fc2e500642deda1bb6051720eecf58d34f67a7381eb485ee5213`  
		Last Modified: Sat, 17 Aug 2024 01:37:23 GMT  
		Size: 4.0 MB (3996608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:70b54cdae5dde6a40b079ac3f105d5da1a15b2647f54cf46434c0cf3c4b86378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4ac8289f411bbf8706ea1f183e1d30f266d21785b9dd9dfa2153c38eecbccb`

```dockerfile
```

-	Layers:
	-	`sha256:ba5b4701aeaf929436005fbcdacd82edf5a853fbd08e31fcad8209084995e173`  
		Last Modified: Sat, 17 Aug 2024 01:37:23 GMT  
		Size: 3.5 MB (3464022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93eafeb5443d3c7ac78fcb48ecba371f3719818b5902a7a63c0b484bf9088b14`  
		Last Modified: Sat, 17 Aug 2024 01:37:22 GMT  
		Size: 24.4 KB (24439 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:637b357b77aeb306c9c9aafa13d141942775f8bf0a01679829809122980d0e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100189348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308973c695357bd531fe9a7f52ddf6cc1d70cca1ca37dba3895e14eac98856a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a83917f7a3690422ed69c46b3c3cc9974d2c6923abc79136b0058ca106546`  
		Last Modified: Sat, 17 Aug 2024 02:04:16 GMT  
		Size: 12.2 MB (12203845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edfb0375e0dae165a8e3d830a3f794e4c660fa33fbe42b4315a2d65faf444d2`  
		Last Modified: Sat, 17 Aug 2024 02:30:51 GMT  
		Size: 54.7 MB (54656856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611f149bdce79e9a65f5d4e11e77c06355e1b4f8363f34fa699ce18c03cb142`  
		Last Modified: Sat, 17 Aug 2024 02:30:50 GMT  
		Size: 5.3 MB (5327325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:de8056bf4e76d036185b04b9bd929bc53eb0ca99f5e84bb3d470d63a6bd875e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c10f7da24746691696e340d46b12b3dbc795898e8c2fa30de1a5e1297c3e964`

```dockerfile
```

-	Layers:
	-	`sha256:b754469f95c67aa2ddb095893decd28e198d610ba4e30d5c8bb7fcfd9b29020e`  
		Last Modified: Sat, 17 Aug 2024 02:30:50 GMT  
		Size: 3.5 MB (3460649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cfbd090e406355a06dc4cf9ccffd08ca015a39f6efd39bd8204cef4963a5c1`  
		Last Modified: Sat, 17 Aug 2024 02:30:50 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
