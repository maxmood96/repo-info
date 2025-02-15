## `ibm-semeru-runtimes:open-21-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:0cc3334c123d2136eb07c7094b3ebc3acf8e3ffb5dc98ddb2b565f36e8fa8830
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

### `ibm-semeru-runtimes:open-21-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:ceaa225afa0e0df486f68e70dc7a04e71d01a13ce7e9a699f2269316a343ac6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105037412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209cc0cac56824ef2ed41f7124ad10ab522e83a2ac8ff55678f1fbe7dafe4f05`
-	Default Command: `["\/bin\/bash"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1090db3f7b30b4a45e3d5f228ac529ace87000bd9b342d91a639f0181a0058f5';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='cca7d1599ff83063dd16965dcbf91915a7654e5086f3b3b71744adf7769d11de';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ece962ee7ce419e25048a89228b61c4ce8c318ec6fade470484d6537bb87ea3f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='ab2070fa866e86978a5a2753dfc6128fc2012b97bf4e95d888d3dda916844a52';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f87bc67efa69550e24f09f7f4725e0fbe7b7fcc03ae95c268e8b13678f502b`  
		Last Modified: Sat, 15 Feb 2025 00:11:29 GMT  
		Size: 16.1 MB (16075997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5359efb5f08488a950f6d7e95a344432d65b9f96cc3839e38f7d328d6791f0c`  
		Last Modified: Sat, 15 Feb 2025 00:04:08 GMT  
		Size: 56.3 MB (56340442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9317cb03e3eb280210fcf19dbf473865bb5ece670e3537b864c5a93d2c85211b`  
		Last Modified: Sat, 15 Feb 2025 00:11:30 GMT  
		Size: 5.1 MB (5109913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2a87a19f55c5722dd652d6b1849094243a57c4cd6ce104d83e8fe6e7631fa1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3614895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cb375751930ae9f1b87b7ee09bc102eb465699c6a262c86fc740d46d0b1b38`

```dockerfile
```

-	Layers:
	-	`sha256:68d4489cfa431072baeffa899d2066b13166762462fda5d9df050a57db2d2eb1`  
		Last Modified: Fri, 14 Feb 2025 23:45:42 GMT  
		Size: 3.6 MB (3590923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:909aa2e546177cd3f4523f0687f9e09c33fbb7dcb596be90c810351c1f8a3ac0`  
		Last Modified: Fri, 14 Feb 2025 23:45:42 GMT  
		Size: 24.0 KB (23972 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:6ee2e30b10f522e0c371b1c0d1680159611e600a2db4a2b3c7da09f2f4dfce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98858176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4a0aeae57d8dcbe46fa08e6fa896eb7f022ef2354bc41b059f406b034323c3`
-	Default Command: `["\/bin\/bash"]`

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
ENV JAVA_VERSION=jdk-21.0.5+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='27fb02bb8e409c5330bbed15f6dce74c3f8255c1f2ef937a697c1b903ca9477a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3cd0ac0e28ad83fe9097569c6ba0c84772d697c1a34fa5b93c9fcbe0493d43c8';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ab533e7d609382cda4e5abee38102f8a467f24db77886fa0f4c680d681cdf87f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='3d5787d519e24fb5de6e4e5db78e29cd25a72d9d6de4cc96d31d377199c25c4f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:9cba5f1f332060ee8dac55716c5418b188afae615154fba308f0608baae58a39`  
		Last Modified: Fri, 20 Dec 2024 03:21:52 GMT  
		Size: 52.1 MB (52065826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342896d787121593f5a3cb7a1f99e553175514493ec61af90c41daeee11034b7`  
		Last Modified: Sun, 22 Dec 2024 21:08:45 GMT  
		Size: 4.9 MB (4873482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8020592f7db7b1eba4cfad295dee6e4d5d0fc608193e11825dc41c815ff5ddc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b104df989fdbb66521d277e42dc1cbe0a1162214f47a3ac5a09b506c6e492b`

```dockerfile
```

-	Layers:
	-	`sha256:cc408eb6cf2d60bcc2dfd25867afbeb52c6a5942479313c8edf1398db202b846`  
		Last Modified: Mon, 06 Jan 2025 17:44:34 GMT  
		Size: 3.6 MB (3582063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1cc994026e502063d69f590272802c288bd0310c5a20bec084c75422d4f90fc`  
		Last Modified: Tue, 07 Jan 2025 08:38:14 GMT  
		Size: 24.1 KB (24106 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:032b63f41abd162b30e5091a3e9685b47ec939a7ffd6fb80ef3661e6d42dc689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110581633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63e1c8825bc1119fd26d8eb0ba4c1858c3b6c2b3969cd9261f9e57932c30ece`
-	Default Command: `["\/bin\/bash"]`

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
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-21.0.5+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='27fb02bb8e409c5330bbed15f6dce74c3f8255c1f2ef937a697c1b903ca9477a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3cd0ac0e28ad83fe9097569c6ba0c84772d697c1a34fa5b93c9fcbe0493d43c8';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ab533e7d609382cda4e5abee38102f8a467f24db77886fa0f4c680d681cdf87f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='3d5787d519e24fb5de6e4e5db78e29cd25a72d9d6de4cc96d31d377199c25c4f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 13 Dec 2024 21:07:44 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03062ba6cc89d48fbed8c001c307b5b41e0a5f776a5ecb43457bcbf48b0c0d`  
		Last Modified: Fri, 20 Dec 2024 10:07:50 GMT  
		Size: 17.3 MB (17256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604996204bc61fb27e6616a35cb437f058f76c1ffda407ead0df6feef4417507`  
		Last Modified: Mon, 06 Jan 2025 22:45:34 GMT  
		Size: 57.3 MB (57302197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e989efc36cfe47c9b696653f3aad96fd8385877504d3c1b642e0303e374b218`  
		Last Modified: Mon, 06 Jan 2025 17:44:35 GMT  
		Size: 3.9 MB (3946388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:56be6c621277153bca1cab9efb456ffa51dbb4566aa978955589e13d46748e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438aebf32f7db622612518b28f36d22ee7d08d1da55f023bc311ee8e3d7b0faf`

```dockerfile
```

-	Layers:
	-	`sha256:96a08917bc09b2d0a028667ffe95307be01868d97c8fbb3c67ea9cb9856f414b`  
		Last Modified: Mon, 06 Jan 2025 17:44:36 GMT  
		Size: 3.6 MB (3593172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0007a26c4dbf30de37bde7ee81306c28b9928a3eda39cfc0b4ba64d7f34ad86`  
		Last Modified: Tue, 07 Jan 2025 06:39:01 GMT  
		Size: 24.0 KB (24032 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:af144ba882bbc4edd9f36f565c9c867a5977bedcbb07756e1792f11b6399936e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102432734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1bb02f6bd1026f36d2b5a996815bfdcdf7b5d0f6b3cca7b6ce420649b11eee`
-	Default Command: `["\/bin\/bash"]`

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
ENV JAVA_VERSION=jdk-21.0.5+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='27fb02bb8e409c5330bbed15f6dce74c3f8255c1f2ef937a697c1b903ca9477a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3cd0ac0e28ad83fe9097569c6ba0c84772d697c1a34fa5b93c9fcbe0493d43c8';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ab533e7d609382cda4e5abee38102f8a467f24db77886fa0f4c680d681cdf87f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='3d5787d519e24fb5de6e4e5db78e29cd25a72d9d6de4cc96d31d377199c25c4f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:1a778403050c927fea60e0e803408ca4528da0ff1a70bc4209ba1a724eb93b49`  
		Last Modified: Fri, 20 Dec 2024 10:07:31 GMT  
		Size: 55.0 MB (55007211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecacfba1b60c81682c94c37e6cc7f6f80877dbb0bfc012277a65336274d7f64`  
		Last Modified: Mon, 06 Jan 2025 17:44:39 GMT  
		Size: 5.3 MB (5286472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:51ed544f479ab5c150dd10be322f4c35b158325894c2f7d93b4fb76ab8a25b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3614150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bbcf8236752d16acb0bd1f234cc6a00960620364a64aef0835d04b0925efc0`

```dockerfile
```

-	Layers:
	-	`sha256:5fd468ef9fc6918e93e7e033eeb936901a82126ff6439e5c087b28276b019bcb`  
		Last Modified: Tue, 07 Jan 2025 07:40:09 GMT  
		Size: 3.6 MB (3590154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0789f393982d31e0134cae5b05ad5e47abf620b6c96d6e8b3a18f6c0a7f11cef`  
		Last Modified: Tue, 07 Jan 2025 01:43:03 GMT  
		Size: 24.0 KB (23996 bytes)  
		MIME: application/vnd.in-toto+json
