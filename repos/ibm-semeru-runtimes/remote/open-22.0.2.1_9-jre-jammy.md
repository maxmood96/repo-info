## `ibm-semeru-runtimes:open-22.0.2.1_9-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:acb6a85d4ec30ab630d37be05d0f3f6abc51060b4d7bd43bf03844ca60e52988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:4b07167c3bdee704b6fa21b41884c367d636f05bf34080863c030552e9069b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102259787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1b2587e495f3bf8a963e4a7724d0396130c328a8bfcf4fd3f71f49381b3fa`
-	Default Command: `["\/bin\/bash"]`

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
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a30f37148392758107c9986eff0640019f62dc07b041aa861e5dabd02b0b7e`  
		Last Modified: Thu, 12 Sep 2024 22:02:35 GMT  
		Size: 12.2 MB (12156624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835046b9e07fd2dc9414b0b97054c14cf25eb67da9ea66ea2213e9d90cf62ca8`  
		Last Modified: Thu, 12 Sep 2024 22:02:36 GMT  
		Size: 55.3 MB (55324819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9148f62c8b7bb1ead97038276cd02c487c6a0346ee1f61f7557232f328a1b8a`  
		Last Modified: Thu, 12 Sep 2024 22:02:35 GMT  
		Size: 5.2 MB (5242319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ff17938d50ab93ed4fed4cc1090b3816ee117419bc9b77b8894eed66bacf5b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e408b5d1bcb36daf19c6df96eb602020b018af21640310b10ebd9efd8c1aac4`

```dockerfile
```

-	Layers:
	-	`sha256:38675e84268cae57665cd0f75c80611bb6f599f8d6473ce97bf9432ac47c7fc2`  
		Last Modified: Thu, 12 Sep 2024 22:02:35 GMT  
		Size: 3.5 MB (3461418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e387dec9b840f47f2507b626a871b7c8ed21858d37f09c9592f1c0d422571880`  
		Last Modified: Thu, 12 Sep 2024 22:02:35 GMT  
		Size: 24.4 KB (24406 bytes)  
		MIME: application/vnd.in-toto+json
