## `ibm-semeru-runtimes:open-22-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:65d9f15be2b262dd26888546e1960494c0e4ef27e766183a6b434574d42a753e
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

### `ibm-semeru-runtimes:open-22-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:f204ee10aa1d862dee46a32411a7d186597c1231a3fe8116117e1f55435b121f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104165966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eca3949541091b5aa7600f67c789bacf7066be3da0b11cf6124ba15a151bf4c`
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
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c940a53494425b86fd67c6b76e65fd3b94acd1d065c32febcbd1037ddd11ad02`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 16.1 MB (16082435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1b88fc1e5e5fd8c6bd07801bf049af23d1f6e4895f992a0bef7628304359cb`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 55.3 MB (55324811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d749651e57312ec2ea57d2bc9b9a68be2cc028b3d760bfae5978d0e46c02953`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 5.2 MB (5247668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:31e22059f282c3f52a5ab9c93ea6026486440642b794839ca6ee491d84d677a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3598748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e66d8b535d4f05469b497904d1e4b725a511b33ded3f62a84e25069aa3dc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:9ed3f5fac3dcdab7f662d5101d10b1a7eb98b02e87282e70f0dde191710084fa`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 3.6 MB (3575021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1de4a2fc609ed0e575fb217bed879e865b215cb668c9a8f80e17ab3d0ae0cf5`  
		Last Modified: Wed, 02 Oct 2024 01:58:44 GMT  
		Size: 23.7 KB (23727 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:e9208200029fae2c28a5e9d51e7f3dc385f530b551f96d67e7f6e528f9d26029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98496387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868f5ec5b78bf5740867c52b16db4096f3be5a2c46c02cfbfbd345ff4915410c`
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
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c7d8c4bddd19eaa00b75ee05bff78a870806bd10ced37fd0dcc3ff729ae659cc`  
		Last Modified: Wed, 02 Oct 2024 02:45:13 GMT  
		Size: 51.7 MB (51691305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a2305fcb58c7c54a3f535d78ca128da5b792065d23e5f070bf288c3df1dc9`  
		Last Modified: Wed, 02 Oct 2024 02:45:12 GMT  
		Size: 4.9 MB (4886581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c7bed404fdbfa023f6220e8490ba917ee3878dd4bc5f15eba9444083fac02584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098e421ba59e9d21eda1300ecdea7174d6513d3632d209422ae2cde23268a9f9`

```dockerfile
```

-	Layers:
	-	`sha256:0e41a10d792d1d963142b59457de322224532080a360ba39efd3e3b11c72c6b6`  
		Last Modified: Wed, 02 Oct 2024 02:45:12 GMT  
		Size: 3.6 MB (3568336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b356d680c086740756d4c7d4445d443248f773afd311c8ddc1d0eeefa7ed15c`  
		Last Modified: Wed, 02 Oct 2024 02:45:12 GMT  
		Size: 23.8 KB (23831 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:048879a9c89dc19dc1272b814f11f7fbf5b0dbcd3732e6126ed6b9b5987a36c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110276457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a19d48e7b1ca621d40ce32f9e791c995ab129ea33ddf04dc59b9de1de51253`
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
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:85ea8192cec60fd6a654e2b698211f8fe9bdc75acdf0c543b8372909d39e152c`  
		Last Modified: Wed, 02 Oct 2024 02:27:51 GMT  
		Size: 56.9 MB (56939310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8106bd11b7cadbaa1efadc6df0f01e9aaae394ed58bfdf1c613f38755843e3`  
		Last Modified: Wed, 02 Oct 2024 02:27:49 GMT  
		Size: 4.0 MB (4004425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c1f5325ef2cf55f5627c3cd1f1e0936fd9b40f571eee30ef1bf623af68ea5618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c2101e64ac7d55a3cec0bd73779b8a80cc1e307756822fe131165fd9dcd9e`

```dockerfile
```

-	Layers:
	-	`sha256:c534088027c45c8d8bcfc173e0257ea61d6671c4dbb5af5581595637e6575930`  
		Last Modified: Wed, 02 Oct 2024 02:27:49 GMT  
		Size: 3.6 MB (3579456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d347ceaf9b67790658b2fb7a67d5009639a036f6c6ae18ce38085f244397fb`  
		Last Modified: Wed, 02 Oct 2024 02:27:49 GMT  
		Size: 23.8 KB (23755 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:651dabe01596cbe8a6688ac20f2af8851de5be761caab0fd6a424da965ac51d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102106104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b42420a83a8cdd8a0fc61ae74edf8cd748e2cf94e269c450996bfd2d68cf166`
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
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:b626c4f240278c517fd5b193d7490dea0ec0b0c10e78c95e26a60d43ff5f762c`  
		Last Modified: Wed, 02 Oct 2024 02:18:08 GMT  
		Size: 54.7 MB (54656456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8c880bd325897318c7408c920cba4881380a7531cf2ac67a897e8e12dcdef`  
		Last Modified: Wed, 02 Oct 2024 02:18:07 GMT  
		Size: 5.3 MB (5310754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ab67d19bfe24533ebade2eacf06620edcf63410aa4526774dbe9970d41824552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3600168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7be0a7b1721bbac61642eb47c62537b026173c0b4f3a4db3ef2b995caf0dc3`

```dockerfile
```

-	Layers:
	-	`sha256:ae6832b103ef36b5a6ab3333bfc703a019a8ec455d07f64f262801584a28718c`  
		Last Modified: Wed, 02 Oct 2024 02:18:07 GMT  
		Size: 3.6 MB (3576442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53b66ed01878c62e8a2ad7b6d3f865dd72d636df6cafd11da764b85bd166f4b`  
		Last Modified: Wed, 02 Oct 2024 02:18:07 GMT  
		Size: 23.7 KB (23726 bytes)  
		MIME: application/vnd.in-toto+json
