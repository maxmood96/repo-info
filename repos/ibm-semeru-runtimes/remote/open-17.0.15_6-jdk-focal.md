## `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:015b875410e888c0d39c99673e48349147d1827fe725fd47d50eeaaf564e98fa
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

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:b56a4d53ae674cee4648882ea34f8309cf9644c546e52d26e513ff1f70a79033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268407774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f6144dd050f5fc49f9ee167963d798c9870827f79c588c1abb6b591fd4a8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in         aarch64|arm64)          ESUM='08a982b6fbca457718bc43d14f1e836d7aa93eeaec7cd308793f990f8a5755ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7df65eeedda313cd73d28e6f46029f48b96e4d329066f0438b9b2b43aaafad59';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='41831486054fab00e1ea925b465ee162ba9ad8b65420d50ff7b3dbccd11e1542';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='214ad153737665e833bc0b5f67bcbefa2448e6254cec265c7e941db1162c3758';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa88cfdb0f96b6cd794ca2159f3423d4e87a5a938a53339bf05bc7c066217b7`  
		Last Modified: Fri, 09 May 2025 16:44:32 GMT  
		Size: 16.1 MB (16082089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566547d309af61b962cb27877d79574a4fff1c9b0c69450ecd563b64aa29f19`  
		Last Modified: Fri, 09 May 2025 17:08:25 GMT  
		Size: 218.6 MB (218635704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7ad3d902e6a4688b2e9179cc36f6866a4e4c979b46050d9201feb98aa91ea5`  
		Last Modified: Fri, 09 May 2025 16:44:30 GMT  
		Size: 6.2 MB (6179587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4a218d4ffcc77c805135283621ed3254340574c5a3bb3ae1ac71748186bb3415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3697007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b530a69f5378a3fed630f84457123e770f52f58dac36ef18712f4ba25b0f75da`

```dockerfile
```

-	Layers:
	-	`sha256:491836977d03f3aa81264bad451df3c8a676b995d3e08ad84847a1ad97389a50`  
		Last Modified: Fri, 09 May 2025 17:28:31 GMT  
		Size: 3.7 MB (3672954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05a69230763641ddc67764d165032b3ae620a29838755f4109845f7df658d8`  
		Last Modified: Fri, 09 May 2025 17:28:31 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:37763b8fa2c89930da393ebac85bd7954d63b82b2d23c6b56505e1c287b3f927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258548081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e618a00a418cb370c1ac72492222c9fdd0d19acb184bdeb3ef3626670b4899`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in         aarch64|arm64)          ESUM='08a982b6fbca457718bc43d14f1e836d7aa93eeaec7cd308793f990f8a5755ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7df65eeedda313cd73d28e6f46029f48b96e4d329066f0438b9b2b43aaafad59';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='41831486054fab00e1ea925b465ee162ba9ad8b65420d50ff7b3dbccd11e1542';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='214ad153737665e833bc0b5f67bcbefa2448e6254cec265c7e941db1162c3758';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba06366998e52bd013bc0ee5850fd47de26823cde6c431c95a5d57a7376d61aa`  
		Last Modified: Fri, 09 May 2025 16:44:29 GMT  
		Size: 15.9 MB (15941239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10678bab6884b1bd32cf940252afe371ed638e78214627963ffea119ffbc5f3a`  
		Last Modified: Fri, 09 May 2025 16:56:34 GMT  
		Size: 210.7 MB (210665051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa230f268b1f4ee7a942dd51850858a25fd846000d0c7529b12d7ff9f6a43613`  
		Last Modified: Fri, 09 May 2025 16:56:41 GMT  
		Size: 6.0 MB (5964130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:fe26555557dee9219b08dae1cfaf4342ad431e2819ae3a228a762b342adf8b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c570e22a288d0e0d6cb8e983efbd172e1d4d731b535ba9e2d724981a9ae5196`

```dockerfile
```

-	Layers:
	-	`sha256:d0e70ab2f861b8c88e9cbb35f9f1c35a2828c250a15fa26f5958fa89b7bd7419`  
		Last Modified: Fri, 09 May 2025 16:56:30 GMT  
		Size: 3.7 MB (3665656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2efc9809dab73555e04e5527ee211c9c65fc0cde2bf6a4545126bfa5c211d2fb`  
		Last Modified: Fri, 09 May 2025 16:56:29 GMT  
		Size: 24.2 KB (24164 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:76ec77429baf7d8dda3913219a6357a254fa56334cab37f5060c68984df0ceb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276310053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96aa6faa10c8a35363768a3ac73722f757dd59b2fd1728a2cb8ee2e84e94c2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in         aarch64|arm64)          ESUM='08a982b6fbca457718bc43d14f1e836d7aa93eeaec7cd308793f990f8a5755ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7df65eeedda313cd73d28e6f46029f48b96e4d329066f0438b9b2b43aaafad59';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='41831486054fab00e1ea925b465ee162ba9ad8b65420d50ff7b3dbccd11e1542';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='214ad153737665e833bc0b5f67bcbefa2448e6254cec265c7e941db1162c3758';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4cb3d0ec443b829573194b08f995a5c552514127b831013e5179ccd13d5460`  
		Last Modified: Fri, 09 May 2025 16:45:11 GMT  
		Size: 17.3 MB (17253640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf7ce62c905c14beb08454d367c7fa69259e7c31fddffd74d87aef05b124d54`  
		Last Modified: Fri, 09 May 2025 17:04:42 GMT  
		Size: 222.0 MB (221996136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad1f2f1ec61a71b441eba4b8cd99922fd903b26b83300d79159014ddff182da`  
		Last Modified: Fri, 09 May 2025 17:04:57 GMT  
		Size: 5.0 MB (4983331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:714f02e15f5e91992e8044f90cec1ac99fb5c0813c504cf4fbf0fe1e5d743125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3701479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9237b300e999a5c9f64ca92c471a123d81313416a2ce0b1b4ee5c5eb2051c50`

```dockerfile
```

-	Layers:
	-	`sha256:0d58087bed240e2d8c699f5ba4b0c20db7475a0abb2ae44fad0855e8f4851bc4`  
		Last Modified: Fri, 09 May 2025 17:04:35 GMT  
		Size: 3.7 MB (3677390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d45bd8f48cad87f15d0ab6441b94193fb60ffedf061d0dac8fb7f5abddd123`  
		Last Modified: Fri, 09 May 2025 17:04:34 GMT  
		Size: 24.1 KB (24089 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:aae0f7878d4684b60b7c50bf069ee3f478f3ccae41e8e93fa043d76335cd41a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265414115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0dca37dc874dfc5de044fbe99b575187208edcbb86b1673934ee85250ec02c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:20 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:21 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Tue, 08 Apr 2025 10:45:21 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in         aarch64|arm64)          ESUM='08a982b6fbca457718bc43d14f1e836d7aa93eeaec7cd308793f990f8a5755ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7df65eeedda313cd73d28e6f46029f48b96e4d329066f0438b9b2b43aaafad59';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='41831486054fab00e1ea925b465ee162ba9ad8b65420d50ff7b3dbccd11e1542';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='214ad153737665e833bc0b5f67bcbefa2448e6254cec265c7e941db1162c3758';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Thu, 08 May 2025 19:47:37 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490e56474dc5a70897468bf1180fb52b70c5adca8652d4449694fee19f2e1af`  
		Last Modified: Fri, 09 May 2025 16:45:07 GMT  
		Size: 15.8 MB (15769605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee64d8389def104107b08e7421a8922e56a7b6a4d1424405751b49ec7527858`  
		Last Modified: Fri, 09 May 2025 17:00:25 GMT  
		Size: 217.0 MB (216974118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57961661162ec13acf54775a59563bf5eb91745095212c8f6c0e56697b6c4912`  
		Last Modified: Fri, 09 May 2025 17:00:40 GMT  
		Size: 6.3 MB (6302202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.15_6-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d295834ff0d9c5a250abb32d3c0cf7015f558b9d52a215fd2117c8536293cc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef79472186b10ca4ee47b6af3bc4ca18a390058926b10d5d9fd153e49423b59`

```dockerfile
```

-	Layers:
	-	`sha256:c83bde91db7516b9ebafbbc642c999cd5365631d2d085fc7fd10c81c37e6d7d2`  
		Last Modified: Fri, 09 May 2025 17:00:22 GMT  
		Size: 3.7 MB (3674372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1ad7e709c35598ec4c7f1764a958ada635ab256c676817c91be5938dfd9ba7`  
		Last Modified: Fri, 09 May 2025 17:00:21 GMT  
		Size: 24.1 KB (24054 bytes)  
		MIME: application/vnd.in-toto+json
