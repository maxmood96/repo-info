## `jetty:10-jre11-eclipse-temurin`

```console
$ docker pull jetty@sha256:4672e17d1c60a95058dc2976919840cbf1eeff701f0a42b8b11fc0e148760539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jre11-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:2ddd1ad0a30ba2e73cca6f6a4a6d39eab0b89114cc1cf4587d6d877a74c34964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101610794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e301e40ba30a06949508475f42243fd372e82b8ba3412081c5e142686cbb94`
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:f1e49404950a550f6205b66ae147060d18dcb3ba07d8df8ee31a5c83c540a67c`  
		Last Modified: Tue, 02 Jul 2024 06:01:40 GMT  
		Size: 47.2 MB (47186001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27110d8581e6469d85c00f6c85d6d5ac62b9a2c38b96919993a0734aea4abe26`  
		Last Modified: Tue, 02 Jul 2024 06:01:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3d9b80aea7a3d789b713c5070a62a15dc28669ec287b0e4d73eeec7b30a62f`  
		Last Modified: Tue, 02 Jul 2024 06:01:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e5555460271dca56ccf82be9f9c291eb1705375dca59692089a53c7178c11a`  
		Last Modified: Tue, 02 Jul 2024 07:07:47 GMT  
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

### `jetty:10-jre11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:d9210c7a125e3f3677c2152b930ed556cc740c3564384782c036469a51623efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d023459eb7768d33f3f1775d99f266deaf516a627800c307a6fd66e14102a`

```dockerfile
```

-	Layers:
	-	`sha256:37f37a29e1b2e06ce1fddb9e805aecb87728624e3ce08f6b48fa5dec276c99d4`  
		Last Modified: Tue, 02 Jul 2024 07:07:47 GMT  
		Size: 3.5 MB (3541268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6b079734618ee635d89c695cef2d1c6933616083b5259725afee59394d56d`  
		Last Modified: Tue, 02 Jul 2024 07:07:47 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jre11-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ec489795aeeb533e465478589a9be701ff7c05afcab2a2f271f42ef26de672f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97883282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a4a5cd0a455a19a514bc24d21b2bf702f8b92bd4b12519e0f422e289ab95f6`
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 31 Jan 2024 21:20:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:625a81e37ff20b4b74fec4fff7a7219056fd47ad045218316bb858d77276906e`  
		Last Modified: Tue, 02 Jul 2024 04:35:18 GMT  
		Size: 45.6 MB (45555005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0e45daf3f3dc8d8f86517f6bb8f8c844997e9f929dac175e163bb99fca8109`  
		Last Modified: Tue, 02 Jul 2024 04:35:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96ca92e0bb1ae2bc7dcba571965cb2c52f2c3bd72cdf74c8a5bb4f96fb36f32`  
		Last Modified: Tue, 02 Jul 2024 04:35:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26bf1e287c4a167f9fbd6ef265e9b9c8202a92c471add10cadb2f5addaef1e2`  
		Last Modified: Tue, 02 Jul 2024 15:29:08 GMT  
		Size: 11.1 MB (11111622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39787279b81236a59235b28aedd5e9779f4c7f45c65a333abf2271ee173cf3c7`  
		Last Modified: Tue, 02 Jul 2024 15:29:07 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jre11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:74f7877917655168363eff79e457230f8ea7cbaa750858d1ab1ecf0ebf24bd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0f58dbeac360213c2abac0a773347e1145dac95aa489c90c59107ace6e7f1f`

```dockerfile
```

-	Layers:
	-	`sha256:6ab9d4196416881cd6d22c76e9494ba3dadd0fa67fce267f960ce7f05f028b01`  
		Last Modified: Tue, 02 Jul 2024 15:29:08 GMT  
		Size: 3.5 MB (3541583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1e4526326e688013bee1dd076135cd38a16cc9b46ce70de62eeb7444ecb1d5`  
		Last Modified: Tue, 02 Jul 2024 15:29:07 GMT  
		Size: 21.8 KB (21750 bytes)  
		MIME: application/vnd.in-toto+json
