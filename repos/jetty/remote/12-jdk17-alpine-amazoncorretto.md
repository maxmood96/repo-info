## `jetty:12-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:96ba4c5ff5382d7ac8abf0ef001fd1cc2d7cb1af5674508e95e8ad6c45d245c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e9f181f316115b1e0f274526b71fe96ec2d5ebdbb1b7e186f9f64abdfacf509f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191630157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4de7b29f45e00eab6c2b226a53fbbab67176f2f7083cc918fc64fbb0e77595f`
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
# Sat, 27 Jan 2024 08:58:55 GMT
ENV JETTY_VERSION=12.0.5
# Sat, 27 Jan 2024 08:58:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 27 Jan 2024 08:58:56 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 27 Jan 2024 08:58:56 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 27 Jan 2024 08:58:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Sat, 27 Jan 2024 08:58:56 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.5/jetty-home-12.0.5.tar.gz
# Sat, 27 Jan 2024 08:58:56 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 27 Jan 2024 08:59:05 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 27 Jan 2024 08:59:05 GMT
WORKDIR /var/lib/jetty
# Sat, 27 Jan 2024 08:59:05 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 27 Jan 2024 08:59:05 GMT
USER jetty
# Sat, 27 Jan 2024 08:59:06 GMT
EXPOSE 8080
# Sat, 27 Jan 2024 08:59:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 08:59:06 GMT
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
	-	`sha256:b2589be2ad59e9316cdf3318f269729f2b0d909a8b8f6e4c3c6dd9454830d1ff`  
		Last Modified: Sat, 27 Jan 2024 09:12:33 GMT  
		Size: 42.1 MB (42146001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a61120f68971e1a7fc997418ccfa5637726a4c9e7e548cf9dbd64e12124250`  
		Last Modified: Sat, 27 Jan 2024 09:12:30 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:98b11241b5ac16a32c7fc2ba5d619ef0f997e1c888aa495c4d4033cbfde0c895
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189626548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017e506f4edff7a7500fbe29e8271e8e7f98e79186fd0f90f8f050811de61c04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 23:45:25 GMT
ARG version=17.0.10.7.1
# Wed, 17 Jan 2024 23:45:30 GMT
# ARGS: version=17.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Wed, 17 Jan 2024 23:45:31 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:45:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Jan 2024 23:45:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 18 Jan 2024 00:58:20 GMT
ENV JETTY_VERSION=12.0.5
# Thu, 18 Jan 2024 00:58:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Jan 2024 00:58:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Jan 2024 00:58:21 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Jan 2024 00:58:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 18 Jan 2024 00:58:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.5/jetty-home-12.0.5.tar.gz
# Thu, 18 Jan 2024 00:58:21 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Jan 2024 00:58:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 18 Jan 2024 00:58:30 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Jan 2024 00:58:30 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 18 Jan 2024 00:58:30 GMT
USER jetty
# Thu, 18 Jan 2024 00:58:30 GMT
EXPOSE 8080
# Thu, 18 Jan 2024 00:58:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Jan 2024 00:58:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f31e5a484e073c448f661f172a9cb84384374aec1f9129b359a533174ca958`  
		Last Modified: Thu, 18 Jan 2024 00:00:21 GMT  
		Size: 144.1 MB (144110968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df8ed97ad101cb3ab2f9fd44a2d4379a88bc4574bf8f50f8618438df09f69dd`  
		Last Modified: Thu, 18 Jan 2024 01:06:57 GMT  
		Size: 42.2 MB (42166155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bba2b324052aad550a6ffc10f8ad4a437704d18e08cf788f58f5d5a143d7dff`  
		Last Modified: Thu, 18 Jan 2024 01:06:55 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
