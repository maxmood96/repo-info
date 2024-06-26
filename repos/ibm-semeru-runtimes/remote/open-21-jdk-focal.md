## `ibm-semeru-runtimes:open-21-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:d7069f61d82f8882d23081d58f9d6f2bf23e0421362bce39ece89cb01df8f2e7
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
$ docker pull ibm-semeru-runtimes@sha256:49478502ce67848837cd3605b371ff90fb6af0a25900e0f44da0a571bcf35c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280448355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759a79294e8f3fa7df514100fd3cf7289024055aaca3087cbbf65f25a4ada768`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='718e465d1b22034d889445e8ae371fc58dfc733c454cf344fa5e10db0ab8a775';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5cccb39dc7ca6c61a11bd7179c4c3c30b747f9f22129576feef921b59725af25';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e3a467fcd088304c08a1c1c61f5ea2c065c10a312b01089d2eca9dd9611aab2c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='0135f03416588197334580c27f9a62f447fb3409907c6049008ce5fd2223520a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e2b5c9fd15350095e3b253adcd73b9a0122983114cd7d2f69ef89c52334ef5`  
		Last Modified: Tue, 25 Jun 2024 22:58:06 GMT  
		Size: 16.1 MB (16059655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdba98e143f9a8e86aab92ebbcb055cc7a1a0d7c67f5a51b43e606dd3bb94d8`  
		Last Modified: Tue, 25 Jun 2024 22:58:13 GMT  
		Size: 230.6 MB (230609840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dcaa863afe7bdd8c4550fe085e3437c82fa47e2f43ae8ab625ae314d801f45`  
		Last Modified: Tue, 25 Jun 2024 22:58:06 GMT  
		Size: 6.3 MB (6267091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:302162a2f3efe2a5531da8e2b0a2ac3573e79526fd68fb7f97e280eb48bfc4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3461974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c57b29161a74e6d71b992f75443ec4d34f40f674c3e92915c05d462edbe60e3`

```dockerfile
```

-	Layers:
	-	`sha256:003ac4caaa3221265bab8769ba1a4dd04964dd30f9cb702195630fcde6cf6621`  
		Last Modified: Tue, 25 Jun 2024 22:58:06 GMT  
		Size: 3.4 MB (3438259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21bb689223b525ef71a07725948965407fd5f90b7115bab0cb7a9f8433abcc8`  
		Last Modified: Tue, 25 Jun 2024 22:58:05 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:d0a7e3765893c893ead00464f8c41a93a9b2890b73cebb4a3253f22b4e801f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269717927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05857ba7a81755d667093805f375c638aded2e0e79e611aa229f85f859a793e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='718e465d1b22034d889445e8ae371fc58dfc733c454cf344fa5e10db0ab8a775';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5cccb39dc7ca6c61a11bd7179c4c3c30b747f9f22129576feef921b59725af25';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e3a467fcd088304c08a1c1c61f5ea2c065c10a312b01089d2eca9dd9611aab2c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='0135f03416588197334580c27f9a62f447fb3409907c6049008ce5fd2223520a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176d538118d9c20626923c1883abdcc6b8627cf4d4d612b9a0dd7f1d0f1b41a`  
		Last Modified: Tue, 25 Jun 2024 23:01:16 GMT  
		Size: 15.9 MB (15921752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf47e0e6e493b661e6b169be37e6613a7037611322bfa4f2ee329c8c9ed1e6a`  
		Last Modified: Tue, 25 Jun 2024 23:23:57 GMT  
		Size: 221.8 MB (221809185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c32c31a66b7c02b0be1a1960c4dbae4c15f59797e680b28ad18b7c36b3619b2`  
		Last Modified: Tue, 25 Jun 2024 23:23:53 GMT  
		Size: 6.0 MB (6012773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0659d31f4586b83cc8f4692617024b9266f526c32309419cadba1778424bf61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc3b493f10709713da5cceb0fc7dd74321ee4ab9b31e835d0debe3b25878fae`

```dockerfile
```

-	Layers:
	-	`sha256:ff260b45ab10c3003488bf732373d555af4a229d1c25d0e157d59245eae1d30f`  
		Last Modified: Tue, 25 Jun 2024 23:23:53 GMT  
		Size: 3.4 MB (3438505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3eaedda6f673f5b6a50c84f8d51e160e48caa50a8e1bab7321e55373146665`  
		Last Modified: Tue, 25 Jun 2024 23:23:52 GMT  
		Size: 24.0 KB (23992 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:4031623b2c6fbbda0406dd61a2e5691eb6083a8bcfe5ba749e7931e2a82b636e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287854856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3021ddb6a685a726d2ffc7a44ddff78ebd2b2e715968ff08bddc9f6a8a75c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='718e465d1b22034d889445e8ae371fc58dfc733c454cf344fa5e10db0ab8a775';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5cccb39dc7ca6c61a11bd7179c4c3c30b747f9f22129576feef921b59725af25';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e3a467fcd088304c08a1c1c61f5ea2c065c10a312b01089d2eca9dd9611aab2c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='0135f03416588197334580c27f9a62f447fb3409907c6049008ce5fd2223520a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a396fd21a1d23e16c5c923d6952275d92d4ae28dc2a5e58de9d21ca3f7e3fe`  
		Last Modified: Tue, 25 Jun 2024 23:01:33 GMT  
		Size: 17.2 MB (17240286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9705bf28d074bd93c143a1ff5645d4bfbfe89080016595d8ffcfeaa459f02d56`  
		Last Modified: Tue, 25 Jun 2024 23:31:53 GMT  
		Size: 233.4 MB (233435181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bddc25fd76e0cfc189978fb38ed50e6a03f977be55dbab9e805b979714dddd`  
		Last Modified: Tue, 25 Jun 2024 23:31:47 GMT  
		Size: 5.1 MB (5102249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2ac5ac747a3eca8c0ed8f2d79fac7b01bfba6275769f071942cd3975cc7168e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3466439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bf50d6ce060c56372c558c54d6fbec3afe6fe7acc0df4edb00900166e44de7`

```dockerfile
```

-	Layers:
	-	`sha256:b926df7a8c070ac923d10a7d2e77cc421d92ca85924a986e6ee83cd914aabad7`  
		Last Modified: Tue, 25 Jun 2024 23:31:47 GMT  
		Size: 3.4 MB (3442694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd3f62c17ee939054e1cbb3934fa2c6911e745dd3103febbf976acf42e90bcd`  
		Last Modified: Tue, 25 Jun 2024 23:31:47 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:4d529e3ce43d70765dd68230bde76da377f76d9e723d753accdbb9b94881504a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275983555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfa694349b3cc9c6c94e5c2ad593437650c53d26697a3f47cdf7b7a45390c2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='718e465d1b22034d889445e8ae371fc58dfc733c454cf344fa5e10db0ab8a775';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5cccb39dc7ca6c61a11bd7179c4c3c30b747f9f22129576feef921b59725af25';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e3a467fcd088304c08a1c1c61f5ea2c065c10a312b01089d2eca9dd9611aab2c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='0135f03416588197334580c27f9a62f447fb3409907c6049008ce5fd2223520a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f28dd05fdcdec551c55aa8b54e4bb1d0df07a936a70442b7d2b536674bd1c`  
		Last Modified: Tue, 25 Jun 2024 23:00:45 GMT  
		Size: 15.8 MB (15751504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8bbbea4bad2c32bdd3d8ed871b15f560007c1ebf7c6da784ecd6df578465af`  
		Last Modified: Tue, 25 Jun 2024 23:17:35 GMT  
		Size: 227.5 MB (227484175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353291bab4a05765f5b9b4112fbe32ea13f5292f83e87e71b84c25d205b4ee1c`  
		Last Modified: Tue, 25 Jun 2024 23:17:33 GMT  
		Size: 6.4 MB (6380682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:eac69aaefa5842f6c8f29e28442e24ba1016c89bc60e1ecc5c41216256eddc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba26f2d64bb9c2fe2350be6c67c4cce45a234b46b844de4e8d023c9465cce895`

```dockerfile
```

-	Layers:
	-	`sha256:a338b2bd7c52c971fbe11ba88c23912528b9ab36178144cb6550a58d89ccfd61`  
		Last Modified: Tue, 25 Jun 2024 23:17:32 GMT  
		Size: 3.4 MB (3438720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2c020873b3912f6546c9b095c3b94a1267a231bbd65d6e30178013686c4768`  
		Last Modified: Tue, 25 Jun 2024 23:17:32 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json
