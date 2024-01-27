## `jetty:9-jdk11-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:9f6495ca312aaf20fb921c2cc9562db97282eba8102638f75543df611ca44d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk11-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ec32f76fb42a623a0c871b72bc2279b95e824f15dd014f87b808fc5a73feb51f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163378846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de6c044aaa65020074069ab100d342dac1e1fd7a1fc34d0e2df20ee52b03731`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:21:06 GMT
ARG version=11.0.22.7.1
# Sat, 27 Jan 2024 03:21:12 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 03:21:12 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 03:21:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 03:21:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:58:24 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 27 Jan 2024 08:58:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 08:58:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 08:58:24 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 08:58:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:58:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 27 Jan 2024 08:58:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 08:58:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 08:58:33 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 08:58:33 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 08:58:33 GMT
USER jetty
# Sat, 27 Jan 2024 08:58:33 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:58:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:58:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84890fd5f43fe98bb0cfe014771801d2764f45ece4d57660d4dc89358c0cb7f`  
		Last Modified: Sat, 27 Jan 2024 03:28:02 GMT  
		Size: 141.7 MB (141675715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f7f918e067d481937a27e1b8475557a69f240077648a2c224fa3ea5bc8a34c`  
		Last Modified: Sat, 27 Jan 2024 09:12:03 GMT  
		Size: 18.3 MB (18292768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493611fa640bef3ce6d21cac7b8924e6c4a93848583dd36ca372fb20648b825a`  
		Last Modified: Sat, 27 Jan 2024 09:12:02 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk11-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:63612dc16d63e293079232bae36f9049098c1dd78692606bd9d6a351c7231faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161458808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e183ee435bf554c161a5f27e1017995f59837984241c0f833a65b4f6d2c3f370`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:27:53 GMT
ARG version=11.0.22.7.1
# Sat, 27 Jan 2024 00:27:57 GMT
# ARGS: version=11.0.22.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 00:27:59 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 00:27:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 00:27:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:34:16 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 27 Jan 2024 09:34:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 09:34:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 09:34:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 09:34:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:34:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 27 Jan 2024 09:34:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 09:34:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 09:34:25 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 09:34:26 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 09:34:26 GMT
USER jetty
# Sat, 27 Jan 2024 09:34:26 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 09:34:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:34:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2a46a66c1b2440844fa9dae87710a244c69bdabe9df13f14dd00e13de69215`  
		Last Modified: Sat, 27 Jan 2024 00:34:13 GMT  
		Size: 139.8 MB (139756642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e21a6befa6eb73e340da621504461e4d591309ab4c4630486ca8b95f146ccb`  
		Last Modified: Sat, 27 Jan 2024 09:39:06 GMT  
		Size: 18.4 MB (18352817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f63c91152d08047a55fceb4e7d0fb12468da18410e54ec587f160bf82e0c76`  
		Last Modified: Sat, 27 Jan 2024 09:39:04 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
