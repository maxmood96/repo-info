## `jetty:10-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:e98a6cb30d4cab2069da2f9dab7610dea12e1f7a31e4122610dae955bbec7c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d95833851d5aeab49073e3687bce3ddf23e90bc4c40aec6d158ec3e23ba101a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182558450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fea51d22efa1edff84c3cc42f49dba499eebe5e2ff3cd7ca3e07450865de35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 20:55:13 GMT
ARG version=21.0.2.14.1
# Tue, 27 Feb 2024 20:55:19 GMT
# ARGS: version=21.0.2.14.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Tue, 27 Feb 2024 20:55:19 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 20:55:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 27 Feb 2024 20:55:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 27 Feb 2024 21:25:01 GMT
ENV JETTY_VERSION=10.0.20
# Tue, 27 Feb 2024 21:25:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 21:25:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 21:25:01 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 21:25:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 27 Feb 2024 21:25:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Tue, 27 Feb 2024 21:25:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 21:25:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 21:25:10 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 21:25:10 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 21:25:10 GMT
USER jetty
# Tue, 27 Feb 2024 21:25:10 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:25:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 21:25:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4589e6e5da0d67f804c83e55296c9d83cdb9e91368a23fc1645ab702d2fdca1`  
		Last Modified: Tue, 27 Feb 2024 21:00:15 GMT  
		Size: 159.8 MB (159770402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda12e4533875af6f590b08216cdfee5e1c14c4a00e7eaf8ceec9ea37f32b31f`  
		Last Modified: Tue, 27 Feb 2024 21:31:39 GMT  
		Size: 19.4 MB (19377685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf70b20ea58ca5481987dfb22164eab9a3ab22d600fa445829f07b52589220f`  
		Last Modified: Tue, 27 Feb 2024 21:31:37 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:aa856358ac112795c4156c0ab1e81f638747abdb4c485933c23ce0bddbbba2eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180127910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270dbd8e8652ef2bb5c2268a36ca8e004a7d27f31ba37406a598180e6c959a99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 21:09:32 GMT
ARG version=21.0.2.14.1
# Tue, 27 Feb 2024 21:09:38 GMT
# ARGS: version=21.0.2.14.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Tue, 27 Feb 2024 21:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 21:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 27 Feb 2024 21:09:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 27 Feb 2024 21:36:57 GMT
ENV JETTY_VERSION=10.0.20
# Tue, 27 Feb 2024 21:36:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 21:36:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 21:36:58 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 21:36:58 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 27 Feb 2024 21:36:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Tue, 27 Feb 2024 21:36:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 21:37:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 21:37:06 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 21:37:06 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 21:37:06 GMT
USER jetty
# Tue, 27 Feb 2024 21:37:07 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:37:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 21:37:07 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25357840a908bb2912a76568c2ae957a450d2aa007eabb22be02e9a54039fd38`  
		Last Modified: Tue, 27 Feb 2024 21:14:41 GMT  
		Size: 157.3 MB (157342245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3806fc70a7c022bb086d67dabc22e9d8d87aa00c7220a83b5f68e656af22d6`  
		Last Modified: Tue, 27 Feb 2024 21:41:44 GMT  
		Size: 19.4 MB (19436316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1def1367f1772b2ef91d3c70bb646e317a1b30dd633846adc9ddb69b34581fc8`  
		Last Modified: Tue, 27 Feb 2024 21:41:43 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
