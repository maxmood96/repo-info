## `jetty:9-jdk11-alpine`

```console
$ docker pull jetty@sha256:413433ffc9a9b81e945997134d8c93f1e535f2c0a2f9834bfec4792fa28d908f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jdk11-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:db0748207a8c6ba1704a75b08d7160017d67fb9b69d4b7a8e1b21d477f883aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174013735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a079190f6ace8a9d555dd339062ccdcbce6763b198a2722aa4d3543301b9892`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 08:47:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 08:47:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0a431310ccccc36c85b1274b5d31e368fdc8cf62cb7c2ed98d7b59eb5a13dc82';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 08:47:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 08:47:04 GMT
CMD ["jshell"]
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
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697d2fc50e80693447d4c30fb0f2de59a8e677d0ea4dd41a6516e6fd3de5421`  
		Last Modified: Tue, 12 Nov 2024 02:38:54 GMT  
		Size: 18.3 MB (18307371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a71d4f1a97296627c71621cd200063f21e9089159ce942c2f717ddcb2d6a5b`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 140.8 MB (140775156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d2db10d8380a5d4c497e2124755f9e73c7cd3b018a277da968ca8af39d8af`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a697b41d652b4fc39bbe88232ba2e043ef173cd912c76b91efc830b8a63aef`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2003f1bc9fba82f9a4ba993071f6938ec541fec028bea3005375b29ea517ba07`  
		Last Modified: Tue, 12 Nov 2024 03:15:01 GMT  
		Size: 11.3 MB (11303227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba6e139d34d11c6403f85f8b8ca126d14195d91ba92aef00de5ac80666758f2`  
		Last Modified: Tue, 12 Nov 2024 03:15:00 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:9e029531c89c1e29d7f633cd4d9186d32207f5d14b99af446acb7e096e3b66d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1118651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984a9d71a580d45055f134751ad53e30bf53e2948905ae15bade7a5e9d5d8289`

```dockerfile
```

-	Layers:
	-	`sha256:793f7fa3e69d9ba193b73a5f38ef58956982c947e1694d644ff1aa53433d9037`  
		Last Modified: Tue, 12 Nov 2024 03:15:01 GMT  
		Size: 1.1 MB (1098598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aad9ac0e8eb97d8bc87b73fcea722d9bb29675f2dafcfa04804f340fd01583f`  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.in-toto+json
