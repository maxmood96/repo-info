## `ibm-semeru-runtimes:open-8u442-b06-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:7247b2de2efd753d852c816f9a9bbcea814f56238752b4a6db48ca10d0343168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-8u442-b06-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:332a6555c245e2086612774a4eac84f5a4de7678ec2adec1d8dd52345c1ce3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96368889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc78cc5f881369e2c96a7b989896f4c72abc123e978c56a22af63e0bbb071c2d`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:6c5c87ac894c18ebaaefd577877954e6b37b15c96c5aef00108587beeeccb153`  
		Last Modified: Fri, 14 Feb 2025 23:28:59 GMT  
		Size: 12.2 MB (12166730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19679bf6a4a3596742288b9b3382b0d1b8d16a0b86954d0180bdf464f39398c1`  
		Last Modified: Fri, 14 Feb 2025 23:29:02 GMT  
		Size: 50.4 MB (50438005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763e0156aa892026a423c25d79bff52f9a200a0143568d9eadb3646ad7bbbad`  
		Last Modified: Fri, 14 Feb 2025 23:28:58 GMT  
		Size: 4.2 MB (4228213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c6e8c6baa432ac8c18320b48c9b246f0af2d91ea14d8f81c3f53c4e560224bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f6ed201db32f320899a2e6f5f10f3d67fc3344666a0cb9afd5c3fcb53d6468`

```dockerfile
```

-	Layers:
	-	`sha256:f12a0da8a2b2adc78e5c251a9eb26045e8ec4ff6255bf38ecbe31b478c3e9a25`  
		Last Modified: Fri, 14 Feb 2025 23:46:56 GMT  
		Size: 3.6 MB (3610730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b3f516bb2d105a8ee1b03f7ee05d08a127274e3d82a4240b508cf74064e632`  
		Last Modified: Fri, 14 Feb 2025 23:46:56 GMT  
		Size: 23.9 KB (23945 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u442-b06-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:055d017ae2d843524125eebbdee2f13f019558f076af9ce106789fe82d34dd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102647494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb9d89bbfcbc71e3996d383381ee177e65ae31553379e204353a8e3210a77f8`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f81735207281899bd98eec233d3e89b4608876ea96661ec6eb121a30a8bc2e76`  
		Last Modified: Sat, 15 Feb 2025 02:10:56 GMT  
		Size: 51.8 MB (51832707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365fbcecde2824a783ec0ba5ce9722572df45e5a6a69322aacfb1092163e5b22`  
		Last Modified: Sat, 15 Feb 2025 02:10:54 GMT  
		Size: 3.5 MB (3471871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u442-b06-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:52f2c23b0a76d762f2ccf96579101082c2c7328507015ffc04cc3995b30ad93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3637758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78070b7a0769cf6eeaf0d4526672af694d12aae355a52fa70db61115a1e9d30`

```dockerfile
```

-	Layers:
	-	`sha256:2fe84d8041de0229a6f69fed89bb5cee6676c32846c8282c5dd7bdf19f90ca01`  
		Last Modified: Sat, 15 Feb 2025 02:45:59 GMT  
		Size: 3.6 MB (3613777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3960d29fb2d519d05f64dd7b469fb2ad89c9330a38b2905ec2e0030f60733b32`  
		Last Modified: Sat, 15 Feb 2025 02:45:59 GMT  
		Size: 24.0 KB (23981 bytes)  
		MIME: application/vnd.in-toto+json
