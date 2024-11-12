## `jetty:12-jre17-alpine`

```console
$ docker pull jetty@sha256:8fde617d627c80e1ea2b541a6f58eb862db012b41575d38224dc9e37a06efa25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jre17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:788c6faca237a97f932b31d3614dc48904ca9592fcfd52d0a61d22899b4f4043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104192205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd2df7619c267f3794512f9a92f975af80d00f621a2974deb87bc1204975c65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154a8c60e9d41fd1022b644faeb992a76d55b7d8d699b8b54816601213ec1b04`  
		Last Modified: Tue, 12 Nov 2024 03:14:54 GMT  
		Size: 35.6 MB (35641014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244ebf920f200dcc92bea8adf17ef31d6805cb530fe2ce65caa555d15a0fad06`  
		Last Modified: Tue, 12 Nov 2024 03:14:53 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jre17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:f8cf234e59e9bcfbb6d5c9ae2429f75542c82346b0fe3b7169923c63652355e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1150324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94855a840c5e799799bb5c51420fb3cb918792b03eaa9cfbb2ee472b76d31d35`

```dockerfile
```

-	Layers:
	-	`sha256:9b6389fdbd1038dd9857354f03ee87d0760d9aca042f6e0bdcdd82ef5bc5a406`  
		Last Modified: Tue, 12 Nov 2024 03:14:53 GMT  
		Size: 1.1 MB (1130298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966e1aa7ee59ea12514987241acd00c7beb72fcc3d7d38e52f505e15c91a8542`  
		Last Modified: Tue, 12 Nov 2024 03:14:53 GMT  
		Size: 20.0 KB (20026 bytes)  
		MIME: application/vnd.in-toto+json
