## `jetty:9-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:fe86966e03c8a9226cfc75c5f871d29fda0bcf74b8de1f0863b0e807388e4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2436c4ac9ccb0ea7f4ed68334b23c64c2d9188b04f9724de47f1a8b4721ac9ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181474394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f0478b42a59295d8085d42417eb22bda013066c4a65913b46da625a4903485`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:22:47 GMT
ARG version=21.0.2.13.1
# Sat, 27 Jan 2024 03:22:53 GMT
# ARGS: version=21.0.2.13.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 03:22:54 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 03:22:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 03:22:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:57:52 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 27 Jan 2024 08:57:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 08:57:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 08:57:52 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 08:57:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:57:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 27 Jan 2024 08:57:53 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 08:58:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 08:58:01 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 08:58:01 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 08:58:01 GMT
USER jetty
# Sat, 27 Jan 2024 08:58:02 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:58:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:58:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2db2a4cc3063ed23414dd17e8966deddb70e67b59176599009c10382d23d15b`  
		Last Modified: Sat, 27 Jan 2024 03:31:44 GMT  
		Size: 159.8 MB (159771385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486c42e2a0c7d8d8d397f41cff671f93aba2b26e649c104ab0d5b82375a01895`  
		Last Modified: Sat, 27 Jan 2024 09:11:37 GMT  
		Size: 18.3 MB (18292646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dcdf72c3cee97e71c81476058f935257cc122306344ef75ca9316343186a63`  
		Last Modified: Sat, 27 Jan 2024 09:11:35 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:aa7026667b276d8bb3299d07cd27dd7dd6e226a437ac41230f362bd8a221e552
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179042715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3bf366da95ebad0b98616f9f143a0276783840f58d620d2fded69f749faeb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:29:23 GMT
ARG version=21.0.2.13.1
# Sat, 27 Jan 2024 00:29:27 GMT
# ARGS: version=21.0.2.13.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 00:29:29 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 00:29:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 00:29:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:33:48 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 27 Jan 2024 09:33:48 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 09:33:48 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 09:33:48 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 09:33:48 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:33:48 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 27 Jan 2024 09:33:48 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 09:33:57 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 09:33:57 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 09:33:57 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 09:33:57 GMT
USER jetty
# Sat, 27 Jan 2024 09:33:57 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 09:33:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:33:58 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d82eab9293cad00735c2143f63ab600dc5f767c9d65becaaa8f48454710f50`  
		Last Modified: Sat, 27 Jan 2024 00:37:30 GMT  
		Size: 157.3 MB (157340715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04edeea73880d3da9cbabc604b549031a0979e2d6ab6246029d0853c0e495b45`  
		Last Modified: Sat, 27 Jan 2024 09:38:41 GMT  
		Size: 18.4 MB (18352651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dda6599cc0be0edab0ef971983a579ef11e4b5bdcba5ee73a470c18bb9e3da`  
		Last Modified: Sat, 27 Jan 2024 09:38:39 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
