## `jetty:10-jre17-eclipse-temurin`

```console
$ docker pull jetty@sha256:cf9a55c785d7413120f791b21aed25b8f7ef2efe5060a988a37365f92fce7e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jre17-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:ba8feeb02c057ee521e9a525d093b5df9462a93a0ca2d38ad82b2a00e190ee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101680831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af29c99cfe140f6f7bb31a293495819750dd4d2f6b335056d281400be135aaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 31 Jan 2024 21:20:39 GMT
ARG RELEASE
# Wed, 31 Jan 2024 21:20:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 Jan 2024 21:20:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 Jan 2024 21:20:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 Jan 2024 21:20:39 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["/bin/bash"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
WORKDIR /var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
USER jetty
# Wed, 31 Jan 2024 21:20:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ea69141092d083d2011e4bef99d88179238845830f3d13a4e385c22865b7d3`  
		Last Modified: Tue, 02 Jul 2024 06:02:20 GMT  
		Size: 47.3 MB (47256035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d590beb7c559e52929bdee57763bf9b4d6993efef2a777ce420cefdbefbf6fc`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850744c99279a291a7993996d6f9a8b25a5cec4bfad603897080ded3217e1b`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782090fbe4bed970d08ba708bc8a5969a8f16dc33319174af235e37bc5642624`  
		Last Modified: Tue, 02 Jul 2024 07:07:45 GMT  
		Size: 11.1 MB (11111301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc813c9e84c01276bc3b5df051055f5e1b54e133e4564b1aad07d8256346742f`  
		Last Modified: Tue, 02 Jul 2024 07:07:45 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jre17-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:ae9afc414157d83b12e7c175b6abdb45a35751bc5930967f308733cc540d5c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c0a912216061057898c50fa91525809f35ccafcc1010bf37cae78f2567cb7`

```dockerfile
```

-	Layers:
	-	`sha256:a602af68cd8699e67df115f74a03e2af5f68b624278305981d2c586806d18794`  
		Last Modified: Tue, 02 Jul 2024 07:07:45 GMT  
		Size: 3.5 MB (3541268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0308b417d96874633def7e4e8e54cb7f08b0224a6f662b53b948ec9e18dfed3c`  
		Last Modified: Tue, 02 Jul 2024 07:07:45 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jre17-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:054b1f79eb044d56d42b2c7b40903918d41da96ad0111b7ea8199e4e36d17813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99044648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090956cdeeddec95697ae8ed1847999284d1aa82fef1847173812a4097bf27c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 31 Jan 2024 21:20:39 GMT
ARG RELEASE
# Wed, 31 Jan 2024 21:20:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 Jan 2024 21:20:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 Jan 2024 21:20:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 Jan 2024 21:20:39 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["/bin/bash"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 31 Jan 2024 21:20:39 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
WORKDIR /var/lib/jetty
# Wed, 31 Jan 2024 21:20:39 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 31 Jan 2024 21:20:39 GMT
USER jetty
# Wed, 31 Jan 2024 21:20:39 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 31 Jan 2024 21:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 31 Jan 2024 21:20:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcba8e4ae31e5690436469ea0cbe8b0380eac630b99dd454816782517fe3ed`  
		Last Modified: Tue, 02 Jul 2024 04:35:53 GMT  
		Size: 46.7 MB (46716436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1bee0a5ee9a69e90c6a18762b53d2f3872890196bef46a24a14c7e8cd7efe8`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e2fe8e514adf85f13f482dc533f6a54a31ca0f7e9f593af808c0a45b5eb036`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259e6ed1d8938aa912ccb55ae043f22dbb9fc8108ea4b95603f437c2d0705bfd`  
		Last Modified: Tue, 02 Jul 2024 15:28:31 GMT  
		Size: 11.1 MB (11111558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4217c7d6ce83cfbbc1bd7719677f7adf23823993d10a5fec8a764bc8d881e2d`  
		Last Modified: Tue, 02 Jul 2024 15:28:30 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jre17-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:a5275c7805714d7780c6d9970ed0f3d9fe052b5cefbade9f88db0199c301e58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa26bdff3800bf3c4f42dcff367007538fd975d1dc741de087da085335089121`

```dockerfile
```

-	Layers:
	-	`sha256:e208368b461248d5305cc307105ed3d99f5dd4dd45b5098a0bbc49ede0eeb37c`  
		Last Modified: Tue, 02 Jul 2024 15:28:30 GMT  
		Size: 3.5 MB (3541583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf04396c7f7c354328a8f0aba63448088ffea646066ddd868d15aa3dddc15c73`  
		Last Modified: Tue, 02 Jul 2024 15:28:30 GMT  
		Size: 21.8 KB (21750 bytes)  
		MIME: application/vnd.in-toto+json
