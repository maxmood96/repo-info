## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:e5adb21ff601cf5c78d52af22712524a4ae109cde1528d806da3000acfb62249
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

### `open-liberty:beta-java17` - linux; amd64

```console
$ docker pull open-liberty@sha256:bbdc443da35f63c3a3b78196cbba4c40504122e0dcd6328e3cac1c01966de10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473858016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349520ba9762dd1946ef55a0ed265a11777029a5557d1491bf5dcebd0d3a624b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
USER root
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_VERSION=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:20 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.4-beta liberty.version=25.0.0.4-beta io.openliberty.version=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:20 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:20 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:20 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec858451a83233992650613d98480fb82d8168770ffc63ea19e0b5e3a3c9e7b2`  
		Last Modified: Wed, 09 Apr 2025 01:24:17 GMT  
		Size: 12.2 MB (12171980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099deadc35482fd85d5cfc88981d4c07b241b56691967c4b46ef6230900f7d7a`  
		Last Modified: Wed, 09 Apr 2025 01:24:18 GMT  
		Size: 51.7 MB (51659750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cb19475be125bbbe9d118ef7e6e21431729962c08faccb0f7d83c6343b1723`  
		Last Modified: Wed, 09 Apr 2025 01:24:17 GMT  
		Size: 5.1 MB (5114655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfc4e23739be4cab819dcbebd39d20d7f63091e6625e5d339c40a1802c89ffe`  
		Last Modified: Wed, 09 Apr 2025 02:14:38 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3209a5d3f451ae0ef354ee29aabfc107edda300c0a2352f00c9ee8831a11d6`  
		Last Modified: Wed, 09 Apr 2025 02:15:34 GMT  
		Size: 10.4 KB (10400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ef1d49d2229ce4c5100849d14f78f81a17802b3318841a0eff8ad949824798`  
		Last Modified: Wed, 09 Apr 2025 02:14:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d72f9ee4291928973810bb24fc00d644b8ac5e50075b598454a2447ae406a`  
		Last Modified: Wed, 09 Apr 2025 02:14:38 GMT  
		Size: 31.7 KB (31744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663d9845cb106539107d33559a0747b59e6ddbd2c747ba1a1a97d4c8775e1156`  
		Last Modified: Wed, 09 Apr 2025 02:15:41 GMT  
		Size: 361.2 MB (361176813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfded4e701060f657b3e9506116bf2cda931ac70005d8220556b6e6a5c863d8`  
		Last Modified: Wed, 09 Apr 2025 02:15:34 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450ff08893f004de72ef66c414daabdd2aad5033bf117968223d930c21f16e3b`  
		Last Modified: Wed, 09 Apr 2025 02:15:34 GMT  
		Size: 11.8 KB (11766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b776108a96bb2fac0cd1424a130187b4568a46451699fb2b85fa5057f66f8`  
		Last Modified: Wed, 09 Apr 2025 02:15:35 GMT  
		Size: 14.1 MB (14146195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:fdfb67dcf49291484b0b42fe7d651910c25a471121cd397b82903378a14e9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42fe425af2b69a125f299ea553970a474d682e5de333dfffea1e3f930ede767`

```dockerfile
```

-	Layers:
	-	`sha256:24f822b7ed8d857f02be2cf1ba68016fd5f5e6d454bf0c93c99459ac4551d7a2`  
		Last Modified: Wed, 09 Apr 2025 02:15:34 GMT  
		Size: 5.6 MB (5592213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95165a4116f0f9acd79c053f3a96706a27d092b1c5133d4f060d0c9250460e67`  
		Last Modified: Wed, 09 Apr 2025 02:15:33 GMT  
		Size: 38.8 KB (38834 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:ae50cf29f5fc5c94d4f9b3f4064d9b8050a2bf76f5d37d1d19010f47cccf19a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466787517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4b3f96ec2b0c59d68bd0662c80812aa628f25305c7d1aa75b46213bb1a6f45`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
USER root
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_VERSION=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:20 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.4-beta liberty.version=25.0.0.4-beta io.openliberty.version=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:20 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:20 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:20 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e483842b440e4fd1b12a18bab983fb09c8751e230e70f7c022dae2765ea706a5`  
		Last Modified: Mon, 24 Mar 2025 17:01:02 GMT  
		Size: 12.1 MB (12123514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51776dd1b36a6774b3e410e2240d06d88f2438f6981ab29cca22ce5ddfa5c7a7`  
		Last Modified: Mon, 24 Mar 2025 17:17:44 GMT  
		Size: 48.1 MB (48083208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76ee805f80d071a780e257de1dd9de801efb61df1c3d9d001c9189e6fbf794e`  
		Last Modified: Mon, 24 Mar 2025 17:17:42 GMT  
		Size: 4.7 MB (4749183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48beec194ecd7d074464528333285ba7c8899bf49c3f1a1fb31b2c247f39ce0e`  
		Last Modified: Mon, 24 Mar 2025 18:10:38 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8cbf4d2f7472e6671b1362dbc775eb3796ab21333543a819b2b369dd230588`  
		Last Modified: Thu, 27 Mar 2025 23:38:53 GMT  
		Size: 10.4 KB (10406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69404d77c8b4314084f1750dc650df2d75db3c10022c06c362e917db5b3513e1`  
		Last Modified: Thu, 27 Mar 2025 23:38:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009fbfb2f214a1f69b4cf509ba05807faf897a46009e2cb8e0c47519dc75dab`  
		Last Modified: Thu, 27 Mar 2025 23:38:54 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d65da01050d7d6f3d5e4d50eead713bbc05c3e92451e82f3bce50dae44de28`  
		Last Modified: Thu, 27 Mar 2025 23:39:07 GMT  
		Size: 361.2 MB (361176827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947b013cf33813b3c82a4065f6c9758de8b446d86cd705c8b3bccab1d197969d`  
		Last Modified: Thu, 27 Mar 2025 23:38:54 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d918eaaec05da72c66b78d141b11cef69fad6388fcecbd6de518bf49f49c08d4`  
		Last Modified: Thu, 27 Mar 2025 23:38:54 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728806ced0d6ea7cb1ee824542e0474dd4cf687685abae83561c61dc1fcee40a`  
		Last Modified: Thu, 27 Mar 2025 23:38:55 GMT  
		Size: 13.2 MB (13229755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:11768a4c42b2a6f904c0bc7ae71acbf153a2006f4ffb3734ed64d0ce34d55fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814cea45cae837b65009dc6ce206c83800101c57b7aa4c8ed9041dddc20d31c9`

```dockerfile
```

-	Layers:
	-	`sha256:649aba29da304706b2e7cf5430325249be9d282f3957121114318a8704e77507`  
		Last Modified: Thu, 27 Mar 2025 23:38:54 GMT  
		Size: 5.6 MB (5586476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab19152132591fe72f60ad6b786751a50416b101f6eb94e4befe9902d8dc82b8`  
		Last Modified: Thu, 27 Mar 2025 23:38:53 GMT  
		Size: 39.0 KB (38964 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:8a0165bcef5d5e21825c8a0265894f3e036deaf7e0b4cbaf273f5aa75d32663c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.1 MB (477143940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb08badc35f81bfe86a9da924e38794d4bca9f80ee0836e2d8c9d2fe8151ac`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

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
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
USER root
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_VERSION=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:20 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.4-beta liberty.version=25.0.0.4-beta io.openliberty.version=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:20 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:20 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:20 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d3723544f563c5caea752a6d25c7e1228adc4e25ad816d88baac9218eacb0`  
		Last Modified: Wed, 09 Apr 2025 05:00:29 GMT  
		Size: 12.9 MB (12892817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a60f352105e0450924c6d8bd36e610f632b2730d1912f591e0d81c6686889`  
		Last Modified: Wed, 09 Apr 2025 05:21:54 GMT  
		Size: 52.8 MB (52766822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dedd1ffe863edbc83596d334ef5bfcd3b869f3b43f160ffa44645bdfd4c9117`  
		Last Modified: Wed, 09 Apr 2025 05:21:52 GMT  
		Size: 3.8 MB (3792652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7d8d58788b693066dde435ebc64fbe4a028dcfee0ec029fd05c36555252e6`  
		Last Modified: Wed, 09 Apr 2025 08:29:52 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e78d0325446a7ce744fccf5af25b6cee38d317f2ddb044a5ba57d992e1c886c`  
		Last Modified: Wed, 09 Apr 2025 08:29:52 GMT  
		Size: 10.4 KB (10398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abf235e114e84e73fa5488ce290e2b96c37844a17e590106afc8642bb8fc2ee`  
		Last Modified: Wed, 09 Apr 2025 08:29:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2c135b48b842347a0f705b8830839d9c2c13f9803c94d06ab0febe17f94d4b`  
		Last Modified: Wed, 09 Apr 2025 08:29:52 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6639c5592b3cec60b1debb940d656ddc046d11f3d2f29f477095bf9a8c0242a`  
		Last Modified: Wed, 09 Apr 2025 08:30:25 GMT  
		Size: 361.2 MB (361177130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2474aecfe74ac1e0c1f83ed1387fb2d91fa2a8053e00184a6b114eb1badc2474`  
		Last Modified: Wed, 09 Apr 2025 08:29:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa928de909b038e451521f7eca3e550ead9b9be190421f4862d6ca4843d5ff`  
		Last Modified: Wed, 09 Apr 2025 08:29:53 GMT  
		Size: 11.8 KB (11766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519f276c5cbc3e1db374b98eea53fffa6af397cf603dca157dc4864e75d5a757`  
		Last Modified: Wed, 09 Apr 2025 08:29:54 GMT  
		Size: 12.0 MB (12010814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4c960c58914f6c09ce0d31f5ab97af0f6fd3c2018b7f66e41169ff6cbb5b1570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5633092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d98bbd3052cd2ce08e7539aeb871bbca55cd11d18df88e656ba386a027b4c9c`

```dockerfile
```

-	Layers:
	-	`sha256:f902e63cfdd781ad2c1f8f35646021af14e56d1919e81740e56e7318529f624d`  
		Last Modified: Wed, 09 Apr 2025 08:29:53 GMT  
		Size: 5.6 MB (5594222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19728dc25a6e4187fde30c2f424515025982ca1bf64afbeeb640ad671c384d16`  
		Last Modified: Wed, 09 Apr 2025 08:29:52 GMT  
		Size: 38.9 KB (38870 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:761daaa6ced8c68b2f78653b5503b10a319103fc43442d83ad6977b893280e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.1 MB (471073762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1cde93011eff776b8fa4ac0996a4586cdf6919913bb0dde0342535f4d49f3b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

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
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
USER root
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_VERSION=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip
# Tue, 25 Mar 2025 15:38:20 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:20 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.4-beta liberty.version=25.0.0.4-beta io.openliberty.version=25.0.0.4-beta
# Tue, 25 Mar 2025 15:38:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4-beta LIBERTY_SHA=412ced0daad2835d2ed5dafaa724b4bcde5cd6bf LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.4-beta/openliberty-runtime-25.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl250320250310-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:20 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:20 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:20 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37c15bd03d2fba2f94f41eed8657555e15fdae30c25e75be803e690fcef048e`  
		Last Modified: Wed, 09 Apr 2025 04:31:12 GMT  
		Size: 12.2 MB (12218864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c2294dd111ee69bcc066d321ec9850a967caf1783fa33cbecdc22539450f6f`  
		Last Modified: Wed, 09 Apr 2025 04:50:29 GMT  
		Size: 50.6 MB (50552921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee9c52d2e2825532b34769e5cf0e2a1cc004b33a9f9fd2bb889a0bca9cee32`  
		Last Modified: Wed, 09 Apr 2025 04:50:28 GMT  
		Size: 5.2 MB (5156372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764f90cb84ecabafc421a8458b12aa56a1a33cb08a636a487b0b54092904446`  
		Last Modified: Wed, 09 Apr 2025 05:54:07 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c4c11f8d612aa6ebf20b2489ec324a62a320abdef62caf8923e5049c8ffa91`  
		Last Modified: Wed, 09 Apr 2025 05:54:08 GMT  
		Size: 10.4 KB (10401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47093ff896e94c78d1f222775b85f247bb35cbe08c447db0a8f1688fbd81c51`  
		Last Modified: Wed, 09 Apr 2025 05:54:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c763f71e07f2ca33305991aa3541f4b2a3d7d2d2d2f887bc915e535dab3a8dd5`  
		Last Modified: Wed, 09 Apr 2025 05:54:08 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b6f44328e6675348644be06b841c8b29056c55c76c6a6a67495d9664d9cd38`  
		Last Modified: Wed, 09 Apr 2025 05:54:15 GMT  
		Size: 361.2 MB (361176526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380caa9d0e8207498f031bff42713f5b8bcae4b12ef311623276ad224b1b761`  
		Last Modified: Wed, 09 Apr 2025 05:54:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372851c4de3643b8ef9478dfd043a8e39446f157a0825813857e254ff768bbf1`  
		Last Modified: Wed, 09 Apr 2025 05:54:09 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c223c3c0d1a4b0a735de5c2bcb1674f5ee0284126f14e561709e651a6c72c3`  
		Last Modified: Wed, 09 Apr 2025 05:54:10 GMT  
		Size: 13.9 MB (13911324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ae2687ba131a595212755bc7e8b65163dd44e6affce8a5bad2ea163e71db17dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e242a90f1f1e3eb2fe7e5e1a7e6ff40ce6e00f85b3d3c70a4a9552a73cb0cd5`

```dockerfile
```

-	Layers:
	-	`sha256:b4fb0caf0be8990e4d4da2e35eae761c7d53e0fc43135ce4dda65dd8c49ebe10`  
		Last Modified: Wed, 09 Apr 2025 05:54:08 GMT  
		Size: 5.6 MB (5590756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2ad0459c4cffcaf136e02fbd77e820468698a1f2df61c66d262a217e342ab3`  
		Last Modified: Wed, 09 Apr 2025 05:54:07 GMT  
		Size: 38.8 KB (38836 bytes)  
		MIME: application/vnd.in-toto+json
