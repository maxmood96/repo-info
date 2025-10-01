## `ibm-semeru-runtimes:open-jdk-25.0.0_36-jre-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:9b6ab69beb73bacfc4ddf10c45e2261c2a2d6e74f07e056f996dd3674904bbab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jre-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:4b24864cd5bfd7b4a4bd3ab6af27393305e40c66ba818c0a2557618074dd0d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116403994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4dee98783ca972511c4c3bb47cb0776c7b6eea460857118eb47c4eb00e1ab2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f917271612b0a29dac208bcbed1544008223ab96e0a000c6c8ca59d58cecd83e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3f3a6e3e1f0f29cebb7b8a0e8661b4e59cba99aae3752f5c7c131eca3ab4ca57';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='386ac1e3ef8560b6c86896e70f27978629f4805e924eb2eea68278c28eed14fb';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='2bdbc0dabb35d4bdcbc7235a60f3249f651b0970c9225d1355885ef4896de623';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b296dfd9d9d1c3cf0d3646953d88c679c811b0189bbfb64693cbadf156bcaf6`  
		Last Modified: Tue, 30 Sep 2025 18:08:01 GMT  
		Size: 21.3 MB (21299595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f4faeecd601115af689d501509dc0ed6fa70a726a2e84b5329151e7781152e`  
		Last Modified: Tue, 30 Sep 2025 18:08:06 GMT  
		Size: 59.7 MB (59660178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5677d5e2f7ac6950f23d4c11e478a19deeb06d2da3d24f7660191907b878ff16`  
		Last Modified: Tue, 30 Sep 2025 18:07:59 GMT  
		Size: 5.7 MB (5720771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a741769614804325790a9d4921c3294e689415742fbc911d8dc3dc6fb1656a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd746844187fa93ec1c00988c88eed4d1ab9703d26b93893bd212c1fa97c302f`

```dockerfile
```

-	Layers:
	-	`sha256:7b6671a5f65eee0d68417001f04c0cd85249fdc0b65c4c9cc855336255e6a5b9`  
		Last Modified: Tue, 30 Sep 2025 22:45:39 GMT  
		Size: 3.2 MB (3177414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343a8d7336343684a704538aec136688c71a6186634bbe95ad972b10f076e816`  
		Last Modified: Tue, 30 Sep 2025 22:45:40 GMT  
		Size: 25.9 KB (25931 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jre-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:d231ea31e79b555746fd059b1a9d1681eff35cdb0f2a79faa947cb6d2ff3b0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112863821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4da7afbc5d7543976a4592be1a2ecd0bb71658668a8ff63de6560c52c2930ef`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f917271612b0a29dac208bcbed1544008223ab96e0a000c6c8ca59d58cecd83e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3f3a6e3e1f0f29cebb7b8a0e8661b4e59cba99aae3752f5c7c131eca3ab4ca57';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='386ac1e3ef8560b6c86896e70f27978629f4805e924eb2eea68278c28eed14fb';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='2bdbc0dabb35d4bdcbc7235a60f3249f651b0970c9225d1355885ef4896de623';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jre_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7211c451726379ebc3bd608c85ab32030b30552025fc975db98a626e0c61b137`  
		Last Modified: Tue, 30 Sep 2025 17:16:09 GMT  
		Size: 20.9 MB (20907846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0788f6b1da1a1ad1b758401a521f67b23e8e10dfb42d8263b74bf90cb2746a`  
		Last Modified: Tue, 30 Sep 2025 17:16:14 GMT  
		Size: 57.9 MB (57900927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd94263f670e829e074dd626cb23e6eba547ec4b5a875083981ff5be22412677`  
		Last Modified: Tue, 30 Sep 2025 17:16:08 GMT  
		Size: 5.2 MB (5193731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-25.0.0_36-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:94b7525b4116d7152655da8e821eeeefdadfe8b4e779dd879978b425183811b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8a34698c9bd76947920d18503655c1809e1ebe53bcbb70cbfec1362033b483`

```dockerfile
```

-	Layers:
	-	`sha256:6a745695e97c6cfedb2876e9184e3877ea3dafd041a3825f624958adfbf84044`  
		Last Modified: Wed, 01 Oct 2025 19:47:59 GMT  
		Size: 3.2 MB (3176603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ec020a86bd074761d4db7e1843b37c223e560be8b5e749e1d41655260f9a4b`  
		Last Modified: Wed, 01 Oct 2025 19:48:00 GMT  
		Size: 26.1 KB (26065 bytes)  
		MIME: application/vnd.in-toto+json
