## `ibm-semeru-runtimes:open-23.0.2_7-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:b2f0e8f8a449821248631c666a239bb58b61429f58889e7b24f861ac9a35c44c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-23.0.2_7-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:91a609416612d9f5273cce5882b6775f0c57239855629dd733de596f3d7d5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287308388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b74d1d9c9c9fb0223b737215a36292a2f5649cff0918cff9258533b6abf4d38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9a93db4e95ff9718684e3978328657532176a2ccc5d9ec2eba32d83def886b8';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76ba23aefc68b2d3838895cf7dedc69a4a28fa3b6cdbff3cae3078b550404c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='278aaf14ae2a291fb4f4d08663675b50dad0a1992230609826c33013cf777dd0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='9db5de0beb8bd50d6971d1b88cf9c7008aab0bd8ef6ec33eee386357b4a9da89';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168c527d1b5907fbeee4adc9ff020f11c25e91f5b8e6986240ea884ae856af72`  
		Last Modified: Fri, 14 Feb 2025 23:30:22 GMT  
		Size: 12.2 MB (12166781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e578e1485bcb1f20b2694070b1b1abc5f19a0b8e610e0a79fbde87f263c10aa`  
		Last Modified: Fri, 14 Feb 2025 23:30:31 GMT  
		Size: 238.9 MB (238906738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4129d592e1551b866fa9f332acbdd8ca0b57b3d00a5cff23554cbbf91db828`  
		Last Modified: Fri, 14 Feb 2025 23:30:22 GMT  
		Size: 6.7 MB (6698928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.2_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:001e6c07fb56bcacc2e4bbbdfa2e8acf77bd62df3550822fe08ee0e60e9eaa2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98bf94f04d90a448c6fe1e2e71eea91b0cbfaeb466e84b4660517234d097bd4`

```dockerfile
```

-	Layers:
	-	`sha256:da2837d0d99266816987fabe071037d5fcc7c4fe1a873e3dc595d14c36784c71`  
		Last Modified: Fri, 14 Feb 2025 23:46:08 GMT  
		Size: 3.7 MB (3668559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90f1116a48b31a7d4644b1be8a4cf2732efbe9bf2ff45a90eaa5cf0b1e8aeb1`  
		Last Modified: Fri, 14 Feb 2025 23:46:09 GMT  
		Size: 24.1 KB (24105 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23.0.2_7-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:6184a407add62563a6c12a58d4e0b3321835951614f0a64e92f40053f9d5c1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292532526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecae6c9f64138187f3aaab9dc9c25c020e0ba4c9f9be31588297f8f32c47c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e9a93db4e95ff9718684e3978328657532176a2ccc5d9ec2eba32d83def886b8';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76ba23aefc68b2d3838895cf7dedc69a4a28fa3b6cdbff3cae3078b550404c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='278aaf14ae2a291fb4f4d08663675b50dad0a1992230609826c33013cf777dd0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='9db5de0beb8bd50d6971d1b88cf9c7008aab0bd8ef6ec33eee386357b4a9da89';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757f7d530f6b57a9f7086a87275499eba37462ad62756a55dcd465daa91caa2`  
		Last Modified: Wed, 05 Feb 2025 08:43:21 GMT  
		Size: 12.9 MB (12894981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375869b3f6f8a65acf454ad67a169dbb45188fe75df7d5e73302e5712e19b399`  
		Last Modified: Sat, 15 Feb 2025 02:45:47 GMT  
		Size: 239.7 MB (239712797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978094936965e0ba4cb547017003039de15d6c47d93a7c4c68da6dee6ecd8817`  
		Last Modified: Sat, 15 Feb 2025 02:45:41 GMT  
		Size: 5.5 MB (5476813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.2_7-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ea4e9609b51f146704e7486e802c58fba8a1567a0eaec454993c22eac3b83261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17121c8996057043553489e5746657223540a47bf8773f254dff615e2dbe421`

```dockerfile
```

-	Layers:
	-	`sha256:5a9346405bb97d0c3fcadd77c789195032d2b7952c304a4f7946c704750f8e6c`  
		Last Modified: Sat, 15 Feb 2025 05:45:55 GMT  
		Size: 3.7 MB (3667096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9837a43c799a5087cf7087e403e26d2d33acddb6af6301fff58168c021f49e`  
		Last Modified: Sat, 15 Feb 2025 05:45:55 GMT  
		Size: 24.1 KB (24141 bytes)  
		MIME: application/vnd.in-toto+json
