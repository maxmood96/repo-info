## `open-liberty:full-java8-openj9`

```console
$ docker pull open-liberty@sha256:fa0e7c21405a2928dbb8423ee689640d69eb1719753f78dc238185d394b592e1
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

### `open-liberty:full-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:47793a06ea7f1c9b5929ba09a3c031d0b2da8f00a9827dbb90871f25aa48e1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441940739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e66108a8f27303684faa3f1a5c9404a25e84a7db2703aa67df522bbc8894c9f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506a1162fbc98a1be75a141a84ea25287cb27db80944dd08175248215eae9d45`  
		Last Modified: Wed, 17 Jul 2024 17:56:21 GMT  
		Size: 12.2 MB (12156609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f25d8830f92315eae6d1abeb903c4e7d2a1504d87635560261663ce31e5f90`  
		Last Modified: Wed, 17 Jul 2024 17:56:23 GMT  
		Size: 50.4 MB (50447719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d672b51bef8a0b9cbf240620b8df7abb91a2d7d5213643d325ed2949354f9803`  
		Last Modified: Wed, 17 Jul 2024 17:56:21 GMT  
		Size: 4.3 MB (4325841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e213679021ebebadc6b69ea9076bb97533fef4d5992286c82b4f928c086ec7e0`  
		Last Modified: Thu, 18 Jul 2024 18:56:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386d85b3339cb1689cc925f72341a50e59379efa821ce86f3da84ceac72fc80`  
		Last Modified: Thu, 18 Jul 2024 18:56:39 GMT  
		Size: 10.0 KB (9991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cbfe685a1b855a02f88fbfb2a4bd0476fb0bf8eda947be1adf077fd98d8e08`  
		Last Modified: Thu, 18 Jul 2024 18:56:39 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a49640056de1451493155d768ea83f930e6964c9f1c28d15bd75d9242d3b38`  
		Last Modified: Thu, 18 Jul 2024 18:55:48 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a438ab0496e38b364a041189f5b4e222c03df631591591df05a9fbc87c0702`  
		Last Modified: Thu, 18 Jul 2024 18:56:45 GMT  
		Size: 331.8 MB (331844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409289e32b4542fff70808d06dd8ac1d3527187d92a0b2e4e8c7afbf93da897`  
		Last Modified: Thu, 18 Jul 2024 18:56:40 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49815dc8c44b97ae3d85c9f0a628c13923c1549956e65001f8f6ee1d0c9916`  
		Last Modified: Thu, 18 Jul 2024 18:56:40 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f157bff13da2fc20a36e39ec794b308997c97a48c3f0661ddb1baeb9f5794`  
		Last Modified: Thu, 18 Jul 2024 18:56:41 GMT  
		Size: 13.6 MB (13576673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:66f1be116060ae5d57b8e736320a2eddb603bc8e1a721e52fa75e5821bd36d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ac75450d2694c3ecfae6814af925a787ce1b1611bd04948f36ee6a78e0ced8`

```dockerfile
```

-	Layers:
	-	`sha256:635ae66d109c45d2980edb7ab19685840b22e9768a2d9f275e755a37fdb04e64`  
		Last Modified: Thu, 18 Jul 2024 18:56:40 GMT  
		Size: 5.3 MB (5332705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013845600e4240de169270164456b7756561fcf1d8dd4d9c2b09534d07ff2799`  
		Last Modified: Thu, 18 Jul 2024 18:56:39 GMT  
		Size: 39.1 KB (39145 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:0096e244ea43ab09d609992b838de12d0e8ca7eb9f5b934c7338059e1d9fc124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 MB (437804178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfe49f2045cc4a9ed70b3ab7551601c3aa3cabd9c37be48c6fba11f9f578657`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a73c992d8ae249d8805479ac497dac9fa0b1b48ab385b7d65a1b68d7dd3f7e`  
		Last Modified: Wed, 17 Jul 2024 17:58:36 GMT  
		Size: 12.1 MB (12114226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2cdc77c3882f4868ecdfdaa856ee064961f235c173d0335ac5119c2021e549`  
		Last Modified: Wed, 17 Jul 2024 18:00:39 GMT  
		Size: 49.7 MB (49726256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f9eeb938101f0b401b9f923870c89d4478bc6b9bcf528d9567914adcdeb1ab`  
		Last Modified: Wed, 17 Jul 2024 18:00:38 GMT  
		Size: 4.0 MB (4035177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c89578d66989a8b0ecdd16f5370228cbc7cb1c35649c08747c9eec6c80a63ef`  
		Last Modified: Wed, 17 Jul 2024 18:52:27 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1544256bafa1554c55bf178b8684f8a09250a438e5ed24a3462b1ff92b23c37`  
		Last Modified: Wed, 17 Jul 2024 18:52:27 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a921253e3dc67fa1b517ab9f90d5bb6ce44f92697a37e420dd84e0fac1a373`  
		Last Modified: Wed, 17 Jul 2024 18:52:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760e4649b719ab5f9a6b9bad8ed391cdaa3a12eb1afae95fbc55cdf61b739138`  
		Last Modified: Thu, 18 Jul 2024 19:06:29 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb023c45bbf25695a55c1289f97ae27abb44b0db413bb53eca76a0b9b69b264`  
		Last Modified: Thu, 18 Jul 2024 19:06:37 GMT  
		Size: 331.8 MB (331844739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c859d240736ccfbad711ff317af4f73880d5983c7886759a39a21237af04a36c`  
		Last Modified: Thu, 18 Jul 2024 19:06:29 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d657dd0feb4116110098ffee603f0c8de5469b6b02fc04a69beaa91847aa8a`  
		Last Modified: Thu, 18 Jul 2024 19:06:29 GMT  
		Size: 11.4 KB (11359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f9b3ea2a33fa8fc25e58f89b82e0c39ceac3afda246680522864783ba450ee`  
		Last Modified: Thu, 18 Jul 2024 19:06:31 GMT  
		Size: 12.7 MB (12657740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:847c6101f3848ca43aa19fbc75c706d5cb97580cee993cf14d5a588a002ec069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5372500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d95e64997e985e9c2a4c0b7eaed55368aae115c2cc8fc950209e14f2463c3f4`

```dockerfile
```

-	Layers:
	-	`sha256:08af51564513bbbef28d43102ff03a36584c1b378045f4426759fbeee7fb198c`  
		Last Modified: Thu, 18 Jul 2024 19:06:30 GMT  
		Size: 5.3 MB (5332982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:710ac98f5411e54e3cc83d862d0190fbf043e7cbfb3a88a5334a8fff54dc1b3a`  
		Last Modified: Thu, 18 Jul 2024 19:06:29 GMT  
		Size: 39.5 KB (39518 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:ad04204b7ab830849f554c3a259c4ed12e9784a532449b336bbff7d25465fcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.1 MB (446086199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fadee8a8a3209aa32bf34ab4b28238276be7330fb262668606af4e1875e9bbb`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba08511b677aee03243955ecffe2cf3bff11dcf9bbc6f35ad5e9deb073b144`  
		Last Modified: Tue, 02 Jul 2024 10:27:08 GMT  
		Size: 12.9 MB (12888223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa280e675d3314e823bbc098f172c8e11b6a04655bd302485d2ae06f1a4a967`  
		Last Modified: Wed, 17 Jul 2024 18:01:53 GMT  
		Size: 51.7 MB (51706122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979e4af8be2feb5da4d9bb26c5a0b7e4c842203e3ba8d51e1dc7c805c612f00`  
		Last Modified: Wed, 17 Jul 2024 18:01:51 GMT  
		Size: 3.5 MB (3460263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bfb9265f9ccbecc50220d027cbc182172b41d0206b6bf6d5473a3216168cd7`  
		Last Modified: Wed, 17 Jul 2024 18:53:21 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a122edf458e609830078f00c54df2d1fbc5679f6336257d9babe21efe10a36`  
		Last Modified: Wed, 17 Jul 2024 18:53:21 GMT  
		Size: 10.0 KB (9986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eac48c2f797b621fe8e4ab60fb2e4e2ba1e3a877060f688c8ad47c6fc8f897`  
		Last Modified: Wed, 17 Jul 2024 18:53:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85364886ffd27982e4a1fe51c2f7ded1b497cef50d52eb6e32979e6486fdb1d7`  
		Last Modified: Thu, 18 Jul 2024 19:09:01 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981f2d187e2a736a76bf03762bbc3f72020f723acf817636b5b955dfc680cef2`  
		Last Modified: Thu, 18 Jul 2024 19:09:20 GMT  
		Size: 331.8 MB (331845068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35ce4ba8508aa5665e86d4a0f1b23a22ea2effe095b78c3817a4f84af689649`  
		Last Modified: Thu, 18 Jul 2024 19:09:01 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8555e40a22d705d302e29c09f4b6996652b962701c02bd057dfa297b7bcfa6`  
		Last Modified: Thu, 18 Jul 2024 19:09:01 GMT  
		Size: 11.4 KB (11361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c2da451ffe033629a4174f5d54ea07c7affe44f3b5849b645ac579da2d9a5`  
		Last Modified: Thu, 18 Jul 2024 19:09:03 GMT  
		Size: 11.7 MB (11665248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a80933eaf7c7a625bc844aa5f6c2e342cbe348b862fc96434a9a1fb2126933f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5376386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8f700a8d0913e91f4d4e86f9141e25951b69e865179ffd0d15a3f6be5f62fa`

```dockerfile
```

-	Layers:
	-	`sha256:30957a57600fa331dad09d4e9cff91be4209ddc691fde7c45a862981019fbc69`  
		Last Modified: Thu, 18 Jul 2024 19:09:02 GMT  
		Size: 5.3 MB (5337195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7f2b62b2005144ea9b1c2544037ce1caa22c2dc0ee49c72161ce73d1d66921`  
		Last Modified: Thu, 18 Jul 2024 19:09:01 GMT  
		Size: 39.2 KB (39191 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:23a642538c22a4e2e9e52d3a4d2a2dc78360f5e35bdeb327da51871114fd4d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.1 MB (440058175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2135960a2909c6adbbbb1720c9349d9cdf190a313c036cec8d47232cfa9cd004`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.7
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7 LIBERTY_SHA=c5a156435340ad754d03375f0ac070dbadb67381 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.7/openliberty-runtime-24.0.0.7.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac3110a5d1eebf9525a140f60c8dbde0133312ec7905bb4cff8ce58bfde450`  
		Last Modified: Tue, 02 Jul 2024 05:55:15 GMT  
		Size: 12.2 MB (12203618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e11ea54c841db42ae4badc68f09af8c9347a3955ada02fe2ae509a1d6d83b7c`  
		Last Modified: Wed, 17 Jul 2024 18:00:34 GMT  
		Size: 50.2 MB (50232659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e094e71b536577f00e09165d828d8ce67687e7023465c58fb1a686e2a1a30b`  
		Last Modified: Wed, 17 Jul 2024 18:00:33 GMT  
		Size: 4.3 MB (4329569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6b4f3895b07fe3bf149e34ed79e4edf6d311e3d144c6dce05f08df0a72679d`  
		Last Modified: Wed, 17 Jul 2024 18:52:44 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29fbdcb80a89fa10eda85bdc067e55d03082f570af71a62b7b43db5b914ba77`  
		Last Modified: Wed, 17 Jul 2024 18:52:44 GMT  
		Size: 10.0 KB (9988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bbbf6747336d93bb5dd5adeca3f5fd317f9ace2bbeb8a14ca414a3813a83e6`  
		Last Modified: Wed, 17 Jul 2024 18:52:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4952804aa4e3a8abfdc6bc0e340e598273f512930a8765b75e1285b7e87112a7`  
		Last Modified: Thu, 18 Jul 2024 19:06:11 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b004f5cfa3d819709e434b4f8c310f2771e6a37ba42f1f7bbdef74dd4aba28`  
		Last Modified: Thu, 18 Jul 2024 19:06:18 GMT  
		Size: 331.8 MB (331844555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7e5a2465608f192af6d3298ba3751f05eac4f9072bcb307ed56e6c307ead8`  
		Last Modified: Thu, 18 Jul 2024 19:06:11 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf58483bc19afbb6328666d5a1e34a96dc860b902b04928b3863e642ad8f58b`  
		Last Modified: Thu, 18 Jul 2024 19:06:11 GMT  
		Size: 11.3 KB (11348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76043de2f9d7849ec887cd2c42cf06a2b19917b508efe41c1e4782ba7163be40`  
		Last Modified: Thu, 18 Jul 2024 19:06:12 GMT  
		Size: 13.4 MB (13390435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:38bd1e37940c78225637e506abdfe0cf5dac71ab99d4ff997d5ade18aa7af730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad7ba727a96c1a6e728f70be3fadcde6cc23ef367a5662d6220796f22a6ec1e`

```dockerfile
```

-	Layers:
	-	`sha256:b108dc10cdb005040c5f4a9e2cce8762cc883c7d0312813120c450081f723646`  
		Last Modified: Thu, 18 Jul 2024 19:06:11 GMT  
		Size: 5.3 MB (5332734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcb0deda68e04c9edc537e900bb80d9e7541d92daf1a29ae1ab74ace9b7fa099`  
		Last Modified: Thu, 18 Jul 2024 19:06:11 GMT  
		Size: 39.1 KB (39145 bytes)  
		MIME: application/vnd.in-toto+json
