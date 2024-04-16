## `jetty:11-jre21-eclipse-temurin`

```console
$ docker pull jetty@sha256:71a15f96714b5084e79f75446779e34f163579af471c1fea29ef68351a2d15bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jre21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:b28544f7b323ea2700401fda88c7bfffbf42b0f56a1a9fc20172de0645c99bc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112133425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621d54b280995a80e0194f2b940e0b9ff5a0e868157a0fe6bd11074d716881e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 08:48:47 GMT
ENV JETTY_VERSION=11.0.20
# Tue, 16 Apr 2024 08:48:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Apr 2024 08:48:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Apr 2024 08:48:47 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Apr 2024 08:48:47 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 08:48:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Tue, 16 Apr 2024 08:48:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Apr 2024 08:49:05 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 16 Apr 2024 08:49:05 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Apr 2024 08:49:05 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 16 Apr 2024 08:49:05 GMT
USER jetty
# Tue, 16 Apr 2024 08:49:05 GMT
EXPOSE 8080
# Tue, 16 Apr 2024 08:49:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 08:49:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf91f29697dbb8ce163fefda79769baf4327db26906f4c89a4ed77136a072ae2`  
		Last Modified: Tue, 16 Apr 2024 04:07:37 GMT  
		Size: 54.0 MB (53983683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3a74fb1693b210d64b4646a434e8f3c0c38e8b0f8450416f9071a7c51df33`  
		Last Modified: Tue, 16 Apr 2024 04:07:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0898461dbcc26fcb4f75acc3be2b31739477ec48134c0392b4b5ff308545a`  
		Last Modified: Tue, 16 Apr 2024 04:07:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc473f411fe8f0ca14f81b2a0306727ccec2d95cd791b2299cf7e19162a03f5`  
		Last Modified: Tue, 16 Apr 2024 09:02:16 GMT  
		Size: 14.8 MB (14802293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa9a1cfc56c880b47b22f6462d0f200cf61e325d16b29f4bef426572b2b52b1`  
		Last Modified: Tue, 16 Apr 2024 09:02:15 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jre21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c5fc00915c7a83ae5208588c0e79012d7036923504afd994209f9381a23811a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109198064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fe132cd3a7e435bf389d40e8ad3671604c9f153dbe1317cbca13f5ad3cfcf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 07:26:55 GMT
ENV JETTY_VERSION=11.0.20
# Tue, 16 Apr 2024 07:26:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Apr 2024 07:26:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Apr 2024 07:26:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Apr 2024 07:26:55 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 07:26:56 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Tue, 16 Apr 2024 07:26:56 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Apr 2024 07:27:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 16 Apr 2024 07:27:12 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Apr 2024 07:27:12 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 16 Apr 2024 07:27:12 GMT
USER jetty
# Tue, 16 Apr 2024 07:27:12 GMT
EXPOSE 8080
# Tue, 16 Apr 2024 07:27:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 07:27:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3442268d30f9e1fa0ab0ac3863301b075ca391dd0f2b2f7e52cbe09afa748750`  
		Last Modified: Tue, 16 Apr 2024 02:59:09 GMT  
		Size: 53.1 MB (53145573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c392e5134670541b93489899ec9b69b0d4096f6d1f26c533e2369c0dfe8e5`  
		Last Modified: Tue, 16 Apr 2024 02:59:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f003285fd6f4f626009807431a00aebb844abcdd9c576761c5bf4222239c894`  
		Last Modified: Tue, 16 Apr 2024 02:59:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7137219777173b6914498d82019247ffcafe80838c9f69042a5e3503e81af1f1`  
		Last Modified: Tue, 16 Apr 2024 07:37:20 GMT  
		Size: 14.8 MB (14802571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2357ef3b81796c9d470f9cda9c8ff10c4d703021b97ad00aac36d34993122c0`  
		Last Modified: Tue, 16 Apr 2024 07:37:20 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
