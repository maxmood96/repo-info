## `ibm-semeru-runtimes:open-22.0.1_8-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:5baae82681a68347a48e62d5bc93423520591bce4a161039ace3397f9d1d4adb
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

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:cb328e71869abf1f814bf629df17d2b168b419bc7417ac56c4507db7b0862e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275915889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cf8c1e8393f2331923c620f7b1ac0ffb173aad64e850f74eb7c199d7a0afe0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='feb2734b519990d730c577254df5a97f7110bb851994ce775977894a9fdc22c7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6e54d984bc0c058ffb7a604810dfffba210d79e12855e5c61e9295fedeff32db';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6856013348e19f3e532e6658827ba8297a8741cdd573e9640b8263562b670f87';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6a6e47d4b4a175bc283049214e40c7cd560c8a133d04429bc444defb075056e5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e97e16e3fec30bd148e83f87029d49ad30d1461bd5fe2b8978c6ceff249d8`  
		Last Modified: Tue, 02 Jul 2024 03:04:15 GMT  
		Size: 12.2 MB (12156414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050d6831e8926680599d07579beb348ef3f015417a1fc9f0b91343572bbccc48`  
		Last Modified: Tue, 02 Jul 2024 03:04:17 GMT  
		Size: 227.8 MB (227824456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34b9670b1d603601b91d801ccd6c56e8da676eaad680f9b5b363eb1c301db6c`  
		Last Modified: Tue, 02 Jul 2024 03:04:15 GMT  
		Size: 6.4 MB (6400964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:47e92b5818b7fd099d83770b9282e4eecd5f9f9a151c3d339a3c0a2c9750b4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44826b8644a31b1eddf1fd47df15c4281a81b0acd6f7322668170f10ea485cf`

```dockerfile
```

-	Layers:
	-	`sha256:5555663f7ae21da1b431c96d0c49d2d3a7c63f9532bcb106af277d2b2682dda5`  
		Last Modified: Tue, 02 Jul 2024 03:04:15 GMT  
		Size: 3.4 MB (3434930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21fddff100da51fd7d1f832fbac6335a8cbe4e17626ff9b675de3ae2ffbe2e37`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 24.4 KB (24395 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:f5171226da319aff34ecb6551cf43c74a5949d3f4a222c7eea3f3423f666178b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265305508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c871fa8f82542913e2aa8fdb221ee118cc00581ac29b12a6997a60a63061cad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='feb2734b519990d730c577254df5a97f7110bb851994ce775977894a9fdc22c7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6e54d984bc0c058ffb7a604810dfffba210d79e12855e5c61e9295fedeff32db';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6856013348e19f3e532e6658827ba8297a8741cdd573e9640b8263562b670f87';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6a6e47d4b4a175bc283049214e40c7cd560c8a133d04429bc444defb075056e5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692adf9a131a320c3ae4ce96d951bd52523484a08c2b71d83bd894fb57af1a9e`  
		Last Modified: Tue, 02 Jul 2024 15:05:06 GMT  
		Size: 12.1 MB (12114298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16cd98ac02b0bce10a6939a1422d4edb7bc39de5eaab570fa4b2f4f9bb0caa0`  
		Last Modified: Tue, 02 Jul 2024 15:14:14 GMT  
		Size: 219.8 MB (219755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdae766039e9935da78bd9deb827959b491fef0b7d5bd3bce0837aee8ef2cc2`  
		Last Modified: Tue, 02 Jul 2024 15:14:10 GMT  
		Size: 6.1 MB (6075801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:939c64ffec3b904ae8d5a9c4061f967b7a8ea7c971d6a55069e88d847618a5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a2f1e91955783f8fdb04a1959e832d1d2c9452106ccd5fef9abd8cb62cefd1`

```dockerfile
```

-	Layers:
	-	`sha256:6f635796593473f4b29eec42404d048f1ff467a48cfed56fbfc26a2de0aa7871`  
		Last Modified: Tue, 02 Jul 2024 15:14:10 GMT  
		Size: 3.4 MB (3435219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98842ceb113236bbc2f8119620ec8d65666c0586dc708248dfdbde924e091df6`  
		Last Modified: Tue, 02 Jul 2024 15:14:10 GMT  
		Size: 24.7 KB (24695 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:7b1759f01b08a46d7fa55e5c14e3b496929ffb7c2b82694799b9ff64dabd3130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283796131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3952d480c2b6713f64eeb1b2eca25db5ceb133843e5b461c6bbf790f9b66b549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='feb2734b519990d730c577254df5a97f7110bb851994ce775977894a9fdc22c7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6e54d984bc0c058ffb7a604810dfffba210d79e12855e5c61e9295fedeff32db';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6856013348e19f3e532e6658827ba8297a8741cdd573e9640b8263562b670f87';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6a6e47d4b4a175bc283049214e40c7cd560c8a133d04429bc444defb075056e5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba08511b677aee03243955ecffe2cf3bff11dcf9bbc6f35ad5e9deb073b144`  
		Last Modified: Tue, 02 Jul 2024 10:27:08 GMT  
		Size: 12.9 MB (12888223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27914d5276679c856bbbafec3ce91ee7ddc502b914c35a996f30adfe8b7ab09`  
		Last Modified: Tue, 02 Jul 2024 10:39:04 GMT  
		Size: 231.3 MB (231270727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b4bb92668554db8a6ba9ca23328026de14b71c6d825ca61c210815fe0c1a1d`  
		Last Modified: Tue, 02 Jul 2024 10:38:58 GMT  
		Size: 5.2 MB (5176100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:16e1ac36944d5998e7cb370344ae1ccdd13fc0f37d252489da923e6d641b47c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504d8957dab263423e6fa874eaf2980fed4a08712383570f3c71bdedebfb9ead`

```dockerfile
```

-	Layers:
	-	`sha256:7fad1824873a22fa7fee3b9ccc645a816ec61ed00ce6bd06e53aa00a7d452173`  
		Last Modified: Tue, 02 Jul 2024 10:38:58 GMT  
		Size: 3.4 MB (3439430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93af26c308c0de52fb179193f1bb645cc19c3bb090482d8e051acef685ab42fb`  
		Last Modified: Tue, 02 Jul 2024 10:38:57 GMT  
		Size: 24.4 KB (24437 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:7cd1f5ed5c8f3e5b014a02b8b9b106c3a20e263de157c0fc18be82b2a36ef786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272872530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e275c42a3d19de623245035034332846553d1f1f981f3bf7b4d8cc7dc06a54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='feb2734b519990d730c577254df5a97f7110bb851994ce775977894a9fdc22c7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6e54d984bc0c058ffb7a604810dfffba210d79e12855e5c61e9295fedeff32db';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6856013348e19f3e532e6658827ba8297a8741cdd573e9640b8263562b670f87';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6a6e47d4b4a175bc283049214e40c7cd560c8a133d04429bc444defb075056e5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jdk_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac3110a5d1eebf9525a140f60c8dbde0133312ec7905bb4cff8ce58bfde450`  
		Last Modified: Tue, 02 Jul 2024 05:55:15 GMT  
		Size: 12.2 MB (12203618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dda02cabe20aedeca641896670a22be43db9931a0b371852e5a19db0e3e227`  
		Last Modified: Tue, 02 Jul 2024 06:05:51 GMT  
		Size: 226.2 MB (226198842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44fcd14a8aaf321ab58d884df177448eae267d8748a9f706530aef89c8f2ea2`  
		Last Modified: Tue, 02 Jul 2024 06:05:48 GMT  
		Size: 6.5 MB (6469530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.1_8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:83e54b2fb4d3a80fe7e69e5bee9e9373228acad40be0636588f7e59ec9c1adfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3460595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1bfe19419003de2c9c8c9adfc16919fd925c84df6b5f251c846638bbab2fe1`

```dockerfile
```

-	Layers:
	-	`sha256:3ddeb51745a631563711378ee015687139b8e9bfbd71ffc5259bc7535ac1727b`  
		Last Modified: Tue, 02 Jul 2024 06:05:48 GMT  
		Size: 3.4 MB (3436200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1bac390fdf0de969069d056667f2b92576b4bf6e43504d69d875a5d28e0195`  
		Last Modified: Tue, 02 Jul 2024 06:05:47 GMT  
		Size: 24.4 KB (24395 bytes)  
		MIME: application/vnd.in-toto+json
