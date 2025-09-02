## `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:695749797a3721d68598d8bf1d97994d80d5afa4413b5f05ced90e05c02d9ee8
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

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:f48ce54a155b571365f5bf5e732b32aeaac7f6d3795aaa3a39fc96c1db344e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107797866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efaeb8a866e57d8a708760a63c0a4d685c9ff764e64bf587af829e8ecedcd38`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:8ebe7e11392db2b14fafa6c44fca2f9a4f5dd1ca43a7d9e5714f4a3a7c458644`  
		Last Modified: Tue, 02 Sep 2025 00:24:22 GMT  
		Size: 12.8 MB (12796806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3006914426e3a942afc8759d9455655a9ef1d4d546a95fae0ba0eabbd6521`  
		Last Modified: Mon, 01 Sep 2025 23:10:35 GMT  
		Size: 59.6 MB (59566005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddd7a81c686fada42acc3f0550a2658414240c79075784ec476990d7bafb2a9`  
		Last Modified: Tue, 02 Sep 2025 01:48:58 GMT  
		Size: 5.7 MB (5711991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:36b18df5b26542add2100ec5e000e5d01701c5926a0d9e2ff1332a6d78f0a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3204042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2546a5c6090a5bce36024cb9c0e3675c89bd3d0a7a626aa78c32c13b3ea48138`

```dockerfile
```

-	Layers:
	-	`sha256:dc819eb2d2f9335e928254ef05fd54ce9708264590bca16a299454257e18fd88`  
		Last Modified: Tue, 02 Sep 2025 01:47:31 GMT  
		Size: 3.2 MB (3178043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59f2d462897d61659057fe5b48d9f833d5ded4e1a9e360b27391bcfc411cd67`  
		Last Modified: Tue, 02 Sep 2025 01:47:32 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:71df1ef8cd639b82d152cdb1de114f999ceba5c798ce89d6af0ac6b2af015da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104765245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e281d27020fc12e6289eca3a9917f67f8f2927994e7fab1d2e31798458a8f1`
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
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:80402b485aadfe9bacb68c41245bffe6796d1e57d020eb861fd1a884ed02df4a`  
		Last Modified: Wed, 13 Aug 2025 22:01:45 GMT  
		Size: 57.8 MB (57806333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856b7b05154d5601a7f049b195d04b231a786c3dc2123450ae8671bf8ba19183`  
		Last Modified: Wed, 13 Aug 2025 22:01:32 GMT  
		Size: 5.3 MB (5266355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5cf951b690ea8e3cfbbf0028eafed0905286e486ea4eb72751f09445f94de909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fcba02331abadcf03e20cce8ff88068813ac1ce876bcb8ddafae6a3314a414`

```dockerfile
```

-	Layers:
	-	`sha256:714a782e005058c6eab86e6f71a3bcc28cb6212aadf0f3a63092e73edc127db6`  
		Last Modified: Wed, 13 Aug 2025 22:46:01 GMT  
		Size: 3.2 MB (3177232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369d31f07c9d95e7938c3ff93c10d7bf3d6da2adbd4902435f633e1665343bc1`  
		Last Modified: Wed, 13 Aug 2025 22:46:02 GMT  
		Size: 26.1 KB (26132 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:5e1e4d60673cd48d339f3407d83185a9cae78bfc7b6b7e4695eb62b62792e1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113779085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efd6cd3c9b0deba47055487f5878204d34ed9e9441fe990917fc880ccaf75d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:5da4db611c51b195e25c10c4977628ff46455b58a9d355a96d0f0454da533652`  
		Last Modified: Tue, 02 Sep 2025 01:04:06 GMT  
		Size: 61.4 MB (61417884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f460cbafeb1e81cfbf94174d8eb06d38cc833d17f29bf48861544b8dab712`  
		Last Modified: Tue, 02 Sep 2025 01:03:58 GMT  
		Size: 4.2 MB (4236391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e734dd0a9aa30b0bdb7623ddf8854ca0fdea800a4c1b7c3d013c76f657835204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4566846385802b9ec6ef72c2f3e278739e263583f679a61a57db920e748cf2fe`

```dockerfile
```

-	Layers:
	-	`sha256:3da7d673832336e0e0534795e5e18a1f766a1cdc5cd8a7409ba81f2526d7f1b5`  
		Last Modified: Tue, 02 Sep 2025 01:47:41 GMT  
		Size: 3.2 MB (3182683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c84a3138e5aa9a15402a161836eeaa91b02b93a6f7a6d19b280b9b2f0da9d6f`  
		Last Modified: Tue, 02 Sep 2025 01:47:42 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:f0126b0d5e23647c3c107ca05795ec16489f854c326f313382c65e102e8286f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107351886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9323f4333c06b24efd4f84d0ee0795a3941903c23f986c17df5a483daf4b464b`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:e34af593af37eb95ac3a97b3fdd2c1d0bf4634e5798be5c4bc1205af959b09d3`  
		Last Modified: Mon, 01 Sep 2025 23:50:46 GMT  
		Size: 58.6 MB (58576918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1deac82c372e34ef97dc8bb2f0e791e9b03d9a26f863bafb725f6a69f3a3a5`  
		Last Modified: Mon, 01 Sep 2025 23:50:42 GMT  
		Size: 5.7 MB (5721004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5fb599c5fa6c7c97d9fde9e5b2c30a5ce99116226795379d8c04c218e5658a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cdbf4289bdf16d43db4d014ad0dea772ac79d92e71eb38cb16eeb8205cac41`

```dockerfile
```

-	Layers:
	-	`sha256:06c9c8a235940237f74ed31fb3780d48d7a2d4319c1c81d4b270eb54f50db142`  
		Last Modified: Tue, 02 Sep 2025 01:47:51 GMT  
		Size: 3.2 MB (3180867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0330fc4e435a9d246559e30d7ad9799ea8499ae2577db78407ee4328bb5cd6fc`  
		Last Modified: Tue, 02 Sep 2025 01:47:52 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json
