## `ibm-semeru-runtimes:open-25-jdk-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:d30e96627a447547785db7601222dea13d203be73238a9949ef159a23377e884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-25-jdk-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:57b116d04ddc29f5ff5ec6de7f28ec649616b6b19f7d0a2478faa02d5600dcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302734547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee6803c66376e4c862f1050f7aa39c10c4730683fce02cdfe836d107b2cc949`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:58aa9726a4ea2ea65460ec6c387684ebb99b94d293b259d10002f903a52e5def`  
		Last Modified: Wed, 01 Oct 2025 12:06:12 GMT  
		Size: 18.9 MB (18895238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee2e28f283539be66f13194c24c315eb3ecac24b45ac6c40b859da9d4beab0`  
		Last Modified: Wed, 01 Oct 2025 12:06:21 GMT  
		Size: 247.2 MB (247190033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3cb34ea87ff29a90931c488319e1fead016b7612ec062b88fa4fc47c7dbf1`  
		Last Modified: Wed, 01 Oct 2025 04:52:56 GMT  
		Size: 6.9 MB (6925826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-25-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ee5c39885b5a6750c3327af5dda8ea79334300021066f495e857a2dc6533cc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3275786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60299dc4985c2ceddcc235d92098c1bbdd28d9503f8c86d34c173303f4ce2310`

```dockerfile
```

-	Layers:
	-	`sha256:561c1d8f3e8d3cc5c3a9f842e292caae65ea58527138d69f2b601a4ceafe9b00`  
		Last Modified: Tue, 30 Sep 2025 22:45:29 GMT  
		Size: 3.2 MB (3249855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe71036c2f80b36f06e395bf62f75a7044ad48ad2f029586f47e89d991e0b976`  
		Last Modified: Tue, 30 Sep 2025 22:45:30 GMT  
		Size: 25.9 KB (25931 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-25-jdk-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:c091daa56bcca6d0a5c6c38d99dbdd90defd03e42c7a2be292b580042df7e7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302185354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7b35f302ce3995f7ad174f13b55aba8ec2451a8aa5d24cfd1348462d712b9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:05 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:07 GMT
ADD file:c24f61277b8ba0fc6a9f5e3c821b272fa1878e300fa010e5e8c6bb6b789470a0 in / 
# Wed, 10 Sep 2025 05:44:07 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-25+36_openj9-0.55.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4572e8bbe1310dc518037d60ac2938bd0dada1c15bba1c94e65e0e9777b1ad17';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_aarch64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        amd64|x86_64)          ESUM='718b4cb10c95a872d63c22254e4d1879011f7fff05dde1d21af6b63d40a5bb47';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_x64_linux_25_36_openj9-0.55.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3229a50f14521d299be655321ea5f89e4a34e1e157bd34e136bce6cfffba278b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_ppc64le_linux_25_36_openj9-0.55.0.tar.gz';          ;;        s390x)          ESUM='c2f859bf40f003536ca4536524995aabe1cec0cbc5ad330f2763cc38414903fd';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25%2B36_openj9-0.55.0/ibm-semeru-open-jdk_s390x_linux_25_36_openj9-0.55.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:1d6a499251c4e5e59ef209845254eb72c5efde9542271f270cf1a08fa823dfda`  
		Last Modified: Wed, 10 Sep 2025 16:24:53 GMT  
		Size: 29.9 MB (29906591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753d14077df09b61573c7c92cf12abb0db007c84839339d0e803f3dc122267be`  
		Last Modified: Wed, 01 Oct 2025 00:13:06 GMT  
		Size: 20.4 MB (20445926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc9e733bdd2cb7c9f76b8cf123e49d4c39208e0cb59e0c51c0d49d50cc4edf`  
		Last Modified: Wed, 01 Oct 2025 20:31:54 GMT  
		Size: 244.9 MB (244896964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abbf73e0ac3ad87c62b6daa2919abc6a1aeab534d5d418dadea48919211e6a`  
		Last Modified: Wed, 01 Oct 2025 00:42:13 GMT  
		Size: 6.9 MB (6935873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-25-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:dfa9531f148d733f5ab1de41ff20493504fae1173c6634cf938edc561029bc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01880a59ca6ed477f19729a461dd141106f9073d3c523dda34a309c6780f9783`

```dockerfile
```

-	Layers:
	-	`sha256:29c34c4ace7f542ee9bfba117d77ac11e59121d9574aeb5a0ef57cfffcb37497`  
		Last Modified: Wed, 01 Oct 2025 19:46:10 GMT  
		Size: 3.3 MB (3252679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e83bf2ebc9f506c729be2afa378004a465c7aacd0e0471449a7a112cb0d4fb`  
		Last Modified: Wed, 01 Oct 2025 19:46:11 GMT  
		Size: 25.9 KB (25932 bytes)  
		MIME: application/vnd.in-toto+json
