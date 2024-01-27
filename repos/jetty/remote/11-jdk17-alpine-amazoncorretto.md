## `jetty:11-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:2cdbac63d9cbace0530c4c80a9fd130f4bbf7d12742a70728df697d108f778ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:675b7492742d4aa552c670b4efeab6e90cecb59baa06680b3e3af8b6654c0bcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172309898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09538e44d4968c7c2f26e32ca1b86436f13f09388e58d3069980dccf0d6e9f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:22:01 GMT
ARG version=17.0.10.7.1
# Sat, 27 Jan 2024 03:22:06 GMT
# ARGS: version=17.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 03:22:07 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 03:22:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 03:22:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:59:27 GMT
ENV JETTY_VERSION=11.0.19
# Sat, 27 Jan 2024 08:59:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 08:59:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 08:59:27 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 08:59:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:59:28 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.19/jetty-home-11.0.19.tar.gz
# Sat, 27 Jan 2024 08:59:28 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 08:59:36 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 08:59:36 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 08:59:37 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 08:59:37 GMT
USER jetty
# Sat, 27 Jan 2024 08:59:37 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:59:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:59:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baca50af88f022801ece65d5df464d777b9e7d437726cbafd617b092393e08c`  
		Last Modified: Sat, 27 Jan 2024 03:29:51 GMT  
		Size: 146.1 MB (146073796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daa6bc01b2db58109200c040e6679c27712343e5f1decb80f8f396f4177269a`  
		Last Modified: Sat, 27 Jan 2024 09:13:01 GMT  
		Size: 22.8 MB (22825740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4367432843319afc15a27c8bc1bedfd51528a6bcbb0f4232a42b60e8fe560f05`  
		Last Modified: Sat, 27 Jan 2024 09:12:59 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c07889a2a0ceef26b854d403a74e4041697ad87bbcec87074f53cce1a88c4138
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170346579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97b3306877b0018a317dc14cfadb1db728b5aa246de20e917388eeac27a5251`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:28:40 GMT
ARG version=17.0.10.7.1
# Sat, 27 Jan 2024 00:28:44 GMT
# ARGS: version=17.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Sat, 27 Jan 2024 00:28:45 GMT
ENV LANG=C.UTF-8
# Sat, 27 Jan 2024 00:28:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 27 Jan 2024 00:28:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:35:11 GMT
ENV JETTY_VERSION=11.0.19
# Sat, 27 Jan 2024 09:35:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 09:35:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 09:35:11 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 09:35:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 09:35:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.19/jetty-home-11.0.19.tar.gz
# Sat, 27 Jan 2024 09:35:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 09:35:20 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 09:35:20 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 09:35:20 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 09:35:20 GMT
USER jetty
# Sat, 27 Jan 2024 09:35:20 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 09:35:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:35:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211f0fe588152fd7c66ae2eeb4e636a407b03b84dd5b7f4a977eb4ce49addb6d`  
		Last Modified: Sat, 27 Jan 2024 00:35:51 GMT  
		Size: 144.1 MB (144110994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d266ad5c1ab2e4e955d550af5dc5889cfce65b291463118b558d99b8e9b5a`  
		Last Modified: Sat, 27 Jan 2024 09:39:56 GMT  
		Size: 22.9 MB (22886236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29780e53f8e51bdfed5fd47edd93b0eb7a0e340b5db7d3a486e4df5cf019ff2`  
		Last Modified: Sat, 27 Jan 2024 09:39:54 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
