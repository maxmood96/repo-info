## `ibm-semeru-runtimes:open-23-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:119c6b26ef3329c149ab8b33c0435d56c800963510faa6cf5163d098a1ea5cd8
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
$ docker pull ibm-semeru-runtimes@sha256:829060ff678c816b5405c31f388cd74f09e5b34e8634e2356878e06e9feb2431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289228665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a51082fe2c7bb985f6775946fa39ce67736f62f802acc4466ab00c6d6c9c1f5`
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
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9a93db4e95ff9718684e3978328657532176a2ccc5d9ec2eba32d83def886b8';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76ba23aefc68b2d3838895cf7dedc69a4a28fa3b6cdbff3cae3078b550404c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='278aaf14ae2a291fb4f4d08663675b50dad0a1992230609826c33013cf777dd0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='9db5de0beb8bd50d6971d1b88cf9c7008aab0bd8ef6ec33eee386357b4a9da89';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f55426ad522cc65c4876e1a68c8bc4bf95f11fa7722fdc1bbf394e6ccb9e3d3e`  
		Last Modified: Sat, 15 Feb 2025 03:14:24 GMT  
		Size: 16.1 MB (16076033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517e9c2de34295d63da0a0e2e7d5c28294c148b1d47146d60cf12e9ab9a4089`  
		Last Modified: Sat, 15 Feb 2025 03:14:34 GMT  
		Size: 238.9 MB (238906736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ca51ac9ef328d91baae480d7b57d07425089e5ee400639ba4db16479691fa2`  
		Last Modified: Sat, 15 Feb 2025 03:14:24 GMT  
		Size: 6.7 MB (6734836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9d7dd1f6713d9c3a8588fa859ac5f68027072daa617af5388b44e76458693b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3699258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10548001912de0653c831b72618477e0ba070fbe2f73269b1dc8cfd27e50adea`

```dockerfile
```

-	Layers:
	-	`sha256:e0eef00cf3ff47ee77f107426f851770a5e552cc1cc3b1886c4aad470e657ebe`  
		Last Modified: Fri, 14 Feb 2025 23:46:05 GMT  
		Size: 3.7 MB (3675153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddfd53bd35405c65cbeaa8049a69efd0735bfc7508f4e2ba6a01068c7d8be1f`  
		Last Modified: Fri, 14 Feb 2025 23:46:05 GMT  
		Size: 24.1 KB (24105 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:5e4de9326dc99ce1723a033f45a20654320fe17ad07ae9a6909f98373a83a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276517679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10543f9f090723a1127cf7d77994121b6ed1f38155e5ef22fbcb15d8ae3d5b86`
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
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='74e88d7b7fa0780ad906f0dd9b3849129d6297d44098929bc89e85d9aa585a15';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2aa3cc78feab5cf1c21a830797694c9b8b7898072a40c252f442b832117a3809';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1deca44079fe35071eba46a4833cc48d9fd9a3f99bca91a02a80b87fc010d52c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='651dfd5091b418f0c8a5372fdeb784c3ed2508a786e414d49268a82fda196fb2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c8463c16baee128300626ada43a184e02bd6bb4ccb4e05176770d7525cd2d4aa`  
		Last Modified: Fri, 20 Dec 2024 10:09:14 GMT  
		Size: 228.1 MB (228146641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605dd8e684577074d24a18a3caa996f79147cc4d3539280dd14b3120a6d33835`  
		Last Modified: Mon, 06 Jan 2025 17:42:05 GMT  
		Size: 6.5 MB (6452170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0c3f04f857f79f16de03247e1f1a978ea00951d6732a0d95415902af37d9d458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02e48b152c1943a14bb78258d89c279960624213922f28b921c3931020b7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:cd16e4e41ef4c4ed32d9f475288a9620df486c38187f9faf2e1726054fdb8e0b`  
		Last Modified: Tue, 07 Jan 2025 01:44:11 GMT  
		Size: 3.7 MB (3663798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45195a8f8ebf219d3d3825cc064a4af2f7246b7eb720a9233a3e04f61ded4063`  
		Last Modified: Mon, 06 Jan 2025 17:45:18 GMT  
		Size: 24.3 KB (24251 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:0f58ead51137e089f39919557a2e2d9232c748ac20827f3ee615c3cc7807f0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294496377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4915fbc64e64d8dd9970fe3eea3c0556b3f0c3d7a44d263faaf99e245efdd09a`
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
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9a93db4e95ff9718684e3978328657532176a2ccc5d9ec2eba32d83def886b8';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76ba23aefc68b2d3838895cf7dedc69a4a28fa3b6cdbff3cae3078b550404c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='278aaf14ae2a291fb4f4d08663675b50dad0a1992230609826c33013cf777dd0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='9db5de0beb8bd50d6971d1b88cf9c7008aab0bd8ef6ec33eee386357b4a9da89';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:d18b0271a1f27683a73ba169ccb6f7a3d70c2f9e95595c41a731ab5d8d935566`  
		Last Modified: Sat, 15 Feb 2025 02:43:49 GMT  
		Size: 239.7 MB (239712819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0912752e32f495121991673a6c861de438dde3c35e1dfbe6e914faaee5f17deb`  
		Last Modified: Sat, 15 Feb 2025 02:43:43 GMT  
		Size: 5.5 MB (5459309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5737273ec505832c0878c505cf0b84af99c5304a372152167e32df2806784b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3699386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac92115e89b94a69ac86879c7b7bd94fe60372af5e869a449550fc7c9e8f517`

```dockerfile
```

-	Layers:
	-	`sha256:396a6c4ff6d2a3d15983223d42c8a495bc9fc950506dad4e7d8b40d42f8bcfcb`  
		Last Modified: Sat, 15 Feb 2025 05:45:51 GMT  
		Size: 3.7 MB (3675245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd21831928aab78555963e8eec5d2865bf39b165e2735a5c5d13d1796fd700f8`  
		Last Modified: Sat, 15 Feb 2025 05:45:51 GMT  
		Size: 24.1 KB (24141 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:60c00ec12ba46fba0a3780ae117c3cf733523e4644709960fa5cdab3f5c2bd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283464434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c7384474cc811a6b3b5dd8960b5c2cb34f9bc9148553c39497e3eadf5b8c69`
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
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='74e88d7b7fa0780ad906f0dd9b3849129d6297d44098929bc89e85d9aa585a15';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2aa3cc78feab5cf1c21a830797694c9b8b7898072a40c252f442b832117a3809';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1deca44079fe35071eba46a4833cc48d9fd9a3f99bca91a02a80b87fc010d52c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='651dfd5091b418f0c8a5372fdeb784c3ed2508a786e414d49268a82fda196fb2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:d5fcc02109dcc6e9cacccd3f09b3ea75e9f34d884dff7864f9afce1348589a09`  
		Last Modified: Mon, 06 Jan 2025 17:45:40 GMT  
		Size: 234.5 MB (234476108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c774dbea441fb0def7fd69bc0aea84720cbcbcd0cab2d24581ae182a86877`  
		Last Modified: Fri, 20 Dec 2024 10:10:01 GMT  
		Size: 6.8 MB (6849275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ed5b03eca81815be0a10610cd2e9096fc8ef4a243195cb32a44de77cfbd6a853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279c796d8164c79cf407e172da728ac71cc8acef68992283e5cc0298b961e2a2`

```dockerfile
```

-	Layers:
	-	`sha256:d79efb7c7472b05b63f2fd796179b900be7db2faf969bcfaf8c7aeea18a538d0`  
		Last Modified: Mon, 06 Jan 2025 22:46:03 GMT  
		Size: 3.7 MB (3672514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cf6c6bc8d20ad79af9cddb9923b0e31005caabbb17cd32f452006eefa93957`  
		Last Modified: Tue, 07 Jan 2025 03:40:38 GMT  
		Size: 24.1 KB (24140 bytes)  
		MIME: application/vnd.in-toto+json
