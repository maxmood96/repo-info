## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:55c3e7b09f759a0859e8907bb3485b05982a21c7299817df902ec912bf2d91b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:23e1403d7075f2ba0d6537b1ee1bafe6a2ba15b1b0d50bedd04230d746a42b35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254355201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9b793c101f575f5b8f7542b7fff0ea909a5c6e892c58c5e026e39e427d96a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:14:50 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:15:16 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:15:17 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:15:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Feb 2024 00:10:27 GMT
ENV JETTY_VERSION=12.0.6
# Tue, 27 Feb 2024 00:10:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 00:10:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 00:10:27 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 00:10:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 00:10:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.6/jetty-home-12.0.6.tar.gz
# Tue, 27 Feb 2024 00:10:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 00:10:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 00:10:45 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 00:10:45 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 00:10:46 GMT
USER jetty
# Tue, 27 Feb 2024 00:10:46 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 00:10:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:10:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e4a3de7d41c914b0b9ba5df50e9c076fca509c8de9c1e6acf5112cae2ffd5`  
		Last Modified: Mon, 26 Feb 2024 23:27:18 GMT  
		Size: 152.0 MB (151993838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1257837bff0090244a91587cc44031eb1693fabf0259b5be378943bd0c942d`  
		Last Modified: Tue, 27 Feb 2024 00:19:02 GMT  
		Size: 39.7 MB (39712998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba13758df21598e1c0b4827cb8e10c8fff573308b0e752e28dc8b222513ee7d`  
		Last Modified: Tue, 27 Feb 2024 00:19:00 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1ac962ae4ccaa567f12b1033c04d74918091623c7237611ba770e0e5df78463b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254934231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e00bd47d38eff3c947ca1539510f0669672041ee0aa05b67dba4b6ffb4233`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:58 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Mon, 11 Mar 2024 22:39:59 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:14:27 GMT
ARG version=17.0.10.7-1
# Mon, 11 Mar 2024 23:14:45 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 11 Mar 2024 23:14:47 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:14:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 12 Mar 2024 00:24:29 GMT
ENV JETTY_VERSION=12.0.6
# Tue, 12 Mar 2024 00:24:29 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Mar 2024 00:24:29 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Mar 2024 00:24:29 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Mar 2024 00:24:29 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 00:24:29 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.6/jetty-home-12.0.6.tar.gz
# Tue, 12 Mar 2024 00:24:29 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Mar 2024 00:24:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 12 Mar 2024 00:24:44 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Mar 2024 00:24:44 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 12 Mar 2024 00:24:44 GMT
USER jetty
# Tue, 12 Mar 2024 00:24:45 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 00:24:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 00:24:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d08b4648c019c286307953327f1386a50e2b199831d1433be794eeb494a0b3`  
		Last Modified: Mon, 11 Mar 2024 23:23:54 GMT  
		Size: 150.6 MB (150578296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7517196186e7d10040b7f974109f5ef536125a7eafd0291670319c2b64550579`  
		Last Modified: Tue, 12 Mar 2024 00:30:43 GMT  
		Size: 39.8 MB (39777929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0f0488d2e43c995d2372458e2f605447cfc62c6f3a01689f8d78d79f23b1ca`  
		Last Modified: Tue, 12 Mar 2024 00:30:41 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
