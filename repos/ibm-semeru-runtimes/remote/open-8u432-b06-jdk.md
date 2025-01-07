## `ibm-semeru-runtimes:open-8u432-b06-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:c2b48c01d0bc26bb20438492bc6e3fc736d1e436cc7a44ba3ef42b708e13fc5d
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

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:752f92457ea28f101e2a3989459799cf20d8c04b54ca7c0e522cea0b28309474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162547808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2d6e8b9a8b7cc734c7fc6df2a4f6b4bc764e685e205b92f37ff1ee49618f53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a32dc297d99435ad1ee70f3527ad2b5b27fb7f0f3f1b452d1539a9b0f19068fd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b8a0a130f471c7c0e5007d6f0682a003eb901d2c73e968b5573b5994a8583f7c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3c036812cfc97c184c3569bf1edec0fd10b6c70c14aa74cfb7cb211b7f15326b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='34c9a92de131fb8ceb8fd092b54c8f2ee204159b49b22d28b0e47cfefe466b15';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5def8ca330cc53fee6c502ac469fc286e7704f8c3689ecdb67710c64b63268c6`  
		Last Modified: Thu, 19 Dec 2024 21:31:37 GMT  
		Size: 12.2 MB (12174601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d3c6e66b81a7a5981306f2df40920721b0f142280cf27f196cd19eabc5ede`  
		Last Modified: Thu, 19 Dec 2024 21:31:38 GMT  
		Size: 116.6 MB (116588005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b08ba21e1f1f49681b2a5c898b3fff3fa1952f1a13971613ed7aca5984ce6b`  
		Last Modified: Thu, 19 Dec 2024 21:31:37 GMT  
		Size: 4.2 MB (4249514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c6f813b78f20664302721a5b9547cd7ffc0b1b8ab08980a1d44fe25d6044f892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9620758e344b0cfa3e66dbbb466b5c455b3343aff35189af6b3f5e824f3f7a`

```dockerfile
```

-	Layers:
	-	`sha256:388b1b97ea4a0c501663f0dca3f1f4ee6715d637a3a38066163d4b8dbd879248`  
		Size: 3.8 MB (3776866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837c909a014a0f66d18b2ec20d84851486e2eb9ff095aa10289cae22ef977023`  
		Last Modified: Thu, 19 Dec 2024 21:31:37 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:cd6af07d748bfb0c247787614ec6717097f8f42cd7cbe9fb0d0aa945f2bc98cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160028157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8f181ccc150515c54c8a0dc211f57184116c46ca7ed17e5b2cd1a40c51073e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a32dc297d99435ad1ee70f3527ad2b5b27fb7f0f3f1b452d1539a9b0f19068fd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b8a0a130f471c7c0e5007d6f0682a003eb901d2c73e968b5573b5994a8583f7c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3c036812cfc97c184c3569bf1edec0fd10b6c70c14aa74cfb7cb211b7f15326b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='34c9a92de131fb8ceb8fd092b54c8f2ee204159b49b22d28b0e47cfefe466b15';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee5b8ee36c4bdc200fb16d7dac358abbea7616e2fc56374ee7dc6bfd46b21c`  
		Last Modified: Thu, 19 Dec 2024 22:15:43 GMT  
		Size: 116.5 MB (116505149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcbdcae2753d83f99dfd0e2acbf0f368fe0db52d1b0cf91765eb8214d81756a`  
		Size: 4.0 MB (4036440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c20b3708806891231f82e83b0a1c157ead787430cabf09c10d0b2c958e17b631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8bc568ca60bf30e42ed162866906d9c7103f3c9eeff7a8d8cd2080ea7f7b56`

```dockerfile
```

-	Layers:
	-	`sha256:015d73796470d9611f7121388d43e6260c17763b064993e5118088bfb9edd411`  
		Last Modified: Thu, 19 Dec 2024 22:15:40 GMT  
		Size: 3.8 MB (3776696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd596f434a906ca623b22e1df7dfe74e8e8221e5f888732936ac121aa3f52183`  
		Last Modified: Thu, 19 Dec 2024 22:15:40 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:e9081719a69730a3ac2b6b8ab88e0fed23ee12cc896619255751b01dc9acb1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168882885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8213701a0bb4dab897536709a6b055c14598cd74284a45f9ab0ed859ace44f1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a32dc297d99435ad1ee70f3527ad2b5b27fb7f0f3f1b452d1539a9b0f19068fd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b8a0a130f471c7c0e5007d6f0682a003eb901d2c73e968b5573b5994a8583f7c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3c036812cfc97c184c3569bf1edec0fd10b6c70c14aa74cfb7cb211b7f15326b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='34c9a92de131fb8ceb8fd092b54c8f2ee204159b49b22d28b0e47cfefe466b15';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f84c441e24b8aa86dd2e912a4b47c2e9a968f30a356918d64edcd9a3f3c5e7`  
		Last Modified: Thu, 19 Dec 2024 21:38:20 GMT  
		Size: 118.1 MB (118079152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4955f1be13c788f52089eb09a4717aff8df6024039efd6e71ec8d5d65788d0`  
		Last Modified: Thu, 19 Dec 2024 21:38:17 GMT  
		Size: 3.5 MB (3467359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:cca1629d997e960d6bfe65cb617cf6a86fcaacda27cfddbd4ab0f6fbf39df14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e6beff6423bcdeeeef6eef2e6dc5c93d7a0cd51b354ea29d8b872b02c8fb33`

```dockerfile
```

-	Layers:
	-	`sha256:913c7f1a5caa3edecd754821efc8f7f514734148be71e2fee9e3934b309f95c9`  
		Last Modified: Thu, 19 Dec 2024 21:38:17 GMT  
		Size: 3.8 MB (3775658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619768856002727416813639461a8bb71df3702b15ea240d1151585b890dff51`  
		Last Modified: Thu, 19 Dec 2024 21:38:16 GMT  
		Size: 24.7 KB (24680 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:dc75de00c00f07f30285b558d1b1c2f5aae7c941c61feb06f4c827331c5d2cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161022081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d76f1376f80472527a3368a3ecd50936665dcf1f8ff30b5bf4b6ed1caaf25f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a32dc297d99435ad1ee70f3527ad2b5b27fb7f0f3f1b452d1539a9b0f19068fd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b8a0a130f471c7c0e5007d6f0682a003eb901d2c73e968b5573b5994a8583f7c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3c036812cfc97c184c3569bf1edec0fd10b6c70c14aa74cfb7cb211b7f15326b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='34c9a92de131fb8ceb8fd092b54c8f2ee204159b49b22d28b0e47cfefe466b15';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jdk_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274ff97d10452570d9f2d8260ca33176da74c7aea42d29ddf7ff4deef219925a`  
		Last Modified: Thu, 19 Dec 2024 21:38:02 GMT  
		Size: 116.4 MB (116425875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6945437837ecb97b6f7f5b70df94398f10efb3b4cd928468753df3a8f9ac3ce1`  
		Last Modified: Thu, 19 Dec 2024 21:38:00 GMT  
		Size: 4.4 MB (4390972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u432-b06-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ed872c00245b5047c1253e4304fa5ca6774bf61af3cc9c93fdc023e69b91291c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3797835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a21ff819b9d4c6c0d10371fa386d5db7801748e6bbb4a0f5cffc23519bf4ae`

```dockerfile
```

-	Layers:
	-	`sha256:0b6831fcc711845fd597f0a0aa92eddcd0e94acb79392ae0330788f08ceb2bd0`  
		Size: 3.8 MB (3773203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7282692b43e3ec85f52f06f3f0d343894e5b81eff031cd74e89cc163004262d`  
		Last Modified: Thu, 19 Dec 2024 21:38:00 GMT  
		Size: 24.6 KB (24632 bytes)  
		MIME: application/vnd.in-toto+json
