## `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:f4ae63f930db813c495084e26a7c5ae7ed6062d2fe6f7caa6ff8781a90a7f22d
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

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:e22f97fd84d8598a260f8e21915df9de8a285366b2512e3f49feb09d6e897fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295882160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61543537f703e18edec00ff3741fc720d5927e4084b83709f7bd7447f549f46b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:58:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:58:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:58:39 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 18:58:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:58:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:58:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:59:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 18:59:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff31dd2809421874b162d5b086dca10667c2766ca3897fa8b0e7379c56d8a5b1`  
		Last Modified: Thu, 30 Oct 2025 18:59:55 GMT  
		Size: 12.2 MB (12171720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7ceab9adbeb34b7195b01112f1bd838b10583715e12b41fca663fa5d2b015c`  
		Last Modified: Thu, 30 Oct 2025 22:22:23 GMT  
		Size: 247.2 MB (247190035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d1d7e601e07f004c6c89898defdf3d4dcbbe1711e39664b85bfb8ea79dac59`  
		Last Modified: Thu, 30 Oct 2025 18:59:55 GMT  
		Size: 7.0 MB (6983587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d63e9104638ebba8e9df868674135dbd4adca5eed619682baaf50d66a96d904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526cf4c25afebf547421d8baad238ec74bf376ed01bd3013a7d3c9e8c427daad`

```dockerfile
```

-	Layers:
	-	`sha256:6af098102dcd40e5ec2d93bc7af6087b2ccf915e3b7c83f1147b3acee4e916ff`  
		Last Modified: Thu, 30 Oct 2025 19:47:12 GMT  
		Size: 3.8 MB (3809112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b1283a52323142a1b65442eed7c253fad9cadef64636c062a10578ad9a99b8`  
		Last Modified: Thu, 30 Oct 2025 19:47:13 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:d30d06ad70ccbe76dab6da296881ce4f03335096e11b7b465af90b4431031fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289390797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30bc4a1192c861fe51608d0ad28a8df8c286f4f8cf033696308fc76874ea38d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:55:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:55:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:55:14 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 18:56:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:56:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:56:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:57:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 18:57:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2b8f7019efc54bde2fbb1333b86cf2c3aec6f777ef5b491e08a6e00d03c8f9`  
		Last Modified: Thu, 30 Oct 2025 18:56:31 GMT  
		Size: 12.1 MB (12129896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef6215213ff3301bd2dd6be85c97b56115e32600b78af08225fec37c53e8bed`  
		Last Modified: Thu, 30 Oct 2025 18:57:42 GMT  
		Size: 243.4 MB (243395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a26ce147913094b466a4d1bf07052f10ef0452eb0cc2700f60716c8aa66240b`  
		Last Modified: Thu, 30 Oct 2025 18:57:47 GMT  
		Size: 6.5 MB (6481961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:35488fe51baff5b46480fa0ff8d6df36ad4f695f06fd734b35883bab32a5e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b79a3da297061b4d31e0f3d5b9067251f599bf3a25abff07913cbb8adf4c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:7fc18a26056d243946d6bcd55eda4bb6329a59e248f7b7b66b23231e2293aa1c`  
		Last Modified: Thu, 30 Oct 2025 22:48:08 GMT  
		Size: 3.8 MB (3807484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797d90cde7b670b02401e7af58f6bd023851bf2e905c5b751db0491fd7aff14d`  
		Last Modified: Thu, 30 Oct 2025 22:48:09 GMT  
		Size: 25.3 KB (25309 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:42d1939aba575e21f827099322b3c5e18010ae38871767e85611ce6d9cea023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303916723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9894e9a263598562aceed6d44cb459fa02479a80204af568784bb3afd8b3661b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:52:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:52:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:52:43 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 19:22:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:22:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:23:19 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:23:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d05c427cc331d7b6dd9baffe91a10981b54840825b7525c3636088e5c3447a5`  
		Last Modified: Thu, 30 Oct 2025 18:54:22 GMT  
		Size: 12.9 MB (12893771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1e693adcd1a2240d95b52821a5976f25fe1ef0fc049389dec8bee1d0b6616`  
		Last Modified: Thu, 30 Oct 2025 19:24:08 GMT  
		Size: 251.1 MB (251056727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f1bad711737404aa570bcb7852ee34285e9d03a06098a416d4781293ec4c30`  
		Last Modified: Thu, 30 Oct 2025 19:24:22 GMT  
		Size: 5.5 MB (5519436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8256fb9f40aca26a1a66cb824ab2370924cf9b23f18ff3a28b795afeef9a0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989bc41e07202a785981db6be26182dfc0414fc83738803053720ff0cf928ead`

```dockerfile
```

-	Layers:
	-	`sha256:2e660be71de87259bb7c96b30091cad15fcc0ee8ad6b93d20b1c2d72a100386b`  
		Last Modified: Thu, 30 Oct 2025 22:48:14 GMT  
		Size: 3.8 MB (3813739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23548e9b81b854747ee3a4cd8f1a8159cd3fd7e8689af616f1ef4a24e9725d65`  
		Last Modified: Thu, 30 Oct 2025 22:48:15 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:2c4e7e3faa4aaf8df0088e2ca0f148826434fa26d0eabe784f1863f22b477659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291840730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22b46ea34d02e6a78563b3102e618a2306b1edd7ee23a9b1c35efae60814a94`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:53:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:53:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:53:24 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Thu, 30 Oct 2025 19:37:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:37:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:37:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:37:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:37:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85ec275e8f24c28d1884cb863f6a811d464cfb2b0e274ec7e8be26978e82f3c`  
		Last Modified: Thu, 30 Oct 2025 18:55:24 GMT  
		Size: 12.2 MB (12219687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd40c424781658474f885c07d13b8f0ebb45620e85cb44dfda1f48ac046c46d7`  
		Last Modified: Fri, 31 Oct 2025 22:25:59 GMT  
		Size: 244.9 MB (244896922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1107eafe7d1680c6876c13c917bc9b98a9ba77927994692797daa3a7f078fcdd`  
		Last Modified: Thu, 30 Oct 2025 19:39:31 GMT  
		Size: 6.7 MB (6720708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e94bdc0255559e90f554032b0fb1fa3ea42378a0fc3fbea66a346254183f69f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a800b8bfc634c5f35416a06e028179aff0502712ae62cee909c2689fdcef3`

```dockerfile
```

-	Layers:
	-	`sha256:7e9236204291d13b1416b044e59c0fb00c060f98437ef73c11f82d5c38514af6`  
		Last Modified: Thu, 30 Oct 2025 22:48:19 GMT  
		Size: 3.8 MB (3811330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08485a19d70a2b017512689247890ddc08ce3026c2e8046c3e6b08b710e564ad`  
		Last Modified: Thu, 30 Oct 2025 22:48:20 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json
