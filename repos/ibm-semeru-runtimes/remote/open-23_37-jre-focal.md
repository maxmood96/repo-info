## `ibm-semeru-runtimes:open-23_37-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:16b2c67a308821b65cb239df56dc4f8a4b40634d42f0c7bf2d8f26f9a93bdd30
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

### `ibm-semeru-runtimes:open-23_37-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:d5266e4d696d00ef6874faa8d59889b4b3d674b764550c38c154dc407aa441e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104268439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7a7ffe5a3d03424c63a245eed4c42fe205b407bd7fe1466f0ea8beff5c1879`
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
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:8db73102262dedb2bb99f597f15cf728cc68a688e3ca993390328e4a6c6a3465`  
		Last Modified: Wed, 02 Oct 2024 01:58:46 GMT  
		Size: 16.1 MB (16082398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573363025f430f10e2b5d44806c1350fa1765b2ad27d8a0e36bfaaa2142ab86a`  
		Last Modified: Wed, 02 Oct 2024 01:58:46 GMT  
		Size: 55.2 MB (55212064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4f3970e7c253f55deb347266b6672ecff4e9a1c027b2246cf9237c33a41143`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 5.5 MB (5462925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23_37-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d1cd1d83fd1a0e478bc1912aa9f2bb803c73a9b44cf07cf1b949a9e84e24fe4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130070fd1f741fafc1509a76e1840b8174c08033cf310802049c2028c800ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:4a0f26d5aa5d9f3e5e1260242c06de0a0331df7d179586b2233f99062a4b1710`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 3.6 MB (3575637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369dd7f6ae992adbb1fb53e46d7f8f439d8438c78e5caa7ea6367513a015cd12`  
		Last Modified: Wed, 02 Oct 2024 01:58:45 GMT  
		Size: 23.8 KB (23798 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23_37-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:9fd0a4fab4be66cb692d07f4de9bdbcc40adee5181be356cc2bb99dbb8df19a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98649127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd693ebd00c788419cab05f94dfc82df7ab32b673abd0b4500c497a0c73d4165`
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
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:40fb83c4ab69f553baf5a3777ad6b95d4f2459886243accb3026a0462530f396`  
		Last Modified: Wed, 02 Oct 2024 02:47:44 GMT  
		Size: 51.5 MB (51547828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbf0963fbdc35e541d902f0e037997a9b728905811cbdf39c62d184df69605`  
		Last Modified: Wed, 02 Oct 2024 02:47:42 GMT  
		Size: 5.2 MB (5182798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23_37-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2f406602a06610b12dc9612cfa522616851a20bf94482e77c72f909fa23c30ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293d682dd104247b0cd1423bcb207b978da517fdf06a9782ef6f7939b03f2a59`

```dockerfile
```

-	Layers:
	-	`sha256:faed0e7bfea9a8fae17387b769a36510642af3fda3da518aea9c42d61c7ca38f`  
		Last Modified: Wed, 02 Oct 2024 02:47:42 GMT  
		Size: 3.6 MB (3568952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a003bb75aa19cbfbe1cd7980020d806e021ba4cc1b237580a11cff784d7b8223`  
		Last Modified: Wed, 02 Oct 2024 02:47:42 GMT  
		Size: 23.9 KB (23903 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23_37-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:90e733efb70dcc50b33e39c94b4626c6107e98de2d800029f5afaa9f4418dc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110356017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19802cffae92aca4f5a904efb6fbe335e9fd46f95b6614e08fc1be90aafbccf`
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
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:513b63afe3e9d8809b698ef47b09b692e136075f63872d154708313b1bd9b8d2`  
		Last Modified: Wed, 02 Oct 2024 02:31:01 GMT  
		Size: 56.8 MB (56806232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b37bc4796da2fadf4e033634bc7706bc49efec86b9d67864f8523d263c09c`  
		Last Modified: Wed, 02 Oct 2024 02:30:59 GMT  
		Size: 4.2 MB (4217063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23_37-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2f7216cda3333e562907e62dafb4a555dd6b47de373d82713ec5edb3637fc984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba7cb8cc1d048ea8048657a0efc54fafd4d20060ecf898d546ca96c6a993f0e`

```dockerfile
```

-	Layers:
	-	`sha256:7e19829a9f4c065db39497903b6d705417bb69c24dd60165014fd18d906d67e2`  
		Last Modified: Wed, 02 Oct 2024 02:30:59 GMT  
		Size: 3.6 MB (3580072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ba022f747b21f98467b49d4cfee35a68cef3fcd713c9b16fd84365e9c52ff1`  
		Last Modified: Wed, 02 Oct 2024 02:30:59 GMT  
		Size: 23.8 KB (23829 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23_37-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:12252370a464c6b15f918a591f2cfb23330407f3d5bed891f932df2fcdd0b716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102282212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a54bb5833e4cef9f44e4e261b842cc9f8d05e4cb6187ed5859fc6c7356073f0`
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
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:070f4f28d992fa8d625518f273669351eeaa4c707bf6ad1099b7e620d377370c`  
		Last Modified: Wed, 02 Oct 2024 02:20:57 GMT  
		Size: 54.5 MB (54522252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822be7a6dc71eb7bc515ce0b2d276205eaf2cc901fc43f937b796fa78ba0d130`  
		Last Modified: Wed, 02 Oct 2024 02:20:56 GMT  
		Size: 5.6 MB (5621066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23_37-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d1b4b6c1f9e118680e5563b477de0852f25f5b106166dee7e3056aa0a4c86f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3600855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aabdc107f5d7428035ac94d150a770bf0a74caecbc131536fb7b2faa4e9cb47`

```dockerfile
```

-	Layers:
	-	`sha256:8d1388b6a817c2228d33c4c6e3d2f24895c5eb15d63c6fa61bd85e7d2ae425bf`  
		Last Modified: Wed, 02 Oct 2024 02:20:56 GMT  
		Size: 3.6 MB (3577058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dff26a70ecae0be078e044aebd4bfe747c6226ce1af35e024a9abe87b5ba775`  
		Last Modified: Wed, 02 Oct 2024 02:20:56 GMT  
		Size: 23.8 KB (23797 bytes)  
		MIME: application/vnd.in-toto+json
