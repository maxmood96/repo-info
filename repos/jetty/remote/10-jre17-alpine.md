## `jetty:10-jre17-alpine`

```console
$ docker pull jetty@sha256:eca4cecd024a5ef1301871b2914f2e687f5d8d2dd8a6c5656ad651f7e6d9e7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:10-jre17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:56d78b34000d591d0d142bf2e5b96ec36f12371c74a23b5967609f24527e9b02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81202944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafa1890007cb1807cec4c3501a10be3c09b2ec41a63564652027c1f110bc0f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:11:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Dec 2023 07:11:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 07:11:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Dec 2023 07:12:38 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Fri, 01 Dec 2023 07:12:38 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Fri, 01 Dec 2023 07:13:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='70e5d108f51ae7c7b2435d063652df058723e303a18b4f72f17f75c5320052d3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 07:13:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 07:13:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 07:13:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 21 Dec 2023 18:43:37 GMT
ENV JETTY_VERSION=10.0.19
# Thu, 21 Dec 2023 18:43:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 21 Dec 2023 18:43:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 21 Dec 2023 18:43:37 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 21 Dec 2023 18:43:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Dec 2023 18:43:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Thu, 21 Dec 2023 18:43:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 21 Dec 2023 18:43:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 21 Dec 2023 18:43:46 GMT
WORKDIR /var/lib/jetty
# Thu, 21 Dec 2023 18:43:46 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 21 Dec 2023 18:43:46 GMT
USER jetty
# Thu, 21 Dec 2023 18:43:46 GMT
EXPOSE 8080
# Thu, 21 Dec 2023 18:43:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Dec 2023 18:43:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5820a814e8c90e2b86457ad1da29a79516ae242489d7bf67ea216d150c1efdc`  
		Last Modified: Fri, 01 Dec 2023 07:15:58 GMT  
		Size: 13.1 MB (13141060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4bda58fd3fe4303d5faeb7934e9d66e104f5c10e87abbe6a56aa9e8ac13d87`  
		Last Modified: Fri, 01 Dec 2023 07:16:29 GMT  
		Size: 46.9 MB (46854673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8eef6580a1394f3c28fa090377e1c16c5936d0b48f51d43d10ad47721121ba`  
		Last Modified: Fri, 01 Dec 2023 07:16:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f4070fc47887c906b01a0a16db321cfb19225e43ff16dfdeab76065122be16`  
		Last Modified: Fri, 01 Dec 2023 07:16:22 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513887c5b6094b8c812a1daede2d4b493ef186ff3940b34b2c6ef3256b639ba5`  
		Last Modified: Thu, 21 Dec 2023 19:08:35 GMT  
		Size: 17.8 MB (17802261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47702b42bd4066147e1997bc550da8273647ade7aaf40c48069b82ad2b30b7e8`  
		Last Modified: Thu, 21 Dec 2023 19:08:33 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
