## `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:0348d3529a41570ee86972bfaaadf9e09920fe03d29e8f9c6ae65c6a0a1d0541
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

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:557b8686708e15125e5f7094726791133972f50aa451e9b24756ff8ee78b65f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280103432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a37e99be3e0a6db613576f0336a87be5d784e9bc676cd296359a4b9e6bf91e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9d51a722837f621e30e8c7f88381d488218c28cda567a950d450fc1e0507ce`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 16.1 MB (16082540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d198c041b898db45b99d1e67152176372b2bd0b9dce2f156e1f7d8ea5a5256c`  
		Last Modified: Wed, 02 Oct 2024 01:59:02 GMT  
		Size: 230.2 MB (230240010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af70675c83d8a012147147e780065ed02584052b7a291966269d0c91feef966`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 6.3 MB (6269830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:efbde7f58402afcfe0c284a396a4316e47ffd04bf589fadd75af6a75b945e4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55edf482727b068d9ba38bd1799823ca3e34c326e480bda5f4330ba625584335`

```dockerfile
```

-	Layers:
	-	`sha256:dc35993852caba2a47b4be4dc91ff03052d7a327ae6d6ea209fa69565f73d68b`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 3.7 MB (3656225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c70092e754e67768567b7b22c76f6d27d4500240248ddd2fffa4f9e908d363`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 23.7 KB (23724 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:2126ad5eed1deabbc745054c36e698043b0be6600f80848a5719b812b9739c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270071403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd873fe34ea52cacd082c0e55cd896e13fe26abd54d20b5fee8e2591d112e93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36171ae5253d58adb579390ef5b05a287b9441a6744830621ef5564b5d3fb96`  
		Last Modified: Wed, 02 Oct 2024 02:34:30 GMT  
		Size: 15.9 MB (15944909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b968de9dfcfc34c724db2529913c62aee128a2564c8c34996d32de04d9f2ca1`  
		Last Modified: Wed, 02 Oct 2024 02:41:37 GMT  
		Size: 222.1 MB (222130522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fcbc66b4cf4d99a14510c937f47b39657eac82c2ab403c41338f9a410e341e`  
		Last Modified: Wed, 02 Oct 2024 02:41:32 GMT  
		Size: 6.0 MB (6022380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1efc180baa5746f3c4e57600129d2bf84378a0eca289e044500da18c9343336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3ca59020421080853b9a9ae7ce9f9607c80f7585193965ca915c5fad3b0222`

```dockerfile
```

-	Layers:
	-	`sha256:2ead45ac8c67dd99fc4e89ab4f3f043d91b913ba1e40a65a5e746ddea8f9ee87`  
		Last Modified: Wed, 02 Oct 2024 02:41:32 GMT  
		Size: 3.6 MB (3648914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40eb9382d60b75abce967ee95d67902e6184e61e91b7d65ff1559e93fde9fbf`  
		Last Modified: Wed, 02 Oct 2024 02:41:31 GMT  
		Size: 23.8 KB (23828 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:6fef344dfe2f8676b3a3305b36c03b78659bbb99ef58bb411ab60aaf045b0c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288141308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b800985a0e17832de93188edb3e63abf5a6682de692cbcc60b16f6ada56b04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ffbeb090b7e1eb7eec8500dda28dd2af82398e770eec9f8262e68ec6c6162`  
		Last Modified: Wed, 02 Oct 2024 02:13:05 GMT  
		Size: 17.3 MB (17256388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c97f39bd238e696708573f01327397c1bb3a707adbcfcfbcd66815b828f4`  
		Last Modified: Wed, 02 Oct 2024 02:23:25 GMT  
		Size: 233.7 MB (233689702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6021756ea91374d7c83f561702a29e3337f8b18d6e81d13bfb4a7f07a52252`  
		Last Modified: Wed, 02 Oct 2024 02:23:19 GMT  
		Size: 5.1 MB (5118884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b79789c95966c0d9b009237acae72962e9d8e5b6323f2b5f3cea2ded5becedb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43f6f9dd798b1e67e1c557c97902d534034655ab0fc703f79c1a58223220930`

```dockerfile
```

-	Layers:
	-	`sha256:43b2c1fc44681888d733e0b7d314594c049fee9b1583c5a0039c65cdbc6b2547`  
		Last Modified: Wed, 02 Oct 2024 02:23:19 GMT  
		Size: 3.7 MB (3660660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c73a37683d26fe9e1ea1796f533ee13d49e0488b80ad06e0e643110e419ad24`  
		Last Modified: Wed, 02 Oct 2024 02:23:19 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:01ca044f985809295a6fccbdb9db095cb35be9ca81b629e786f768b177187370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276310399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfa257ec7c1cc1eae0996bc8c8403d7245528dabf079a7a351e53943048a800`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a8a8abf61da58ee0db5ce5ea0b786838a19827df6e3446cfd094f0fb01823cd';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eaf8a35c50167da06f1e103602df40aac2a74a1fd170f4701b2076152e104e5c';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='279b7384ab301385d01c15cbb590b88b4aa9e613e57ec2f672353b970cf65e4b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='8b0aab1bfe677cd4f3a1de0b16f3a79dbed258d98778924525f3b62629a3dbe6';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_21.0.4_7_openj9-0.46.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:5e84e73c86cd80310316bdb1d20baeccb3a0d4ffc98a27283aa05f904ec53469`  
		Last Modified: Wed, 18 Sep 2024 05:33:10 GMT  
		Size: 26.4 MB (26365746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b9a2b361f32bab4ccc11380a820a76e721926a15104f1b1d92fc1d9c64b152`  
		Last Modified: Wed, 02 Oct 2024 02:04:47 GMT  
		Size: 15.8 MB (15773148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e28a53aed29198d1d43f73941541a2d1c9b12e43687b9ac305dbedb26da46`  
		Last Modified: Wed, 02 Oct 2024 02:14:00 GMT  
		Size: 227.7 MB (227725944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1f5e5a5c787f8d6511de0eb6a3a2aac177578bdfc2c3ae715571d065dd1144`  
		Last Modified: Wed, 02 Oct 2024 02:13:56 GMT  
		Size: 6.4 MB (6445561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4.1_7-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:786a50964042353616f953263b16efd2da96f6e7a09f7ef46d54ebfdf46d15f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072af42a14f5b9d1981c0106c914b012b583e0649eb437665371bacb720b14fd`

```dockerfile
```

-	Layers:
	-	`sha256:f5eb5d8652ff75b70b169598100141ae7f73d3574c75652544ab45dda05ee1e5`  
		Last Modified: Wed, 02 Oct 2024 02:13:56 GMT  
		Size: 3.7 MB (3657646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee3fccba9adc5c6c80cbc2797fc6e633e53da515ed89fed8ad6992d52f534e6`  
		Last Modified: Wed, 02 Oct 2024 02:13:56 GMT  
		Size: 23.7 KB (23724 bytes)  
		MIME: application/vnd.in-toto+json
