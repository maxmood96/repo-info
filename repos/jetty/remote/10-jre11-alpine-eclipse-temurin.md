## `jetty:10-jre11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:5edb0a8e248166c29a11eeb319a59e1773102484a7992803787c00ffc2581ffc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:10-jre11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:9620b2076a5b3e01005618a8f0cb367101fc45c3d15673a1951ae5c3d624b735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73762871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb81c435c38b462b739af3dd47b466eef534fc0d40ae26cd1f646eab7b5d6a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 08 Jul 2024 06:35:54 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6972a6251bc88d6fbb64a188557cf165f1c415ded550d2a280bbcbc4272caff1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=10.0.22
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.22/jetty-home-10.0.22.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f359cd8d0e18fe23ad96c88a4ed275ce3c28c031f134b2223544d799cb126`  
		Last Modified: Tue, 23 Jul 2024 01:05:20 GMT  
		Size: 8.5 MB (8537043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091119e34d69cac2a35e30b98f0cfbff9a6d037d2d324a8abfb3d662ec8bb8bb`  
		Last Modified: Tue, 23 Jul 2024 01:06:21 GMT  
		Size: 43.6 MB (43550557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ac9340cc093223cdecf60b7ded38bde7fdb00db2d76e13ae67a0c95eba63c7`  
		Last Modified: Tue, 23 Jul 2024 01:06:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df56a50d57b12c2cb8bfc65308c13ae432b091371142723fae5104cba52438`  
		Last Modified: Tue, 23 Jul 2024 01:06:15 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7576d09d26c008035e1199c0c97684ed329ebdd99906e17d89ac14ae4fb757`  
		Last Modified: Tue, 23 Jul 2024 02:04:22 GMT  
		Size: 18.3 MB (18253710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5c631e8547d63f2ec1f2fd4073c1aec1f40953730aff1def1aa7eda61c0a9b`  
		Last Modified: Tue, 23 Jul 2024 02:04:17 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jre11-alpine-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:239982a8ba2ef3335a29109a160f09ff3fc995e70b27fb83a2bb9d14140c0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1308680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f42de106891292f79c26b3429e1350b67898fb69d5217e6dfa43682d793bf5`

```dockerfile
```

-	Layers:
	-	`sha256:0181785fa46d571700fea014a518ab022f792b2204d85c82b15a9795d5c2d1cf`  
		Last Modified: Tue, 23 Jul 2024 02:04:21 GMT  
		Size: 1.3 MB (1288746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dff3e12e70e36aa02895e68113a4bd20fe50f687955fea07d3dac7184e5a81`  
		Last Modified: Tue, 23 Jul 2024 02:04:20 GMT  
		Size: 19.9 KB (19934 bytes)  
		MIME: application/vnd.in-toto+json
