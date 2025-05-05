## `jetty:jdk21`

```console
$ docker pull jetty@sha256:b58b55bc764651710a9d1d345af9dbe34b33bd56586d97849e8826d36049930a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:jdk21` - linux; amd64

```console
$ docker pull jetty@sha256:17ef119c48f4aef7d299fc2b4936f2de39095a2df3e8c80b69da061d7bdc94fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245054420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a477bf78b83b7395e49bdde8b7e36d9dfa2b0bf2ffb2b37c246bf4c469e29a87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 04 Apr 2025 01:30:23 GMT
ARG RELEASE
# Fri, 04 Apr 2025 01:30:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Apr 2025 01:30:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Apr 2025 01:30:23 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Apr 2025 01:30:23 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["/bin/bash"]
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["jshell"]
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f526e30db5f3400aedfafd9fee4a897e6136cad2ba5377063a3ba2f4d9372697`  
		Last Modified: Mon, 05 May 2025 16:35:19 GMT  
		Size: 23.0 MB (22952890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb17fdf011e86a2dc27b9b6d8df16cacad4a411aaf601bc9ab24f7f4b326db`  
		Last Modified: Mon, 05 May 2025 16:35:22 GMT  
		Size: 157.6 MB (157648162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4223556ed03c6bd1c69dff886afb2d3500c92850eaa663c9d88b1c0488b7f7a9`  
		Last Modified: Mon, 05 May 2025 16:35:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cc8efa6ea79682d3418b90549eda220179c60092f15c979408627839067c6c`  
		Last Modified: Mon, 05 May 2025 16:35:18 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bae31da1b0af216e874a5469449688a26d10c8a662865e6365042119b4c897`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 34.7 MB (34731706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454605e9c19316090440bd570453258a5d850998a18b730891ab6505e204e33c`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:jdk21` - unknown; unknown

```console
$ docker pull jetty@sha256:335241ee972430fdf1086e46e0a17c6712098bddaf9e09b580e05bc1e7d5e9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206029df3d8996076a1bce6232457e56146490a6093d2bb1d38e57bacdf46954`

```dockerfile
```

-	Layers:
	-	`sha256:44b530303b3a625d175e2d4bd39be382bb87d0cad4cbe57c73e8572753de976d`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 3.6 MB (3578988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1e0e3c105f766a7b1feac17bfba61ecc512f75916c5536f20d4f543053d0d7`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 24.0 KB (23968 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:jdk21` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0bcb0da9e71f1182922ab93fa939421afc4a2366897366b0e1c768b69f8c44fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243677749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce38ae342326765996423d947baa7913e47295099c448a6d133e2d094017be7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 04 Apr 2025 01:30:23 GMT
ARG RELEASE
# Fri, 04 Apr 2025 01:30:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Apr 2025 01:30:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Apr 2025 01:30:23 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 04 Apr 2025 01:30:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["/bin/bash"]
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["jshell"]
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bb4e2189afd83aaf4ebaa5d182e82cf4839444cb97cb855a17178b08a9012`  
		Last Modified: Wed, 09 Apr 2025 07:05:34 GMT  
		Size: 24.2 MB (24163226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec97dc59ee233054f8d7bf5b57d9689c3089c661f956a44ccbcf0fcdeb66e7c6`  
		Last Modified: Wed, 23 Apr 2025 16:41:40 GMT  
		Size: 155.9 MB (155931644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef1db96a7cc3025d288ca83344c3cac3383743cfae873cfc56a15ec45f5ad67`  
		Last Modified: Wed, 23 Apr 2025 16:41:35 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e356729a6ec520e7b03439a358ca84bc189c4d1feea8ddd711b1bd66d7bc3abd`  
		Last Modified: Wed, 23 Apr 2025 16:41:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e40003386506f08d87a6d504e27fc111df8c105bea81ace5f28fe38aedc30`  
		Last Modified: Wed, 23 Apr 2025 17:49:15 GMT  
		Size: 34.7 MB (34731789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bb3caac29967c416002ec66c8cddc552d5bb241e00203220ffae6c3a76ba2a`  
		Last Modified: Wed, 23 Apr 2025 17:49:13 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:jdk21` - unknown; unknown

```console
$ docker pull jetty@sha256:e3d087c8ee10e45ad6b229f6235fc4554ec9a5339e90be2b4549820e668f5099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ef3fa1b4f3394dc6600dc2066f1f5771393d994b40a1f00a644a0377b9be2`

```dockerfile
```

-	Layers:
	-	`sha256:7dacb5ca55ea0f512171cfcf255bf93aaaa689ea3ca8117eb72800e6d41a7cd7`  
		Last Modified: Wed, 23 Apr 2025 17:49:14 GMT  
		Size: 3.7 MB (3710624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ef69e5c805ff5c7268f42e403a3b5b7743f3e9d18b51bf9b2eb3553de4ac40`  
		Last Modified: Wed, 23 Apr 2025 17:49:13 GMT  
		Size: 24.2 KB (24192 bytes)  
		MIME: application/vnd.in-toto+json
