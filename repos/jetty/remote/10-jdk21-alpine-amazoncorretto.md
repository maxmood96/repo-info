## `jetty:10-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:5c725cd62cbdc0157ca67b820302f3889b23a84193814c000675d423a26cb93b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d8602394430f6224f17b51c513a460ea7294815189f4239e74e8c25157523db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183243386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6817158bd74abf38aec2af99d5a7b8e13d1ac5dc89baad26263bdbf7d65a79b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 19 Aug 2025 02:05:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
ARG version=21.0.8.9.1
# Tue, 19 Aug 2025 02:05:55 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abd098eb11584626a85f0b70e78e75f2a2af9f0880291ae1a3a57e2edfc79e0`  
		Last Modified: Wed, 08 Oct 2025 23:41:19 GMT  
		Size: 159.4 MB (159379386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996decce92efc7c5f5e1253d694d0bc47bfb35af3404b4e300e6b97b6804a4f`  
		Last Modified: Thu, 09 Oct 2025 00:35:05 GMT  
		Size: 20.1 MB (20059672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f1856f37bfac01e1fbafb4c4438a9dbb18690586b3d7dffd8c5028449ba62`  
		Last Modified: Thu, 09 Oct 2025 00:23:23 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:996773465f6d4dfee73de239257f2e40160488e759e5c093f662dc87f28cb8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5baf876e8c5b2c8d7e979f87b3691682149069d0d6e862612064078e6bccbc6d`

```dockerfile
```

-	Layers:
	-	`sha256:a86b7247cd130a789efe2e9c496db109309cc5e91544136fdbcecd768bbc7050`  
		Last Modified: Thu, 09 Oct 2025 02:16:03 GMT  
		Size: 620.7 KB (620696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f90ab2a541e99f1500e8716d0bcc7038b7746db0c552457cbe0607db9ffd28`  
		Last Modified: Thu, 09 Oct 2025 02:16:03 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:749d6e7b64c88d4eb9b0a43397975ed58a1da874119d2d532939d4054aaeddbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183709473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19af43752bf461a46d0514854094cbc9dc34e38f4ae93cc66e04379e96c1587e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 19 Aug 2025 02:05:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
ARG version=21.0.9.10.1
# Tue, 19 Aug 2025 02:05:55 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd998d4c35c3887cf9b7d0f274f70b8cae4a0a1bcf69e39670164930f639106`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 159.6 MB (159595117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597aa7018ae392f1602be13508125ced835a2eea57075d3cb47ce69caa69706`  
		Last Modified: Tue, 21 Oct 2025 22:15:17 GMT  
		Size: 20.0 MB (19974411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d825d0754c7402721303777a596ceec5f750c784bb58363c44492ba6bf078206`  
		Last Modified: Tue, 21 Oct 2025 22:15:13 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1b321520513333fa16ba6344eb2d24c6a5c8643b539aab23d8564612b9ff40de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.9 KB (839892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b574631ed34d9bd621a713bc845789ee3fb598b7b26cd1c2b3a0e56c121b62`

```dockerfile
```

-	Layers:
	-	`sha256:dafa11b28d4b986971c5a5a141cc023ef4b45c55fc1d974b1064b95f19e6798f`  
		Last Modified: Tue, 21 Oct 2025 23:15:25 GMT  
		Size: 822.7 KB (822682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acce9fb398b4d7292c211c84bfd9e0bba5a9ce43f8d645a09b74bdb383aaf13c`  
		Last Modified: Tue, 21 Oct 2025 23:15:26 GMT  
		Size: 17.2 KB (17210 bytes)  
		MIME: application/vnd.in-toto+json
