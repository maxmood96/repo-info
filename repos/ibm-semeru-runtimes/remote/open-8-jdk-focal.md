## `ibm-semeru-runtimes:open-8-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:eee2218b4dd74a4430dd9cb9ada74df1be8f5f0b979f819c44e17ac68886a010
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

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:86121c1b1489b5a21e5c31f26ad8510b8cbea446a26a234635781edb65e174c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164320186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470bae97883954ad5ac02219ce2e8e1e7dc7e7e2108fe650633bf8759bd737c`
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
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:4e213fdbed1c283526e8c1bf7ad8254ef739c4ba0c07c63e904bab44989ed129`  
		Last Modified: Mon, 04 Nov 2024 22:04:47 GMT  
		Size: 16.1 MB (16082663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ff3e48007f6de98a1efc7bf77973def183c16282135a9b2fbfbdd37161cecf`  
		Last Modified: Mon, 04 Nov 2024 22:04:48 GMT  
		Size: 116.4 MB (116441038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f0e3a50726432aeccb925553d7a0cacb25e7303f6830596836855f4da72a96`  
		Last Modified: Mon, 04 Nov 2024 22:04:47 GMT  
		Size: 4.3 MB (4285425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7c4ec1a0f50e6c5cf2bb68c42d76bd48c898577957a3a067edcc6b41ed559bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0f5cce0e5240f91952f73eaf223dedc31f73eca88ee4c108529a632c4ee843`

```dockerfile
```

-	Layers:
	-	`sha256:551ed2bdb4202d57380f938d5a099b71d8f268a7708b63d0f25856ec508849f9`  
		Last Modified: Mon, 04 Nov 2024 22:04:47 GMT  
		Size: 3.8 MB (3785761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7375810930a0690b3b2fc789cd679eb315c064de807d8ea66fed035b13147b5d`  
		Last Modified: Mon, 04 Nov 2024 22:04:46 GMT  
		Size: 24.0 KB (23954 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:c85a3f845dd6ddf2e09e986227da5378f6fb29ee1479361c078f3a2afcd59170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17148b30556718314c6c2e0215a8084446f729d22a5f643281c166221140c41d`
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
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:410528a593c17c3df9023c50a474f1eee961324bb1fb9a53e5ab93324284451e`  
		Last Modified: Mon, 04 Nov 2024 22:06:04 GMT  
		Size: 116.4 MB (116432324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c13e9a1c80acf991188479826cef946c495e2f1194018d618d46d8dc962965`  
		Last Modified: Mon, 04 Nov 2024 22:06:01 GMT  
		Size: 4.0 MB (4035906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8b68291061668ebbd298583a89483744fc5966858eabfcc77877b8418358e4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3258000a611680c33ad22f91041689e87f1f4f2af60ad64be9bf9606aed80bae`

```dockerfile
```

-	Layers:
	-	`sha256:1da8702b08a706db3daec14280e5ee53e7b19aa106032658cc49a16389a59d05`  
		Last Modified: Mon, 04 Nov 2024 22:06:01 GMT  
		Size: 3.8 MB (3785546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f729fdd91e30bbbbd45ae9bee2dd7957c7921498bb91f515863ce929d85a7c1f`  
		Last Modified: Mon, 04 Nov 2024 22:06:01 GMT  
		Size: 24.1 KB (24064 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:8cfab195a871bf6ab4f34e2ed4b63c22fc530c1341e4f030c1844455f8e52a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170831975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2a9f8afd791a92ce40d058ff1d0ccee0c20264d7a18cf0c1f76b46cefafa9e`
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
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:bfb97d1d16be20e54ef0cb2838cccb7ebd5df5be42ec35e534eec12fe3773371`  
		Last Modified: Mon, 04 Nov 2024 22:05:28 GMT  
		Size: 118.0 MB (117999610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f9d3eaac7097841275617d1324503d72edce4a2e990cf73c0fe4475bdfb0db`  
		Last Modified: Mon, 04 Nov 2024 22:05:24 GMT  
		Size: 3.5 MB (3499317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3f0b875941bea6bf3e6fefd2715de44c26527e89814990aa403d124a5cfb832a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7934e9750d336449f9eacedc21410a53ce5b5d3ce4d0bbf2d076e771ca4cce`

```dockerfile
```

-	Layers:
	-	`sha256:3faeee610f675f568da09940d334c5b0b4724accdb230b2b172df4f71e90832d`  
		Last Modified: Mon, 04 Nov 2024 22:05:24 GMT  
		Size: 3.8 MB (3790368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88b170505115a8726c46e51d1ec83a6581c9a1bcbc5ba519147d2b8001e2705`  
		Last Modified: Mon, 04 Nov 2024 22:05:23 GMT  
		Size: 24.0 KB (23990 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:8056f06eb1f77022da6a373f12b2d80e7554e2ab1e419a2f27f7a0d03b00bea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162851459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418b0431bdc69c9d89b05215fb6bcd7ace886687fe5da09269d3607dc63debaf`
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
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:6021955cddca1c24ed712e92b0467be52576c98898a789626ba17763f45e820a`  
		Last Modified: Mon, 04 Nov 2024 22:08:01 GMT  
		Size: 116.4 MB (116355130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913ebcafb32c3144370e4977717e7b04adcbc1635771ae9420aaa894383dc57d`  
		Last Modified: Mon, 04 Nov 2024 22:07:59 GMT  
		Size: 4.4 MB (4357278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:017d805fb006a2304230841b77843f47fa37a9db2c45525424dc02506b27d162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b870f479d02e8c5ad489ae8ff4faae5551a64965e9d3d206df570f18d9e66034`

```dockerfile
```

-	Layers:
	-	`sha256:3d59a133ed12694e116d3a486b2166ef495d9cd216807c6fea56327a804bcb12`  
		Last Modified: Mon, 04 Nov 2024 22:07:58 GMT  
		Size: 3.8 MB (3787182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48384427da3eb2b819c595837d998e6c23076235b086b3d2d9887a30171d5ac`  
		Last Modified: Mon, 04 Nov 2024 22:07:58 GMT  
		Size: 24.0 KB (23954 bytes)  
		MIME: application/vnd.in-toto+json
