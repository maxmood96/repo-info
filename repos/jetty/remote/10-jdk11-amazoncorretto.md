## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:1fa79bdb2c64ae7fecab253586212ef8ebf4c7dc72399034d1db457a0357508a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c0d28fb0e9b76dfd277fda8e54f30603585f894e873f184a9f46513f61381f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227512155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017ffa6558c9f7af083d2a4fbbf8a2791925424ce4f5b0d07268a1811bf116be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:11:30 GMT
ARG version=11.0.22.7-1
# Mon, 26 Feb 2024 23:11:55 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:11:56 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:11:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Feb 2024 00:13:08 GMT
ENV JETTY_VERSION=10.0.20
# Tue, 27 Feb 2024 00:13:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 00:13:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 00:13:08 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 00:13:09 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 00:13:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Tue, 27 Feb 2024 00:13:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 00:13:26 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 00:13:27 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 00:13:27 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 00:13:27 GMT
USER jetty
# Tue, 27 Feb 2024 00:13:27 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 00:13:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:13:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a8bc6d336f73791958c91856aa0f280b15ac4fcd8dbea657011f8d50eee432`  
		Last Modified: Mon, 26 Feb 2024 23:24:59 GMT  
		Size: 147.9 MB (147934364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a215ab36d05fef929c05c9f34d9e6d6c1bc377f52b8972a0b2ed8a6afa5671`  
		Last Modified: Tue, 27 Feb 2024 00:20:30 GMT  
		Size: 16.9 MB (16929426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b71b02f6b07aaa9d401a4ac360064f4f4536197b8cec38bfb789c8b57631a1`  
		Last Modified: Tue, 27 Feb 2024 00:20:28 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f7fe915322a4eabd63fabfd7b726dc15a5a1a7de2c035693e5ee8637bc7d5834
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226617489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f0e0536b0d9b786c738e3fddc37369ddc53deb51e375fd075f35035d9590e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:58 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Mon, 11 Mar 2024 22:39:59 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:11:45 GMT
ARG version=11.0.22.7-1
# Mon, 11 Mar 2024 23:12:05 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 11 Mar 2024 23:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 12 Mar 2024 00:26:36 GMT
ENV JETTY_VERSION=10.0.20
# Tue, 12 Mar 2024 00:26:36 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Mar 2024 00:26:36 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Mar 2024 00:26:36 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Mar 2024 00:26:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 00:26:36 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Tue, 12 Mar 2024 00:26:36 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Mar 2024 00:26:51 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 12 Mar 2024 00:26:51 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Mar 2024 00:26:51 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 12 Mar 2024 00:26:51 GMT
USER jetty
# Tue, 12 Mar 2024 00:26:51 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 00:26:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 00:26:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f6b91a2f6b8e4be4797bf4e8deb57335399979d51d5765b1eb8e8158dd4226`  
		Last Modified: Mon, 11 Mar 2024 23:21:54 GMT  
		Size: 145.1 MB (145059293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb57121386293bb2afffc5ad4c4068e1bd4e44c85ff85e993d4d47cc7843095`  
		Last Modified: Tue, 12 Mar 2024 00:32:06 GMT  
		Size: 17.0 MB (16980189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc3fc95a4598f7e7f4302ed9e45634358ca9a340fbc0a0326f647431d47ce51`  
		Last Modified: Tue, 12 Mar 2024 00:32:04 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
