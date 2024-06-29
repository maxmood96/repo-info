## `jetty:12-jre21-eclipse-temurin`

```console
$ docker pull jetty@sha256:782a48e15dd2e3787489d02143b7429d5867687b2f0766d9457f13f4172c754b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jre21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:e753612aa20b7e7a30e06fe72988c08af663c971c860511ea8095921bc8ae38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131251889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd4d667363f382ee66a0bc0e66096286d26d7effe820a1da3dab4e194316e0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
ARG RELEASE
# Wed, 08 May 2024 22:29:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 May 2024 22:29:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 May 2024 22:29:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 May 2024 22:29:47 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d859b28d5306bac2883873dfd359a793fe2086ce99608de5dd6137ab2445a8d1`  
		Last Modified: Wed, 05 Jun 2024 05:02:04 GMT  
		Size: 53.5 MB (53472211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c5c06d3c33e2779e44f13e323ac953809d196d828c1376242cb73f239ab0a8`  
		Last Modified: Wed, 05 Jun 2024 05:01:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fb58717a078f857d9a88d9e05ebe0c9a92bbb905490889ee02778ace8b73b2`  
		Last Modified: Wed, 05 Jun 2024 05:01:56 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922dd71b3fd10875a2d45f2beddddb6409bec4696dc89addf0c4aadf1b16a59`  
		Last Modified: Fri, 28 Jun 2024 20:56:31 GMT  
		Size: 34.4 MB (34433020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce440ea07f96bf41cb530f892e7b8764bb827cf0d5d869aa99db55b6a06fc7d3`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:57713f6db1df5fd827c7a455917395bbbaa29d3589311d967ea88088a6446fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39ec1399e564b8b7ddc6cc9d75e99d5c40711bf4db282914bdf16f9c6c65dbc`

```dockerfile
```

-	Layers:
	-	`sha256:986a53dbb26a94575d565b176c5f0d00fbfcf20dd6c31b9e2f30ccda36245fb9`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 3.6 MB (3640258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3389a41014532b195c93538ea257df7cd0e00a3addbf057ed2ad9d2040a3f5d`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 21.4 KB (21407 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jre21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:fea8f3fdfafb090c9a3db0062b72e918e12443475ee659496fe8c8d820bcb941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128287654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12773e75cbab1af338d58b2b12d6745165d19956587ecc854a89b88a99e6d8e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
ARG RELEASE
# Wed, 08 May 2024 22:29:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 May 2024 22:29:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 May 2024 22:29:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 May 2024 22:29:47 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dd329103023d18ce41eb44652e30ca689a1d755661726432a511d48d5b8890`  
		Last Modified: Wed, 05 Jun 2024 04:58:24 GMT  
		Size: 52.6 MB (52600169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503519ffa3903a117a59b2eb3a0f023ffc97a0090a85df1b75cc000d939844a`  
		Last Modified: Wed, 05 Jun 2024 04:58:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f3b62f3663e6c9ca03fe5533e86a7b8d60753f4fb61c55d859e48259774de9`  
		Last Modified: Wed, 05 Jun 2024 04:58:18 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ab48f12258ef748f5b411af6a435f54da96777869cbcc094d984e3bc88dd33`  
		Last Modified: Fri, 28 Jun 2024 21:02:33 GMT  
		Size: 34.4 MB (34434780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf0d4a535eaaf5f38802f21cf5d6d16f289bb8852464c13a00a2b0b1622019`  
		Last Modified: Fri, 28 Jun 2024 21:02:32 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:fc005ca665acf1cc201eef740c5b7c5866fa3fa5ae2ffeafd4d5d20840f5527a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0bf4029a4f3b305fe12b41a392c7fbc5526df1595993e2a3bbb71e961bcdc7`

```dockerfile
```

-	Layers:
	-	`sha256:f31244f4c305b36791524659bbc0d39cf444293786bd41fef763f136ac9f4421`  
		Last Modified: Fri, 28 Jun 2024 21:02:33 GMT  
		Size: 3.6 MB (3640573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aadb80696f4f5587d273362f54690c29efe8f927619a2f4305a427058013fde5`  
		Last Modified: Fri, 28 Jun 2024 21:02:32 GMT  
		Size: 21.7 KB (21741 bytes)  
		MIME: application/vnd.in-toto+json
