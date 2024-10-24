## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:abf3d4c7ac98c0656fb0557cc9dedae49651b84c679c3d2df689be18d3e14a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:be64d8b2be732359d19087b5f7c8ee45164cfbe2b4d595b9a88b3055fac887a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490696265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bc025f1ca2bf158999a48d5e8c8fec5818ffe9609a393c65f01872ed614e33`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 18 Jun 2024 10:58:54 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:58:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:58:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:58:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 18 Jun 2024 10:58:54 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fecb30141570a731edee87c026461e9c712f6054de530ee056f4952fdb250d`  
		Last Modified: Thu, 24 Oct 2024 00:57:10 GMT  
		Size: 20.3 MB (20256480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b422ea96815defdbb728a2121cd21380a015dfc440ab411bf307a8e9b9c8f8`  
		Last Modified: Thu, 24 Oct 2024 00:57:11 GMT  
		Size: 145.6 MB (145607865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6ad6b0d588f93cbd34f31fc89ea6225d5532e125cc95b92f7c0340c8f995b3`  
		Last Modified: Thu, 24 Oct 2024 00:57:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3dcf3cad75ca87429190095861c1687ad2f9743dd9b98021b17b84f4dd1b1c`  
		Last Modified: Thu, 24 Oct 2024 00:57:09 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8631c78d046c898a6802c5240ed3d20ea34037622fc4d3d93d3ccf4df5abbb5`  
		Last Modified: Thu, 24 Oct 2024 01:58:18 GMT  
		Size: 10.3 MB (10298059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d7aa9a944db3d9b68c2829036eac6ca6ffd8c5a00d30b087779a902ad5054c`  
		Last Modified: Thu, 24 Oct 2024 01:58:18 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac93186f7edd416e6c3b67e84ff3472f70779f8f8532e101e72b352729f692d`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 254.4 KB (254361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de8537909152fba143eccb37f7eea75d015187df355b7b2bd7e7cc7f5d67aa`  
		Last Modified: Thu, 24 Oct 2024 02:58:40 GMT  
		Size: 286.8 MB (286763073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60325782ce3ffb57a41f72dbe4a41ca8439a3b3a27ccdc79b978805eb4bfa62b`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf62121b249e223e32cfae03f7a3a34de23135a5bd80dfd4a7adb3d2fb221ad`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43a8bf9927d744e0f7636b81dd032b2812d52d6f20e26273a3eadd73143206f`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:347c049801a99b93c49cf5ef5f4198093418fb81263e92a850ce515c90333118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89acd99ab694d3d2556190b521d91a4cfe65a3cc1c1db9cdc05758d55a40f3e9`

```dockerfile
```

-	Layers:
	-	`sha256:f297fe358dc526078f9c2c2d9bfe0f30067eddccf9485a9485f22f253423554a`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 4.7 MB (4705496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54eb1f04529e965440bfda21307c1b6788ec96e757cfc8b7bdc95b39aebd9286`  
		Last Modified: Thu, 24 Oct 2024 02:58:37 GMT  
		Size: 25.7 KB (25700 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:d58d1f4de7dbf9b68a4611f89e6c45bffc8bf14d8fda6103c698a9bb4dc2821e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.8 MB (485773086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396155c372b7831d3c8ca9c2e7b6cc104a00c24b2c95d8b03ce141c200471b1`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 18 Jun 2024 10:58:54 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:58:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:58:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:58:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 18 Jun 2024 10:58:54 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a3e66345d6c3b65770e2c550bec5d714edfbd1c008d2ea26934b922d995e1`  
		Last Modified: Thu, 24 Oct 2024 01:03:06 GMT  
		Size: 142.4 MB (142386782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dae6efc417605891adfdaabe571620be2a01c3f04ab4943fb70dc223d8cc4da`  
		Last Modified: Thu, 24 Oct 2024 01:03:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484d0449ba0f410941dbe268337659c735746bd2fad93d915ac2fcc6ec0d771`  
		Last Modified: Thu, 24 Oct 2024 01:03:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0263e7ecd632ae47edc88cff88a006ec6d2f1a518edc6e8ce723f6c462b20de`  
		Last Modified: Thu, 24 Oct 2024 03:05:37 GMT  
		Size: 10.3 MB (10297886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba45f668917aa24fc99c0373094bb830e7dc938c18eea772d6b5beba6dbe4d92`  
		Last Modified: Thu, 24 Oct 2024 03:05:36 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b5e31588b742f6ca20cfef4b57fa33e71343ad49c55df8789b7b21a384d862`  
		Last Modified: Thu, 24 Oct 2024 12:59:30 GMT  
		Size: 252.2 KB (252240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59356fe1355d1101f6b5ece862e187a7051ef8d65e290e391ac7e35e86e50f1`  
		Last Modified: Thu, 24 Oct 2024 12:59:35 GMT  
		Size: 286.8 MB (286763039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5613fc33a5a684897752af103ae1fa824825630bd1a6a2c0239d0b1ac4718ea`  
		Last Modified: Thu, 24 Oct 2024 12:59:29 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e53f5ae5df91e5ac3cd2bb5d2862cb7afab486fc4a7b74e3525c8b5fd39c3`  
		Last Modified: Thu, 24 Oct 2024 12:59:29 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13589c0fe3b699956063291da53f14d1242139a27bf06cb1d976557b500e52cd`  
		Last Modified: Thu, 24 Oct 2024 12:59:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9d41707b0bea7e3ab99c7c58061fbeeac5050439b1996c4c42c3c8ab283b1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341b006d2cb221f2b46282cc7a8c0aef6bbbaf69b787eddd57abb8ba8fc4f2e4`

```dockerfile
```

-	Layers:
	-	`sha256:83288598a99db947a603348b703ff2f6fc463e9dee41b272e724f5518ae508d6`  
		Last Modified: Thu, 24 Oct 2024 12:59:30 GMT  
		Size: 4.7 MB (4705769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6146a35dd6c9593d022136da9f4e47f5fcc06b328c1e136d6bafbf99e86c41d6`  
		Last Modified: Thu, 24 Oct 2024 12:59:29 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json
