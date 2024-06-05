## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:fef7e2a56f15fb1c788b425bc020e740e7eb73782a1443333db5d047e76b62c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:12b4615def0b969c17bed9a8293c32d38dee03e39af00867f305c621a379815b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114724839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae68f307c7ec4e3bbfb4cb97f63dc79f618a455df834a3892b0f849f98480ed`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 00:30:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 00:31:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 00:31:16 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Wed, 05 Jun 2024 00:33:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 00:33:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 00:33:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 00:34:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Jun 2024 03:55:10 GMT
USER root
# Wed, 05 Jun 2024 03:58:17 GMT
ARG LIBERTY_VERSION=24.0.0.5
# Wed, 05 Jun 2024 03:58:17 GMT
ARG LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24
# Wed, 05 Jun 2024 03:58:17 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip
# Wed, 05 Jun 2024 03:58:18 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Wed, 05 Jun 2024 03:58:18 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Jun 2024 03:58:18 GMT
ARG VERBOSE=false
# Wed, 05 Jun 2024 03:58:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.5
# Wed, 05 Jun 2024 03:58:18 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 05 Jun 2024 03:58:18 GMT
COPY dir:38b34b4d2a90a4e46f2e857756efd7505e693612d72fdf3d4ab5795896a9f0d8 in /opt/ol/helpers 
# Wed, 05 Jun 2024 03:58:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 05 Jun 2024 03:58:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 05 Jun 2024 03:58:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 05 Jun 2024 03:58:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 05 Jun 2024 03:58:29 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 05 Jun 2024 03:58:29 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 05 Jun 2024 03:58:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 05 Jun 2024 03:58:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Jun 2024 03:58:35 GMT
USER 1001
# Wed, 05 Jun 2024 03:58:35 GMT
EXPOSE 9080 9443
# Wed, 05 Jun 2024 03:58:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 05 Jun 2024 03:58:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3228adc4e21dff5477e2d02c613164457247b781b68b96a2d89e80535283159`  
		Last Modified: Wed, 05 Jun 2024 00:54:34 GMT  
		Size: 12.2 MB (12156888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a2d291a18c36c2899a71de5876e4774284beb3d1321beaf7ab37b4fb85f64`  
		Last Modified: Wed, 05 Jun 2024 00:55:30 GMT  
		Size: 50.4 MB (50447726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23deda73013b5eccfde8d36aa2e47a304421ccc4dce2a8b58cdc3ad747a6faf`  
		Last Modified: Wed, 05 Jun 2024 00:55:25 GMT  
		Size: 4.2 MB (4226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf869fb5f7e83955da9071b3c5f444553a698d0daba9b62b02007cdd4252cb75`  
		Last Modified: Wed, 05 Jun 2024 04:13:00 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7844496ebcaf685579d4c5fc12a58ba1f4217c400a795bbbc6f1254c64c21a67`  
		Last Modified: Wed, 05 Jun 2024 04:13:00 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b375266977a907f5055747237d44baee9481cced8cf480239e3befc84d43f32d`  
		Last Modified: Wed, 05 Jun 2024 04:13:00 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f358bd88aefa3eb519c585b93278d9bb09d1bdb4885cce1d3c0e8a8a3ce957`  
		Last Modified: Wed, 05 Jun 2024 04:12:58 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037c6c5f6f4d6a032ab2fad1024fc8818bb2160cec8c0768750b3e39382b6acf`  
		Last Modified: Wed, 05 Jun 2024 04:12:59 GMT  
		Size: 14.7 MB (14678449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5966ef5f1889dd07a83e599c0735fd891782730754d4e7e4161aef501d622f54`  
		Last Modified: Wed, 05 Jun 2024 04:12:58 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ca1ecd51a0d3851a9db79545df2501c224344d0ec2da866cae71afbf15797`  
		Last Modified: Wed, 05 Jun 2024 04:12:58 GMT  
		Size: 10.6 KB (10559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da0545674b6788f1ad57f30a68f8f12a5efc2744b913ca9d3f2e49d6d58e5f8`  
		Last Modified: Wed, 05 Jun 2024 04:12:59 GMT  
		Size: 2.7 MB (2721794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:c397052819cd295b4882c8166f01432b023c89695ba426a47a6446abe5aefe2b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111754499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b199c957715e146a8e07d803a0eb9ae3e240a03757fd53b312a30f3d66a667`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:00:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 06:01:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:01:22 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Wed, 05 Jun 2024 06:02:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 06:02:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 06:02:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 06:03:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Jun 2024 11:20:14 GMT
USER root
# Wed, 05 Jun 2024 11:23:08 GMT
ARG LIBERTY_VERSION=24.0.0.5
# Wed, 05 Jun 2024 11:23:08 GMT
ARG LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24
# Wed, 05 Jun 2024 11:23:08 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip
# Wed, 05 Jun 2024 11:23:08 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Wed, 05 Jun 2024 11:23:08 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Jun 2024 11:23:08 GMT
ARG VERBOSE=false
# Wed, 05 Jun 2024 11:23:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.5
# Wed, 05 Jun 2024 11:23:08 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 05 Jun 2024 11:23:09 GMT
COPY dir:38b34b4d2a90a4e46f2e857756efd7505e693612d72fdf3d4ab5795896a9f0d8 in /opt/ol/helpers 
# Wed, 05 Jun 2024 11:23:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 05 Jun 2024 11:23:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 05 Jun 2024 11:23:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 05 Jun 2024 11:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 05 Jun 2024 11:23:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 05 Jun 2024 11:23:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 05 Jun 2024 11:23:21 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 05 Jun 2024 11:23:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Jun 2024 11:23:21 GMT
USER 1001
# Wed, 05 Jun 2024 11:23:21 GMT
EXPOSE 9080 9443
# Wed, 05 Jun 2024 11:23:22 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 05 Jun 2024 11:23:22 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb8d6134690c858cfd9f9b81a6adb73767cdf8efe4e439360fbd094b85dde8c`  
		Last Modified: Wed, 05 Jun 2024 06:16:39 GMT  
		Size: 12.1 MB (12117024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684b00a671cc206ad0371beab4e9129d7eb0215b90b59e37cea7292529bb39dd`  
		Last Modified: Wed, 05 Jun 2024 06:17:10 GMT  
		Size: 49.7 MB (49726322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8782221adede579904a2034868b7313499b72d2906458d7ddc6dfc34471301`  
		Last Modified: Wed, 05 Jun 2024 06:17:06 GMT  
		Size: 4.1 MB (4058642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884159d2eb0935d1d15ae91b309adb349b952b03f6d5ec21aba9db1a2ed71f13`  
		Last Modified: Wed, 05 Jun 2024 11:35:41 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8887ebf8b0cf596ff84d5d62a246bf608d319fcb4d13f163f1b656978e4c2a6d`  
		Last Modified: Wed, 05 Jun 2024 11:35:41 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c212232f0adeb813cb16f5366db22c6fea1cb281909671f7d79c9f28dc331f57`  
		Last Modified: Wed, 05 Jun 2024 11:35:41 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58f7739b543cbdfba01613bafc0b9126dd4230875dc3a2b953897e8f07603f`  
		Last Modified: Wed, 05 Jun 2024 11:35:39 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c81bb0225cd08a1a47dc92ce05a37f77d1097ec3363f36a09c406dfed86f29f`  
		Last Modified: Wed, 05 Jun 2024 11:35:40 GMT  
		Size: 14.7 MB (14680264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed79a54d4c692c7b911153ab982b836b95b2fdd83d7b1e6f2f03dee8838f2746`  
		Last Modified: Wed, 05 Jun 2024 11:35:39 GMT  
		Size: 824.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecd7f91510b0c104130fb576b4c2c7280ebc5d7eb1e3e5742e766fde0d6d532`  
		Last Modified: Wed, 05 Jun 2024 11:35:39 GMT  
		Size: 10.6 KB (10562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cd8d2e0886d762257c9d18fe3207b6e841620f75403cb943e784ae172fce47`  
		Last Modified: Wed, 05 Jun 2024 11:35:39 GMT  
		Size: 2.7 MB (2705412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:4c13a92a7f610332990f588ac23e1d0c349adc5a27d72fcd104c65c6329ae80f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120960854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc842007b0986b9bb0b59f94594612bbfd8800a2bc0c5251e8b48d5cfb9378e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:09:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 04:10:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:10:04 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Wed, 05 Jun 2024 04:11:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 04:11:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 04:11:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 04:12:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Jun 2024 09:43:41 GMT
USER root
# Wed, 05 Jun 2024 09:48:25 GMT
ARG LIBERTY_VERSION=24.0.0.5
# Wed, 05 Jun 2024 09:48:25 GMT
ARG LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24
# Wed, 05 Jun 2024 09:48:25 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip
# Wed, 05 Jun 2024 09:48:26 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Wed, 05 Jun 2024 09:48:26 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Jun 2024 09:48:26 GMT
ARG VERBOSE=false
# Wed, 05 Jun 2024 09:48:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.5
# Wed, 05 Jun 2024 09:48:27 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 05 Jun 2024 09:48:27 GMT
COPY dir:38b34b4d2a90a4e46f2e857756efd7505e693612d72fdf3d4ab5795896a9f0d8 in /opt/ol/helpers 
# Wed, 05 Jun 2024 09:48:28 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 05 Jun 2024 09:48:29 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 05 Jun 2024 09:48:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 05 Jun 2024 09:48:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 05 Jun 2024 09:48:41 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 05 Jun 2024 09:48:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 05 Jun 2024 09:48:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 05 Jun 2024 09:48:50 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Jun 2024 09:48:50 GMT
USER 1001
# Wed, 05 Jun 2024 09:48:50 GMT
EXPOSE 9080 9443
# Wed, 05 Jun 2024 09:48:51 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 05 Jun 2024 09:48:51 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98c5621e9cde7a31d0331e179ec18fc66523065d973f996e2d2dc3d2b24ee95`  
		Last Modified: Wed, 05 Jun 2024 04:28:48 GMT  
		Size: 12.9 MB (12889842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80471b6a2750b9146a55314f706d7287a5cc6899a10bf119c32fd50ab6ae7101`  
		Last Modified: Wed, 05 Jun 2024 04:29:25 GMT  
		Size: 51.7 MB (51706152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fe45236a037dc59d701ce1878145c98bc84fd0dfc9e94064ab101908df963`  
		Last Modified: Wed, 05 Jun 2024 04:29:20 GMT  
		Size: 3.5 MB (3456645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cd0c73cf7ec6a53b97259ab376d6d9d504dc208cb4d176d641dd73bfb5a9d7`  
		Last Modified: Wed, 05 Jun 2024 10:07:52 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ced7a819f16274a8eeadebd9c04e528aa1419acdfd8d13efecb0d11e61a782`  
		Last Modified: Wed, 05 Jun 2024 10:07:52 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d715622653b70ae0cadaf73fea6c6f4547bc19098950e7965df66c78e25334`  
		Last Modified: Wed, 05 Jun 2024 10:07:52 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de68a8c4958b1475d63e4627f160551e314319f369f0533a6b5a64d4a7c86d4`  
		Last Modified: Wed, 05 Jun 2024 10:07:50 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386710682d35d564f103718e8059e926e87e7038f69abe2e7bb8a84affcd92dd`  
		Last Modified: Wed, 05 Jun 2024 10:07:51 GMT  
		Size: 14.7 MB (14679056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ce66a111240d991655df7625a98e111713c3af1944b3dd89c5642267972520`  
		Last Modified: Wed, 05 Jun 2024 10:07:50 GMT  
		Size: 827.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5369c62d1034d00588feb44190b83869a9a46ce6e5c4112c2cc900ae4c397d72`  
		Last Modified: Wed, 05 Jun 2024 10:07:50 GMT  
		Size: 10.6 KB (10557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000990af1efc2e8f7e357b00b0ca355aa2dd8214b414c7255bee0bf341e9b936`  
		Last Modified: Wed, 05 Jun 2024 10:07:51 GMT  
		Size: 2.6 MB (2582123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:09e80926cf9782defde4c78798323bc1bd07d5dce835ecf52ad641bc1d938c9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112903994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837ea439fa8c40f85b00dad546d0242752cb98acbbf8d526b7f13ec211bc408d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:39:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 03:39:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:39:28 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Wed, 05 Jun 2024 03:41:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 03:41:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 03:41:08 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 03:41:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Jun 2024 06:09:26 GMT
USER root
# Wed, 05 Jun 2024 06:14:37 GMT
ARG LIBERTY_VERSION=24.0.0.5
# Wed, 05 Jun 2024 06:14:37 GMT
ARG LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24
# Wed, 05 Jun 2024 06:14:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip
# Wed, 05 Jun 2024 06:14:38 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Wed, 05 Jun 2024 06:14:38 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Jun 2024 06:14:38 GMT
ARG VERBOSE=false
# Wed, 05 Jun 2024 06:14:38 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.5
# Wed, 05 Jun 2024 06:14:38 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 05 Jun 2024 06:14:38 GMT
COPY dir:38b34b4d2a90a4e46f2e857756efd7505e693612d72fdf3d4ab5795896a9f0d8 in /opt/ol/helpers 
# Wed, 05 Jun 2024 06:14:39 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 05 Jun 2024 06:14:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 05 Jun 2024 06:14:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 05 Jun 2024 06:14:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 05 Jun 2024 06:14:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 05 Jun 2024 06:14:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 05 Jun 2024 06:14:53 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.5/openliberty-kernel-24.0.0.5.zip LIBERTY_SHA=ed1515ff9d8faafeae0ed6b3adf00646320d3c24 LIBERTY_VERSION=24.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 05 Jun 2024 06:14:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Jun 2024 06:14:53 GMT
USER 1001
# Wed, 05 Jun 2024 06:14:53 GMT
EXPOSE 9080 9443
# Wed, 05 Jun 2024 06:14:53 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 05 Jun 2024 06:14:53 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec82a3649a60c81782d42d575ab21e0b591737fe7cf76c87eb0ee6dad4b737`  
		Last Modified: Wed, 05 Jun 2024 03:56:08 GMT  
		Size: 12.2 MB (12204558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f62f3f30e003da488b6b6cbb53c77d50efc7c34585e05a0766d0786d8cb790`  
		Last Modified: Wed, 05 Jun 2024 03:56:38 GMT  
		Size: 50.2 MB (50232662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1d0006ef87dc97591a50f21b96a1cf7c877e518ae6789a12cf18505a2860a`  
		Last Modified: Wed, 05 Jun 2024 03:56:33 GMT  
		Size: 4.4 MB (4359349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bd18fe7ed455f1f7603b20a9225fc3f83fb54efe1457ffddf1895762036bee`  
		Last Modified: Wed, 05 Jun 2024 06:30:15 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5b380fca4ad66515dfc69da820e101fcbddfda766b51433c302ad7227aed27`  
		Last Modified: Wed, 05 Jun 2024 06:30:15 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0702c0a26fbe34345f1f041fe9d660a39761832225a2b573314a53ae76abdb6a`  
		Last Modified: Wed, 05 Jun 2024 06:30:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f56f54dcc1bda0cb55c2ebf2839e082fd8780c095069973486336b009adcf9`  
		Last Modified: Wed, 05 Jun 2024 06:30:13 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab227a03ce1d0f5b9def9af1fe9141d84fa833e59f163e4da24fe175e0857896`  
		Last Modified: Wed, 05 Jun 2024 06:30:14 GMT  
		Size: 14.7 MB (14678675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984d334ae47b2262ab4b3ccbc47460d2bcb5143cefad042cdbf7fdfd09c93798`  
		Last Modified: Wed, 05 Jun 2024 06:30:13 GMT  
		Size: 823.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1158f2871e9d58a90782de13ad772b9f99f34ca7de6bafb295c650d23d604`  
		Last Modified: Wed, 05 Jun 2024 06:30:13 GMT  
		Size: 10.6 KB (10566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2982f45272c275c9d42e82341ab9b35089194e16882ea58d01c7635709ce88`  
		Last Modified: Wed, 05 Jun 2024 06:30:14 GMT  
		Size: 2.7 MB (2736028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
