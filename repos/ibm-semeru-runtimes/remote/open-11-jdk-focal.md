## `ibm-semeru-runtimes:open-11-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:63ab340939539500afb94ee026e3defb0826a323595baf90937033fc625e6088
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

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:64973ab4044dfc92174a397a12aa229a47463e5047fd15fcec579e6df57f35d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263388513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fc2060f9d6115a060143b4ba4ef8038ad1501ee70a0d44fd68fa8c84ff7f5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b3f5347f835524f0e228ce9f81da16974ba1a519472fde8de0f7d62140d73`  
		Last Modified: Fri, 14 Feb 2025 23:30:29 GMT  
		Size: 16.1 MB (16076082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93ccd1a93b537867b996a104fde2acfd583e1bd22a5cc68f25d8009d081f2d`  
		Last Modified: Fri, 14 Feb 2025 23:30:39 GMT  
		Size: 214.4 MB (214399984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c8606e1ff11fa9425718b7eb2613a97a07394d7faceeccc9c8659032f6f47d`  
		Last Modified: Fri, 14 Feb 2025 23:30:28 GMT  
		Size: 5.4 MB (5401387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ccafd28ee9f74fcd27ba981aa05daf03680167f819cd716a36eb6e5572be8a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cca7eb112b865cdc0902f622eff93998e3afd69ee47c3dbed8966ef212e5d4d`

```dockerfile
```

-	Layers:
	-	`sha256:dc0f6df6be597f778baf5cfb8b531abdcff7002b8567451b59bfcb2d18320ed7`  
		Last Modified: Fri, 14 Feb 2025 23:44:20 GMT  
		Size: 3.7 MB (3687113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3796ff0fdbbd6f198d961d2a924250ef1cb2d8df0e437771665dafaf9d8bc5a3`  
		Last Modified: Fri, 14 Feb 2025 23:44:20 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:2a2a060aab97a46c634c119b6feb6b53815373744e2c24303e513dcdb33b8cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252396212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13f484f360cc1880aba43d70a8b3c71580e849b66670bc7768d9d5a0792491b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='73eac0441938990a87d188d8ae3f9de6a0cdb89c3b75e1647411ec0a093ca414';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1dc99080a9e1b3b19f0c9c7063d920d9a0ced8b35e5f7c1fc9f6769c5a9c6a37';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8bdeed45af4087352e969f1206fe697473b1fa2ee2e75e671bc32c54c38fa420';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='c908ca250d85067813de0fcfad4d9d0f06b4b09c42bba7c446a0250c55f817fb';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ef414821b192c760ac142f4466c76cf31f2fbfd0e37a74b4ad61c78e57b23`  
		Last Modified: Sat, 14 Dec 2024 08:03:17 GMT  
		Size: 15.9 MB (15945040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cba4c58c0b6c69bb7011b91ca2b20325f681e95e56be7ee745629e3999876f`  
		Last Modified: Mon, 16 Dec 2024 09:18:42 GMT  
		Size: 205.3 MB (205346139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854ada12ca31ef05d6596aedcfe424b95b889765c51ee907641ed9939c16dd7e`  
		Last Modified: Fri, 20 Dec 2024 08:03:32 GMT  
		Size: 5.1 MB (5131205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:31ac7bc19dd1cd9e0c11a71953611278d9480d8b47deed18cab2dc9942faad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f920f3109702c6e6f3212889c70f5c7cd6dfd251041cbbef7a1840bcfa6f62`

```dockerfile
```

-	Layers:
	-	`sha256:4d3271e877c619bd56f1bbf027e26e1949b35d494de31ff42eb661ec1be31091`  
		Last Modified: Tue, 07 Jan 2025 02:37:31 GMT  
		Size: 3.7 MB (3676371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c139e13e980e7baf90b339526393d7ecd356e87b66e6130f7d593f2dba209cd0`  
		Last Modified: Tue, 07 Jan 2025 00:38:09 GMT  
		Size: 24.1 KB (24136 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:47c346ffd9985a66455002bb48115090d65055e2faeaf58e5579436dac7cc45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269704088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2952a3f0cb4f087bbf778f3f35633f3f432e0b1f5d7dd14777338fb940b6047`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 13 Dec 2024 21:07:44 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55caf6c5ab5a2f4dd7778bf3241e397e7a5a65adbf72e89249f83424684d3d6b`  
		Last Modified: Sat, 15 Feb 2025 02:03:22 GMT  
		Size: 17.2 MB (17247743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a406c8ae148b14d5b5bb48cd5d1efbcc7f873f19f8455e203a5159eac454ba7`  
		Last Modified: Sat, 15 Feb 2025 02:14:16 GMT  
		Size: 216.0 MB (215967177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53018a631332b0ba4adbcd22074ada4c3418d11f227b28fe7262a1210f4b7827`  
		Last Modified: Sat, 15 Feb 2025 02:14:11 GMT  
		Size: 4.4 MB (4412662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e894c40dc5d312bf27118e1898b5d64eec2e65fc312ff58fd4f87fd5ef18c3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1050696e602ed219516cb67dbd0020198587fed72481438fbdcb2b6041415c`

```dockerfile
```

-	Layers:
	-	`sha256:93a84dbae6368477804c80f1aead67ab0beca08d2994f714b119acb6dbf2df65`  
		Last Modified: Sat, 15 Feb 2025 02:44:25 GMT  
		Size: 3.7 MB (3687822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64393d430402962e91b3588267f4badcd50821ac16f9ac817e09e6a8d2f9b386`  
		Last Modified: Sat, 15 Feb 2025 02:44:25 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:3f74fe7a7deb763f11530d7ba3ecd7210fa479993f4def5f59900e1f16fc4e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257725722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a027836303b3a591dc2529d3933be9f0f7cd7f359b33352a0d94c83cf4dd971`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='73eac0441938990a87d188d8ae3f9de6a0cdb89c3b75e1647411ec0a093ca414';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1dc99080a9e1b3b19f0c9c7063d920d9a0ced8b35e5f7c1fc9f6769c5a9c6a37';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8bdeed45af4087352e969f1206fe697473b1fa2ee2e75e671bc32c54c38fa420';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='c908ca250d85067813de0fcfad4d9d0f06b4b09c42bba7c446a0250c55f817fb';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 13 Dec 2024 17:08:28 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76440d6755e318199681b6d987a4b8660d5945e0ea29db0a034c2ad4c00548`  
		Last Modified: Sat, 14 Dec 2024 02:44:22 GMT  
		Size: 15.8 MB (15773072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d6dbe1cc28ea5319d157a55e0a4a8dc844ab7dc11de146a83fa1bbf7f9e9a2`  
		Last Modified: Fri, 13 Dec 2024 18:12:24 GMT  
		Size: 210.6 MB (210571605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9fd9616776ce0ebf9353e6da0ddf349bb68167843efcdb2a64556368fd03ab`  
		Last Modified: Mon, 23 Dec 2024 19:56:41 GMT  
		Size: 5.0 MB (5015066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:92fbbe1ee5b5ac01871f766ecb78ac9bae77a280cafa8d01898f777ecbec9542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3709112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877ec162091d5b0dac12ade877f1e574279c36191c67ec53e030c003b6ea26b`

```dockerfile
```

-	Layers:
	-	`sha256:fc08526784beb052c7f84fc2b079cfadbd29aa27ac24382d9c5f37adf29629ce`  
		Last Modified: Mon, 06 Jan 2025 19:44:26 GMT  
		Size: 3.7 MB (3685087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdefd4a4a448205b7f011c805a89d615d98fb59403ee2984bf634e8e0d1ae823`  
		Last Modified: Mon, 06 Jan 2025 22:40:39 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json
