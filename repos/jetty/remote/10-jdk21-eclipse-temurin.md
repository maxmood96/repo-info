## `jetty:10-jdk21-eclipse-temurin`

```console
$ docker pull jetty@sha256:897c1f7dc5c489f7bd2cbf7350afc5cc215800245c3905a9f61070d1b61c8ac4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:2ae122ced6d7004ccfe196ee41a1322c59c46088a910554ee414ca34c6a15214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220082535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc998c29249a1333437471e96174e47ed117c40409c6d8eb405b1d26bfd5bdf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["jshell"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=10.0.22
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.22/jetty-home-10.0.22.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e44a677d4d83c1d6ba203c24d85609638b21fc91ef60c5e4b2ad465fdca98b5`  
		Last Modified: Tue, 23 Jul 2024 01:07:36 GMT  
		Size: 19.8 MB (19765101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f561a59c51745f113da0b8d14a8a3e26e6e068ae45177caf2da7edfdf9a0f52f`  
		Last Modified: Tue, 23 Jul 2024 01:10:22 GMT  
		Size: 158.6 MB (158587297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc851d1d586088490c3978839d308c2ecb7b3034d96538529d5b5fc8b419d3c`  
		Last Modified: Tue, 23 Jul 2024 01:10:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80b90d7bcc710a00162e38d8c67326714d1479444aaa3d5addf9e86e39dca8`  
		Last Modified: Tue, 23 Jul 2024 01:10:09 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcd70428aba33c830449edfaf1de188b70df8b7bb05038dae632f7e2c28862e`  
		Last Modified: Tue, 23 Jul 2024 02:04:22 GMT  
		Size: 11.2 MB (11160238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0428ce529f2bea01b8df1741462292c1b0b1608385485dea2b93a0025b97fd95`  
		Last Modified: Tue, 23 Jul 2024 02:04:08 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:0c787b600cbe38a857f03724d348db89fe3d22ca887dc9bcc5df499e1df6d2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f694bbd12e55e407725fc0c63e21f7939c5f52ee39d8722469bc0cfa69392792`

```dockerfile
```

-	Layers:
	-	`sha256:8e80606f0d374b44e81bbfeee1ffcf90797acc41ceb47cf406f3ba16ed2c81a0`  
		Last Modified: Tue, 23 Jul 2024 02:04:22 GMT  
		Size: 3.2 MB (3185688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a01aad2df8910cc6349f935a3c9fb5ed184b5b71d2f01709d284820eb34f7e0`  
		Last Modified: Tue, 23 Jul 2024 02:04:22 GMT  
		Size: 23.3 KB (23274 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1628f331334b0fc1dfdf9a92e9d4a69098223cea589d49f80a748cd066a94f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215032953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f270d58d2fa4bfd3273707b773ffe3b882ba4134465cd864edab5b49deeea78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

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
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=10.0.22
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.22/jetty-home-10.0.22.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595a5d127b59ecf75423f0ef5367642a9d021fe56a7d618121f1c21d2fd7`  
		Last Modified: Tue, 02 Jul 2024 04:35:30 GMT  
		Size: 18.8 MB (18827827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d6ba0b879fa6d398d17648ea1c3af3c7d1dd7e0248d96e5536c99b96cff327`  
		Last Modified: Tue, 02 Jul 2024 04:36:13 GMT  
		Size: 156.7 MB (156672751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0b7c6bb1eed26555bd38a8578f462429d71c8779230606b7701820a5cef78`  
		Last Modified: Tue, 02 Jul 2024 04:36:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb0e5ab31274f676212fe5806c73e9d703539f6db7d7cc81103d9d38e0d054`  
		Last Modified: Tue, 02 Jul 2024 04:36:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a59a89f4f94da2a58f0268190a4bbf90462addc22fb1a9c28f2fc06cc32a3a`  
		Last Modified: Mon, 08 Jul 2024 18:21:20 GMT  
		Size: 11.1 MB (11128671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161484be6d8fc9744a96fe6c29c7b3d01919162834427314928c6f3641e94df5`  
		Last Modified: Mon, 08 Jul 2024 18:21:19 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:9e0acaa7dd934ea2ea1bb5034905cf84324d44d77e6d00b2de6e3895a85fe1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3819624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ad8db621b4d26ea925de3e93bd69f3db081a83fe067753249ea2aa1a42ea0f`

```dockerfile
```

-	Layers:
	-	`sha256:c0420b71ca5e92cfc56db7c25646e804c87df61b67658e097dacf683b3d34ff5`  
		Last Modified: Mon, 08 Jul 2024 18:21:19 GMT  
		Size: 3.8 MB (3795947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0980e85bcda11af82409292721d39e9b0d7f1b7c46d000da43ad4b080530b8`  
		Last Modified: Mon, 08 Jul 2024 18:21:19 GMT  
		Size: 23.7 KB (23677 bytes)  
		MIME: application/vnd.in-toto+json
