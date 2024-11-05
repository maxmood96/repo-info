## `ibm-semeru-runtimes:open-21-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:50c9b7da25b3530947bdc25ae7914a0cfab6282974a1865ffdc098813b8edcae
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

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:71ad656635410f231ecd38bf9201ae1aa61bae4eaf136579b7fed26db75d9924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279999844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b5c151667e63e385ea18beee2f30d26cd9408832775621b013de50c76ee8ed`
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
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:44477ce4e1b3bc3a41df8c5540df1f3aaa6c280c487c8963424b9832089aee96`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 16.1 MB (16082733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a45c7a5e983d30a59776395b119c7c983d836b79d41a8882ec91484929c852`  
		Last Modified: Mon, 04 Nov 2024 22:05:04 GMT  
		Size: 230.2 MB (230240040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a91c9bdffc3ec9a705a9a81fe5430eb136774db10ccd7b7467e9d9c317ea47c`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 6.2 MB (6166011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:70ad9397626347a9674d01dbf50ab56e4dbd51f2e6abf7146ec096aee6b3c789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2408defd9c9972ba43f5ca007efd69708bab78062db13a9c9e64f5151345f4`

```dockerfile
```

-	Layers:
	-	`sha256:46510ee93d7c6fbe209df75fd143ab4b26df8f6b000663a3722fd76a14e1399c`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 3.7 MB (3672854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f6be61aea517e3262a40f39155a3e5134a1cdc3052d1d16035a79799ebc991`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 24.0 KB (23973 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:6b8bf686a2c197e94de0fb5041e76a60645d95994ae927c6fdd4a7ac949df38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270079583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7230230da335cb374b154a4745151cef7272a191e2eba5187a7e0100a501a7`
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
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:57eb564d23ff3e3837a4af3d53db3cc3d25982fce3f7cbd2f141b917273ee171`  
		Last Modified: Mon, 04 Nov 2024 22:21:54 GMT  
		Size: 222.1 MB (222130499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d83d50913c9d0da2d0a87a7b114f84d2cd8d57260f352f5eb0d474a8506ae09`  
		Last Modified: Mon, 04 Nov 2024 22:21:50 GMT  
		Size: 6.0 MB (6030250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ea2b3d88badd682f45c757c274093237c8fac55bcad81760a10c4afb38ce658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0584bd4be38c6d1dc8f3ae33919f9ca486686290a133dc98a4d584efbb1a6e68`

```dockerfile
```

-	Layers:
	-	`sha256:a0d28daed6e4ad2b585f43993ad7dfb6777c9ae5e165330540ef5c4fdd100307`  
		Last Modified: Mon, 04 Nov 2024 22:21:50 GMT  
		Size: 3.7 MB (3665543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cb109061a71f86668508a676872e21a4f0dcfebeaea20566abdcbe6af70ddd`  
		Last Modified: Mon, 04 Nov 2024 22:21:50 GMT  
		Size: 24.1 KB (24083 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:b02d8edae9246d4b9c9642cf40a7de7106048264662bdfcc9ec2bcb73bdcf16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288135346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0225166c8df98710c08aa114bfba2953c6d51a34ee985b05dbb52b8f310d7c67`
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
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:26d80483cd7c23bf7dd67fae2e6f97ed4787452eefe2b51ed5c2fbc00eea548b`  
		Last Modified: Mon, 04 Nov 2024 22:27:01 GMT  
		Size: 233.7 MB (233689727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d654db0ec2d60f46907811efc5f735ed1e7814f8741c50a5871efb01f1f499`  
		Last Modified: Mon, 04 Nov 2024 22:26:53 GMT  
		Size: 5.1 MB (5112571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c86ff5678874e08cb6b9e774ce5974fc23dbff6d65b8785c78ee0c31ab6670fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3701298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14552306c749639a774daa836b1f432a3b23e068a1a20d29e0fb3ccf63328d2`

```dockerfile
```

-	Layers:
	-	`sha256:f3f2b2b98c6e807337d29f59f9c46fec296a9deea914cefd661d7fcb4ff477c3`  
		Last Modified: Mon, 04 Nov 2024 22:26:53 GMT  
		Size: 3.7 MB (3677289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2685c6e520aef2a7b42ee3873bcfb58ace53210ecff414ca8fc4a72c8809caf`  
		Last Modified: Mon, 04 Nov 2024 22:26:53 GMT  
		Size: 24.0 KB (24009 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:f538d8a7bbab3de64a79130224024793ddff4189dccdb3486eae69dfa1003497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276308075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b5ba813b4c214265b3ac96dedc5ae4716ce95ba5fa38395160e088eb62d73b`
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
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:60e29c8cf5a425233ceba137551148413cb238ff4a5f21117007a631526ea6f2`  
		Last Modified: Mon, 04 Nov 2024 22:26:41 GMT  
		Size: 227.7 MB (227725904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c2472776fc2666b6f00a9620ddf7fa71a764eb349b0832a9a2718fa456215`  
		Last Modified: Mon, 04 Nov 2024 22:26:37 GMT  
		Size: 6.4 MB (6443120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e3f153a52782a714991ce9333f994814ba02110885df4a2618c05c954de6a464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaf4c39074f828f38724062e13b3113c872c6a1350538b00f37be8662ac6bec`

```dockerfile
```

-	Layers:
	-	`sha256:9ca0ff1253808ff52b23429cc6287112c1447f87b74bc7450c7902937706861b`  
		Last Modified: Mon, 04 Nov 2024 22:26:36 GMT  
		Size: 3.7 MB (3674275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:609e4837a4ac3be7d3cf0ca2fb7062d9fdf55ee54e1f0067507f9e2b817e3e00`  
		Last Modified: Mon, 04 Nov 2024 22:26:36 GMT  
		Size: 24.0 KB (23973 bytes)  
		MIME: application/vnd.in-toto+json
