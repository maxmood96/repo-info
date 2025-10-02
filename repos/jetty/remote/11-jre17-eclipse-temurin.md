## `jetty:11-jre17-eclipse-temurin`

```console
$ docker pull jetty@sha256:f426d4fe19036535362cdafe9f961463809a098d91291b80adc024a92adee234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jre17-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:9e26b6a3a64d7e078d4bdf3f7e78c83b98eef8dc6f4f67ea7b2083b3fa49aed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108376437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d01944257b774d4ee7251859915610930a9bd453b0c80687d7239c453926ac1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14664fbcab656cdf1605406ad130342006e9c758aeca00e777d8d3b35a910245`  
		Last Modified: Mon, 15 Sep 2025 22:13:49 GMT  
		Size: 47.0 MB (46986174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243291111c96615fc0a5d0c0f7213f78ea5a733c26b16e9d06b56e347807082a`  
		Last Modified: Mon, 15 Sep 2025 22:13:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ce538b8c996a28ae83301e73322796d0a03099940f9c4f9720f5fa832a9a07`  
		Last Modified: Mon, 15 Sep 2025 22:13:44 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bfc0b3c5b4324c32371b7aa6f0d26ee7d6aeb60629b7f07e41b042e9e3a0c8`  
		Last Modified: Mon, 15 Sep 2025 23:16:39 GMT  
		Size: 14.7 MB (14690906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf780228b85e73b83542a6e9424e975ce6a3f6c4c106ab99871975a5ec44fdc3`  
		Last Modified: Mon, 15 Sep 2025 23:16:39 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:0b43e03cbedeff58ca3cb8273e07f197034c999248c848a9bd9652c0e645d448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3413876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bbea34a1f165f5546fc9d98dbd49c54206038954adbf8a8ebfdddb0d4fd1b9`

```dockerfile
```

-	Layers:
	-	`sha256:b51c97c5aef14d63bbad845d34156010d9f4763e778203c74d1c17ad7be32049`  
		Last Modified: Tue, 16 Sep 2025 02:18:34 GMT  
		Size: 3.4 MB (3392353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30427a765a1308dad8654428cb33bb55ae960162da8b2ce2540e2f26d8315af5`  
		Last Modified: Tue, 16 Sep 2025 02:18:35 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jre17-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a195b22ac95f44095c9b6e5131b7585f34f6df5c845ebb0dad50888afd9121e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109245141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d16a7d5942bd8de8a37256cafd2c9bde7e5e824b0a642715560068d5eb03c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61ea3d0cc515835574128a1f4508ce3cd84046c84f5adfdd31329471a200f56`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 46.5 MB (46481685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b517f5a2189728afd33be6639f2a5e5c4b8aee4303360f7de0b50358dae34`  
		Last Modified: Thu, 02 Oct 2025 01:17:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1b0ab5bd79a9fc3c444d3bad8851b0a3692b7066fdf6e1f0d7b2e6e709d54`  
		Last Modified: Thu, 02 Oct 2025 01:17:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0250238997093f00203cb4059945e43456f0d3c56f894a163c10273376c2109`  
		Last Modified: Thu, 02 Oct 2025 02:21:00 GMT  
		Size: 14.7 MB (14691203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076fc50a9f65648a0fc0222eaab7aa35051c313fd447d9f58523cd357c104534`  
		Last Modified: Thu, 02 Oct 2025 02:20:58 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre17-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:87f23b7335de54632cec3a765553076a5518d0a761ce35a45cb465286fe3dd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3414499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13fee8f178bca9a1bd19c9a080492a78724a473d86512565577164461e1a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:8d13744f16cc9ca4a39060f07819496b61dcbd1d1b963afd93b6e9403befdb43`  
		Last Modified: Thu, 02 Oct 2025 05:18:12 GMT  
		Size: 3.4 MB (3392848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f178c36395cad35db19a3bc45326d70c43c367d9985597ddfae80bc02a7fc2`  
		Last Modified: Thu, 02 Oct 2025 05:18:13 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json
