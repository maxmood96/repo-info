## `jetty:9-jre11-eclipse-temurin`

```console
$ docker pull jetty@sha256:674e2e52fb77834e577a28a72b97b5bfbe3bacec4d227c5dc627b81e2292359f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jre11-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:4436c5c368ba380376f3cb9c1a212f6d3e60cc23f85a80f486d4b3114030b197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101913769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e36c5b1292e5b19a8737162562f33fafd9a7302fb3ba63d50fe9b038bda38af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 09 Sep 2024 08:47:04 GMT
ARG RELEASE
# Mon, 09 Sep 2024 08:47:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 08:47:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 08:47:04 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 09 Sep 2024 08:47:04 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
WORKDIR /var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
USER jetty
# Mon, 09 Sep 2024 08:47:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008231199fa1eb506c15d00c549c6fe54d44b67540ce3d6f953338c39e33581`  
		Last Modified: Sat, 12 Oct 2024 00:54:10 GMT  
		Size: 10.3 MB (10326299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a49c6267d589719155b00f144d89a496eb9bf25210d93230a957c6225cf863`  
		Last Modified: Sat, 12 Oct 2024 00:54:10 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:14c4084a9e98ecfc599479b4b3578356c58bdf0fe73c2cc22605245ab1b91c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d60f47faa92efcec599d9f7a4b47114e762a05e9a47a81f1ff1852dff37b870`

```dockerfile
```

-	Layers:
	-	`sha256:855502b7d12d85d5de84a88e899e1209f8d2a24faf9131c8f60387c292a4ab56`  
		Last Modified: Sat, 12 Oct 2024 00:54:09 GMT  
		Size: 3.1 MB (3105730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0fca9ef3ee86050ed68e149852515abe1624bc356336c43cadd601f1f6ef87b`  
		Last Modified: Sat, 12 Oct 2024 00:54:09 GMT  
		Size: 21.5 KB (21480 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jre11-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e5c5bc789c0c7887312ec922e35714864f58fd6375fcfb9d9dba96cffe6f8a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99637916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d43ac91e11fe9c681c4d795f396ae49eb6c0e6c64d9e5edd7d128ee0ac77d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 09 Sep 2024 08:47:04 GMT
ARG RELEASE
# Mon, 09 Sep 2024 08:47:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 08:47:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 08:47:04 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 09 Sep 2024 08:47:04 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_VERSION=9.4.56.v20240826
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
WORKDIR /var/lib/jetty
# Mon, 09 Sep 2024 08:47:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
USER jetty
# Mon, 09 Sep 2024 08:47:04 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a1f6703825bc1ab890a74dbcf6461f732a29cb694c6d7c8c6ad9977ab58df`  
		Last Modified: Wed, 02 Oct 2024 01:26:57 GMT  
		Size: 45.6 MB (45557310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ff191c9dd4f08b1ad924a59b3c126887f036a38c7bad1aae8e12272bbbf93`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85053618bd30c13b6f45f967fb5b27aa26228d70e12cee43591fce42647d7417`  
		Last Modified: Wed, 02 Oct 2024 01:26:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03b8ab5497b510aa373a78cd007107391104003ca6598f9aa004995bb792834`  
		Last Modified: Wed, 02 Oct 2024 05:04:23 GMT  
		Size: 10.3 MB (10325932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ee0649a6f8694885b0c1b073aed5ea44163a21c1a147b4e753cf70f41bc70`  
		Last Modified: Wed, 02 Oct 2024 05:04:22 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre11-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:1b6656c5d458b69d9576f095031a432c16d03711ca5183f07286491d64545e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c0bee5dcfa6287c6afde80a051241e41d5b7004375c6312f4f568ee87e3b58`

```dockerfile
```

-	Layers:
	-	`sha256:ceb9b59a0949bc024e25bd39ad9805ab6dca1865349565149b722a8bac9d34a0`  
		Last Modified: Wed, 02 Oct 2024 05:04:23 GMT  
		Size: 3.1 MB (3106200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e23202195314c21148c0212a01bf6ff1443294888fbb42b4792fd48e852a22`  
		Last Modified: Wed, 02 Oct 2024 05:04:22 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json
