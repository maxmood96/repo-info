## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:48952252d6d9acbcb31a5bcc8021724abf0f3f9f67596d1ab0da9cbd66a99551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ca31689613b510d0bc7e46c0ec704913fa50b5fc5693f855355d0a875c2bad0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230654477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d11a83d59a80546be4aa161ec4e1a9e796123936c6e4d92d14822f3e228dca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 22:23:20 GMT
ARG version=11.0.20.9-1
# Fri, 08 Sep 2023 22:23:45 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 08 Sep 2023 22:23:46 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:23:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 08 Sep 2023 23:21:59 GMT
ENV JETTY_VERSION=11.0.15
# Fri, 08 Sep 2023 23:21:59 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 08 Sep 2023 23:21:59 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 08 Sep 2023 23:21:59 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 08 Sep 2023 23:22:00 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2023 23:22:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Fri, 08 Sep 2023 23:22:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 08 Sep 2023 23:22:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 08 Sep 2023 23:22:18 GMT
WORKDIR /var/lib/jetty
# Fri, 08 Sep 2023 23:22:18 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Fri, 08 Sep 2023 23:22:18 GMT
USER jetty
# Fri, 08 Sep 2023 23:22:18 GMT
EXPOSE 8080
# Fri, 08 Sep 2023 23:22:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Sep 2023 23:22:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2beb3689f7212f7dc37c727b16dbf363543f2f36a1b21afff731c3f71e89da`  
		Last Modified: Fri, 08 Sep 2023 22:34:44 GMT  
		Size: 147.8 MB (147814905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaaba0ca7985d4002c054224f0892d158af2290be89b229329b6e0e866258ae`  
		Last Modified: Fri, 08 Sep 2023 23:29:04 GMT  
		Size: 20.4 MB (20360676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd868e6c70c39efce7616befda042acac5ca3d97ca87899c045a3bd89b92b34`  
		Last Modified: Fri, 08 Sep 2023 23:29:03 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:46e011df7d641ee0eeb4f0fc3bede7016e480db917864cfc2050599ea395a5f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229436812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d7bb9f9d77e1bb29a2e4ba9483e3fe2362629c8d816f44c9af4dbe8aa48c7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:42:11 GMT
ARG version=11.0.20.9-1
# Fri, 08 Sep 2023 21:42:32 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 08 Sep 2023 21:42:33 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:42:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 12 Sep 2023 22:48:53 GMT
ENV JETTY_VERSION=11.0.16
# Tue, 12 Sep 2023 22:48:53 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Sep 2023 22:48:53 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Sep 2023 22:48:53 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Sep 2023 22:48:53 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Sep 2023 22:48:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.16/jetty-home-11.0.16.tar.gz
# Tue, 12 Sep 2023 22:48:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Sep 2023 22:49:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 12 Sep 2023 22:49:08 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Sep 2023 22:49:08 GMT
COPY multi:04e96d62b43d0ed55ad32900f133ff3fa46502048db2c67b0ea7a783ed3acc37 in / 
# Tue, 12 Sep 2023 22:49:09 GMT
USER jetty
# Tue, 12 Sep 2023 22:49:09 GMT
EXPOSE 8080
# Tue, 12 Sep 2023 22:49:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Sep 2023 22:49:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c9ca958d143c7af3c3a576bc2cc78206b0b882d65dc8ac65c21eb4ba5f51f0`  
		Last Modified: Fri, 08 Sep 2023 21:52:09 GMT  
		Size: 144.9 MB (144934731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3befc868d5e9160f16e8651f7cd05e460af077881e0c53851e3933ab1554a95e`  
		Last Modified: Tue, 12 Sep 2023 22:58:39 GMT  
		Size: 20.4 MB (20370466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d6c4abb289b00ea2c83afb1ccd2ba5fddc174857bdef07062b1e5acadad512`  
		Last Modified: Tue, 12 Sep 2023 22:58:38 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
