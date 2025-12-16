## `jetty:9-jre21-eclipse-temurin`

```console
$ docker pull jetty@sha256:14c01cfb01248f2f98f7f145f2ac169adc2987afb2d93a44ec6cb6c65925df86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jre21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:22ad8b093efa8b87ab5b37229a67ff1119ebb3f5905ae02a68e6cb39d61c0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110044646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c72742a9bd4ef62e2bedced5d9e89fa2b9def4f1901005f48b4c6b26ea927c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:21:33 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 14 Nov 2025 00:21:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 00:21:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 00:21:33 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 00:21:33 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:21:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 14 Nov 2025 00:21:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 00:21:33 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 00:21:33 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 00:21:33 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 00:21:33 GMT
USER jetty
# Fri, 14 Nov 2025 00:21:33 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 00:21:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:21:33 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878172f1ac3121519dd1795c821097cda557a10d8ac4526d248f9fe1738b942`  
		Last Modified: Thu, 13 Nov 2025 23:21:35 GMT  
		Size: 17.0 MB (16972399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92fa77023f1881e077b68fb149d30aade157324fdc1181dacf19b57e1313b9`  
		Last Modified: Thu, 13 Nov 2025 23:22:21 GMT  
		Size: 53.0 MB (52978772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1321ce5b3e3ab111f1a88d34df69fbf748e96e3338e9f3d403b062e3e26d99d9`  
		Last Modified: Thu, 13 Nov 2025 23:22:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e444f3c26062a0908ef59f39a3b8894225b2faef3d5b877c11441d3a52713`  
		Last Modified: Thu, 13 Nov 2025 23:22:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d1f79ad18264d3a57ff929e681c5ef4c68d42b3f0e1713d789bae66602587f`  
		Last Modified: Fri, 14 Nov 2025 00:21:47 GMT  
		Size: 10.4 MB (10364470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259ee7d97e5809d82db19d07b5768e2fc0220d7dfe5c7a77050420fbb82a5584`  
		Last Modified: Fri, 14 Nov 2025 00:21:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:77a51debca4f9ff4bef8e62bc03ce82eeab1db577603f3ff1425b0b51bec301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3402061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b0f0e27fdb9005b3428d1f25c8b8264ac51e60ee4a80232c79a16dcd155b1b`

```dockerfile
```

-	Layers:
	-	`sha256:8f4a3c87d86c61d71e540fe05da448029cc801b4f51c4bcf1f48f7097b19513a`  
		Last Modified: Fri, 14 Nov 2025 03:24:22 GMT  
		Size: 3.4 MB (3380558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7f23bfe6b6c4eb7743a27b5cfbdb891be11e1e054e75e71a2bd43b5855dab8`  
		Last Modified: Fri, 14 Nov 2025 03:24:23 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jre21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:8f1308c3eab5730dff5f68a4d21a76194f96e5589485ec831671a5d646c676f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108368707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d9bcd7dc3e26f54b97bc527076111d450e97d6021e8110b141c1fb7997d042`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:21:34 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 14 Nov 2025 00:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 00:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 00:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 00:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 14 Nov 2025 00:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 00:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 00:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 00:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 00:21:34 GMT
USER jetty
# Fri, 14 Nov 2025 00:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 00:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:21:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e052f7b40adf3e6b8172dd9f3385e9469f4dcfbea63c3518933c4239901bcc`  
		Last Modified: Thu, 13 Nov 2025 23:21:05 GMT  
		Size: 17.0 MB (16989179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df04fa133324a49bb96c54d2b02e9d4463a8a2ba701459d09aac3d20984431`  
		Last Modified: Thu, 13 Nov 2025 23:21:47 GMT  
		Size: 52.1 MB (52148635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3225358e001b3b4abaaa7eddcf1179402e80dd7e5627430be9ec054cf2e309`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9456815a95ef9b83f26a22eb86c7592068f9daf313c9f4a58668db87fc1d4e2`  
		Last Modified: Fri, 14 Nov 2025 00:21:49 GMT  
		Size: 10.4 MB (10364619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc27966b89616d6ce4488ac0441dda679295d7e185c27025372fa1f2015771`  
		Last Modified: Fri, 14 Nov 2025 00:21:42 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:436c01f7977c7ce2cc76f87bfeb12fc60e3567b9eed4e1f9760abab8e96f922e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3402685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae39a0fe6ba11552ec841daa4d5de7f3bf11e81fec4ad657df3d930b44cb13`

```dockerfile
```

-	Layers:
	-	`sha256:13dfbb73f2105911ddf3c73a4d9b6406a932704460c96326990b915d52551be0`  
		Last Modified: Fri, 14 Nov 2025 03:24:29 GMT  
		Size: 3.4 MB (3381053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461f1a84e76275fdf13e1927a430bcb454ad2c38501fbbfe8749ab837a71fe42`  
		Last Modified: Fri, 14 Nov 2025 03:24:30 GMT  
		Size: 21.6 KB (21632 bytes)  
		MIME: application/vnd.in-toto+json
