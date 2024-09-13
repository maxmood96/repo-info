## `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:754bf31435d2f2fec3e54c6215a4a19e683586c06f128f037056a6a7fcbc22de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:68e78c2b02893d0c6df6e20940e20d9ad3f7dd6e991c8db1ccfde51f39825840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261880879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd10e99e8665ee94cb8645e8ad9b6165ca4b4c8c6439b60af1ef39e3428fbee2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868500367f40fe8df8a85d88bc755192cccb20de3f34e6df7a996cde2b8ee4`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 16.1 MB (16061270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7cbda723f6f96e4d9a9f43438f64e2c8fbe44a0cd4aae69178d6e93a971581`  
		Last Modified: Thu, 12 Sep 2024 22:02:27 GMT  
		Size: 212.9 MB (212875444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40610ccd72a70f2976aec480fb4cdb1fba2ea4f5ecfb0bbbbc89d66502ca17d6`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 5.4 MB (5432396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.24.1_8-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2e2cae8f4286a42c164657104f5c084e1eb199d03f2e80cc1bf33abc879760ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685af6082666c58f7b3bd66e78e7589d5e99b06ea71943a6571e85c2f97d92fd`

```dockerfile
```

-	Layers:
	-	`sha256:cd06848705088deb60ab1d6e4f9609d829f94aa529d3e50b36174f67da18e8dd`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 3.5 MB (3464799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79df0a1f6272dde29da0c824fb89a0e2ed266b1c98428a7e74a95adb60866ca`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 23.8 KB (23776 bytes)  
		MIME: application/vnd.in-toto+json
