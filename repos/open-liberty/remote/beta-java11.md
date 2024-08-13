## `open-liberty:beta-java11`

```console
$ docker pull open-liberty@sha256:9206196e521a4b7a5f279443ee546940c4e332060b3bb0e62dcec304c3354048
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

### `open-liberty:beta-java11` - linux; amd64

```console
$ docker pull open-liberty@sha256:874bda50e3e0441443d118fa93469026bfd9be5d562e3e00265cb0ca22449a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.6 MB (470612916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e17fcaf53f6530de795460acc8bfef1a0bc9285bc87ab75def768de2be730a`
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
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:49cee9ca828c62e3afeadc410eca3d4ee8a25f3416df0c510f36cb80f525da60`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 12.2 MB (12156467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2282879d248ee453bdd65051fdd90db8a305ddd2baefddca877e3b0cd1dee`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 52.0 MB (52021125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729a8573c77e572e08acc3dae0395893965a3bc53024b11674b5a1694e77b512`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 4.5 MB (4507421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7920eddca53776f37226495e7d1b938aa2f149b1a46fa6725038ef7262e0d704`  
		Last Modified: Mon, 12 Aug 2024 18:53:37 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b01fd321f312d6ee9df1afe8da4080cb56632be4ea3dce6f18e64a797bee5`  
		Last Modified: Mon, 12 Aug 2024 18:54:34 GMT  
		Size: 10.0 KB (9988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f463c0472adef542dc0de77b8d5081ad7cd9776247f5d251623ad6e1119ae654`  
		Last Modified: Mon, 12 Aug 2024 18:54:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f8ae53a9413354a3601e4f1fb8cdac83053bc8941461fa0dc42656d9e9ef57`  
		Last Modified: Mon, 12 Aug 2024 18:53:37 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df17540d2e32a1a5d5d17660fa07b8490c895ee2ee7e6dfe2ff1ce3f9916c634`  
		Last Modified: Mon, 12 Aug 2024 18:54:39 GMT  
		Size: 358.5 MB (358519343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a57139958eaaa665bc018e72965341d5259e42b4ba758a0f4f358aa6899e104`  
		Last Modified: Mon, 12 Aug 2024 18:54:34 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92abfe642f0f24bab120b4b9f8f2d1e4a5eb8923f337a428eaf57656918fa1e0`  
		Last Modified: Mon, 12 Aug 2024 18:54:35 GMT  
		Size: 11.3 KB (11342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073498e75d53e4cc9a24336c133b04c01178a2f27cc0bc0582c3352c01f8183`  
		Last Modified: Mon, 12 Aug 2024 18:54:36 GMT  
		Size: 13.8 MB (13819081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:d142bc99bf6310aa6dae7fafce2b29c6212fe51db3a3b70fc53dd7bfe8907085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bed3bee7b12dec2e7d621cf770751b4928cf95c005503095e174eb21ec30798`

```dockerfile
```

-	Layers:
	-	`sha256:36f7ecdab886f05bf8d7af9ae2ed9f0cc9f4ce19465782c255d3b140ecdd0a04`  
		Last Modified: Mon, 12 Aug 2024 18:54:34 GMT  
		Size: 5.4 MB (5405081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f6dc4c8f13d1452be677fe83007e783c2cfb7731114c8c6dfc3785b3ff9d69`  
		Last Modified: Mon, 12 Aug 2024 18:54:34 GMT  
		Size: 38.7 KB (38661 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:e3bd7785cf6bf5afc4d948c0a63cdcefdabfcc388e3738442e410ea19367827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.7 MB (463684179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62fa2a15d91f0e13f3594727d7818d6849bb727d83adfcbdd72bd0bf99465c5`
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
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:d3bd8d80133d843daaa8d5b12adef4a1bb1a9950ef8a5bb999ca2111d459a677`  
		Last Modified: Mon, 12 Aug 2024 18:01:16 GMT  
		Size: 12.1 MB (12114290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de547aafba9c0ebaeb699f9834b505ee1942efb7a0425efb3633823b6d65449`  
		Last Modified: Mon, 12 Aug 2024 18:07:58 GMT  
		Size: 48.4 MB (48416900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975f03e91d05f2030af20e5cdc9359b5e61a8cf8e5f2380dbef11b104ce5b34`  
		Last Modified: Mon, 12 Aug 2024 18:07:57 GMT  
		Size: 4.2 MB (4182784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8d125eb489835e3d701edf429568b84b9b48e690910679461c99a48c105b0`  
		Last Modified: Mon, 12 Aug 2024 18:58:38 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a48b0d8f22762a7cb1c6ac0137d3a4d46e8e8b8ac5b6060f3a2822a4fef24e`  
		Last Modified: Mon, 12 Aug 2024 18:58:38 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae646cfa6d8e858b667e03c8a27c23f64fd604660762a2fdb8cdaca72a56900f`  
		Last Modified: Mon, 12 Aug 2024 18:58:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a305c6e6353e24985907ee2203d12f8287e74d850785f2cc298f525286749d`  
		Last Modified: Mon, 12 Aug 2024 18:58:39 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65b798ac77ef2a30b32455e40502173c3101a9fd7cb76fc83711e2ccea96d44`  
		Last Modified: Mon, 12 Aug 2024 18:58:47 GMT  
		Size: 358.5 MB (358519751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84268a6cdac083f3998993170762d978acd1faad2b4add1cf1dacdbd78992f1b`  
		Last Modified: Mon, 12 Aug 2024 18:58:39 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d92aaedc0d870c20aaf0983808d1e952ca71178012960b347106d9017cc969`  
		Last Modified: Mon, 12 Aug 2024 18:58:40 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b58560c524c00c9f45f6393b853165b45da479261459870ad2f431e2f3363`  
		Last Modified: Mon, 12 Aug 2024 18:58:41 GMT  
		Size: 13.0 MB (13024437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:17c2ffaabedcd77ce20c44ae15d191f6282be2fdd9f3c1ed822fce9534cf46e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa25eba749f1398f7157d9672ac00f5619b4b07d6f338a0a991ee5098e510c5`

```dockerfile
```

-	Layers:
	-	`sha256:1163becd7370a8749b7e1137c50656d352f25975ecafc4211170e469e5014b29`  
		Last Modified: Mon, 12 Aug 2024 18:58:39 GMT  
		Size: 5.4 MB (5405334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbad509e76d22f10fafde6059c68bc1aa73a3a407a73f7e445326b2df21fd2c8`  
		Last Modified: Mon, 12 Aug 2024 18:58:39 GMT  
		Size: 39.0 KB (39008 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:3057670bacbd36f6b255c556705b1ec12fe01e0c38ad5cc8a694fbf241aeecd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.9 MB (474865114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33053b89bd3cb3bbcfce5d22072d603c605eea4b3ee0c1ca09bc439424ddb54`
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
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:346f6b0caf9e82f11ff311008151b002cbef7156dabe22bc30c0b0bfab72dcb3`  
		Last Modified: Mon, 12 Aug 2024 18:04:26 GMT  
		Size: 12.9 MB (12888358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec4eda6def70bca9707b23eedbdda98db9884338cfae00a92951b9112339e1`  
		Last Modified: Mon, 12 Aug 2024 18:13:48 GMT  
		Size: 53.6 MB (53619797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ea3052422fe08d790d1a5ad21ae80758109b738125570ce3b2e621968cae2`  
		Last Modified: Mon, 12 Aug 2024 18:13:46 GMT  
		Size: 3.4 MB (3436299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc064c33f863941832caa349dd36a2c7e56905503b98450118ebd6925cbe61fb`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67064cae38eab1aefccba09cf2407774c27b42544242ce4f6ec3ebf42e667cd0`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cde2eb16cdbbb444c10118e46019ddb535c257c47801cb5cdbceffeb7746b58`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d20b0f81e14bbf4b4ba8619898d01acd3c3e66bb618adab46e2cd0487a57b4`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b118bd678da4947d70b8d0ca7cae62973a6d8eb1652f37071828488b26f8a54`  
		Last Modified: Mon, 12 Aug 2024 21:57:30 GMT  
		Size: 358.5 MB (358519944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b38e0e370eb94c7f1b2b65d2bfea47d9397b027a38b7b510715be28f962148`  
		Last Modified: Mon, 12 Aug 2024 21:57:08 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659152ec1011af085e7d74717d3a338beb336ea7888b3c79b7e671418cb852f`  
		Last Modified: Mon, 12 Aug 2024 21:57:08 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ca5581a20f28d76def0afd6746af4be23c9305b2f6cff80072dfb3a77913d`  
		Last Modified: Mon, 12 Aug 2024 21:57:09 GMT  
		Size: 11.9 MB (11879447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a138824234e3e13f88d2b1c04f602c30af24908b3a1250fb89ab3f909ff27ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6598106d7bc65e818405f0f5944f0fcffbc4928c024c19856ace0ebe064a39`

```dockerfile
```

-	Layers:
	-	`sha256:0c214b48257067faa834692770e53a11987b873a9ee9d100219e9e9ff10e2c39`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 5.4 MB (5409563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67677983258c54c2bf45e704d1337ee8224686ed341002f704ed00d067b05010`  
		Last Modified: Mon, 12 Aug 2024 21:57:07 GMT  
		Size: 38.7 KB (38695 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; s390x

```console
$ docker pull open-liberty@sha256:ff308f35b33ee6789294d394c829f689bc7dd614e9b000d8c6a8fad0b3257cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.8 MB (467764705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe8ed4a175f7bf26dbcc66c45a4facf5d352272d40e0b167c5b575fe00c1894`
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
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:928fcb5dd7fd89cdaf703469776b84f22f2a0896c6669206b1c3e5fd07dd7ccf`  
		Last Modified: Mon, 12 Aug 2024 18:02:49 GMT  
		Size: 12.2 MB (12203937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64aa1a0712885951f4c82604c80c08958bd5d549f99f99a49f950e1ce02757b`  
		Last Modified: Mon, 12 Aug 2024 18:11:39 GMT  
		Size: 50.9 MB (50892182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00674f439326ffeb6d1e650a1e87c8aaad05f74437224ac09297bcb419640d79`  
		Last Modified: Mon, 12 Aug 2024 18:11:39 GMT  
		Size: 4.6 MB (4617298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d2303e226cc0144a2f6c43dcea43568ee1c0f3239f106d9fe0b9eb8305e216`  
		Last Modified: Mon, 12 Aug 2024 18:56:45 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a5b553242722ff184e1a4dd3f60198c822a4dac4feb0190bff9e247767535a`  
		Last Modified: Mon, 12 Aug 2024 18:56:45 GMT  
		Size: 10.0 KB (9991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e93e79408284f2cb0b859f45f83ef8843baf2616b6fa3b0e7c577f7a0c6f32`  
		Last Modified: Mon, 12 Aug 2024 18:56:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b729d85e333de6363fe1b527c56e51b6707f1530a7a56c70b58811824d56da`  
		Last Modified: Mon, 12 Aug 2024 18:56:46 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29d633d039be03056f8f4c67d831f22510e7484e45e1e8c4b473c39c68193f5`  
		Last Modified: Mon, 12 Aug 2024 18:56:52 GMT  
		Size: 358.5 MB (358519565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cca03f483fa2f21ba8aecf55cbfc77811427514517e60eb691f1b389bf1cd7`  
		Last Modified: Mon, 12 Aug 2024 18:56:46 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dcb04d0c98dd28015726042708dd3ff16b2bba94e291b223715e46c41c46b5`  
		Last Modified: Mon, 12 Aug 2024 18:56:46 GMT  
		Size: 11.3 KB (11342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f66a29a009d4859b2b2c2a02255f2540a1f06285609ab25b0d8cbe6b1c99416`  
		Last Modified: Mon, 12 Aug 2024 18:56:48 GMT  
		Size: 13.5 MB (13474390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e46a7ac50b4e64b1a4895c8057498e69a90eb63397dce3b07e18c909b71255a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15806ce108cd29150bc58934b20fa5c287a72b419ab7157f86b27138b5ef8733`

```dockerfile
```

-	Layers:
	-	`sha256:3432f9ce3ad5b6be737c0961cbc75260a3f01e9695991b5e36115df591f44f74`  
		Last Modified: Mon, 12 Aug 2024 18:56:45 GMT  
		Size: 5.4 MB (5405120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994c22f09196cfa8902f96fc77437c8791ce442a9f7a8e9f1d3f9629a629db9c`  
		Last Modified: Mon, 12 Aug 2024 18:56:45 GMT  
		Size: 38.7 KB (38661 bytes)  
		MIME: application/vnd.in-toto+json
