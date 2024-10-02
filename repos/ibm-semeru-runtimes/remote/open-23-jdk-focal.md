## `ibm-semeru-runtimes:open-23-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:2682f04fb0766f44047060490d1a652cdac7390e6b138e0809ee07f9e1ee6a11
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

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:b15058e25d2c5a0cecf948465fea9fb3a67b50f7471b4e73be2b7bcb1fea8770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286929896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162e180af75785ec516bc8a28404ccee50bcf00a5fb7dac9b386dcd39945deac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fa85b1be0cd0db4306e401b57c1d3ec1d61b4ab7e1acb752e98b0962949be`  
		Last Modified: Wed, 02 Oct 2024 01:59:10 GMT  
		Size: 16.1 MB (16082602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0906883253f48f991f517373610f4833b196c41a47a3b1d87b9cc916411b82b`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 236.5 MB (236532675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698e25ca620abb3410fcbcf9f04e188426302fe1eef8771d189708564be2e007`  
		Last Modified: Wed, 02 Oct 2024 01:59:09 GMT  
		Size: 6.8 MB (6803567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e2f04e0809ed3dbd38a3b7d6b0c7db7ef81cc0fcac1c13d6edc0925c0d4cca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6cd23390a14b694f63088ee5d3b4ffd8e2dfc3ff1e022dd3c5fb5037537f7a`

```dockerfile
```

-	Layers:
	-	`sha256:2096ef2bb7ba954d4639897238e2f627c3796bb7f196cfdaba215ce32bfa2902`  
		Last Modified: Wed, 02 Oct 2024 01:59:09 GMT  
		Size: 3.7 MB (3657497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adfdb0b5f1453bcff81fe03f41d221a1d35b4346a2c9b58d5de32bc3997a61f`  
		Last Modified: Wed, 02 Oct 2024 01:59:09 GMT  
		Size: 23.8 KB (23796 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:ed0a15c1bec8ca01d5a757d8c0daf4ab309e2a29df07395196c88bf6fd181e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276595400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b32f00c6e5eede8c20195978c2b15fc4bb009af9b69eb40998b37620a0dfb7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36171ae5253d58adb579390ef5b05a287b9441a6744830621ef5564b5d3fb96`  
		Last Modified: Wed, 02 Oct 2024 02:34:30 GMT  
		Size: 15.9 MB (15944909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ee59feea7ba0ec4259af49a76953e59a6cf95566a0fd3cc759a4eb10bfb8af`  
		Last Modified: Wed, 02 Oct 2024 02:46:40 GMT  
		Size: 228.2 MB (228229383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed8fdf9fa2a3582f4e60beddefe69fda3459265303935ef7ce6445d38b4996c`  
		Last Modified: Wed, 02 Oct 2024 02:46:35 GMT  
		Size: 6.4 MB (6447516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:42852e63ac827b175c81bd285587b1bfc1e68ede17f0a5dabf2e782d2492b2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578d2e0a15166ab2d7921d734e7825e74b0c5fc33d59eee52db2466fc2857e73`

```dockerfile
```

-	Layers:
	-	`sha256:3f9cbbb8c1515bec8c0724d6c7948a72eb6cb20b123131f3ee36b2c5d7d5c992`  
		Last Modified: Wed, 02 Oct 2024 02:46:35 GMT  
		Size: 3.7 MB (3650186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f45da4c039252e17e5b54cd7a784e88f88c7246c13e3cc7ae082258fa31ec78`  
		Last Modified: Wed, 02 Oct 2024 02:46:34 GMT  
		Size: 23.9 KB (23899 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:b58993940d2c352f129794391183b71d8feda113a2ff3fb28150f64819c7b7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294451654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179dfe7796af00b70d3be3a9817d39f2e57f2ef43f5243158820672a50ca9712`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ffbeb090b7e1eb7eec8500dda28dd2af82398e770eec9f8262e68ec6c6162`  
		Last Modified: Wed, 02 Oct 2024 02:13:05 GMT  
		Size: 17.3 MB (17256388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa6dd4b787b0c47dc02c68651737fd4c9f61000d11e4eb471f9ff5efa3937`  
		Last Modified: Wed, 02 Oct 2024 02:29:40 GMT  
		Size: 239.7 MB (239670399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cece8308962887fec20301d5004fde7eb3a5aaf786cb9e2450755f9f472dd80b`  
		Last Modified: Wed, 02 Oct 2024 02:29:35 GMT  
		Size: 5.4 MB (5448533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:952c4234abbe8b9ca0cd4d232c386f3703698e64e0cf6ca01c8d00b604258741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5852646638c78110990df962a1b6266bf1ef4f5ddff5c9506c719e14fe00dc1c`

```dockerfile
```

-	Layers:
	-	`sha256:0a2c8f8b859760a5910e5284b07af0a3df76da25a4f3bb331fed8c452456781a`  
		Last Modified: Wed, 02 Oct 2024 02:29:34 GMT  
		Size: 3.7 MB (3661932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee1461994abc8d2bc610db3018857f6a04b103671e7372bf5837be13507e646`  
		Last Modified: Wed, 02 Oct 2024 02:29:34 GMT  
		Size: 23.8 KB (23826 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:fc8ebccfbf221a8a8b085538c84d25f385e5c6739aaffec1f91ae128c6d14377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283609528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8653283a4fb36a9598a6d58bfaacc39842ea0d458b18c814238a1a9918589047`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:5e84e73c86cd80310316bdb1d20baeccb3a0d4ffc98a27283aa05f904ec53469`  
		Last Modified: Wed, 18 Sep 2024 05:33:10 GMT  
		Size: 26.4 MB (26365746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9a2b361f32bab4ccc11380a820a76e721926a15104f1b1d92fc1d9c64b152`  
		Last Modified: Wed, 02 Oct 2024 02:04:47 GMT  
		Size: 15.8 MB (15773148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d710c944f4d453955b51d0f025eaf11ff907c2a96b0d4982afe26be3f01363`  
		Last Modified: Wed, 02 Oct 2024 02:19:41 GMT  
		Size: 234.6 MB (234626072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39ba47f2cdd7aba5a9febea667744952f17da02f29a771313e74192d5e55b80`  
		Last Modified: Wed, 02 Oct 2024 02:19:38 GMT  
		Size: 6.8 MB (6844562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8d793f0f8f3f55f62826fb50ff2ff4ae53382b1031f2c8c62a04fab423c6c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbd111c1ef5ab6f152e9b5fce37b12fd46cc47e4df65735a885f50da6b1c423`

```dockerfile
```

-	Layers:
	-	`sha256:dd86db6c47f0f15f35461d38112dcfb167b5fccbde65c2a67cfe534dfda462e6`  
		Last Modified: Wed, 02 Oct 2024 02:19:38 GMT  
		Size: 3.7 MB (3658918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a6c13c815b0a5d36fe529a3309f1716bab988a1775a4b787dc39b7d3b5ebb3`  
		Last Modified: Wed, 02 Oct 2024 02:19:38 GMT  
		Size: 23.8 KB (23796 bytes)  
		MIME: application/vnd.in-toto+json
