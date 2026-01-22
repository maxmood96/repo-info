## `jetty:10-jdk11-eclipse-temurin`

```console
$ docker pull jetty@sha256:5863f2f08e83c0512f3622c4f6365a198e55b086cb0a482dc9be1931fcc4bd2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:0b21e110e2432dd3da77493edcf7c7de81039e32eae750937d4d24a5f926fff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202929545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8ef22daf285de4363fcd5559c6963a3530af4985aab7384557c7e3a9d98190`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:18 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 00:15:55 GMT
ENV JETTY_VERSION=10.0.26
# Fri, 16 Jan 2026 00:15:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 16 Jan 2026 00:15:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 16 Jan 2026 00:15:55 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 16 Jan 2026 00:15:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:15:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Fri, 16 Jan 2026 00:15:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 16 Jan 2026 00:15:55 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 16 Jan 2026 00:15:55 GMT
WORKDIR /var/lib/jetty
# Fri, 16 Jan 2026 00:15:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 16 Jan 2026 00:15:55 GMT
USER jetty
# Fri, 16 Jan 2026 00:15:55 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 00:15:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:15:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996467dfb4d0179a2f091bc2a9d9749646d7fc320067d1147a6df2b4833f1c82`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 17.0 MB (16975950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc5119c534e7104b853fb64c646a227f4bcaeafa618b9ca5e2b09d52c623277`  
		Last Modified: Thu, 15 Jan 2026 22:19:37 GMT  
		Size: 145.0 MB (144977604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0387e47dbbdeef0f57f3f2e42af7373ddc21eb592674782cfcb5d8e5565c6`  
		Last Modified: Thu, 15 Jan 2026 22:19:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7feaec1b5ae6c7e6e38638d964d4991ce35f3a13191880a163bdef3d12c7312`  
		Last Modified: Thu, 15 Jan 2026 22:19:26 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec8b357c552629cd7b8fa96a112a13e82fc1a48b4253ebaa4d6c0e6ed851de5`  
		Last Modified: Fri, 16 Jan 2026 00:16:04 GMT  
		Size: 11.2 MB (11245661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580f51cf3b8f4c615d89638bcca617cb878129637b77732c17841e52b2f762e0`  
		Last Modified: Fri, 16 Jan 2026 00:16:04 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:93869949ef29870e133b7002c057e1ddea9df5296f82aff39e15dfd1c5691cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b240cbe2d77d3aa6695d422d216b27e31b7fe2f0c38969bbe089e11f922858a3`

```dockerfile
```

-	Layers:
	-	`sha256:83b8dc413e013955f12d660e2c022416ca0fd06de1688bbbb3197e881d8d52a2`  
		Last Modified: Fri, 16 Jan 2026 00:16:04 GMT  
		Size: 3.5 MB (3496603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f8274d0b9647ce43cca2631068ea21ae33667ce5349a477f551802c9afaee1`  
		Last Modified: Fri, 16 Jan 2026 00:16:04 GMT  
		Size: 21.5 KB (21484 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e51b38f92d28334b5eee3eb8aae8206bce646750f6c20510f99284d3309aa367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198843150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6756785ac321f76530139b56d9b3d5db41269d2380598e4e8dcdf64056b5529`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:05 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 15 Jan 2026 22:19:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:19:12 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 00:17:34 GMT
ENV JETTY_VERSION=10.0.26
# Fri, 16 Jan 2026 00:17:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 16 Jan 2026 00:17:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 16 Jan 2026 00:17:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 16 Jan 2026 00:17:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:17:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Fri, 16 Jan 2026 00:17:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 16 Jan 2026 00:17:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 16 Jan 2026 00:17:35 GMT
WORKDIR /var/lib/jetty
# Fri, 16 Jan 2026 00:17:35 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 16 Jan 2026 00:17:35 GMT
USER jetty
# Fri, 16 Jan 2026 00:17:35 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 00:17:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:17:35 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d86faf901014b881d59806c6abf8e875f57ff4daa33840feb636ed7ad84b75b`  
		Last Modified: Thu, 15 Jan 2026 22:19:29 GMT  
		Size: 17.0 MB (16991546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb774c9f82e8606924b43aa7a125018f65d382d013bcc52f89528a0e6bb73229`  
		Last Modified: Thu, 15 Jan 2026 22:19:55 GMT  
		Size: 141.7 MB (141737695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fee430355e8efa91b7cf59aeb7b202afb080c1ddc3d2474779229d9b3009c25`  
		Last Modified: Thu, 15 Jan 2026 22:19:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb954ce4c40c8ba7cb4d1b301537c9468fbdb35dc33337742e5163bb52cb3c0f`  
		Last Modified: Thu, 15 Jan 2026 22:19:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a2b47d7beffa0088cd0ef065a464797e300f38cdc089683f25ea2972db2874`  
		Last Modified: Fri, 16 Jan 2026 00:17:44 GMT  
		Size: 11.2 MB (11245765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83764a9d3e55af39bd89cbc2a9f42e0511c0285a371b92a73d9ec703c627d1fd`  
		Last Modified: Fri, 16 Jan 2026 00:17:43 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:79d710c66ea9a788332bea5e6c3588502541dad82879a6625a25250115975a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10e7edc563b5f039e00d050a8e8d6867589750af2cc24ae6eca2c56ff651b86`

```dockerfile
```

-	Layers:
	-	`sha256:0764194f0129ffc16c82a6fea85db0a3048e9ddc395964590545ff438787dfe1`  
		Last Modified: Fri, 16 Jan 2026 00:17:44 GMT  
		Size: 3.5 MB (3497716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39c8618204ce0d42663cb9d6e54989f6bc01645d734bbb878c54ecd3579c25f`  
		Last Modified: Fri, 16 Jan 2026 00:17:43 GMT  
		Size: 21.6 KB (21612 bytes)  
		MIME: application/vnd.in-toto+json
