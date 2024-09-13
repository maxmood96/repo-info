## `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:ecbc89be9f0d9fe87ab2ffb2ea8b2e137f37ce5053447e2f2f448df6d9bed714
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

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:5421ebc4646e8f11eaafc607fb8d316055283f1074cd0961afd48602d3a4c544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259972341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ac8c2090e6d283e62654ea28ffc3317ce7151fab8f2e2564126bf30e734eeb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccdc160c9dd5ef12cd7aaa7823d01aeb5ac43d88b02714a9b6653d67058e957`  
		Last Modified: Thu, 12 Sep 2024 22:02:37 GMT  
		Size: 12.2 MB (12156576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b229dc7700c498c466fb88da2c39cc02ca6f7cbe811667fd738c988f1a79f5c`  
		Last Modified: Thu, 12 Sep 2024 22:02:43 GMT  
		Size: 212.9 MB (212875445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1075e3311f5bd5a2c852512eaa26ef7cd6439b430e8cca4bbc931d49f6dd2d`  
		Last Modified: Thu, 12 Sep 2024 22:02:37 GMT  
		Size: 5.4 MB (5404295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6bfe631915ded4c7cbbf9fff7382b21b3a0e32d3274dfcbc9327fb1bf100e710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3af1105531a48d76e31fe3a9687d3e15021a18ea517fe7b31d222299d46bd9`

```dockerfile
```

-	Layers:
	-	`sha256:e8e7db52e935bcd59d3d9f1c1a000e8e8a46ec56986b55cb9e450e42edc8f3c9`  
		Last Modified: Thu, 12 Sep 2024 22:02:37 GMT  
		Size: 3.5 MB (3462522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c28fe877a81cdd22a3d0241df48d2ba5e9d59db43b749994b27155c8a53d1bf`  
		Last Modified: Thu, 12 Sep 2024 22:02:36 GMT  
		Size: 24.5 KB (24462 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:32bc3e275f1c35a57c76b8eac5cef13b6d086fa64b8016fbeef0b6fd43458632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250013731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab37cf2cfc4ed0176e74b86489d376e4d958b590ecc7f93dc0e646298e0d640f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ed8fbb37936532e8074cb248e6ef98c9c8787b05e8363f059b2b7aeb599fcd`  
		Last Modified: Fri, 13 Sep 2024 01:55:51 GMT  
		Size: 12.1 MB (12114242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5ac8be3bfc6cc4c75c1fa54c51d7e66d6f01d6e114e9259497dfbf1b0c7f01`  
		Last Modified: Fri, 13 Sep 2024 02:00:25 GMT  
		Size: 205.4 MB (205357542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c04130fdc0690c7c1acc8b638e4c0c22d9889e67bdaa14f6834bacd6ba472`  
		Last Modified: Fri, 13 Sep 2024 02:00:20 GMT  
		Size: 5.2 MB (5183264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:77c6f2eea2c74bbef81ec3d8fc34eda903f46d0f65af120dc1edc35afb8da3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa23a0748199c7af04fef6487dfde92177f51f54889258144c1ca480f804b6d1`

```dockerfile
```

-	Layers:
	-	`sha256:6f0355c570c9a6eed9a3db63b4fcedca1474d70eff015d1c2b6efcfec153979c`  
		Last Modified: Fri, 13 Sep 2024 02:00:20 GMT  
		Size: 3.5 MB (3462811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8168c3b92ab9215aae5e9209af1fd789ca2d5e1aa968fc6d02d6fae8554ba8ff`  
		Last Modified: Fri, 13 Sep 2024 02:00:19 GMT  
		Size: 24.8 KB (24763 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:8db0f9afe20ea209a83e2aa16407bb2ead2ab0f182e6048b483d3186bc734fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267763357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f3ad436c219bada12c0e785d40a5be047bf2f3364ae1b55a38cd3fe783321`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3547de1dae695643c2f9bf25f1853d4797b69e18520a3dd466106a42a6ce71ca`  
		Last Modified: Fri, 13 Sep 2024 05:40:26 GMT  
		Size: 12.9 MB (12888474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfc325bd28a4b601a888ec6919f033be691ce174f53a6a386b4809e577d7303`  
		Last Modified: Fri, 13 Sep 2024 05:46:25 GMT  
		Size: 216.0 MB (216008462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24c0fc676f46ae3083fe81dbbbdd63cde183371da4c613337d2d734b2935bc9`  
		Last Modified: Fri, 13 Sep 2024 05:46:16 GMT  
		Size: 4.4 MB (4402243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:00fd5e69b618fcb4d5a0d1d4d8bf99ec3c405d2fa04982ff8eb576f340bc057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e05b83c8a4ad2a855585046a52b5f4498bcff9b57d7509671d6723126a4145`

```dockerfile
```

-	Layers:
	-	`sha256:be6805643f3d3fca9b1b0dbca0ead94ce2fd727342ae419003f3c28cd5010a74`  
		Last Modified: Fri, 13 Sep 2024 05:46:16 GMT  
		Size: 3.5 MB (3467022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701106df9b909bf0ffcf2ad96676290100e837813c22614d4a88f9a6c3182534`  
		Last Modified: Fri, 13 Sep 2024 05:46:16 GMT  
		Size: 24.5 KB (24504 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:f62ccc42d541059f75ddc989659a5d20b56124c0a6c6ed33cd90f5ca7e0ad1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256439137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419b9db8203f36ffb937b2af91de6a8728f8a8f94cfe07026ee3b3734e325195`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484aae066bc222a7012e23d2a5a35b76528d7c4e7a9d942e1be50489095c73e4`  
		Last Modified: Fri, 13 Sep 2024 02:24:33 GMT  
		Size: 12.2 MB (12203896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f406f2d0f9694c2897916a2366ced046b57179ff7db01d5ba0015837f0cdb33e`  
		Last Modified: Fri, 13 Sep 2024 02:32:06 GMT  
		Size: 210.6 MB (210619538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52097c864b9ca1543db43d8b7cee473a6d777bc49d91e85dcb16a7849ce08a`  
		Last Modified: Fri, 13 Sep 2024 02:32:03 GMT  
		Size: 5.6 MB (5614381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:95044c593f3a77074c0051b2dc5ea09359b9bf7c4f2a39a3e19566ba0788faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c36410f495a2bf1d84fb64f8d740c0fbeb7474a677345d26189d5c7310dfa55`

```dockerfile
```

-	Layers:
	-	`sha256:4e668534f53535cd552771f9669e9ea8d27dc1080f1e6362d71e078c41191554`  
		Last Modified: Fri, 13 Sep 2024 02:32:03 GMT  
		Size: 3.5 MB (3463647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04617424bfe612b804b52db4cc02a08444758d77db19e1b4578fb290047c19ae`  
		Last Modified: Fri, 13 Sep 2024 02:32:02 GMT  
		Size: 24.5 KB (24462 bytes)  
		MIME: application/vnd.in-toto+json
