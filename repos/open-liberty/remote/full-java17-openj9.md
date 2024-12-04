## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:9add3041c296f4e51b9d4e81f7205867945ec9bd952bef1e4a50d6910e8f890f
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

### `open-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:4bcc142428e1b0eb0ae787eefdb3d8c3b5c8f6b7e735f8ab00aa2e8aca53855d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.2 MB (450163977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529bc851c2965ff0b2c5ba2cc96f58fd31e7ada13714cf01d7398b71f439eec7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6414d03c2b0485d19a9eedadfa3506c7d6b3aa2fd7f92ca5cc9b0dfbf42c3`  
		Last Modified: Mon, 18 Nov 2024 21:06:16 GMT  
		Size: 12.2 MB (12175060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe6084c4786be715649408fbe05daf01251ad3ab08ebc3193d3c830d482d56b`  
		Last Modified: Mon, 18 Nov 2024 21:06:17 GMT  
		Size: 51.5 MB (51533608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f79bbc470e2639578fb88cd2c9e6f368b8c37ab13c89e06e0ba5d8d954686b`  
		Last Modified: Mon, 18 Nov 2024 21:06:16 GMT  
		Size: 5.0 MB (4965093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ae5edc2674b59c5b6f1c3e0126c805aad84d54df7481b3b0625a218fd993ac`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54b14510d9904405f65b1ac6b89e8e5a6e731afe817b0c1388e7cd113180369`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b18da83942190a9df6938e0ec34f8420202b3f32056ce92e8a6b4e20267bb1c`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d167ec56346851b66bbe21be40f9c790b090fb450ef590d80cd194d172c2eed`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddc01adfd19e28cbf94158bf57a5ba439612fca3d11c719b5fb2880e532f494`  
		Last Modified: Tue, 03 Dec 2024 22:29:58 GMT  
		Size: 337.9 MB (337911952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0a7da1cddec506c84905eb845da15d8e4a70217a64c5f7ef256a6f7b7d4c4`  
		Last Modified: Tue, 03 Dec 2024 22:29:54 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e909113ab12de113fda4b4af7a92bf77f6ed0e85cede87078ff564c40b868b2c`  
		Last Modified: Tue, 03 Dec 2024 22:29:54 GMT  
		Size: 11.3 KB (11336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554e247bafa6a00230b97a27ac0cd21b5140cae777a9b7708273c923219cc61f`  
		Last Modified: Tue, 03 Dec 2024 22:29:54 GMT  
		Size: 14.0 MB (13987161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ccf0c18bc2c998b833e1c7c9075e1fc96d5ef1f9b4adc9a1edf696d0187f25e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5659474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8b0c7678adacd5c01d03690f54a7bc9a7b696d2b2bbce66e9458a20974f74`

```dockerfile
```

-	Layers:
	-	`sha256:37774b011183e2a4b52aa2b7909ba8d9d2507fa809f5f0b1a112c01f4eb75dc3`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 5.6 MB (5620881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78c4c08ef1c1f74f02691c21a5e0d92be82bdf59b43d778649881bc6cb61f1a`  
		Last Modified: Tue, 03 Dec 2024 22:29:53 GMT  
		Size: 38.6 KB (38593 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:5df8746db2a49bfdb8c27c494b84c31cec9a0149f63ea196093d0cf200a874ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.3 MB (441270324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804ab41226e5184047a47f5300f3226e6ebde5842656b82cc82657e738a42e84`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
USER root
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:56:24 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:56:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.11
# Wed, 06 Nov 2024 14:56:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.11 LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.11 LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.11 LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.11 LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.11 LIBERTY_SHA=0b8185bd6809625b09a5a7516d9ef8bf1b70bba8 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.11/openliberty-runtime-24.0.0.11.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:56:24 GMT
USER 1001
# Wed, 06 Nov 2024 14:56:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:56:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:56:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Last Modified: Mon, 18 Nov 2024 19:12:40 GMT  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf2d4b2e2296540c2e5d354b52aeaddcb98a98da98203357f0e3a1528ad0ab7`  
		Last Modified: Mon, 18 Nov 2024 19:24:53 GMT  
		Size: 47.6 MB (47553927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823a239827a007e8948393395137942949dc3dcd27f4476004f4179771e99a8`  
		Last Modified: Mon, 18 Nov 2024 19:24:51 GMT  
		Size: 4.6 MB (4641171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8616a41d05111eadca191e5f691147b241a25cd3efafa26befae3854ffa9c230`  
		Last Modified: Mon, 18 Nov 2024 20:52:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd773092412366f680a27615cc328ee6586c2a4dc0ce92cc328085c8b5bfd467`  
		Last Modified: Mon, 18 Nov 2024 20:52:39 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927715588f8534e278a740511a5c10d155d3397cb6345995624d88af7cb5a8fb`  
		Last Modified: Mon, 18 Nov 2024 20:52:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833dad26b2e80e7c69a3debef1a15df74f8ed4ce599890a76cefcefd619805b1`  
		Last Modified: Mon, 18 Nov 2024 20:59:49 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670d4c233660522dd73c2b4a962fdd3d6df011458963a6168efdfeb84c652398`  
		Last Modified: Mon, 18 Nov 2024 20:59:56 GMT  
		Size: 336.4 MB (336377919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6ad69c951929e62028bc0440b577571ce7cb267f6b1068bee04bfef8834c14`  
		Last Modified: Mon, 18 Nov 2024 20:59:49 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eddadebaa88032f57eb0afa0356590d99910ba6b6dfdbe376f52b5cb394e53e`  
		Last Modified: Mon, 18 Nov 2024 20:59:49 GMT  
		Size: 11.3 KB (11339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec40e9729aa98a741b7ee06d5c8551c3a14332c7889eb428df829ae6eed5659`  
		Last Modified: Mon, 18 Nov 2024 20:59:51 GMT  
		Size: 13.1 MB (13144746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:c55c1b40fd5d32ee150d0bcd3b816b2b0ed73655d40547d53d59303d9b8cdc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d89a9cb7411be40a10d52e14d66c6741a7cff01e7ea502fe41d4b1dda96fb6`

```dockerfile
```

-	Layers:
	-	`sha256:91c328145b5f5d218dc8ec959b8879f758d93a77381e831c0e06ba0ea85790ca`  
		Last Modified: Mon, 18 Nov 2024 20:59:49 GMT  
		Size: 5.6 MB (5600620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4c0614cede250879714c2a367638e808ba79b5f69465e6fefb1677053c3ce0a`  
		Last Modified: Mon, 18 Nov 2024 20:59:49 GMT  
		Size: 38.7 KB (38721 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:790ce413e65f6c76ae6749bf055d887d81b521c48ffad1864ccb5b235119f557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.7 MB (453745291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5224af7a8e4e2fb2adc946edd2b9a57b6ed49369c3fbce5aa5d0f2006c0f1db0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b633c72eef8784ea9595d670ce842eeba8e5553d35ca87ad4c67cca8990160`  
		Last Modified: Mon, 18 Nov 2024 19:24:15 GMT  
		Size: 52.7 MB (52701675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b9e795bb832eab2d94d4c368e3ab9ab8b88498a0f8103594d5bc5cdc57f353`  
		Last Modified: Mon, 18 Nov 2024 19:24:12 GMT  
		Size: 3.8 MB (3787364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd1534ff72cad55ff8c24c37db52b81e39975d85cf1152f947be22e0180aed1`  
		Last Modified: Tue, 19 Nov 2024 00:18:38 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c63a6dab48d7e3ec1f261111c9b84cfe8bda729a5ab85195b50344a4ac4d436`  
		Last Modified: Tue, 19 Nov 2024 00:18:38 GMT  
		Size: 10.0 KB (9988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c810b3d9648177cfbbcf53c5e6697169a72488c3bb9aaced938276100a4b1d3`  
		Last Modified: Tue, 19 Nov 2024 00:18:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc795b8680eefe0b6b2c7d1d5592399c6a880033042cba387697bf8b7b45366`  
		Last Modified: Wed, 04 Dec 2024 00:03:03 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d3f84aab394d2dd4aa479e0b450f198fe904a8d9f3172e399b483f36928fb`  
		Last Modified: Wed, 04 Dec 2024 00:03:12 GMT  
		Size: 337.9 MB (337912786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3c16978a1a61a0be9e77df26763ba5daa2cf5c162006201abd899e2f6e6b78`  
		Last Modified: Wed, 04 Dec 2024 00:03:03 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b137342da45be58a70f48773c539d100928111e26e4bd0b980020a9d3a5ee11`  
		Last Modified: Wed, 04 Dec 2024 00:03:03 GMT  
		Size: 11.4 KB (11371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0f31621f04f7acf19395f4f1d363656fa4e11a840563d9c06efac81ab648c`  
		Last Modified: Wed, 04 Dec 2024 00:03:04 GMT  
		Size: 11.9 MB (11946877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:75fa3ce984b3fde864a5a4ae7a6ab0df069f93f292aad0057786b79b7a3d1a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5656243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd2792da27858b0621455f913a4aa249798268aa5a6dba23931190c0a3a8489`

```dockerfile
```

-	Layers:
	-	`sha256:b0a73f45c2520f769fda1bdb149133d695d0e5e59951505527f73e38cb078a78`  
		Last Modified: Wed, 04 Dec 2024 00:03:03 GMT  
		Size: 5.6 MB (5617616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d70fcfe4808a377d68a38900e1c2843e899362b225d93f3b8b9ecea3559c41`  
		Last Modified: Wed, 04 Dec 2024 00:03:02 GMT  
		Size: 38.6 KB (38627 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:d26becbb83ac873c64bbb5b9505a079f70c5555cb8a408767373b00bec1abc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447714840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9dfc0f7d3dea305db09e915aec903c0a58c6bf424bb81534f0bc97bbefc06`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-17.0.13+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e737c9d2f4fc5a4fd5e58ec044ef9f118ffe2fbd5a7a4953fa02cd9d56b6cb47';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d3e0c4e9f612093833a7d651835d6e65c2ff0f1ed8dd7afd2f0359945ebf7d34';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0cbc8917a20d7c495d765f6986b5fe0b08133fcf48ef6b43d92b61f5c4f325d7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='a2f3588d940696ef58d3a588e6bbce940c1aa64938fabbf9a14a551a5e15385b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.13%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_17.0.13_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64585d59beb7fda1e426078a20565e947b4a08facd5634107edeb0461019cb4b`  
		Last Modified: Mon, 18 Nov 2024 19:46:16 GMT  
		Size: 50.5 MB (50482039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc680e6482e9a9e2661d44ec3829818bbd7de592549b4c5f2a01e5c3498dded`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 5.0 MB (5034579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1f3bce924b79200292950658b82a44dc35caca507efa4c6aaec07e51d320b`  
		Last Modified: Mon, 18 Nov 2024 21:51:31 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ac9a265cab209c9b46b75853776e9458ed18b0224c6c1541815a3750f4124`  
		Last Modified: Mon, 18 Nov 2024 21:51:30 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a5f7c8ee36c0189dbec936b845d5ccb93dcc1f6d9ecbe313b6ed3d91a6d005`  
		Last Modified: Mon, 18 Nov 2024 21:51:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f68da2392ae20ff1270ad20991c62f468aa2502231e3e8422b8b2ee75112a3`  
		Last Modified: Tue, 03 Dec 2024 23:02:45 GMT  
		Size: 33.1 KB (33117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f219a49946d4043d272ef9cc70525d24a4c6b729c49890b068fda5597dafe82c`  
		Last Modified: Tue, 03 Dec 2024 23:02:50 GMT  
		Size: 337.9 MB (337912467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a860d4ba74a527ea5c5d5381f709fad017729b13d8711e2edcb103648d0ce0e7`  
		Last Modified: Tue, 03 Dec 2024 23:02:45 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78009af1460e29979671b43ff36b3611a42f55a3e7b88d3bb95ad022d62a317d`  
		Last Modified: Tue, 03 Dec 2024 23:02:45 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb95a2b3a026ef7f5c758964fe07b4b0d6fe6fe303d9e29ef95aaef93b165c2`  
		Last Modified: Tue, 03 Dec 2024 23:02:47 GMT  
		Size: 14.0 MB (14023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:55577120de852cf964e00e0712d4d5abb1ba2d285a34e1ad780e5cb9c2a2aff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80802a75e5781c3a4b9f72fc57c25d3fac1ed45275e6f92c734eaf18b664e9a6`

```dockerfile
```

-	Layers:
	-	`sha256:cc7142ad8a0b79a40276011b8b658a99ca92e54a01bc3b40d87a667432d978f7`  
		Last Modified: Tue, 03 Dec 2024 23:02:45 GMT  
		Size: 5.6 MB (5614164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d5f3498c20d0a5558e18e57210defe7caeab5cdde9576f38b46d2c0203b77c`  
		Last Modified: Tue, 03 Dec 2024 23:02:45 GMT  
		Size: 38.6 KB (38593 bytes)  
		MIME: application/vnd.in-toto+json
