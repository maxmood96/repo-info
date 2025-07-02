## `jetty:12-jre21-eclipse-temurin`

```console
$ docker pull jetty@sha256:4cddffe704c628870002a8544520a97d656435818b2347811b7f93ac62afe4a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jre21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:c613cc4d18d005c5008062a5608ffcda754d1288cdb99bee4fdd7933aa550e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134364960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032a133574970c1865937c4c5d05b1250653424e8bc8c980d145e73d06e68057`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c435c063d543b912f39fc6e178600f6b62187fd7a34ab8dc5b5fcb1206dd2dd`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 17.0 MB (16969494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798510c0a2db2aee23c3cd77ae21513d0e29201f5a7b1fccea8c428beaf4905`  
		Last Modified: Wed, 02 Jul 2025 03:10:38 GMT  
		Size: 52.9 MB (52891084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5cadd8df76d038e3f113d905144cd7efa62929be4d443f95b87cc6f107a91e`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b99df4756a56b22d3dc6b877cdd97b034981ce870e7f2313ccc3f63cc5ebe`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baa57a7b9155027273570985ca0aaaee14667fbdd617d3070ea32b119d065fb`  
		Last Modified: Wed, 02 Jul 2025 04:12:02 GMT  
		Size: 34.8 MB (34781885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f1587622e45affd3454dcf1a0f2beabe94bae42cb995f95128899e96d97fb`  
		Last Modified: Wed, 02 Jul 2025 04:11:57 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:2a0b9f3e4792a55d4de946d6cbfbb6ace80124c94526d4ec66e7bfd09b4d8558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3531394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e27856abd6998358afe9ec0d98d609d06c015a3ede8c07232b254753e4dedec`

```dockerfile
```

-	Layers:
	-	`sha256:81d58d61ad9e0d111f8d351f4c045493e99614861bdd59f16015ae7e9f4f8021`  
		Last Modified: Wed, 02 Jul 2025 08:18:39 GMT  
		Size: 3.5 MB (3509872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20633b9ac0a46c2ceeb95d2c0f00a1795d2af8c96e3935f41cc10435a2d977ac`  
		Last Modified: Wed, 02 Jul 2025 08:18:40 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jre21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1bad679eb52545633ae49cbb1c73ac42041462b92fef4d60d5f0672e7393c57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132697292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d15aac91798db364d6a1a5143072b58dc94cc11584a7072475665c3f6829cc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911347bfc36c43690c78dbee1e4214c6e79e6c2b6bae6572423040611ba80da`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 52.1 MB (52070812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763e1dbf3e148227fb25ab13d25e10e5ae8fcef8987f96fed0240d4ddc176b`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d536b8cff2c9920c7cc9f8410384ff797ae6e3f12ba749e6295cc4c780c62`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f8c7e6509ed0461990b22e743e957c72a298a0d23b2e55ab3cb3a7a52eb3e6`  
		Last Modified: Thu, 05 Jun 2025 17:00:52 GMT  
		Size: 34.8 MB (34782140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e3d6c3913a01e96177219cb6d39f4dd1bb65a609d0e1e507137a7d3674796`  
		Last Modified: Thu, 05 Jun 2025 17:00:40 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:b4e57db0696b85138b8f1f77330aafa2ebc2269c22cf4f7090ec7558115bf131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3392639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd63ac9dd8546d8e2e9f2d25b9416e0c28cd71f4e249fc2c170c2627582446f`

```dockerfile
```

-	Layers:
	-	`sha256:4ed855f8006a8c8a4c6d59928dfaebb18a2c8ec9b1eceab5013ef2e35954f59e`  
		Last Modified: Thu, 05 Jun 2025 17:19:01 GMT  
		Size: 3.4 MB (3370989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a582830584b8138b2418630b6d247b546c380b6b411dc3d91486faa572e1b982`  
		Last Modified: Thu, 05 Jun 2025 17:19:02 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json
