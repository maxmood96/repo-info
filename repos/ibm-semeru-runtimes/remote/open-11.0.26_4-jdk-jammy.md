## `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:98171878b9e60c2426f0c9f0c1147527e4f503d44aa0fd6b08e1f6a846034578
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

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:21486bbd56b3c001ab9d4cd68b6162bbbea73c227c046b3d7d99bc57b17bf675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261519101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30297e9583b97c69032bcd6b7c2b0c3ed8fb17f4681ed871851fc103e192ed`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691e06394eaedd808a512549eaf7f697c72ef3f5897f7bfac8c2fd32cd1daad2`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 12.2 MB (12172153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a1291ac104ac3a6bc0e7348777dd1ddbd4da788f9d4d11b1ee00e3900ffc4`  
		Last Modified: Mon, 05 May 2025 16:35:47 GMT  
		Size: 214.4 MB (214400025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b809924643ed07ff52902e8c7f8797fbf0fd6561fbbfe2ba72163b52f3670`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 5.4 MB (5414309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:58bad481ae12dc2f4265a6a26b8375b52e68e6c0b9d26ef33d310d6269437caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3705517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc3652bcf5d1d21088d05b97e7b790e3fa854a3d39ca7bf264bb6409c6a1cfb`

```dockerfile
```

-	Layers:
	-	`sha256:76f19c7614dc139661e5833f469337cfbb67750171c6922c29cbb0ac59e7b829`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 3.7 MB (3681489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7bf314f8e28cf2c70d226b8d8794eb1867c81976ade09fbf83492fae346e02`  
		Last Modified: Mon, 05 May 2025 16:35:44 GMT  
		Size: 24.0 KB (24028 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:c72d9c86368b1a2377818684029de4897b2ea66ff0b33562cad3bb00e5e9c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251644216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d144c5f2a4bc392cbfb845a68b1a963ee04a787706064ffc9c8404e407b0be`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Thu, 08 May 2025 17:57:19 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e358edaf77f77c16c6caf77ddbe3f45d35c88134c76be9ca9d3ee9b10ac55b3b`  
		Last Modified: Mon, 05 May 2025 17:18:27 GMT  
		Size: 207.0 MB (206969752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b801f2215a63eb02e6d3faf63ef1e48e3c986b344a5d2e3e195024cfe4cf361`  
		Last Modified: Mon, 05 May 2025 17:18:21 GMT  
		Size: 5.2 MB (5190836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6672854ddd66e589ff20aa9d7e8d4a5bd9c70e763eeabaa44492d7eb1b64cad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d358a37f09a307ffa80ff9877c9385dd6eb3ebaf0d1f64e6a37c625d71fbc43`

```dockerfile
```

-	Layers:
	-	`sha256:707b0d75fc691647b3316ab7cb49044ef7c7a0ce9c191582be668a9d5ba7b4b8`  
		Last Modified: Mon, 05 May 2025 17:18:21 GMT  
		Size: 3.7 MB (3674210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a1751c3b9871d87b310b66612459b564a11910e5acd451f108e920e0a54336`  
		Last Modified: Mon, 05 May 2025 17:18:20 GMT  
		Size: 24.1 KB (24138 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:0d31a8855364659a6f458b23b505f52355e2b2ca46357038c01c220ce66b1634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267726136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2611a754c029b8982df7df810d2fe3bcf9d469d7dd9cf04cbf025bdcb74ad79f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a64c9f5a72745f3bafe1231a1d79f060f125195fbcd3f510afac643f962e127`  
		Last Modified: Mon, 05 May 2025 16:55:41 GMT  
		Size: 12.9 MB (12893020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3a6556483d66223f0b3cf872af8c561403ea2b7d172407f158c186ef457f5`  
		Last Modified: Mon, 05 May 2025 17:30:11 GMT  
		Size: 216.0 MB (215967142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf33a3dcc061a2235866a43c570c642cd29c2afdf2aa112af390fd75351e64b`  
		Last Modified: Mon, 05 May 2025 17:30:04 GMT  
		Size: 4.4 MB (4422759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:cf86774a2b417a2f4115fcbd23a1f0f8638a137edc8dc23002aaf97f35a5a2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3706315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483c3b5b93913d11cf252c7937a6620a249070334f03a70b29b351c2e84332bb`

```dockerfile
```

-	Layers:
	-	`sha256:849e3ab999a29ed94f382b2c28a6eece48a9ababf735558cc328288b263fe334`  
		Last Modified: Mon, 05 May 2025 17:30:04 GMT  
		Size: 3.7 MB (3682251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c68c9d6622bd3d90c29beb709a5546000444af532154d233e83940e4d16cc`  
		Last Modified: Mon, 05 May 2025 17:30:04 GMT  
		Size: 24.1 KB (24064 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:87f2152e2e995e0db50db9fde32f73a26729e19672edb87f286ae9b8b356fef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256362658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2209b05d6de23e052670e1e3de2f320396080e010b67ced78140bbad65cd48d1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6d20a7bde624df0d1f07a501edaa63573a4550aa50c1eac105ef0afb3957664';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5d53d417a08514dea2ed88d3efa0a04ba330189ffaaa1da4e349ae00f86c7e69';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e8e60ed9442617476bf5141ac61af1b6b99dcd13a379c88ed95f9a752677590f';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='42c35f8146777c82b9fc69ea42d57615739ec34116e2d8bb9b3568b71114d915';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573305c63c6b8034a976ad865f575e2879ba561788a75b917f925a7f6f45b358`  
		Last Modified: Fri, 09 May 2025 07:53:46 GMT  
		Size: 12.2 MB (12219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708d43bf5c016cda826bf1aef463d111f529cb51b53e78fff2712ce9a88b66bc`  
		Last Modified: Mon, 05 May 2025 16:52:09 GMT  
		Size: 210.6 MB (210590157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23191217904214404d11f0c0d08464465eece8b6a15d08444a0d83d9c3421275`  
		Last Modified: Mon, 05 May 2025 16:52:06 GMT  
		Size: 5.6 MB (5553316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11.0.26_4-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4df588d2e754612fcf4948f960536a05f1acb4bdec94f4569f179026c404cec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3704008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b340a92b488eb5431430817bed4d322b436375606f58135aacf3913dc1c170`

```dockerfile
```

-	Layers:
	-	`sha256:9b62ffbb3f9ee8cbc1df485ed961718b5c8e90dd43560115c3870877a194ee02`  
		Last Modified: Mon, 05 May 2025 16:52:05 GMT  
		Size: 3.7 MB (3679980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88f4677b071092c275f21cb060e1d212e0b9ded4498bd34198cadd75b427bb9`  
		Last Modified: Mon, 05 May 2025 16:52:05 GMT  
		Size: 24.0 KB (24028 bytes)  
		MIME: application/vnd.in-toto+json
