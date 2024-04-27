## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:c35273c6f91d9332608a18c7960e2a233e54ef058bf04e0bf85edb884418a0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:afca22b8493ba96adfa6f7cd53549decb56a8f5a77759ee136be96146afc8a99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482187949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd18675ba52d01fce3b7e74dac21257790d0da193edeb72e3f72015b2c3bcd97`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:01:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 05:01:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:04:48 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Tue, 16 Apr 2024 05:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 05:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 05:06:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 05:06:57 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 12:41:27 GMT
USER root
# Tue, 16 Apr 2024 12:57:57 GMT
ARG VERBOSE=false
# Tue, 16 Apr 2024 12:57:57 GMT
ARG OPENJ9_SCC=true
# Sat, 27 Apr 2024 01:17:41 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Sat, 27 Apr 2024 01:17:41 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Sat, 27 Apr 2024 01:17:42 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Sat, 27 Apr 2024 01:17:42 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 27 Apr 2024 01:17:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 27 Apr 2024 01:17:42 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Sat, 27 Apr 2024 01:17:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 27 Apr 2024 01:17:43 GMT
ARG LIBERTY_URL
# Sat, 27 Apr 2024 01:17:43 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 27 Apr 2024 01:17:51 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Apr 2024 01:17:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 27 Apr 2024 01:17:52 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 27 Apr 2024 01:17:52 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 27 Apr 2024 01:17:52 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Sat, 27 Apr 2024 01:17:53 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 27 Apr 2024 01:17:53 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 27 Apr 2024 01:17:59 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 27 Apr 2024 01:17:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 27 Apr 2024 01:17:59 GMT
USER 1001
# Sat, 27 Apr 2024 01:17:59 GMT
EXPOSE 9080 9443
# Sat, 27 Apr 2024 01:18:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 27 Apr 2024 01:18:00 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 27 Apr 2024 01:26:24 GMT
ARG VERBOSE=false
# Sat, 27 Apr 2024 01:26:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 27 Apr 2024 01:33:34 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Sat, 27 Apr 2024 01:33:35 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 27 Apr 2024 01:34:13 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7174e6ca1f346329bcdcb2b0c9e4a5deec1e5e895ae1fc065cef54ef5b38ef80`  
		Last Modified: Tue, 16 Apr 2024 05:14:19 GMT  
		Size: 12.2 MB (12156612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7813e670f47517ef41da687dbdf2833e6e736e2a0b292007ebbfe6afa050b369`  
		Last Modified: Tue, 16 Apr 2024 05:16:15 GMT  
		Size: 49.0 MB (49000326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af15d098fa45359b70ffeaaffbde76c9bdf740abb49eba0298b5b15d65a6a61`  
		Last Modified: Tue, 16 Apr 2024 05:16:09 GMT  
		Size: 4.3 MB (4340244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e74f1413271f582fcda6db93383f5dfd349d31f4ed7c9ca9b1cec5abbb292a6`  
		Last Modified: Sat, 27 Apr 2024 02:31:08 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb15e12598f42d54ef4d7f08fcf8641e0742bdf00c31345aea282a92c2a7f1d6`  
		Last Modified: Sat, 27 Apr 2024 02:31:10 GMT  
		Size: 17.5 MB (17463830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb20b8183e0e4b9800ae16373a6d325913dab2b5f33d1e6f24c9ec4e56032795`  
		Last Modified: Sat, 27 Apr 2024 02:31:08 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1eb321d61aa8e900f926a0649b95fc8006b622875f79de1ef557db9fed418b`  
		Last Modified: Sat, 27 Apr 2024 02:31:06 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e72d87ac85271ccacc1b53efd6fd579e8c5c5f274ec6cb3ba0c3ce9c51aecd5`  
		Last Modified: Sat, 27 Apr 2024 02:31:06 GMT  
		Size: 11.9 KB (11867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f20cbffb514226e342e201cc68636a668fc2b43555c2e099fd511122c319e7a`  
		Last Modified: Sat, 27 Apr 2024 02:31:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e259117ef4d6d37d0b2d56b0c6905a542fc0672aa178535a72f704d9d99c295`  
		Last Modified: Sat, 27 Apr 2024 02:31:06 GMT  
		Size: 12.8 KB (12792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9d05e3a8e323b61d7aaec4d6e1791b3d0d6dcc7ff54dfbe7da0be04a9b048d`  
		Last Modified: Sat, 27 Apr 2024 02:31:07 GMT  
		Size: 2.7 MB (2720459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5fe2d8c8f1fc505aeb0ecb03ee919c3b3c6cf94aea9c6b6cc0897c437173c1`  
		Last Modified: Sat, 27 Apr 2024 02:32:09 GMT  
		Size: 349.9 MB (349855054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b34ed562bebb51d6ab09be18de4caa5a04fb43745b6e81755b4edc8401b0f11`  
		Last Modified: Sat, 27 Apr 2024 02:31:53 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edd8f83c1dcfd618cf698f7431079232f31fe373d7157b83299d5172709cf0c`  
		Last Modified: Sat, 27 Apr 2024 02:31:58 GMT  
		Size: 16.2 MB (16151901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:e3e35e96fadfcb18902209b8107c978ff767efe102569575fbfee4d63348ff4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.9 MB (475879922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66dcdab0083053698d8a752a87aab424729d31fb3491d2680f02969cf159e07`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:01:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 03:02:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:05:13 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Tue, 16 Apr 2024 03:06:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 03:06:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 03:06:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 03:07:19 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 08:49:59 GMT
USER root
# Tue, 16 Apr 2024 09:04:00 GMT
ARG VERBOSE=false
# Tue, 16 Apr 2024 09:04:00 GMT
ARG OPENJ9_SCC=true
# Tue, 16 Apr 2024 09:04:01 GMT
ARG LIBERTY_VERSION=24.0.0.3
# Tue, 16 Apr 2024 09:04:01 GMT
ARG LIBERTY_BUILD_LABEL=cl240320240311-1901
# Tue, 16 Apr 2024 09:04:01 GMT
ARG LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071
# Tue, 16 Apr 2024 09:04:01 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.3 org.opencontainers.image.revision=cl240320240311-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 16 Apr 2024 09:04:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 16 Apr 2024 09:04:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.3 BuildLabel=cl240320240311-1901
# Tue, 16 Apr 2024 09:04:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Tue, 16 Apr 2024 09:04:02 GMT
ARG LIBERTY_URL
# Tue, 16 Apr 2024 09:04:02 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 16 Apr 2024 09:04:15 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 09:04:15 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 16 Apr 2024 09:04:15 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Tue, 16 Apr 2024 09:04:16 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Tue, 16 Apr 2024 09:04:16 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Tue, 16 Apr 2024 09:04:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 16 Apr 2024 09:04:16 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 16 Apr 2024 09:04:21 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 16 Apr 2024 09:04:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 16 Apr 2024 09:04:21 GMT
USER 1001
# Tue, 16 Apr 2024 09:04:21 GMT
EXPOSE 9080 9443
# Tue, 16 Apr 2024 09:04:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 16 Apr 2024 09:04:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 16 Apr 2024 09:04:48 GMT
ARG VERBOSE=false
# Tue, 16 Apr 2024 09:04:48 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 16 Apr 2024 09:14:35 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Tue, 16 Apr 2024 09:14:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 16 Apr 2024 09:15:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf623939c01b82bafd9b4d9e769ce2119ef976cbd0968b69dfb1bd1590dbe55`  
		Last Modified: Tue, 16 Apr 2024 03:14:17 GMT  
		Size: 12.1 MB (12115565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393a382e7eb48a6fb1989d4cc8bc37feaabb7f42af7a4135176b216940bc23b5`  
		Last Modified: Tue, 16 Apr 2024 03:15:57 GMT  
		Size: 48.2 MB (48208805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810f030c8d58517b128d82d99c80f620779cd8e5d105f142c76151b5ce867bf6`  
		Last Modified: Tue, 16 Apr 2024 03:15:53 GMT  
		Size: 4.1 MB (4143079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c9318021b39b15ef48ba0ae41fd93b6094068c6523ac59f2a24ea9d3407455`  
		Last Modified: Tue, 16 Apr 2024 09:46:56 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b134b8465eb54145670220815c8ff249e7a5c16acd3c86ba1f2cff626a7309f8`  
		Last Modified: Tue, 16 Apr 2024 09:46:57 GMT  
		Size: 17.1 MB (17129426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6574ab4854535e2165267ddece89f9b3fb0d04e0376523e74f5d0d272ee42a`  
		Last Modified: Tue, 16 Apr 2024 09:46:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556ca2a230829b01e057c195150a96724534e3b5e63a120af25f2b69b8aa92c`  
		Last Modified: Tue, 16 Apr 2024 09:46:53 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac514ad5f71ef09e384e62ffaf6355d2a07bb5602f2d2fc1f7c60d74eba38d08`  
		Last Modified: Tue, 16 Apr 2024 09:46:53 GMT  
		Size: 11.7 KB (11729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e881404c3535063f358a692bb353e1ffb15b75c809712e36d5e0cf6b1f7360`  
		Last Modified: Tue, 16 Apr 2024 09:46:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359410abe30f01286cfd8096f68f9a28bbeaeb2fee960768cd80f804250a2509`  
		Last Modified: Tue, 16 Apr 2024 09:46:53 GMT  
		Size: 12.6 KB (12646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb3972feb5b9684152a7a136d99e472043823e74e0b19a59b4e09569249f340`  
		Last Modified: Tue, 16 Apr 2024 09:46:54 GMT  
		Size: 2.8 MB (2751181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32979c431125ed8ae915a41cff2c8184aa89c08f84bc78f3965d5d5dd60c37f`  
		Last Modified: Tue, 16 Apr 2024 09:47:25 GMT  
		Size: 349.6 MB (349589385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb64e92b860f3487f247c046ff6211c4699169aa75f06c2515521a1e28b8ffa5`  
		Last Modified: Tue, 16 Apr 2024 09:47:12 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5d4ebc4ed62485f17a19c0ae715fc867e66152b11b82f5263395dd1340f6e7`  
		Last Modified: Tue, 16 Apr 2024 09:47:13 GMT  
		Size: 13.5 MB (13472147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:9fdadbea139d5087cd1a370b24ccce3d3ebae0e637c6a2b890009ccd416cce59
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.9 MB (485889227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d67d8ea17c2649eb5c56375b764ab1891f481cd3d2a69db2d4e22bd2db03068`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:45:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 03:46:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:51:01 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Tue, 16 Apr 2024 03:53:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 03:53:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 03:53:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 03:53:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 07:09:57 GMT
USER root
# Tue, 16 Apr 2024 07:09:58 GMT
ARG VERBOSE=false
# Tue, 16 Apr 2024 07:09:59 GMT
ARG OPENJ9_SCC=true
# Sat, 27 Apr 2024 02:14:11 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Sat, 27 Apr 2024 02:14:12 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Sat, 27 Apr 2024 02:14:13 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Sat, 27 Apr 2024 02:14:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 27 Apr 2024 02:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 27 Apr 2024 02:14:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Sat, 27 Apr 2024 02:14:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 27 Apr 2024 02:14:21 GMT
ARG LIBERTY_URL
# Sat, 27 Apr 2024 02:14:21 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 27 Apr 2024 02:14:43 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Apr 2024 02:14:45 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 27 Apr 2024 02:14:49 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 27 Apr 2024 02:14:49 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 27 Apr 2024 02:14:50 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Sat, 27 Apr 2024 02:14:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 27 Apr 2024 02:14:57 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 27 Apr 2024 02:15:09 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 27 Apr 2024 02:15:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 27 Apr 2024 02:15:12 GMT
USER 1001
# Sat, 27 Apr 2024 02:15:14 GMT
EXPOSE 9080 9443
# Sat, 27 Apr 2024 02:15:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 27 Apr 2024 02:15:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 27 Apr 2024 02:25:42 GMT
ARG VERBOSE=false
# Sat, 27 Apr 2024 02:25:43 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 27 Apr 2024 02:34:11 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Sat, 27 Apr 2024 02:34:20 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 27 Apr 2024 02:35:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8539c6f8a1607ac59b46c0a3f097a0d7a8e240093007cf5df2caee4abe59a476`  
		Last Modified: Tue, 16 Apr 2024 04:02:51 GMT  
		Size: 12.9 MB (12890585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9079aa02097185399bcd3d3b2e19397459eb89ff90419a829a2b47d88acbab6d`  
		Last Modified: Tue, 16 Apr 2024 04:05:00 GMT  
		Size: 50.6 MB (50565687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2961a01cb165ab99e2ac7dfb34dc620af7ed008b923e302807f5ed76f58dea65`  
		Last Modified: Tue, 16 Apr 2024 04:04:53 GMT  
		Size: 3.4 MB (3391982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120e5d193c249ace94de112cf61237bf9c2dcddba17f9a838cf8fd9c18ffc0fb`  
		Last Modified: Sat, 27 Apr 2024 03:49:09 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04652ded39ce972870c7fc9ca4cf02517195e32b3e168f25843695ede9d76403`  
		Last Modified: Sat, 27 Apr 2024 03:49:10 GMT  
		Size: 17.5 MB (17464735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92a8139fbc959436f448134bc5342ba06e46d0cf9b505ddbcac6cec55cec6ff`  
		Last Modified: Sat, 27 Apr 2024 03:49:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ba3e3215ef29a9d0a45a7b12209d39ed796e46d9913624898c9a7a898ac2df`  
		Last Modified: Sat, 27 Apr 2024 03:49:06 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a37ae6ad8edc8a22ad3040a824f3e647c4d4df76d10c8c25f180833293ab1e`  
		Last Modified: Sat, 27 Apr 2024 03:49:06 GMT  
		Size: 11.9 KB (11862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d5c58ede383ef8c29a98897f1161c3f05fb84a9fed2193645f6d6b99d0a655`  
		Last Modified: Sat, 27 Apr 2024 03:49:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc8bcdf9c696661017f4165d1610d367ead15db791de0d5c01d373625a3d644`  
		Last Modified: Sat, 27 Apr 2024 03:49:06 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79245a228fddd6bf2ff97c49ac1a3a413b4130f0e898a22d1912f49a88476c6e`  
		Last Modified: Sat, 27 Apr 2024 03:49:07 GMT  
		Size: 2.6 MB (2639036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8476713e8c5e604ac7dde7279b1221ca401aecf3d0c40867e6878b26838256`  
		Last Modified: Sat, 27 Apr 2024 03:50:18 GMT  
		Size: 349.9 MB (349856775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad6d481473cab1cb8f9d247bc0de042008bdfc397755105a3ce539a011d9325`  
		Last Modified: Sat, 27 Apr 2024 03:50:00 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b1096a14e769286252ad842a8c7dddf2c73799911234eefb20113e8d25de7`  
		Last Modified: Sat, 27 Apr 2024 03:50:02 GMT  
		Size: 13.4 MB (13428678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:b7965ba3e6837e7e60af8977ebdf44e4e4291c37aa204ea0013e135776662642
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.3 MB (479349041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0729595850039222e44c51425e6b05db8b707a94d9234e037b3560b66f156d53`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 01:55:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:02:18 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Tue, 16 Apr 2024 02:04:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 02:04:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 02:04:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 02:05:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 03:16:46 GMT
USER root
# Tue, 16 Apr 2024 03:16:47 GMT
ARG VERBOSE=false
# Tue, 16 Apr 2024 03:16:47 GMT
ARG OPENJ9_SCC=true
# Sat, 27 Apr 2024 00:49:21 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Sat, 27 Apr 2024 00:49:21 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Sat, 27 Apr 2024 00:49:21 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Sat, 27 Apr 2024 00:49:22 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 27 Apr 2024 00:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 27 Apr 2024 00:49:22 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Sat, 27 Apr 2024 00:49:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 27 Apr 2024 00:49:23 GMT
ARG LIBERTY_URL
# Sat, 27 Apr 2024 00:49:23 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 27 Apr 2024 00:49:29 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Apr 2024 00:49:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 27 Apr 2024 00:49:31 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 27 Apr 2024 00:49:31 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 27 Apr 2024 00:49:31 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Sat, 27 Apr 2024 00:49:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 27 Apr 2024 00:49:31 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 27 Apr 2024 00:49:36 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 27 Apr 2024 00:49:36 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 27 Apr 2024 00:49:37 GMT
USER 1001
# Sat, 27 Apr 2024 00:49:37 GMT
EXPOSE 9080 9443
# Sat, 27 Apr 2024 00:49:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 27 Apr 2024 00:49:37 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 27 Apr 2024 00:58:10 GMT
ARG VERBOSE=false
# Sat, 27 Apr 2024 00:58:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 27 Apr 2024 01:05:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Sat, 27 Apr 2024 01:05:38 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 27 Apr 2024 01:06:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:800aa7ed945a05dec0024b71aaef6a3ed35eb8fc8eef0982ff134513d2295713`  
		Last Modified: Tue, 16 Apr 2024 01:37:03 GMT  
		Size: 28.6 MB (28637157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c848c934aa4ef4451fd4c7c2a114e25882400ab8f06c52583083702c9b804a`  
		Last Modified: Tue, 16 Apr 2024 02:14:32 GMT  
		Size: 12.2 MB (12204328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbde1ccf04f4a478054de97fc3f3cdbdd4c92c7af6583e54e3cccf106fcb0d6`  
		Last Modified: Tue, 16 Apr 2024 02:16:12 GMT  
		Size: 48.3 MB (48268520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9a5587e1838b5dd59296b51a6bc970a6387caa14a0a42c45e09ed45157f62e`  
		Last Modified: Tue, 16 Apr 2024 02:16:05 GMT  
		Size: 4.5 MB (4485704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd66029ea8ebcda97752f572261a745ac2f14f8eb401726aa4f2dcc3adacd970`  
		Last Modified: Sat, 27 Apr 2024 02:05:44 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8b7f0fdc930639e3232e2c9b60cdbf97c0797a326d025436ef403b41260eaa`  
		Last Modified: Sat, 27 Apr 2024 02:05:46 GMT  
		Size: 17.5 MB (17464159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bccf3fbe1d2fe56a4ce25656dd28e1ba4d32119a518390f9c15b186b092e5b`  
		Last Modified: Sat, 27 Apr 2024 02:05:44 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de52f70d15818cfdb850629c210b4aad803996f77e15534330e837d1cbcfb6`  
		Last Modified: Sat, 27 Apr 2024 02:05:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c542afdf0e5ada64b69588f0ad000eab349a66988407ef9726b36699623438`  
		Last Modified: Sat, 27 Apr 2024 02:05:42 GMT  
		Size: 11.9 KB (11865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b042c1a9de6de100755943b38a54beba2c7f067405bb83c16dbc6b5911cb7a3`  
		Last Modified: Sat, 27 Apr 2024 02:05:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4865315eee50c2260db679a95ca8e0bb1cc7595c935f232257a37d5a17f352aa`  
		Last Modified: Sat, 27 Apr 2024 02:05:43 GMT  
		Size: 12.8 KB (12783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e327cad86beaa4543ce7f893f7d2e8347a87cdd56c544cfbed5e257aa478`  
		Last Modified: Sat, 27 Apr 2024 02:05:43 GMT  
		Size: 2.7 MB (2732981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173abf67562a2f1b570dd117a7e7c685cfc0dd6a2ad053456980b6ddec922d3d`  
		Last Modified: Sat, 27 Apr 2024 02:06:46 GMT  
		Size: 349.9 MB (349854578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedbb8a05dfa211d16fd42e1cb826cf9010b837c7c9eb1543b5076e4dceaeb92`  
		Last Modified: Sat, 27 Apr 2024 02:06:30 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fa1757b899dfbec22f7a99005fd86a61cd717b77cfdb7fc7547b8380a87a91`  
		Last Modified: Sat, 27 Apr 2024 02:06:33 GMT  
		Size: 15.6 MB (15640513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
