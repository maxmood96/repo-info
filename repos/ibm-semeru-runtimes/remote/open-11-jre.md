## `ibm-semeru-runtimes:open-11-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:5b6fa466ecb654ff73328721a8b304ad601e41d9e0f699413764151f71de4edd
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

### `ibm-semeru-runtimes:open-11-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:0c21f0864852c901028c4b92c9eff8e9f80bbe37e7e94a5f0d5f984ec11df8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97935619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1958e0cd3ab51fd747336aa728ce07ff1b1a9cd94d5d472697fecec4b4c36ac6`
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
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:cc38ae42bef3b66b9b1ed085cb892125d59651ac60011e184eb972f80b4490e4`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 12.2 MB (12156246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208f7b191850ef94a748438bceff6d217e8a6d4b218de64e8f4c4a323386324`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 51.9 MB (51931207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be8bd0e56977369fdc3debe0a43a91ed263a1640b5a82e384127f13837fa41c`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 4.3 MB (4314111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a3b645d6771e7b4cf6505b78a5455160be4b82dcbd447bdc728dffe358040323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d549d0bfee3df996a8ff1712cd70ae167b6c55f670e99065bd560cc9915d526`

```dockerfile
```

-	Layers:
	-	`sha256:416e0517b19cf6648ea3c87c1f4354c9941d1f5e03f25942d8283fe5659695b9`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 3.4 MB (3433987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee50b0ad2f98db37c16895b6f8736ca5f9130710965449135b97fe1c4711ab2`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:8f04145a22bad37932c3a309ed22ddf7b222e975d2707d8cdaec617e3dbe8fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91949924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00eb83494b2acc5bee5096d61b478755b647583209552e6039e9f6b670a5d490`
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
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:17cc601006bcd4bdb5e7f1f0982fc1eb59bfc8e22bd3a2fac16d763c6f8dd54c`  
		Last Modified: Tue, 02 Jul 2024 15:08:24 GMT  
		Size: 48.3 MB (48326036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5249dc135c6b92027746e07ba8ed8850e2ec23a0e773f3e9aa04869abb98ee`  
		Last Modified: Tue, 02 Jul 2024 15:08:23 GMT  
		Size: 4.1 MB (4149565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:29ac1b7f5c2c5fe0720ce887d8d624a6d3d73a6578fe73dcd86e283b72636c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7780960b75c8b357f7496c20d03ca7d6c2528fa1df083bf36930d27554ccef5`

```dockerfile
```

-	Layers:
	-	`sha256:d6d8257f509bf5a67e86ae9100410eb3f2fbed85d490a6c7e21a9e4b729df314`  
		Last Modified: Tue, 02 Jul 2024 15:08:23 GMT  
		Size: 3.4 MB (3434276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6dd045ff403c3353b59556345e028ea411ff72dfc985c1264aa871ba8459bfd`  
		Last Modified: Tue, 02 Jul 2024 15:08:22 GMT  
		Size: 24.7 KB (24733 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:0fdfa9b9795c8f95800d006750f2d4972d7faa5756476dda111d69be9a3db386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104358905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070bbbbcbf8f1262360e989eb022bc9c0fe2847214db19d8398a7a99356f9810`
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
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f76ce5d3844420c7907330f7af456a5717516a0725b34782ae0c2ef8c606485b`  
		Last Modified: Tue, 02 Jul 2024 10:31:23 GMT  
		Size: 53.6 MB (53571354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49253f280f3788ddeea7c2d74de9041f4ce179f51fb9ed7335e012bb48e6bcac`  
		Last Modified: Tue, 02 Jul 2024 10:31:22 GMT  
		Size: 3.4 MB (3438247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:af66777c3a386d19031ef7f8269cae4664050bc3380227de5790e7d5994de21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a32533cdc18501f86d09d4956bf718773dc4cf8789fa1a3d23067cec32a027`

```dockerfile
```

-	Layers:
	-	`sha256:777e1e44899b841760aa5d418f5478ad99135b148cc42e8317046dd89d9b918d`  
		Last Modified: Tue, 02 Jul 2024 10:31:21 GMT  
		Size: 3.4 MB (3438487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e2a8d89391a75aeef75a002b9d2c6e017415ebfab84e285c30049efc434c4d`  
		Last Modified: Tue, 02 Jul 2024 10:31:21 GMT  
		Size: 24.5 KB (24474 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:4c48c5cccbce4cff86faa029b5fc87ce8461bd28347b1b3c2c99b924d169b60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95543561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb3f19bbdfc8ec80b9f30aa058a6dd22b4629bb9979b911c14413862a41544e`
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
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:974717a8dc82f7310bcdd38953a9c17858b41eae0d61aac5d4a4c42b6f1ef96c`  
		Last Modified: Tue, 02 Jul 2024 05:59:03 GMT  
		Size: 50.9 MB (50851650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d8f39dad97c6140d50d96aa19ffb406aa10613be35ee5a32037a2ca4ffd944`  
		Last Modified: Tue, 02 Jul 2024 05:59:02 GMT  
		Size: 4.5 MB (4487753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2316275656caaa90125d1e01e57bb41a245c7ad14ef295b00d9ee4ba48460462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e8d26f8ea83fed86d82f8ca759c04f1357c2b6a64577e6b44dd93f6f83bc3b`

```dockerfile
```

-	Layers:
	-	`sha256:e12eef49493cdf6a7e3dff7b559d690faa34c8c942779e5d5bc5d8e0024ac292`  
		Last Modified: Tue, 02 Jul 2024 05:59:03 GMT  
		Size: 3.4 MB (3435255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a381e3c99e42d562c75d2e00fd75eec15ebcbe7e0d07c450c46444dd20db9c`  
		Last Modified: Tue, 02 Jul 2024 05:59:02 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json
