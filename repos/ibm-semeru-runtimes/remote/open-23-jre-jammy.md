## `ibm-semeru-runtimes:open-23-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:7d3ed314dbbfc38974e8074f67ffa12213a87790b66f2902d96cc8f61831101a
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

### `ibm-semeru-runtimes:open-23-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:0938ad416c27ea7fe3e48a2f92e049bdbf3ba34a6d35c9ba97178347590c3291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102934211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab47f3a442a8727a4ded8122ed382daefb38d6422f93729b99f14b2876bfd0a`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5fe867c329d8f7d14df62b1091a7fa3ee07b283c3ad435600e249bcb665a9`  
		Last Modified: Wed, 05 Feb 2025 12:50:07 GMT  
		Size: 12.2 MB (12166008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b6ad9d845fe26034c6542180574d287694768d3fe9ef91b398912f01484595`  
		Last Modified: Wed, 05 Feb 2025 13:01:57 GMT  
		Size: 55.7 MB (55676325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71450772e2af344125114cbab37c110e57947145785dfc3d21e18f87b490322f`  
		Last Modified: Tue, 04 Feb 2025 23:13:28 GMT  
		Size: 5.6 MB (5555937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:bfd7424d0ffbf07d1c94a314b0c4db5b5bf03e2d45b7b7016601eb277f2d020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750f4d3834412a8ffdd12b0008975b64f1e8152257711409c5c7d64f96a6c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:c22ddeee5df7ceb0be9fc7b2235671e3ac75ff35e96ce2dfaa8c739eae1f9b2c`  
		Last Modified: Tue, 04 Feb 2025 04:42:17 GMT  
		Size: 3.6 MB (3583418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9082368498b51448533fdd9879bc2783a7426f34fbb972b73140142002d2f835`  
		Last Modified: Tue, 04 Feb 2025 04:42:17 GMT  
		Size: 24.8 KB (24826 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:ff2e4aa73f616a82a5cd3861a18af44632066df354154674925573edb9a6aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96187283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4712f4636df9800841bb04928c070d96dc34ade9d60dc4841a7d9ce74098e3`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:8ea765cfb7407c0581580b0a50d4776d1e5e6d7307785b14248765a80ec186d5`  
		Last Modified: Fri, 07 Feb 2025 08:10:20 GMT  
		Size: 51.5 MB (51498104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33b09ade94c7a5df859f156191585733e76364994dc2c605bfb884304d24dcb`  
		Last Modified: Wed, 05 Feb 2025 18:27:34 GMT  
		Size: 5.2 MB (5207560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e4e662bf35de10ccfce65fae020fc062640e81b825b6f3698ffd1bdc8be48779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d71d9aceaa0cf8b6ea24789bab5f494bfdd4258ca5caaf896ceacf00e14b0b5`

```dockerfile
```

-	Layers:
	-	`sha256:58b5f3945d7a0b713b4104fe59d7bad94c20da243779e154c1e44b8f72f01c2f`  
		Last Modified: Tue, 04 Feb 2025 09:57:24 GMT  
		Size: 3.6 MB (3574934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91175042fe26a6cca8ff123fcaa5b641109f0d1ee3559f566c74216fe1a64c90`  
		Last Modified: Tue, 04 Feb 2025 09:57:23 GMT  
		Size: 25.0 KB (24959 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:30be341e48fd97342b64e7c76d3595c0b56eddddfb23b2ce7bf26852be38e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108306007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fd5088dd11165048f5f8b279f6327590dc96ae1de24abec5d656ad5b26cab`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:291bf37dde1f16010ee10a005e33b0e111ee0c6a5ba31a82042c250a5f62032d`  
		Last Modified: Tue, 04 Feb 2025 08:20:23 GMT  
		Size: 56.7 MB (56734527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb93186f19a0306aa27595d6142d87c61a37548014472b1fa2bd2d87d18ed3a`  
		Last Modified: Tue, 04 Feb 2025 08:20:21 GMT  
		Size: 4.2 MB (4228564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4b6fab6945b96a8017f8d7cf9511f8a2ba20fe85361c4ee9bcf879e9653daa5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae98359d5730aa1bb87de5d54ac1b1cfe3240de89b3e91c2a9d31ae187326e`

```dockerfile
```

-	Layers:
	-	`sha256:2ce5b39bc1c467cabeeaab870b416258051ebdf6b4638d139f2aa967c0e0ddcb`  
		Last Modified: Tue, 04 Feb 2025 08:20:21 GMT  
		Size: 3.6 MB (3586065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29e2858b623c6eb645155bac89d43eb1bb13ef6610db31b3627427433687074`  
		Last Modified: Tue, 04 Feb 2025 08:20:21 GMT  
		Size: 24.9 KB (24874 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:6b55d66164f3f31c8bf513d8e05c3c971f180158985d5ce693570250dc9eb666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100252199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01953286215a43616f9470da77274cb31d0f463fcaceacbfe376acf414d6cd19`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:807777af48de6570181ba857876d670d753d7191e8861647fadf5369b8ba02f9`  
		Last Modified: Tue, 04 Feb 2025 08:29:12 GMT  
		Size: 54.4 MB (54434413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381f856eb81830cc2946cd6ae37b5eabb49c18ad41fb3f04b6f33db755ca854c`  
		Last Modified: Tue, 04 Feb 2025 08:29:11 GMT  
		Size: 5.6 MB (5604576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:dbaea331b8a2ab8e71ade0d125958ed98106efa40c6a11b6721ad47efcddfbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6f2e6a0a06645044c43197af6e7d2e4efb730ed1e0b374010d9955a6b1076a`

```dockerfile
```

-	Layers:
	-	`sha256:3e3ea0ece22693a56fa6fd89edf7fc15f3a82f650e7a263459433c0f4c638475`  
		Last Modified: Tue, 04 Feb 2025 08:29:11 GMT  
		Size: 3.6 MB (3583782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d974b472a9d0a76d60ccfef39eb1e45103ae0a885e220d053201dd1cefc432ea`  
		Last Modified: Tue, 04 Feb 2025 08:29:11 GMT  
		Size: 24.8 KB (24826 bytes)  
		MIME: application/vnd.in-toto+json
