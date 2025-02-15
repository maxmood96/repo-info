## `ibm-semeru-runtimes:open-21-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:b8e1653dd379d6ebc58b68e28a5b1c753b955c41311cfcfbfa18f8ebc7aa8ba2
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

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:eba91f77efddba9f2c165495303bbd275fea60fe42cd881092e8e49740286d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd363c2b4904b20546a177e64ff33068f4a970b461a4e9c4e9b4a417bb35159c`
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
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1090db3f7b30b4a45e3d5f228ac529ace87000bd9b342d91a639f0181a0058f5';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='cca7d1599ff83063dd16965dcbf91915a7654e5086f3b3b71744adf7769d11de';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ece962ee7ce419e25048a89228b61c4ce8c318ec6fade470484d6537bb87ea3f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='ab2070fa866e86978a5a2753dfc6128fc2012b97bf4e95d888d3dda916844a52';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:4f22e917081dfcc29c0dc543d05ea5009ee0338e628b4f1ecf24a4e1ffcf30ae`  
		Last Modified: Fri, 14 Feb 2025 23:29:16 GMT  
		Size: 12.2 MB (12166785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eda57f25b43a3c3094fd048202809a97e7b6a1a634325b0c9c207ae9a531a9`  
		Last Modified: Fri, 14 Feb 2025 23:29:18 GMT  
		Size: 56.3 MB (56340443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53a289df694c62a355475714f3b36ec441eb53405f6c92cc459df0034c5afe`  
		Last Modified: Fri, 14 Feb 2025 23:29:16 GMT  
		Size: 5.2 MB (5219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5b8d4ddb8606dfe88be4fea9b91021e20e46a67dcf8c5c1c57b7a2f9e212c7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca3d8f37465aad44e6f7a2f11270324d9342126a669039344be5943e027166`

```dockerfile
```

-	Layers:
	-	`sha256:ef567f3d6c81cd781f4f5e6d5643d503ae9481772c0550a687a33ccbf4eef18f`  
		Last Modified: Fri, 14 Feb 2025 23:45:45 GMT  
		Size: 3.6 MB (3584329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77377ae0b2c15263a94c0e79c0d4dddae0d85680788e55588cf3a65b81a27fb1`  
		Last Modified: Fri, 14 Feb 2025 23:45:45 GMT  
		Size: 24.0 KB (23972 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:4b9cc7f337d6adb6da53a81cdf911a9743c5fd8f91e04a9de3cbae7ae72603d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96418021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98f729917a47b82f98b27bcb9f867c03b5ecf332c548503c93f26fcab06ac22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-21.0.5+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='27fb02bb8e409c5330bbed15f6dce74c3f8255c1f2ef937a697c1b903ca9477a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3cd0ac0e28ad83fe9097569c6ba0c84772d697c1a34fa5b93c9fcbe0493d43c8';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ab533e7d609382cda4e5abee38102f8a467f24db77886fa0f4c680d681cdf87f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='3d5787d519e24fb5de6e4e5db78e29cd25a72d9d6de4cc96d31d377199c25c4f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc27324a20ba7e580ad161f241011b423fdcd169bcae5cc324e63f8db8fe6b2`  
		Last Modified: Wed, 05 Feb 2025 00:32:28 GMT  
		Size: 12.1 MB (12123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ab25dd668656957e4723ca0221883251c5098e3c7ef38ba4f771c42ac72699`  
		Last Modified: Tue, 04 Feb 2025 22:52:44 GMT  
		Size: 52.1 MB (52065820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af4e680daf6ffc1fe72693c794e2aa003e07bb5791b73e760bda951f24a18f8`  
		Last Modified: Tue, 04 Feb 2025 22:52:28 GMT  
		Size: 4.9 MB (4870582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3f56478c11901d597e5c6854df56a28384e8b878e77ef681ebc2e336e5fc05f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5099fca69c1adf8fe701512c6d1b8d3fac87f4f368ed209e5ba6fdf55b8a2d73`

```dockerfile
```

-	Layers:
	-	`sha256:f33fa68b1c1cb718a7336209bd5341d0505e29ff4808deef84b2d91e497932ae`  
		Last Modified: Fri, 14 Feb 2025 23:45:40 GMT  
		Size: 3.6 MB (3574303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56de288e8fb983e69c0bda091533033d393400e6ad6fc080cea7f0b6fb2962da`  
		Last Modified: Fri, 14 Feb 2025 23:45:40 GMT  
		Size: 24.8 KB (24812 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:3664a39a78f7f7f27775bc0f1ae1da9f21ef29c0363a2ccefcdca70e5449b5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108644763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8f19945f3d0a350d8ddf253406633452ee0d34bab31d42a84ba7de9ba1fd71`
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
ENV JAVA_VERSION=jdk-21.0.6+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1090db3f7b30b4a45e3d5f228ac529ace87000bd9b342d91a639f0181a0058f5';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='cca7d1599ff83063dd16965dcbf91915a7654e5086f3b3b71744adf7769d11de';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ece962ee7ce419e25048a89228b61c4ce8c318ec6fade470484d6537bb87ea3f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='ab2070fa866e86978a5a2753dfc6128fc2012b97bf4e95d888d3dda916844a52';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.6%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_21.0.6_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:22e85892e9684b1af2c5fde93616997a79c49c07614c9c3ed75fb1dbb3e0065b`  
		Last Modified: Sat, 15 Feb 2025 02:40:20 GMT  
		Size: 57.4 MB (57365722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29110a81a40571e532da528f9bb73831b69211f87141c3f243c574ace94ccc8f`  
		Last Modified: Sat, 15 Feb 2025 02:40:18 GMT  
		Size: 3.9 MB (3936125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ac6810ad2d95ad19eac0558960965cc5f2515cb08111ef1414187a078a6466b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c64213b55b4afc406374b6639780812b590d3d95b31f195eb36d19ef491553`

```dockerfile
```

-	Layers:
	-	`sha256:373c8ae99bdcd46555f7dea4d3277643cd05b63d0f313b8b31907adf2cbfd678`  
		Last Modified: Sat, 15 Feb 2025 05:45:28 GMT  
		Size: 3.6 MB (3584736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbb64cdf8afbb9dfac240fb6135f04c817cba562a35474ddb38393df5a73f41`  
		Last Modified: Sat, 15 Feb 2025 05:45:29 GMT  
		Size: 24.0 KB (24008 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:f5ee7f387176c5e723bbabbb1633cbc47c507e5a1767b74b95fc401dc28d050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100490440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925504e91fcead5c2bdb14821f3ddd630c82b62883b85e6daef63902b4ed2b53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk-21.0.5+11_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='27fb02bb8e409c5330bbed15f6dce74c3f8255c1f2ef937a697c1b903ca9477a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3cd0ac0e28ad83fe9097569c6ba0c84772d697c1a34fa5b93c9fcbe0493d43c8';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ab533e7d609382cda4e5abee38102f8a467f24db77886fa0f4c680d681cdf87f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='3d5787d519e24fb5de6e4e5db78e29cd25a72d9d6de4cc96d31d377199c25c4f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.5%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_21.0.5_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Tue, 04 Feb 2025 06:45:54 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a504edea95fbee01cd3ff3d84972a695acb9423b1d0fea8abc1fa3cac5e26`  
		Last Modified: Wed, 05 Feb 2025 08:43:39 GMT  
		Size: 12.2 MB (12212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fc851be52a3e4c38271c8591b9c2278e17f1b56cf3ebf6476be17cf4675d3`  
		Last Modified: Fri, 14 Feb 2025 09:25:31 GMT  
		Size: 55.0 MB (55007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500bb7d137410e97d337e74c6a72c50b12addde53eb245a18978e8e762e82ec1`  
		Last Modified: Fri, 14 Feb 2025 09:25:29 GMT  
		Size: 5.3 MB (5269981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d174134ebf5694bc4831dc2033a44c479a1bbd29fd1eb8cde2be85fe99dfaab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7150da44112ce34a472e6927601574ec37e8823b4169ada077ae61d33f1ee7`

```dockerfile
```

-	Layers:
	-	`sha256:876a4ff1429fffb21c73406ffb9f2340d72a078202f8987caccd15181b13df63`  
		Last Modified: Fri, 14 Feb 2025 23:45:44 GMT  
		Size: 3.6 MB (3583151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc680d1fbdd9caf5e8ac7e0192662095b4ab3e631186779d4de1600bf28b95d`  
		Last Modified: Fri, 14 Feb 2025 23:45:44 GMT  
		Size: 24.7 KB (24678 bytes)  
		MIME: application/vnd.in-toto+json
