## `ibm-semeru-runtimes:open-17.0.14_7-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:4b02e2dce1c4ea179235f576544c7d63714bc1c5923beed66e15c3ef9dcbf92a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `ibm-semeru-runtimes:open-17.0.14_7-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:9c0d9cd76a540caf702fa7044bab3f39793e10db6c692e971a02dadc8c7d54f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100275959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c4bbcb2c48c0a57ba05fae8260277eaa455885f7de9f11cae7e6c355463dcf`
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
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:5f7f5238001632678204542d7479468444f253111f9933c2d2287106dffe428f`  
		Last Modified: Sat, 15 Feb 2025 00:31:08 GMT  
		Size: 16.1 MB (16075902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c662afe7c0ccef9c235243d9fbcb597f3157ea915147c7daed7944b91a93f2`  
		Last Modified: Sat, 15 Feb 2025 00:31:11 GMT  
		Size: 51.7 MB (51659766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef3095b82c9e8e95f6ecf0eb32ccf4671fecceced27246f67e18f449b78d8fe`  
		Last Modified: Sat, 15 Feb 2025 00:31:08 GMT  
		Size: 5.0 MB (5029231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.14_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3b3958873c183409fa639db32da7ae3834f10b6cbcfd28591fbe203b832f3c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3613046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53586b5d56884137f82fbf0514946dc2e5d195ae8fcd03e8dca36dbbb30e7fdf`

```dockerfile
```

-	Layers:
	-	`sha256:b9cc1e2df95d9f10e8e702f6ff7736d32a95b0715754ca903dc191085d8e439a`  
		Last Modified: Fri, 14 Feb 2025 23:45:08 GMT  
		Size: 3.6 MB (3589042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd005f6287a1089e1fc66215497498dec3c05717e1110d84107ecdabdf7d199`  
		Last Modified: Fri, 14 Feb 2025 23:45:08 GMT  
		Size: 24.0 KB (24004 bytes)  
		MIME: application/vnd.in-toto+json
