## `ibm-semeru-runtimes:open-17-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:5ba9cdf225404a866bad41ca742b1e0fc551c4b5190c3ca379c73c4d3b69c423
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

### `ibm-semeru-runtimes:open-17-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:fd74bfa86a42068919e40b5d2865f5b12d5e2f11e3cf69039779e2e805c1f52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274171191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ef182f9e0fffdbc06e8324127db1201fe6453cb79c0379348f439150469e1`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:2051635c9f279868fc9a51956803b48649be8902cc72c0a91212dea3d949759c`  
		Last Modified: Tue, 02 Sep 2025 00:21:11 GMT  
		Size: 12.8 MB (12796809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2db2a9b639faff12e61cfabc31008b9c287328b789e05008ab76b30b9f546`  
		Last Modified: Tue, 02 Sep 2025 01:13:33 GMT  
		Size: 225.3 MB (225320019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34053314d83c4e2986ba9b142f768ded1812b3b312d03c5191642620b57f54ba`  
		Last Modified: Tue, 02 Sep 2025 00:21:12 GMT  
		Size: 6.3 MB (6331299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7c11db907951767de54a98d7273f573fccb025df88bf166c1d529620de8eaf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3279398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0adab30d2983b2e0698e9d54a27f15f1d8e3d9cee99a6e712810441dd385e8`

```dockerfile
```

-	Layers:
	-	`sha256:181427d0b6c514d22a2bd4060424ffdc0cfaaae407e97e80f1ffa31f4efeb687`  
		Last Modified: Tue, 02 Sep 2025 01:45:19 GMT  
		Size: 3.3 MB (3253416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f76062d4f12e3af36293e6ddc8b89a3e88e136a43b1597de3667fbd274b281`  
		Last Modified: Tue, 02 Sep 2025 01:45:20 GMT  
		Size: 26.0 KB (25982 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:6d103698fb548909f073562abe5ec24341a75bace101500728f9e6cb24853da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269241664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62cde2db612d972ddbe2fa2055b377952ac6a33020cd53b33fd5d1760ab281c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fa021ed4ae64b8298c455703a2b4e4fbadd3c86bd0d1872f0f2590d828887`  
		Last Modified: Tue, 12 Aug 2025 19:09:19 GMT  
		Size: 12.8 MB (12832180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a294fb6c6e6fc53e4eb3dd6ed8aad94a32019b14ef2a9181c39fadc914d89552`  
		Last Modified: Tue, 12 Aug 2025 23:04:29 GMT  
		Size: 221.6 MB (221561515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc167523ee72b69ae9a7e5cb6ef4467d7efd273d2d1089b9fc1dcb05d3e6e37`  
		Last Modified: Wed, 13 Aug 2025 21:51:56 GMT  
		Size: 6.0 MB (5987592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1d8c4416bfc7e0f89461ceb429533cc49f37609bf3d342f67380b499d9b402ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aee23514f4e5ad41f0b6f5652c0a1e408ba56e34e87aa9d0645986515f0650`

```dockerfile
```

-	Layers:
	-	`sha256:7ff04e9da62f34d7e00ef48862e32757327df8022bbf065dc09a45128c38101c`  
		Last Modified: Wed, 13 Aug 2025 22:44:50 GMT  
		Size: 3.3 MB (3252605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84bfb3073a9aa814087d8e1d7a167d99932014c58d63d26e70e6b938191d114`  
		Last Modified: Wed, 13 Aug 2025 22:44:50 GMT  
		Size: 26.1 KB (26118 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:1074ed8ebbc6aaa8debc9af7cee175bf8c699ec11e75cc72c3405fbf4f247c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282227985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93dd77a5efca186ea9b1fb34590fbf5ef20a763dd689e20c91d6b50b0671b46`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:2add11591a07685747dfc1a07f833a23929a1938a411a563f215c771ee105dfc`  
		Last Modified: Tue, 02 Sep 2025 00:48:38 GMT  
		Size: 229.1 MB (229090377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d88ba1e64f34e93045ef54e27f47dddcb7428b334ccc69af083fd08ff79d41`  
		Last Modified: Tue, 02 Sep 2025 00:49:02 GMT  
		Size: 5.0 MB (5012798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8bb2bb88b408ff39a4fc1a6a893f6add84012abdfbae8e7b935cbf5ae5068fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3284088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f3d57ca298ae4a2253646efbbc6d05e3dc37e7d65b28ed16b9041adc7ec39a`

```dockerfile
```

-	Layers:
	-	`sha256:6c977876955c8b80aa9b985e6bd552ad667a366866299b7a77bd0dbdbc0031f0`  
		Last Modified: Tue, 02 Sep 2025 01:45:28 GMT  
		Size: 3.3 MB (3258056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986ef12027df0fac3304a754f96e12ba72267ef6d95c610a51bc9b22511b7af2`  
		Last Modified: Tue, 02 Sep 2025 01:45:29 GMT  
		Size: 26.0 KB (26032 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:f4da5872e21cb53562467f520f0bb1c049606cf76cd889afdd5e751c6092e4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272452332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4abe05871199d694e710c7598baa03f664e0758952859a5e64c8170c303218`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:56bd681605fb87f78f9262f7351411336fdc692ef64d00b136d553a3744d269b`  
		Last Modified: Mon, 01 Sep 2025 23:37:46 GMT  
		Size: 223.0 MB (223034705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9306c3527a7621ab9c47b891b9da6ad471f9c3d95a1269097fb7b7bc6916c8bb`  
		Last Modified: Mon, 01 Sep 2025 23:37:52 GMT  
		Size: 6.4 MB (6363663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:bc885c88835143230ab923ac5ca4fcf7c11a2f90d92c3161605f1f8c4585050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3282224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f7875febfc8918e079dc046d49f9ef9f19085ba63e30be28c683cfbf120fc9`

```dockerfile
```

-	Layers:
	-	`sha256:9d7f095d50bfc0946e3d00761906f9dc88aac26f35296404d2d259d9d5704a58`  
		Last Modified: Tue, 02 Sep 2025 01:45:34 GMT  
		Size: 3.3 MB (3256240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9304110869155e22d3ee2e8beb56474b1dec3c5f181eacae5e1f0ad960769c35`  
		Last Modified: Tue, 02 Sep 2025 01:45:35 GMT  
		Size: 26.0 KB (25984 bytes)  
		MIME: application/vnd.in-toto+json
