## `ibm-semeru-runtimes:open-21-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:735fc8771491f71de0e961758ea3fb40599dc4695d4f6484af00dd9419ece00b
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

### `ibm-semeru-runtimes:open-21-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:12bc4be4c98da5e0728ef4e7e4853017184babbc27b93d32e5120a126158d30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288160185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d00f067c0eb4241cc7fee103646751250659fe56ec1d5f6f2f0668b86127f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='78180c518347cefc2610186686d03c892d05afa3a0002b15d6d7b646049db994';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='822fd2ac6f4c2d460ac3b10ce63464b078cb9837f07aa72f8ed3c1cf265a1200';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3a95f7f9ce9070804b016e1ae679c067f38ce130141f06d0a645e10eb395a0ab';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='816542ee795318fa946d03965c288545c67303654b7edb81a98063571b18d222';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad8cce26236d0b7fa743e4990183522ed77a897c2259471ae0de2b992bd6693`  
		Last Modified: Thu, 09 Oct 2025 21:18:11 GMT  
		Size: 12.8 MB (12796733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b65209ed3e3b3473486287061eebcb40ee2782914811f4440b2888e0f563ace`  
		Last Modified: Thu, 09 Oct 2025 22:50:28 GMT  
		Size: 239.1 MB (239107020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f9891e104c23c35c0867297a7f7914a46d70a96144f6196563fbadd0eb8a6`  
		Last Modified: Thu, 09 Oct 2025 21:18:09 GMT  
		Size: 6.5 MB (6533285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7d73c353c5d47745e0673978cf94b37c1afac1e8c41e4027a7aaa1ebb239f1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d4054e9a2982a2a059370fdada381d616d56a95a53b6e975d157da3e774632`

```dockerfile
```

-	Layers:
	-	`sha256:7a9b244c40a8f56bf68deebda8135d446584b95130ea6e643060e7cf10b0b67a`  
		Last Modified: Thu, 09 Oct 2025 22:46:24 GMT  
		Size: 3.3 MB (3255903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11a693eb5835a09f3ea310a90866c34bd03bebd8983bedd6400e90482452c86`  
		Last Modified: Thu, 09 Oct 2025 22:46:25 GMT  
		Size: 26.0 KB (25958 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:f83a720388e460081b6b78097c8fe7d897fd9792236d018107ed4825b41c28af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283156893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48239bac6a87a71e05ff948db74f187dd6b2faee8d5aaede5c382ae83704a80e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='78180c518347cefc2610186686d03c892d05afa3a0002b15d6d7b646049db994';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='822fd2ac6f4c2d460ac3b10ce63464b078cb9837f07aa72f8ed3c1cf265a1200';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3a95f7f9ce9070804b016e1ae679c067f38ce130141f06d0a645e10eb395a0ab';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='816542ee795318fa946d03965c288545c67303654b7edb81a98063571b18d222';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5e906b6fa577b3b2536b18285c920b4a8cca94e805a03b3f91f9d887b15c4`  
		Last Modified: Thu, 09 Oct 2025 21:18:10 GMT  
		Size: 12.8 MB (12832108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62188b85aec2a399e801bbce10349bb0e24395afa8618653ad8003985f6cfa7b`  
		Last Modified: Thu, 09 Oct 2025 22:54:04 GMT  
		Size: 235.3 MB (235310455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaac30c31bce2ed64f5dbacc9bac9e32dc6e4043eb8f7b63d04241fefc7479b`  
		Last Modified: Thu, 09 Oct 2025 21:19:25 GMT  
		Size: 6.2 MB (6152618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e83c02fabb6044c6440809d5e01d2cbda67689f176ab4867065a343670a97e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a3b93e85b06eca1a0cd41aed643f30aefeecb8d1f934e67faf10a93eaf29c2`

```dockerfile
```

-	Layers:
	-	`sha256:be5395190163c509d972704a6ba42c903697e8ce696fb0ac760f324e0eb10f1e`  
		Last Modified: Thu, 09 Oct 2025 22:47:27 GMT  
		Size: 3.3 MB (3255092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21297b47ad80d74a860e58ca9aeb6f2d4245cfbd67aaea81ad3e3611f8b61cf9`  
		Last Modified: Thu, 09 Oct 2025 22:47:16 GMT  
		Size: 26.1 KB (26092 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:afd0e3bea659c05349d69c08ff29c8d5c945bff00c924212c758d7601e31e344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296315397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229f5f9ea3effe1dae440d7515409f1af149faba3066f3f52bd73a3f922713d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='78180c518347cefc2610186686d03c892d05afa3a0002b15d6d7b646049db994';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='822fd2ac6f4c2d460ac3b10ce63464b078cb9837f07aa72f8ed3c1cf265a1200';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3a95f7f9ce9070804b016e1ae679c067f38ce130141f06d0a645e10eb395a0ab';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='816542ee795318fa946d03965c288545c67303654b7edb81a98063571b18d222';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90d60290856efe2971970dd841be418b3d4aef5c79e531fd5259b73b4161e6e`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 13.8 MB (13795688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9969a84542022e538a353847c1bff0d50233c0ed5b2909ebe1047724be66b4`  
		Last Modified: Fri, 10 Oct 2025 16:18:16 GMT  
		Size: 243.0 MB (243028771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70711c66cd3de3c1a7b20e69df0cd3ee64f5dfca96ce933f9cef4c48d743e49`  
		Last Modified: Thu, 09 Oct 2025 21:35:01 GMT  
		Size: 5.2 MB (5187413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:49486abbc02b8728baa1714e8589c557b9ec4e40cbcd79678268f77cc063209d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033f97eea64ad5f7c57b737565b8f22ce1a0c6f380e2e0dc0f2b6bf9fe175dff`

```dockerfile
```

-	Layers:
	-	`sha256:9c9ee49694e1bd6dcaf768df93241ab782189cae02ab227729869313ffc50838`  
		Last Modified: Thu, 09 Oct 2025 22:47:21 GMT  
		Size: 3.3 MB (3260543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc9debce895d16470e62cac6d0d10c520da1e1187d154890a3774e22b1bea64`  
		Last Modified: Thu, 09 Oct 2025 22:47:22 GMT  
		Size: 26.0 KB (26006 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:b5d37d69cc701176f439ec66f2b3fdf9cdd05ac96fe98110d5de0adfdacb733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9237e1d0badcafab354bb4a8c937b37f2b4474e0be4aa82f282ed81b38b15031`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='78180c518347cefc2610186686d03c892d05afa3a0002b15d6d7b646049db994';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='822fd2ac6f4c2d460ac3b10ce63464b078cb9837f07aa72f8ed3c1cf265a1200';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3a95f7f9ce9070804b016e1ae679c067f38ce130141f06d0a645e10eb395a0ab';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='816542ee795318fa946d03965c288545c67303654b7edb81a98063571b18d222';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.8%2B9_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_21.0.8_9_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abb1773fa607c3929aac3eb861ef6680d8e809e96bed56147de3baee3d0361f`  
		Last Modified: Thu, 09 Oct 2025 21:19:11 GMT  
		Size: 13.1 MB (13120820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec820df88d58b936f4fc3d381e63d97815bdc6ace1c22a66af9fb49b7bbdcccf`  
		Last Modified: Fri, 10 Oct 2025 16:37:11 GMT  
		Size: 236.8 MB (236795123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3713ab44e23a01b174d6e6fd234e824c4dec84a098a1f59195c1bd63fb7f23`  
		Last Modified: Fri, 10 Oct 2025 01:07:30 GMT  
		Size: 6.6 MB (6633191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:200c67739d5c2878c852d8680a820288f54c88ccb22c64e522244230ed173f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3284685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686221a578565de08727c8c710b7d5bc7d0cb1bd601722cb3a242a6091cb29d0`

```dockerfile
```

-	Layers:
	-	`sha256:29f82ffa211e27774ad240930e8374ec6d9a682cbacd0713d29b44b109adcf15`  
		Last Modified: Thu, 09 Oct 2025 22:47:27 GMT  
		Size: 3.3 MB (3258727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c84b9b7ad6303fbbdefbc534a18c61ff56b6af8ee2132c08149874213979194a`  
		Last Modified: Thu, 09 Oct 2025 22:47:29 GMT  
		Size: 26.0 KB (25958 bytes)  
		MIME: application/vnd.in-toto+json
