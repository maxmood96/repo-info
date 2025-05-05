## `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:a18874a1e5e7ad46e106823c56de20a9d630d014f613540b49431cd468e9c0d0
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

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:ef95da148f87cd9153157b715b43cae54d0fd05aa69b6e3ea2ef249b6e4f50d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280086803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdad254f3a3cc124bc884304647da860baaae95d5bde9a3ac258e106a1ec422`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a71681168cba543a0c4d2bd43c4125cde3a908492f14e2c2549b4eb0e922ab20';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9a37a30a3803c00a3dbdb9c7d61f8a1cdf2d798e1a08903d35d7b55cc6ac2747';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de58bccd963972fc756c6b4689d27b7286b3c7ade89270fc554d2c88fa5e204e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='a09f026549a91d8d53f4c1abdb1cf26219f1ce98a46ba03b4f300f8fe3ce846e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f767a66409ced8901656a294b622a942fe8dd64c62b58378bb77e10c64e810`  
		Last Modified: Mon, 05 May 2025 16:36:12 GMT  
		Size: 12.2 MB (12172195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5106135ebe3ca15d2437f23ca2571caa9ccbd9e01ea9c58628a460d96713230`  
		Last Modified: Mon, 05 May 2025 16:36:18 GMT  
		Size: 232.1 MB (232052154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48314291ceba87fbe8f4307f0dd00ad703eef33eb0c1cc1cc56e777456fa596`  
		Last Modified: Mon, 05 May 2025 16:36:12 GMT  
		Size: 6.3 MB (6329840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9084f06610504880c219569c0622eb953a4529626e55c5b5d5351748449c1c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2160ff631d7111c8717ad223964fbe26ce204c2cb8945761b8ce6271ae64c39e`

```dockerfile
```

-	Layers:
	-	`sha256:b09a0da2952f905a18c1b21d68c560b0ccd04e289432e27effcf247f00ee4955`  
		Last Modified: Mon, 05 May 2025 16:36:12 GMT  
		Size: 3.7 MB (3668235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e10bf56363dbca086d2ef337a314b74533df17d64b0dad07b09ee5fc540de01`  
		Last Modified: Mon, 05 May 2025 16:36:11 GMT  
		Size: 24.0 KB (23975 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:1afbf6793f3452fbf7a012a6e6b4938148e230992822f48ad4d1e4d48ccbc965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269597246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fb57982d83fb4aa1b89fa6d6e2960e958fcff540cb50b679e986bb31063dfc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a71681168cba543a0c4d2bd43c4125cde3a908492f14e2c2549b4eb0e922ab20';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9a37a30a3803c00a3dbdb9c7d61f8a1cdf2d798e1a08903d35d7b55cc6ac2747';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de58bccd963972fc756c6b4689d27b7286b3c7ade89270fc554d2c88fa5e204e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='a09f026549a91d8d53f4c1abdb1cf26219f1ce98a46ba03b4f300f8fe3ce846e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Mon, 05 May 2025 17:14:03 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590f7e678243a5c44f467ab72bddc8b062fa5e396ea63a80583f451c93a1e450`  
		Last Modified: Mon, 05 May 2025 17:27:19 GMT  
		Size: 224.0 MB (224030076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286525dcb2d28c1da96b0d238314b18255b758c1d2de69e652a9ab0e9ddd5b3a`  
		Last Modified: Mon, 05 May 2025 17:27:15 GMT  
		Size: 6.1 MB (6083542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b8319c53bc28649993088a332e4439efed1e85baf85140c35a1b116ef405fbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0916c5f52cf1fb16b21e26eb4a4fd8818564b89c691f34952d0a22755a8ea6`

```dockerfile
```

-	Layers:
	-	`sha256:361fe92fcc5df15543781408a48b8391dbe2507400316895638209dac47492c6`  
		Last Modified: Mon, 05 May 2025 17:27:15 GMT  
		Size: 3.7 MB (3660956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e193c27ebc32ab9e504e932b02d42861a6f08305648ff3bf23fea2f217746b`  
		Last Modified: Mon, 05 May 2025 17:27:14 GMT  
		Size: 24.1 KB (24084 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:429d87a4d4074e26ffbc60d0b8ed4e7ce4a1ed55cf7188a1dc666606c1dfb996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285353983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01529d96577a442e3d617e2fb3cd83dec3920471a321630bb2a24991595025b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a71681168cba543a0c4d2bd43c4125cde3a908492f14e2c2549b4eb0e922ab20';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9a37a30a3803c00a3dbdb9c7d61f8a1cdf2d798e1a08903d35d7b55cc6ac2747';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de58bccd963972fc756c6b4689d27b7286b3c7ade89270fc554d2c88fa5e204e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='a09f026549a91d8d53f4c1abdb1cf26219f1ce98a46ba03b4f300f8fe3ce846e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a64c9f5a72745f3bafe1231a1d79f060f125195fbcd3f510afac643f962e127`  
		Last Modified: Mon, 05 May 2025 16:55:41 GMT  
		Size: 12.9 MB (12893020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444cf94c2a4554c40a6b17650dde6b43349b5191b18a23581edfad2aaf59707`  
		Last Modified: Mon, 05 May 2025 17:12:08 GMT  
		Size: 232.9 MB (232908069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3156c0d780d00829197c909a09ec8aa05fba8ac8cd217dbcff9ad78e6ebb62`  
		Last Modified: Mon, 05 May 2025 17:11:57 GMT  
		Size: 5.1 MB (5109679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1b0552ab7a7fc3ba03b0efdfdc19213671860e19292326f6c528a03d241dced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653871bfb288635c979f18faaf154871c4647e7c559359a292fa2b5574cd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:252db12cb70b6680057cd3a84cf640d03eba4b180ac9c5172dcfb0854a8d53fc`  
		Last Modified: Mon, 05 May 2025 17:11:57 GMT  
		Size: 3.7 MB (3668380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4252b6ed2b72114a33111a150379253676bef28d752b16c634cb66cea5a6d6`  
		Last Modified: Mon, 05 May 2025 17:11:56 GMT  
		Size: 24.0 KB (24011 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:cbabf8fdb572107f5e0fc57dc35416c1988f09835ee6305e213efb0d0f6a5910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274489193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c1dcb8a02e430fbdadcb4440f58764286efd03ebbbb6b0ba113bc8b9b806cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a71681168cba543a0c4d2bd43c4125cde3a908492f14e2c2549b4eb0e922ab20';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9a37a30a3803c00a3dbdb9c7d61f8a1cdf2d798e1a08903d35d7b55cc6ac2747';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de58bccd963972fc756c6b4689d27b7286b3c7ade89270fc554d2c88fa5e204e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='a09f026549a91d8d53f4c1abdb1cf26219f1ce98a46ba03b4f300f8fe3ce846e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573305c63c6b8034a976ad865f575e2879ba561788a75b917f925a7f6f45b358`  
		Last Modified: Mon, 05 May 2025 16:47:08 GMT  
		Size: 12.2 MB (12219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abde9e6ff1a63681ee553c5ab727b9b75b672d62f76739c491d91ff86e855b96`  
		Last Modified: Mon, 05 May 2025 17:02:00 GMT  
		Size: 227.8 MB (227809508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0928aceafb900c0fb07c0053cc982a2a890fc02751e1cc2b0feda62c2dc2ed6`  
		Last Modified: Mon, 05 May 2025 17:01:56 GMT  
		Size: 6.5 MB (6460500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0de4e98b4f5f2af1e3dd9212e9e0e2bf3387a3a59c60bb6e6b772209275b8161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0791b5536bd007b15f2d25710d6ea1a96dd11b0de413883b912eecf0128d1ceb`

```dockerfile
```

-	Layers:
	-	`sha256:24a08e1e16b47c99cd3176d878dc51240ae92ce6f581d8aa70d11ba43b4d69f3`  
		Last Modified: Mon, 05 May 2025 17:01:56 GMT  
		Size: 3.7 MB (3666109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285c34f1da6d5ccee6a1a252a98a79415bad907e4db5e31d22db5602c335f534`  
		Last Modified: Mon, 05 May 2025 17:01:56 GMT  
		Size: 24.0 KB (23975 bytes)  
		MIME: application/vnd.in-toto+json
