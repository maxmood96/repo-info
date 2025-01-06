## `jetty:11-jre21-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:a21cf26d06dfd66cea0121ca5515246cd35162a0fa2dd0586f0643061bc3dbf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:11-jre21-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:1c2189d618193de6f501e249e89a4988061babbadaeaa3cf5bb3a04fb460ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90560524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98adc178d4665b70b20b8a1f1de96e1eff6d4abf8f08bb6070919e28e713f8ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='12b988a3d934e3eb89c6a981a93f8e2adf0a62cc9030487dee76c0c29b93714d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='2dfa33fb8e9474e6967c6cf17964abb5ddce9c17fa6a9f8d7aa221a0ae295df9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=11.0.24
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.24/jetty-home-11.0.24.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e2267938c7b753ae1f61657d8e242003015f599c574e7e9e5d0cda5b57da28`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 18.3 MB (18307457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cea13850a52fd4a14930fcf2f25eac5c673e6742a0c77a96538d812e24b918`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 53.0 MB (53039419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2894231efec63bf4121ddce14edfea5728d14b236ec707613e673a3e7d5acbbf`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2ff43196970b1cf8f1216bc83e626ec1d82f0d494ef8e0ff3e3a87519fddc`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b57dffea0e68cd463b7b62d7082b5ad9ec1e8691ffe1940bdd386863ce7df60`  
		Last Modified: Tue, 12 Nov 2024 03:15:20 GMT  
		Size: 15.6 MB (15585672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c822f55bbaceb32f76cc93797d7a58b621f979c05f13bdb5c66cfbfcc864cf5c`  
		Last Modified: Tue, 12 Nov 2024 03:15:15 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jre21-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:88fc88f44be5a14039e1630c3c09703829b3e688ec8199190d9428a48b660a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb82ac53b50385914f0a24c032df116b10e83f27886be1186051471a31ea862`

```dockerfile
```

-	Layers:
	-	`sha256:f48981b44470d22979cdb720b9c72b37df2d39896cd74f4fb41fb8e8f24314b5`  
		Last Modified: Tue, 12 Nov 2024 03:15:19 GMT  
		Size: 1.0 MB (1011456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb6ff3d13133d6418dff3df06a0ce57089689ed4bf39522a5ed52641a44da9fb`  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json
