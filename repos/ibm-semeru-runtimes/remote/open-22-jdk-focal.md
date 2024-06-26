## `ibm-semeru-runtimes:open-22-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:cb0ce596b843e7f8e7ba7714d95ed2c6ade4a629593ab03630974b66d821bb56
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

### `ibm-semeru-runtimes:open-22-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:2d2d93e0342b2624a0e89ba171f894741f0f9694b49e6d0f407b375f3d944bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277789855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39978ca1b5207517c6dfb8c3d15473fab2ca6957b27b16de8f4cd076ac58b886`
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
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f4a7fea4e32bb4f53bf3c6ba094c56a84b28021ddac7329feb3f2a07d6ab6d`  
		Last Modified: Tue, 25 Jun 2024 22:58:10 GMT  
		Size: 16.1 MB (16059496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dca657e7a7e5a78d565f02cc78e5451edf27a22151c4d72bec51e35385f44d6`  
		Last Modified: Tue, 25 Jun 2024 22:58:15 GMT  
		Size: 227.8 MB (227824445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43235925e78d470151e4f045bb2ed4d915a5fee5f9f83dcaa125a5d938969e9`  
		Last Modified: Tue, 25 Jun 2024 22:58:10 GMT  
		Size: 6.4 MB (6394145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9642845d950a11bdece505b88fb1eab34fd400fa8503b4228a5375aa5064a860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3461958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4ae888ce5ac6fc8465dda751fb69876a14ca6e397e72b83a8a48b868b66382`

```dockerfile
```

-	Layers:
	-	`sha256:5c8e9d74f66d1e8aadcbc90fc5de0c4c26ce7871110146652f99d372c85def96`  
		Last Modified: Tue, 25 Jun 2024 22:58:10 GMT  
		Size: 3.4 MB (3438243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e7cf5a8d601af1470d0d188b29ccebd02223bd7a9f4719719a65be3a5f2b22`  
		Last Modified: Tue, 25 Jun 2024 22:58:09 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:c48dab4a871eab293e61633d6c7f6ea0d83c24bc85f57dd25a0712cfea038131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267719453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe98fa993e7368bb106c55358d99673a6d39216366e79f4d9806ecc9157b3ee`
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176d538118d9c20626923c1883abdcc6b8627cf4d4d612b9a0dd7f1d0f1b41a`  
		Last Modified: Tue, 25 Jun 2024 23:01:16 GMT  
		Size: 15.9 MB (15921752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b4016b7f7f43dd1072693fabfded001a2a84b437cb161cbf10aac061ef8c5e`  
		Last Modified: Tue, 25 Jun 2024 23:32:55 GMT  
		Size: 219.8 MB (219755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdcd5be60b1a267591f190afcd4bf0f9bb0695ebbc1315503dcf3b508d69b48`  
		Last Modified: Tue, 25 Jun 2024 23:32:50 GMT  
		Size: 6.1 MB (6068100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:293c90aa2957ed3284b3574864433254f1b2ffd3d6a30b0ad36ea79d76983a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c8b9c1106e7fbbcbf4463ba29d5e37d5655a560cd0bd666d5a48af6f341bb`

```dockerfile
```

-	Layers:
	-	`sha256:6b063aa630f40205122d1b065d26046fa02b6e0b5f6dcb88ba4223cba38ba6cf`  
		Last Modified: Tue, 25 Jun 2024 23:32:51 GMT  
		Size: 3.4 MB (3438489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321e9a1fd5b72728a57731b7eabc686d45e6b623a7d75a548ae7db86eccfdeaf`  
		Last Modified: Tue, 25 Jun 2024 23:32:50 GMT  
		Size: 24.0 KB (23992 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:80507d8d6a767ae7533e5258e6bfdc8845b38a0dc2588cfb1239927bff35636d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285764727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11c6ceca976dfa6051aced94805dd205caf3fec53189f9ec02ca1685d43a31c`
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
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a396fd21a1d23e16c5c923d6952275d92d4ae28dc2a5e58de9d21ca3f7e3fe`  
		Last Modified: Tue, 25 Jun 2024 23:01:33 GMT  
		Size: 17.2 MB (17240286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a6a9c14c5bc12b511d8b9d0874beccd4ed4763236926d270d88fc03ae4253b`  
		Last Modified: Tue, 25 Jun 2024 23:41:33 GMT  
		Size: 231.3 MB (231270727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaa92dcffa5999e29e1565a8d1931ca047f984e013a52c830979d148b50f21e`  
		Last Modified: Tue, 25 Jun 2024 23:41:27 GMT  
		Size: 5.2 MB (5176574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c8d64199b2b9eeae96ae192546e660b3071fccf7a97e3e46dfb41b7858fac470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3466423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cff4ce19fd2d738f88bc25c27b286a8aac1130fe289f28eda1671b89ef0958e`

```dockerfile
```

-	Layers:
	-	`sha256:f8cca59f44bfd2b85db9484fa2ed7a9c7c5c350cd25321ae3b15a9977bce7a1b`  
		Last Modified: Tue, 25 Jun 2024 23:41:27 GMT  
		Size: 3.4 MB (3442678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1fa0c50d54e002656c7b0d6ea3f5c7914f74031bd41686fc227ec2a7ae7e778`  
		Last Modified: Tue, 25 Jun 2024 23:41:27 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:59b0efec355d01f3d32c4098fcf2d26404fe01af77bd6ace2f55ee936088fc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274793752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7df7d467ecae5092228a644422e45532bc0cd75e55b9a8869ea269aed0fa59`
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
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f28dd05fdcdec551c55aa8b54e4bb1d0df07a936a70442b7d2b536674bd1c`  
		Last Modified: Tue, 25 Jun 2024 23:00:45 GMT  
		Size: 15.8 MB (15751504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708bc0c5074e7c1e122f3a4007f57553e9ce4ea9a15920339a4341f4d40e9ec2`  
		Last Modified: Tue, 25 Jun 2024 23:23:07 GMT  
		Size: 226.2 MB (226198811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97869e57cdd3cf1c586616eafefda37e73ef1a1f5560ae4f6c3dae956067407`  
		Last Modified: Tue, 25 Jun 2024 23:23:04 GMT  
		Size: 6.5 MB (6476243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6fe67150bc1d108efa2a7e5bd1614956ec111769c88ef4886d99ac64dbabe70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0430a27b9bc23d2c48231041660120ba20c0f36fafa28ba9c12bad117db28cf0`

```dockerfile
```

-	Layers:
	-	`sha256:e1c81136202e29b7e1b3152226b447891d86aff4c2b6b511bea47b8068074947`  
		Last Modified: Tue, 25 Jun 2024 23:23:04 GMT  
		Size: 3.4 MB (3438712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d96f5d0d73a7de40b0a78d59160c1b84e8ba7e31630f4d38f248c9f7f39e8e1b`  
		Last Modified: Tue, 25 Jun 2024 23:23:04 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json
