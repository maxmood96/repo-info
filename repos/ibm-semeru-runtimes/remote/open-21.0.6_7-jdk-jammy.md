## `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:fb98b962707245ed16bc4b2fa9a726ac4679694874199c7537dbf2c88e82f7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:4ad4bd806a2ac481544d7fb6e06e6f38b78b1a769823baa0e79e6aaac94e0040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280095123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901cb193140fe4aa0ae51fdb71cee22d0365c3ff537c726dd1858e8fe4cfd6a8`
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
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a71681168cba543a0c4d2bd43c4125cde3a908492f14e2c2549b4eb0e922ab20';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9a37a30a3803c00a3dbdb9c7d61f8a1cdf2d798e1a08903d35d7b55cc6ac2747';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de58bccd963972fc756c6b4689d27b7286b3c7ade89270fc554d2c88fa5e204e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='a09f026549a91d8d53f4c1abdb1cf26219f1ce98a46ba03b4f300f8fe3ce846e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:bf2dbee6db66b3a109b99cfbbf8b20394f707f6e9a798cb196d8998345b94090`  
		Last Modified: Fri, 14 Feb 2025 23:30:26 GMT  
		Size: 12.2 MB (12166780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a059521ac4c046d050e148ad1df63168ae6227c0e14c64d2cd408b69956b432`  
		Last Modified: Fri, 14 Feb 2025 23:30:33 GMT  
		Size: 232.1 MB (232052202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170fb7daf9cf20da9ad388bb0cb7780d1b6010fcfa681f0549755107d3b9c236`  
		Last Modified: Fri, 14 Feb 2025 23:30:26 GMT  
		Size: 6.3 MB (6340200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.6_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1b4beddd5a6a90125ff21be02e169bd249f2554b1ec0d983519df167085fb3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639f774a578ef37bc05f379241e7a6e50ae75a75a9cccd918bc33ced02703ad8`

```dockerfile
```

-	Layers:
	-	`sha256:c17417407be664d92b4260d2078c1a6282bdde253bfbfc8e0e84ce1ae6fda7b1`  
		Last Modified: Fri, 14 Feb 2025 23:45:32 GMT  
		Size: 3.7 MB (3667265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d928bfc9f00821a29ca5ad8d30d6cf36c38ae2a93b1687764e2a01d2543673`  
		Last Modified: Fri, 14 Feb 2025 23:45:33 GMT  
		Size: 24.0 KB (23969 bytes)  
		MIME: application/vnd.in-toto+json
