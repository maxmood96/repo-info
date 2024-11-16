## `jetty:jdk17`

```console
$ docker pull jetty@sha256:94d741b6187c20d5dc7c1f2c8710d1aee6875fe1e7a1941188e6faa1763b54e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:jdk17` - linux; amd64

```console
$ docker pull jetty@sha256:84a1bd7d6b12c424739ca9a3d7d85959ec14f58aec8f9b1d42ce572a7a5f4d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231876708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8875b769589ed7d7dcf8d238ea887f783fb7c447eff5f382ee22fa5190d91535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 02 Oct 2024 21:05:31 GMT
ARG RELEASE
# Wed, 02 Oct 2024 21:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Oct 2024 21:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Oct 2024 21:05:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Oct 2024 21:05:31 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["jshell"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_VERSION=12.0.14
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
WORKDIR /var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
USER jetty
# Wed, 02 Oct 2024 21:05:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5efbbaa7b086da219a1fb5ed73e2f81f28c1891c47843b4d1a2fa7036dabf`  
		Last Modified: Sat, 16 Nov 2024 03:49:48 GMT  
		Size: 22.9 MB (22948239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3d65b153fc79a60b4aec7d9c2e4c1197f78cecf6857e385e443f3d3dba1a6`  
		Last Modified: Sat, 16 Nov 2024 03:49:50 GMT  
		Size: 144.5 MB (144542454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116eafb494a5073ca1c4fad8c6af4995388f205c037c5fd7ff9117c4e965570e`  
		Last Modified: Sat, 16 Nov 2024 03:49:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31516dab25e5d4be72ff2bbab0cfd8bd71d3a12aa0a0352996a6b82786457197`  
		Last Modified: Sat, 16 Nov 2024 03:49:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734d047e63d9dad2087e5b1a4fc0037b61b39f0e5163dea206f5330c677adaa`  
		Last Modified: Sat, 16 Nov 2024 04:49:50 GMT  
		Size: 34.6 MB (34630124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f628dcf4d0845341fd3fb1aaa342c71ac8f5a7c0f74ef060abc416342bfd07`  
		Last Modified: Sat, 16 Nov 2024 04:49:50 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:jdk17` - unknown; unknown

```console
$ docker pull jetty@sha256:f0b427347be04b91a94bb6798ad8b2cb8c9ed66cdb08d7d5e9d12b03af01e90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff962716b6d4b76d517b3073aae39810d4fb8acef501f7bfda6d9c77597dc74`

```dockerfile
```

-	Layers:
	-	`sha256:38822cf1bd0788b568f0b630a27e5f53b70b4523b8598fed8e27470042b3a041`  
		Last Modified: Sat, 16 Nov 2024 04:49:50 GMT  
		Size: 3.6 MB (3587583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a4d9fcadf5db2132c71674013c0ee51deb3226b184ee5ad8fa267c389b05a8`  
		Last Modified: Sat, 16 Nov 2024 04:49:50 GMT  
		Size: 21.8 KB (21822 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:jdk17` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:64510666b729977769e305288abebde5e647481f9be929d71a9a2adc3785e26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231054016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ba6b94924479ef4135eb2ee8fa090b6ded359c1e98bd600087e3253c98b87b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 02 Oct 2024 21:05:31 GMT
ARG RELEASE
# Wed, 02 Oct 2024 21:05:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Oct 2024 21:05:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Oct 2024 21:05:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Oct 2024 21:05:31 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8682892fc02965930b9022c066fa164dd6f458ef4a5dc262016aa28333b30f49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='0c17fa4f14c0d2cc9e9334f996fccdddc5da4459d768f3105c7ff0283c47bf62';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='e69d43be937e05dbccae4cc98f732ed86aa11993234bf5ad6e81c30475a78ce7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='d4e553c6fa7afdfe2577420c6e77a558db8113a3cef84e755384148f5610834e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='e7c82833a7381a05cae2be0e947c08e971bbae4f2e4142c6ec87bbd7530a5646';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='1f824d7369dfd570dc561e2a56035fdcd2970c97cbd355f6deb6ed0e7c6bcb79';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["jshell"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_VERSION=12.0.14
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
WORKDIR /var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
USER jetty
# Wed, 02 Oct 2024 21:05:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a900d84d7bc826cc48aa6025b009b9237a6520a839e83739c6a27d99c7a9693`  
		Last Modified: Sat, 16 Nov 2024 03:10:20 GMT  
		Size: 24.2 MB (24159194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8b799835fd6507d925be5074010b81b8a251987b7abfb2edc7fc49ad560c80`  
		Last Modified: Sat, 16 Nov 2024 03:10:23 GMT  
		Size: 143.4 MB (143368233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cc07316a7c52d5dedc4a9a61d8b905f99aa7c8d4a86cc2300c60ac5a8dd3e2`  
		Last Modified: Sat, 16 Nov 2024 03:10:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a95871622336ec2fab8436068b136d32fbe3295c953cc3c317e5a35ec96c4d2`  
		Last Modified: Sat, 16 Nov 2024 03:10:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b618c230cfce3afba5f38eba350c56747d1235fc441798f4f5cbb818234405e8`  
		Last Modified: Sat, 16 Nov 2024 04:18:38 GMT  
		Size: 34.6 MB (34630058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d36569783d6a54c1649390cc21919bcfc1b6e7c45c1dd67191605f1cb1c273`  
		Last Modified: Sat, 16 Nov 2024 04:18:37 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:jdk17` - unknown; unknown

```console
$ docker pull jetty@sha256:b68521c699ae34eda74978158bd62e8de070a737c5a8327a5ced129f5105220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319580b6db7db9e0a2957daa1e6efa5306b41ede8d7309e7a04b7ba2ef987cd6`

```dockerfile
```

-	Layers:
	-	`sha256:45f32cc6216c5e055b06c854607709d858161e3f2b4e0ac89b5f28f2af82e7bb`  
		Last Modified: Sat, 16 Nov 2024 04:18:37 GMT  
		Size: 3.7 MB (3719300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d762a41aa5cce86be8bbb8d69073c9832cbd224d5ed923766ee66a9b76c73a`  
		Last Modified: Sat, 16 Nov 2024 04:18:36 GMT  
		Size: 22.0 KB (21962 bytes)  
		MIME: application/vnd.in-toto+json
