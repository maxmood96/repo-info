## `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:1afbb73e8b8b2bd3287e8ec8264b50066c051abdd9748d9a7e20fbbbec9a20d3
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

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:9edfe344075ebb329e28a1d0611096507adabe4cdcd14fc3983f7cfe0139c55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104090356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b78fb93d9be29e04693e14bab0371c86d522164fa5ea16af00d73dd63e5c15c`
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
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d34ae11b6a37da60e58a0524e885a04eccd24a4164b8b8b8e6543b37c349f2`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 16.1 MB (16082600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066051e677d14afb3e2c328ac47a76746fadb086d19350270b5a9190d444be0`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 55.3 MB (55324812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81f46dc9ac62e9f9e8e25588ff88af144d6579d610f84a52a18c85a75c0bc2`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 5.2 MB (5171884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5a54a0035c9773c0ee6d2df9ff28ac4cec77b85161bbcb5d343ece267a4c2428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4753a5621cdcb106d0173fe7f94a42c3c168c1782361300af12f8be164dc8f4f`

```dockerfile
```

-	Layers:
	-	`sha256:a298bc2e669c1f1bd4e9602590880d16a03dee6208bc8e655740556f8e6c79cc`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 3.6 MB (3591650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3d628886b4ecca7139d26503a9de1bac626d34a9b246ee8f0300fe1e6c604e`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 24.0 KB (23976 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:83ce14a6b14ce4fbb47953247d077661746bc11b3c0497be77911fe59fe2d212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98493402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30e97a066165d3bd9232f8a447f732115ed253ae184d0db8548511a050370e`
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
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c87aac1d4ce7ba28204a4f8c7ccbc4da254cdd092097b48a1bbda757f24ae4c`  
		Last Modified: Mon, 04 Nov 2024 22:06:02 GMT  
		Size: 15.9 MB (15945006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6d8d0e59261cdea7a4b93b9fd1536e67ba07b8b9c675b125c56686448c1559`  
		Last Modified: Mon, 04 Nov 2024 22:30:32 GMT  
		Size: 51.7 MB (51691338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90bc77a6a4587d4a0df4139f7ea569d24597e03ebb58cc63c2cc7c3b058612d`  
		Last Modified: Mon, 04 Nov 2024 22:30:31 GMT  
		Size: 4.9 MB (4883230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a31ece04b96771e8a9eaf739549ca86eb8d7a8cde0e60d18150dab21189f25d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9932f6e74480ea577c08928ed5c6456bf250470e80aa5dd4973e087acea794`

```dockerfile
```

-	Layers:
	-	`sha256:a558072f27b0daf32b343c7090ea20bff72fd523513dbb917285543d8291529d`  
		Last Modified: Mon, 04 Nov 2024 22:30:31 GMT  
		Size: 3.6 MB (3584965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f357b7c47ebd516bd09d9f6d80da05c0937a3b2ebe602fa12c258c59760dde7`  
		Last Modified: Mon, 04 Nov 2024 22:30:31 GMT  
		Size: 24.1 KB (24085 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:d62cf2c7d043d76a6e8909e5c8162e6113406872f062616fedd89c5c7ca460b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110256705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f375f06fc25d124351710ea20778759a298ab04293e75d14ff87ec7064b300`
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
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03062ba6cc89d48fbed8c001c307b5b41e0a5f776a5ecb43457bcbf48b0c0d`  
		Last Modified: Mon, 04 Nov 2024 22:05:24 GMT  
		Size: 17.3 MB (17256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fb8998db4ebfaa5b2a38425fdeae5c321599d452a078b53cb18c5e04b423fc`  
		Last Modified: Mon, 04 Nov 2024 22:38:09 GMT  
		Size: 56.9 MB (56939289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff001295025ace93b32b4dbe9106bcf2206729cad45f3dd90b5ad16387d5a8ac`  
		Last Modified: Mon, 04 Nov 2024 22:38:07 GMT  
		Size: 4.0 MB (3984368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1e27f3fcaa1af45a0a9c4537507a77813abbbde4924298cc4d99f1a81a0c7e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871c0b0dfa3607881272518a447bd1c193fac998b116e6f6b75e996a61e52b6`

```dockerfile
```

-	Layers:
	-	`sha256:2f6fb76d720ad8759f2ceb5efd63fec25ecc0484cf91add6966b66bc9afdde4c`  
		Last Modified: Mon, 04 Nov 2024 22:38:08 GMT  
		Size: 3.6 MB (3596085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e856904dc514ed84c6bed241baa52af3c2cd29edae9a063cd08983cd7655bc1`  
		Last Modified: Mon, 04 Nov 2024 22:38:07 GMT  
		Size: 24.0 KB (24012 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:68cb003b2db23a709c8f8bf6b6733d98f133ccbff9eb37e7aa68238ca899b941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102147919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d986b9af07a39216a2559ed8a6a6c7467dc0cf09a0268b40437200f9724eb3b`
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
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76440d6755e318199681b6d987a4b8660d5945e0ea29db0a034c2ad4c00548`  
		Last Modified: Mon, 04 Nov 2024 22:07:59 GMT  
		Size: 15.8 MB (15773072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5513f81d9c7dac258db8d6a6389b8a8954ed956d072e7c161015a23fa57b8181`  
		Last Modified: Mon, 04 Nov 2024 22:41:32 GMT  
		Size: 54.7 MB (54656425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211f371637207411640bc6cba20d67f970ab7af56265b17f807c35709016110`  
		Last Modified: Mon, 04 Nov 2024 22:41:31 GMT  
		Size: 5.4 MB (5352443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:fede687f2fb05fbaab53609704be4ed9f265fe12069e8bf8dc4ba3889251ce91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607dd9bf94bf5817b86b315fdb067f7993cbb14a888083f7b1564a37ecfe14c3`

```dockerfile
```

-	Layers:
	-	`sha256:41444b203ec7ef8d600a6ed5be3e4326133d2bf4d98b19535193f13c6b841b76`  
		Last Modified: Mon, 04 Nov 2024 22:41:31 GMT  
		Size: 3.6 MB (3593071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b954531f63869ab489a92d25c44ca536b79ad99005a27c76d64804a369b04e1`  
		Last Modified: Mon, 04 Nov 2024 22:41:31 GMT  
		Size: 24.0 KB (23976 bytes)  
		MIME: application/vnd.in-toto+json
