## `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:ab543f7f6707dddeb4100409dd00b66e15cd6e7ab8d243963662294afae7ce93
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

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:4e09ebc3c7a5596ad5fcb3459bb12e0623fb2c730086cc801c701217d9455526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296453269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b668bd1701cad0760dae5b546f8b7218a03b39d036bf7ff4b3dd1bcd3e3ec9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4695efbd5c5eb5c64c9fa44eb3afbdffe54e0bdc35e3e9fdf34bbf9e03bfe`  
		Last Modified: Tue, 02 Sep 2025 00:25:08 GMT  
		Size: 12.8 MB (12796775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea7252e28ddfe3fbed034218e253cd6d6bde9fa345af3b38e666f30597e38e9`  
		Last Modified: Wed, 03 Sep 2025 11:58:20 GMT  
		Size: 246.9 MB (246915510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047295c29f5494495b6a0034e8ee77d251fe4fbdd0cd3ec6403fc60a4e9e4b3f`  
		Last Modified: Tue, 02 Sep 2025 00:25:08 GMT  
		Size: 7.0 MB (7017920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:bab278b3022aaeeed4a6a2b4bc38b5d8341c98e2dc076ba659793981c00bde2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3275849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bce8c08e541efe6fab5293f65b3e0c68b4464a1a200ecfb8be415b6fdba1f5`

```dockerfile
```

-	Layers:
	-	`sha256:948ad50d79affd0428f18a52aa33abbaa5ecdb9475bc7e172568a61119f462dc`  
		Last Modified: Tue, 02 Sep 2025 01:47:09 GMT  
		Size: 3.2 MB (3249849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45db1d1b042c8eb4535870ff0e6d215c63d0b1312e8e77911e301cf1fe0bbf4e`  
		Last Modified: Tue, 02 Sep 2025 01:47:10 GMT  
		Size: 26.0 KB (26000 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:33c6d6cc626b9c63adc4dc336e9bc91df585ede209780e59b502b2e0e366c4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291234385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85cb552f9dba900003c293a869d6644a3ab79a1b9874c4989a75a645b452eb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eebd346760d27ea43bdb286252d25038bfe86ecdeabdde926450628e38db126`  
		Last Modified: Tue, 02 Sep 2025 01:30:55 GMT  
		Size: 12.8 MB (12831979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0757619fd4972f4fccf8a425ce215634cac51e66b2e6bef01fc2a647cb6a66b`  
		Last Modified: Fri, 12 Sep 2025 13:54:11 GMT  
		Size: 243.1 MB (243114410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06df4372e169f1ea044ed01bb014698f3710ea7201bcad06a07af6d37ee68c4d`  
		Last Modified: Tue, 02 Sep 2025 01:47:50 GMT  
		Size: 6.4 MB (6427756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3e8df8bc5fb5380d42fb9437aeeb55408e7d7c84a8e62ff9e727f65d345d271b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3275172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59182a41c3f1b7fdf0dda1fd2c1fa602a1893aaba1956a240142c1d1af0cba8`

```dockerfile
```

-	Layers:
	-	`sha256:93c4268544173ad7d4aea0241c102587dd2ea2b256d14632635bf6d1ac886b39`  
		Last Modified: Tue, 02 Sep 2025 04:45:56 GMT  
		Size: 3.2 MB (3249038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc94266a2f82ddd1cf583499152ad9af111de76880da379e5e6a4ba331e51f1`  
		Last Modified: Tue, 02 Sep 2025 04:45:57 GMT  
		Size: 26.1 KB (26134 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:09085b8aa631cd4cc38d6340eb77c7135c79db0e0baff6c728bf317930378104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304326220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e35b8667db2b8ae79e03c5eb067fd2c2d3471586a93365fbaadbc07fa3112a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da3911e6b758d282ab66b0b0fc71200d133f4696e469454e6e87cf14d1630ea`  
		Last Modified: Tue, 02 Sep 2025 00:37:02 GMT  
		Size: 13.8 MB (13795277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce8f8fd1017ef6e9c942beea686dc7a0c9ffcd5c8a0ec8bac46d415291abacd`  
		Last Modified: Tue, 02 Sep 2025 18:41:52 GMT  
		Size: 250.7 MB (250749492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6d155312f60e9ad38e0dcebb7ddd5ff2134c3e49849cc751d014c075929f0e`  
		Last Modified: Tue, 02 Sep 2025 01:01:40 GMT  
		Size: 5.5 MB (5451918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6b16bc39844ea83ffe81050cd4e1849372e3f194b2db6308240893617cfa2f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16de597a06432f764a50712349d75b1a47347731a2dc8e7894566302652fa1`

```dockerfile
```

-	Layers:
	-	`sha256:ba033abe6b7a88a356f625514c99624d03e740c6dab116884e64289edc664322`  
		Last Modified: Tue, 02 Sep 2025 01:47:18 GMT  
		Size: 3.3 MB (3254489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7850e4ff5b750c161e7a321c711003d966598d83edda399e1485583cf66a5b6`  
		Last Modified: Tue, 02 Sep 2025 01:47:19 GMT  
		Size: 26.0 KB (26048 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:42ccc0ddfbfe5e4da0393b559d89f51a85894ba265a3557d2a2987336ab1efa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294635340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050f60d995b215103301f2cd5f67210c5ea86fdd1638b7e132a2e3844c61c9ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607d171642e4dfd2794c14ff8a44918bed32d5bf9b225263c0f901bf8baf13e5`  
		Last Modified: Mon, 01 Sep 2025 23:26:45 GMT  
		Size: 13.1 MB (13120955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af835c0322eb2eae6ca18a2586cd9b18626d758a6720a1cff35d2c4fe11657`  
		Last Modified: Mon, 01 Sep 2025 23:48:07 GMT  
		Size: 244.6 MB (244610504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264c16dcd21e85b2940908e475176e42e41efdd81c3e56c823b8f51c70ae7c`  
		Last Modified: Sat, 06 Sep 2025 22:53:03 GMT  
		Size: 7.0 MB (6970872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:32297a520f31c6929a4f7db0bef8c410a20ce14197a13b7a5b98f6579deec568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a284f06aecbc3bd097bbc9f68935f20c77d1e288ccb0cc3e176df87143b632`

```dockerfile
```

-	Layers:
	-	`sha256:29d639e355928d6700f6b3b9ee362c224af3cc7f26de107b0b428c20c1b19561`  
		Last Modified: Tue, 02 Sep 2025 01:47:24 GMT  
		Size: 3.3 MB (3252673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1261b717e071aa19c7c12584358acc71eff56c2ac923d0965bf855218f3ea2f7`  
		Last Modified: Tue, 02 Sep 2025 01:47:26 GMT  
		Size: 26.0 KB (26000 bytes)  
		MIME: application/vnd.in-toto+json
