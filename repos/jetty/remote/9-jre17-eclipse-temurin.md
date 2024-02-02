## `jetty:9-jre17-eclipse-temurin`

```console
$ docker pull jetty@sha256:0eeb90f4402443d4656074de4aa23e1809301a9335bdce260177e6294466a750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jre17-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:4fd6c7093ad29b99f0f59af02e5559dbbfc8c2a91460d4c410d6a43c74e1ef96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105341750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6d3fb0e2b59a31142711b0083ace8d14e732b11f2c20fadbfc31fdf7ed25c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:32:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:32:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 20:18:15 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Thu, 25 Jan 2024 20:18:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 25 Jan 2024 20:18:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 25 Jan 2024 20:18:15 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 25 Jan 2024 20:18:16 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 20:18:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Thu, 25 Jan 2024 20:18:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 25 Jan 2024 20:18:33 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 25 Jan 2024 20:18:33 GMT
WORKDIR /var/lib/jetty
# Thu, 25 Jan 2024 20:18:33 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 25 Jan 2024 20:18:34 GMT
USER jetty
# Thu, 25 Jan 2024 20:18:34 GMT
EXPOSE 8080
# Thu, 25 Jan 2024 20:18:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 20:18:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4080cbbe938d7cadb00eda7a89a93f5878d7e968b4e8b23640b11c37ad69ca7b`  
		Last Modified: Thu, 25 Jan 2024 19:36:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0279821d4f422edb76c5833b7a6719fbebfb993085e8e6015d1332579868e3cf`  
		Last Modified: Thu, 25 Jan 2024 20:33:06 GMT  
		Size: 10.3 MB (10270727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95727c24b46422b3b93654d862bf80da07b49a0835d1b3cc8f1fc10a575f010c`  
		Last Modified: Thu, 25 Jan 2024 20:33:05 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre17-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:cdc08288ebb5f75bfbcd92d1daff30a70c93d64d11408ed5c40ea98c416f7fdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104173396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65666d68a5d747c35b71739d50241bbbc5ed0d725fab844cadc6e0c3bc1df64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:12:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:05 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 02:12:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:12:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:12:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:12:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 04:25:54 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Fri, 02 Feb 2024 04:25:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 04:25:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 04:25:54 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 04:25:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 04:25:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Fri, 02 Feb 2024 04:25:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 04:26:11 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 04:26:11 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 04:26:11 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 04:26:11 GMT
USER jetty
# Fri, 02 Feb 2024 04:26:11 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 04:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 04:26:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0007a9ef9bab7b317a14a0d8594647e9c47755fcb79f9fa388e560fab31690`  
		Last Modified: Fri, 02 Feb 2024 02:17:22 GMT  
		Size: 46.6 MB (46639311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917c6cc534cfc01e73da456384906c210ffa86f1df265b8ee7255561e2a7c5fa`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7a0f038262842ffcfdab428e9f3a7a1d0dc2e49da53bdde76335cbc0c02b48`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c38219622a3b1adbbf20fc547c94547e6dd794810322da27af3d90071217b42`  
		Last Modified: Fri, 02 Feb 2024 04:40:15 GMT  
		Size: 10.3 MB (10270792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41fa56be40d325b633bd0430ab64a3f055e7cdf9331f4b7166a73b135d16fa2`  
		Last Modified: Fri, 02 Feb 2024 04:40:14 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
