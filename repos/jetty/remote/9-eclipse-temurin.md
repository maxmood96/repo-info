## `jetty:9-eclipse-temurin`

```console
$ docker pull jetty@sha256:d9c03db96111f7ec69132adf23dc2a10ec8c3a516802d90d77134f9493dafb05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:15d94a23930220d93036f4e2308fad24a6d46b4f893fbfdc24903ee957f84c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216427506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351a68d0769fcf45bf7a341121ebb2452430dd03577a677137119f9803fdca20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c930bd25dd53355206fb22462e8fbde127b1d43483ca67962d2bf2bb4a534c0`  
		Last Modified: Wed, 05 Jun 2024 05:00:37 GMT  
		Size: 17.5 MB (17456370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae78fb28ee8ad64497b830c9c46950ab9448341cbdb14f4710d143671487c61`  
		Last Modified: Wed, 05 Jun 2024 05:01:45 GMT  
		Size: 158.5 MB (158511802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b2709c988772d4f722fa842b200b424f5873a64a9b4c5cfaeb86a6293a3b1`  
		Last Modified: Wed, 05 Jun 2024 05:01:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e071b974f417bebf03dcba8690670bce9d7d83d647b1775d42f720b2813da09d`  
		Last Modified: Wed, 05 Jun 2024 05:01:33 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a30eab99015a0aceadda1af26b0c865bde4f0914fbdef5fd74f7bb2e80c213b`  
		Last Modified: Fri, 28 Jun 2024 20:56:23 GMT  
		Size: 10.0 MB (10017476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68268d1cf8321d0e270fd9335783f5cbb4738564b8abfb6b4d933bae626a5d5b`  
		Last Modified: Fri, 28 Jun 2024 20:56:09 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:0941a46a476f785ed9645d96643ddd8c6db6e4cfce7f7a449773dd9d450913ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a5964feba4e552e599221bd03c225147c35eb9bd749af329a3a9263f6fb3bf`

```dockerfile
```

-	Layers:
	-	`sha256:9dfbc3fa1e9f80314f0e05c8128ef25a9a0e5674ea8e5e7c1f9ab7565521bad1`  
		Last Modified: Fri, 28 Jun 2024 20:56:23 GMT  
		Size: 3.7 MB (3688311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc2c58a1b21a15c01a108d06cfce38113b942d2cdc7516b711657cc0fbbe4bf`  
		Last Modified: Fri, 28 Jun 2024 20:56:23 GMT  
		Size: 23.3 KB (23282 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c5e235ddc8862835574737f2c0a5ca4f4a9f40d05ce71b5aeca542922a23bbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213955992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1521faac83aabe73cdf450fbf74e8afaf4d2ded7d2dac59acdf6bef3b943f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd5d7dbc0eb75f9bc71643e6dcfed8b6cef6295e5c7d5f5ba90aa14f0d9cc6f`  
		Last Modified: Wed, 05 Jun 2024 04:57:07 GMT  
		Size: 18.9 MB (18859083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a2a7710d9d7d0f88f9f13ede1b7ff2f89343d79308778db178dc4f312ae4a`  
		Last Modified: Wed, 05 Jun 2024 04:58:04 GMT  
		Size: 156.7 MB (156672853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e96aef1e76c15d9c20747e43105bca90537c6bb652ea98bc96ef69728de212`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a3dedce6ac6bb05c0e8a5dbdcc1f91df5880b0dd7eb1e077172730f1f2322e`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2977f7c55597e531ee773d6eb6ee16c6c5490d33d59388b5f43d39aeb47d995d`  
		Last Modified: Fri, 28 Jun 2024 21:00:22 GMT  
		Size: 10.0 MB (10019177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8380d27b8835fc594a514863c105f18d3012deaee09a9bec89cef375252111a`  
		Last Modified: Fri, 28 Jun 2024 21:00:22 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:7b5e2066ea0a7dfddffe3487f7401557991efde96a9f66df04a613511ae900da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34e9088ad2f9af3ce1db293ab562e863b7da56995d2c954334949f80bfdcc9f`

```dockerfile
```

-	Layers:
	-	`sha256:b529453eeadc852505cf2e2b4e5d55b226a3649286ea6473f7d71af84496ee59`  
		Last Modified: Fri, 28 Jun 2024 21:00:22 GMT  
		Size: 3.8 MB (3784617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd9266aa5001b69c8b931db71595ab16419d6d320a5d499991c3aff9f9008ec`  
		Last Modified: Fri, 28 Jun 2024 21:00:22 GMT  
		Size: 23.7 KB (23688 bytes)  
		MIME: application/vnd.in-toto+json
