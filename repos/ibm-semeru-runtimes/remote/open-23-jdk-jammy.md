## `ibm-semeru-runtimes:open-23-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:3ce85f77688ab25d11fe8d49251ede3e3ee96c59c42dd87860e4a73221bba932
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

### `ibm-semeru-runtimes:open-23-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:91a609416612d9f5273cce5882b6775f0c57239855629dd733de596f3d7d5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287308388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b74d1d9c9c9fb0223b737215a36292a2f5649cff0918cff9258533b6abf4d38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c527d1b5907fbeee4adc9ff020f11c25e91f5b8e6986240ea884ae856af72`  
		Last Modified: Fri, 14 Feb 2025 23:30:22 GMT  
		Size: 12.2 MB (12166781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e578e1485bcb1f20b2694070b1b1abc5f19a0b8e610e0a79fbde87f263c10aa`  
		Last Modified: Fri, 14 Feb 2025 23:30:31 GMT  
		Size: 238.9 MB (238906738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4129d592e1551b866fa9f332acbdd8ca0b57b3d00a5cff23554cbbf91db828`  
		Last Modified: Fri, 14 Feb 2025 23:30:22 GMT  
		Size: 6.7 MB (6698928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:001e6c07fb56bcacc2e4bbbdfa2e8acf77bd62df3550822fe08ee0e60e9eaa2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98bf94f04d90a448c6fe1e2e71eea91b0cbfaeb466e84b4660517234d097bd4`

```dockerfile
```

-	Layers:
	-	`sha256:da2837d0d99266816987fabe071037d5fcc7c4fe1a873e3dc595d14c36784c71`  
		Last Modified: Fri, 14 Feb 2025 23:46:08 GMT  
		Size: 3.7 MB (3668559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90f1116a48b31a7d4644b1be8a4cf2732efbe9bf2ff45a90eaa5cf0b1e8aeb1`  
		Last Modified: Fri, 14 Feb 2025 23:46:09 GMT  
		Size: 24.1 KB (24105 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:75dfedd234f18ed3d3f3f58014ff1c1a7865973955eb235dc0835c3fa14cae0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274055322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47abba5ebf7a4507047ebaca682cc651a6ca7beb3d9a0b392ba2a83cf0cff83c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Tue, 17 Dec 2024 06:18:06 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc27324a20ba7e580ad161f241011b423fdcd169bcae5cc324e63f8db8fe6b2`  
		Last Modified: Wed, 05 Feb 2025 00:32:28 GMT  
		Size: 12.1 MB (12123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aa685527a9bbd44990ad40696ca149dda2e61aea9c1bc612c234369955553`  
		Last Modified: Wed, 05 Feb 2025 17:51:24 GMT  
		Size: 228.1 MB (228146605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f77064cf54d920e7cfa6c0d36f7c2e6906f0fd16575cc2e495bead0bd13a28`  
		Last Modified: Wed, 05 Feb 2025 17:50:23 GMT  
		Size: 6.4 MB (6427098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ae33ab09409a6ec3e4d574e2040b4b9cbfee0f8ee81a018c83230462aa5cc400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827e5b6117298cc5890de7523641360406485151dee16092e347488330dff5a4`

```dockerfile
```

-	Layers:
	-	`sha256:13ea7ef2c84a6f1c320225fc8f6b190921614487d56443538d14a13bc0c1558a`  
		Last Modified: Fri, 14 Feb 2025 23:46:02 GMT  
		Size: 3.7 MB (3656038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c106834df0494c6039f5b0e0383e6b51285bb681bb26d48881ab98c9de4d8f`  
		Last Modified: Fri, 14 Feb 2025 23:46:03 GMT  
		Size: 25.0 KB (24957 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:6184a407add62563a6c12a58d4e0b3321835951614f0a64e92f40053f9d5c1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292532526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecae6c9f64138187f3aaab9dc9c25c020e0ba4c9f9be31588297f8f32c47c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757f7d530f6b57a9f7086a87275499eba37462ad62756a55dcd465daa91caa2`  
		Last Modified: Wed, 05 Feb 2025 08:43:21 GMT  
		Size: 12.9 MB (12894981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375869b3f6f8a65acf454ad67a169dbb45188fe75df7d5e73302e5712e19b399`  
		Last Modified: Sat, 15 Feb 2025 02:45:47 GMT  
		Size: 239.7 MB (239712797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978094936965e0ba4cb547017003039de15d6c47d93a7c4c68da6dee6ecd8817`  
		Last Modified: Sat, 15 Feb 2025 02:45:41 GMT  
		Size: 5.5 MB (5476813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ea4e9609b51f146704e7486e802c58fba8a1567a0eaec454993c22eac3b83261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17121c8996057043553489e5746657223540a47bf8773f254dff615e2dbe421`

```dockerfile
```

-	Layers:
	-	`sha256:5a9346405bb97d0c3fcadd77c789195032d2b7952c304a4f7946c704750f8e6c`  
		Last Modified: Sat, 15 Feb 2025 05:45:55 GMT  
		Size: 3.7 MB (3667096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9837a43c799a5087cf7087e403e26d2d33acddb6af6301fff58168c021f49e`  
		Last Modified: Sat, 15 Feb 2025 05:45:55 GMT  
		Size: 24.1 KB (24141 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:ab8ad07c4318745cd239b7849c38915e9e47ba0e68598badce72246d1b1f2b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281583392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a0083f66c8988167ecfb24874310c3923c79e3df8ee5e103865f320c1c88a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Tue, 17 Dec 2024 06:18:06 GMT
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
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Tue, 04 Feb 2025 06:45:54 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a504edea95fbee01cd3ff3d84972a695acb9423b1d0fea8abc1fa3cac5e26`  
		Last Modified: Wed, 05 Feb 2025 08:43:39 GMT  
		Size: 12.2 MB (12212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89261cd159698f9309017c93ddbcb8e3e2b0d9c397106b29bcf30d9077147639`  
		Last Modified: Tue, 04 Feb 2025 08:27:40 GMT  
		Size: 234.5 MB (234476099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89acbb324943cf6309dadc841472a30fef3245802a021e87ec73e8e21b4500`  
		Last Modified: Tue, 04 Feb 2025 08:27:37 GMT  
		Size: 6.9 MB (6894083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:daab816a26c62d7b8dbc9e8d4f3e4d4bf5f8602b59a75ff40ac3582174c9018b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b34035a8d612600b25393c25fc86f11eb9e13814bcdc1a4cbda95ae45558de`

```dockerfile
```

-	Layers:
	-	`sha256:3e49fb25c7b3d304f18e1494f95fd69e9c3069108d62989d42eaeef314c6f8a9`  
		Last Modified: Fri, 14 Feb 2025 23:46:07 GMT  
		Size: 3.7 MB (3665511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038f96eef2eb0f7456a6192d4609e73e23dcc70837533e6734b13501df81efae`  
		Last Modified: Fri, 14 Feb 2025 23:46:07 GMT  
		Size: 24.8 KB (24823 bytes)  
		MIME: application/vnd.in-toto+json
