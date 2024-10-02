## `ibm-semeru-runtimes:open-11-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:1f3c497d47535769bf754232facc192d5e7f05379f5710543b57ef26458072b9
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

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:1c6659f5a40d489c389f53a810d0e85dcc921c8916fcdd9d7d38ded4f552a576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261801722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4837e1b6678745c17702bad7c96bf107dd2a20cf9076240e4ba6b2b4c80900`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40e22cc81a65dece15235c0ddfa9eb2069735331b7f152937cf6514b892e7b5`  
		Last Modified: Wed, 02 Oct 2024 01:58:51 GMT  
		Size: 16.1 MB (16082423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb57a262859fa9c3912f14c4f658095e2c6e3a2301d72b0d95733b3b67e516e6`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 212.9 MB (212875469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825336e8d9c115734817f38e25e5512a09f46c042945b46db0c468de087d5d8`  
		Last Modified: Wed, 02 Oct 2024 01:58:51 GMT  
		Size: 5.3 MB (5332778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:23c862405a18dd47e3d25a384397e39837a02a93d63cf671fe4f2eed7f872e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216230f518af7f1235f8cc0a929eb77e90c80c2e0e9552d6421ee080b2fc0cde`

```dockerfile
```

-	Layers:
	-	`sha256:19fd08e999be225e3a24f21b69a2983e1fe2441e14172a2d7569ffb9e11fb975`  
		Last Modified: Wed, 02 Oct 2024 01:58:51 GMT  
		Size: 3.7 MB (3670118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac665d87d8467a534e5ff9035f121cb702930f7841e5a89c4c3d5c30a75abced`  
		Last Modified: Wed, 02 Oct 2024 01:58:51 GMT  
		Size: 23.8 KB (23781 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:1dbbf1fc75851947cc39c4d2b59d601f813c235a3f30180e77f4aa5c0dd3bf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252378711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716b8891210c29b652666b88bfefc36df19cf552f3401cb74fa1576065862287`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
CMD ["jshell"]
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
	-	`sha256:e0d12c6d78c000f86ab9b81baeef22d28a82e6ed7cadc20c936ec7de83be7919`  
		Last Modified: Wed, 02 Oct 2024 02:36:53 GMT  
		Size: 205.4 MB (205357451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2bb94a84a92a475eca445fd52aef64f09dd3947fdba604dcb7ab4fd9d747db`  
		Last Modified: Wed, 02 Oct 2024 02:36:49 GMT  
		Size: 5.1 MB (5102759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b887594c99491754c523680d9a5512a933b5331a1658d821a81f765b3a47d667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a027ce185692afcc6054c04880da0a60587f06163bbf00db6a7f569ebf54e1`

```dockerfile
```

-	Layers:
	-	`sha256:c603964bea1e0e8ac9db17d52b62087a7c5fabba1ce10a8abafe02db83085eb9`  
		Last Modified: Wed, 02 Oct 2024 02:36:49 GMT  
		Size: 3.7 MB (3662807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fe22c07d4c5dc6b2faeaa63795cc522f92d4df573d526dae651725bc7930fd`  
		Last Modified: Wed, 02 Oct 2024 02:36:48 GMT  
		Size: 23.9 KB (23885 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:6231fe84cc46e20cbe0bad5227cd97eaa0db81fc252f740e57c4449eb1a13cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269728543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fa954b31197852713a31fbd041ef9abfbf2184a0330eb385acec8c63431a08`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
CMD ["jshell"]
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
	-	`sha256:ddb42b86e091beb9b8e6e584bbe7c80b0f2b62d11ac30f6fd5d9353c638c170d`  
		Last Modified: Wed, 02 Oct 2024 02:17:16 GMT  
		Size: 216.0 MB (216008485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec2c9b35b2ede673ef1aad1c04955156b5f20ef8b133c0b939977d9901ab133`  
		Last Modified: Wed, 02 Oct 2024 02:17:08 GMT  
		Size: 4.4 MB (4387336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:cf94d63bb15b70c477b03b08694926f7c4bd7a19298cc8757a068252193e0575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110c94acb7909e046f7763d45291358f5ff2eb0590f83c9f0f7a56f543bc8d5c`

```dockerfile
```

-	Layers:
	-	`sha256:a6a12513296f99469cca5610b7527eb2ae3c921bde8a62ab35af3aa4f4e5867a`  
		Last Modified: Wed, 02 Oct 2024 02:17:08 GMT  
		Size: 3.7 MB (3674553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a73b7c317d78829098a49d86c53e8443d0b813b6b43c4440c5991d075f926a`  
		Last Modified: Wed, 02 Oct 2024 02:17:07 GMT  
		Size: 23.8 KB (23810 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:1e145c5b09b0e4bb032ef65772a152182bfc3295e6d0a4078fbdf994a639077b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258304972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f715177fda0bb06c3638647a0dff6830a4ced9aa52cde9bcf45b747abb8adbe0`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='14f982221bb61f8ea5d11f2cb9a3470639004b825dcbb5640ffd27ed479a38c4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='37b6e363eb06c27bcfa9c8c1396839ce4a0e03eb58e0b79312fbc470eb968b63';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='34a59f13ee3070dcc64408331bb838c1286b7b7ea1ad71c693395aa3ef16c07b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='7a632e6503e77604a2f82668a0ef79991c2cb20a0baebf36aa5c8b0426ace796';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jdk_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
CMD ["jshell"]
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
	-	`sha256:c01e8fb9488f968047bddbbd8b285a418f2e70f909c5d89026f6804d4826a5bd`  
		Last Modified: Wed, 02 Oct 2024 02:08:15 GMT  
		Size: 210.6 MB (210619476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4c9f17b75d9e289967d82fadb959ce00200acbb2b9be624207fa90d593366e`  
		Last Modified: Wed, 02 Oct 2024 02:08:12 GMT  
		Size: 5.5 MB (5546602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0d990fd906f1458e4bcfc8d524441948886eb132c51983c713d69daf38c70e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a66f654f1a99921472cef2be2e7f643fb5d87d9cae6eabb843972662097e518`

```dockerfile
```

-	Layers:
	-	`sha256:7af11368d37b4c168c62880497313a024e0e5dbd83c3471ec812b5b3c0bf6fb2`  
		Last Modified: Wed, 02 Oct 2024 02:08:12 GMT  
		Size: 3.7 MB (3671539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517e82f47447087d542acdf64bb84d42aa23eaf548cfc3193c5c5d07eeb39ac0`  
		Last Modified: Wed, 02 Oct 2024 02:08:12 GMT  
		Size: 23.8 KB (23781 bytes)  
		MIME: application/vnd.in-toto+json
