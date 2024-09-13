## `ibm-semeru-runtimes:open-8u422-b05-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:affc8bbe4a6b884b1131660849051c4f18acf20b62b631863942b8708c336fd1
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

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:b36aca4d962b8d35e6ac6fb2fbf0287d612773f5a965ae09ab8a83beef3d8bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8dda50c22b837dfe91f2304e4f84b9cda5633526d53ddb158b030f88f1e0b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d861ad392e53e966619eff2c5e65fcf86e00897e71d5b4946bf31c70c98f0`  
		Last Modified: Thu, 12 Sep 2024 22:02:24 GMT  
		Size: 16.1 MB (16061295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e69ec30d85a84513d51999029dba90dc645c64503e6498952ea61d148f4290`  
		Last Modified: Thu, 12 Sep 2024 22:02:26 GMT  
		Size: 116.4 MB (116441016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3ea715e8c571ece37a2a6b2792321d0cdfb64202da876ac00fe53dc182e3`  
		Last Modified: Thu, 12 Sep 2024 22:02:24 GMT  
		Size: 4.2 MB (4235714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:f591bd651966a49db3d196026376bc841e62f9292087be37263c935f7906de27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a3b2b05cf693f21b88ebb662a78475bdd809c84e25e19a278be2e10a4a811c`

```dockerfile
```

-	Layers:
	-	`sha256:039d5d92b5cdb5177c20ecc699b0f64e35f54801be9cf020347654d78eaf0917`  
		Last Modified: Thu, 12 Sep 2024 22:02:24 GMT  
		Size: 3.5 MB (3492557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ee8b3a7c1eed17c938c33b2296d4cb130803ba1bc43a5abd44bc962f5edd3`  
		Last Modified: Thu, 12 Sep 2024 22:02:24 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:fd5daa89580f9d033e0f99aca0e25b7cd657d264eb98b0d4ed0901295080b76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162435902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab4531e1ca057171aed0db986840cb5dac6b65439042829459660a33f1155e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2bfb687179cbe19551365186a120e8f0cd6d43a6cb5b4ed94041823a689f08`  
		Last Modified: Fri, 13 Sep 2024 01:54:18 GMT  
		Size: 15.9 MB (15924339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c2723592c376172e5f988fb58ac90aaa6feaa390c991b6db34d0a7e34bd298`  
		Last Modified: Fri, 13 Sep 2024 01:54:20 GMT  
		Size: 116.4 MB (116432313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e483a02077f0f264a06a4b568dd1b52d8af725480878c475e2567abffba874c1`  
		Last Modified: Fri, 13 Sep 2024 01:54:18 GMT  
		Size: 4.1 MB (4105033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:01adb5038225da01ee120c37e651fcbd0b88da76460c3c859cb44403849ca912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d037394effc35f26d1c44cad15843b386ff7b55f704e695156d23eb7d9cbd35`

```dockerfile
```

-	Layers:
	-	`sha256:2eac8e7a4e6946d5a3a5b9b3e6cc8376a5c6ce80a95c1fa3e2f073e843d34356`  
		Last Modified: Fri, 13 Sep 2024 01:54:18 GMT  
		Size: 3.5 MB (3492803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6703ebb6660ece4dcba95692e2419f0777decba01e7c86cdcecbcaa07172be`  
		Last Modified: Fri, 13 Sep 2024 01:54:17 GMT  
		Size: 24.0 KB (23977 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:1fe9253a4f4001e8ef387577f16d5ff940445a58ff4ce66c3d0ad5a5498146ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170807486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd727aa9e7722e4c9668b395361fadc78a095f2b23f49f22af7ff7635f196d89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4909862bb393ed96fe85e381a9732712712fb18fb01f20c0faa2ea028eabece5`  
		Last Modified: Fri, 13 Sep 2024 05:38:21 GMT  
		Size: 17.2 MB (17242516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfa60a7bf9a881252ef33f6c95664c2160a848f82cf3219d6bf6aebb617c49d`  
		Last Modified: Fri, 13 Sep 2024 05:38:23 GMT  
		Size: 118.0 MB (117999604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d29a315af2a4e2134ed5778f0ff30ffd58210007537852742ccb8bc1150bcb`  
		Last Modified: Fri, 13 Sep 2024 05:38:20 GMT  
		Size: 3.5 MB (3488226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4d6529b56be99833719def7257d8ae909f94e00fa959508de684dba97257b67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3520722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211299bccedaefeeb2ddecc7b1357c24ea0f87c2dec1e10020e920dde80f3ec5`

```dockerfile
```

-	Layers:
	-	`sha256:8441121a246355ae7939a5317fd3de64f1435c182e7e4986bf608e0f5c707149`  
		Last Modified: Fri, 13 Sep 2024 05:38:20 GMT  
		Size: 3.5 MB (3496992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256fd2f2577f919dfb42aed8b7b14b7625bdcb0a6312e7e1785a597ac9fda962`  
		Last Modified: Fri, 13 Sep 2024 05:38:19 GMT  
		Size: 23.7 KB (23730 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:43861b01b31ca22e44c1665c486d2cab8600ce8e3a8c231bb870c2b129e5990f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162843448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e54ed5d30f308c3f36ff761ad38af76d0c11fe26fd1f9b1daa51a2d26e44114`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a55f53caabd0e3ef017534ce350abda2e8201b47719c9cc81d70a0e388085964';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='afc08f089267e5258742f29429654a5877fa106e42c815b458659d3375a986b7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dbf8199d4c90a3a02a2133e364cd49b46111eef3bbc7e1ee5e5a482c72ccc9d8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8e73d091ab2b9d8ee557abbb7ed7cd379c098e72c310f8a0833ccd94afd394df';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_8u422b05_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:43a275ddff09c9f4397e978092ab9952ebd3393a5572a06df70e3545dccb0c4d`  
		Last Modified: Tue, 13 Aug 2024 10:24:18 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d59eaa0200787a041bd8220cb7f34aced7071473572370459f90d9eefe6da68`  
		Last Modified: Fri, 13 Sep 2024 02:22:47 GMT  
		Size: 15.8 MB (15753804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2259014818b35950496e1d5d5d25185d151f1349aed38fd764b6368d16d413`  
		Last Modified: Fri, 13 Sep 2024 02:22:49 GMT  
		Size: 116.4 MB (116355104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d092e919ff4033c396e2a8e412820cdca278cb1f18b2bad4fae6b827e7730d3`  
		Last Modified: Fri, 13 Sep 2024 02:22:47 GMT  
		Size: 4.4 MB (4367346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b911ac3431fc14f5532f8a0b6b9c8cbf18bca7bd502433cbc035e4a6520ca306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3515981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96fe535804b2cbf309a7025c00e4c15a1df14cc8d1dceae0f4dd8a8d1c629d5`

```dockerfile
```

-	Layers:
	-	`sha256:5de1c9777c5c2e38131114f7c426a81b04f869894ff2a393ac8fd90a67de40df`  
		Last Modified: Fri, 13 Sep 2024 02:22:47 GMT  
		Size: 3.5 MB (3492281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06394ffecf5b756171463d8aa84c7c2beae432e57524c1197f1bd6d63d8448a9`  
		Last Modified: Fri, 13 Sep 2024 02:22:47 GMT  
		Size: 23.7 KB (23700 bytes)  
		MIME: application/vnd.in-toto+json
