## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:f527e3d549d6d9facb832c436360e3a937900def4a0d88bd3329b757a2712f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d8418271f16cac880fdd223cb0ab8a444f048264f6c5facd5a04874d9c60bfe4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227470659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b99e37ab6b289954c948cdc4b1438ce61fc3cb8cbfb5b8d126c94343964e344`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 21 Nov 2023 03:21:54 GMT
COPY dir:ddf8ce4c235ebf92718d40c0041035b283a61cbd94b49610e57999ebc78d3ec6 in / 
# Tue, 21 Nov 2023 03:21:55 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 04:15:55 GMT
ARG version=11.0.21.9-1
# Tue, 21 Nov 2023 04:16:19 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 21 Nov 2023 04:16:20 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 21 Nov 2023 05:08:21 GMT
ENV JETTY_VERSION=10.0.18
# Tue, 21 Nov 2023 05:08:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 21 Nov 2023 05:08:21 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 21 Nov 2023 05:08:21 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 21 Nov 2023 05:08:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 05:08:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.18/jetty-home-10.0.18.tar.gz
# Tue, 21 Nov 2023 05:08:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 21 Nov 2023 05:08:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 21 Nov 2023 05:08:39 GMT
WORKDIR /var/lib/jetty
# Tue, 21 Nov 2023 05:08:39 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 21 Nov 2023 05:08:39 GMT
USER jetty
# Tue, 21 Nov 2023 05:08:39 GMT
EXPOSE 8080
# Tue, 21 Nov 2023 05:08:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 05:08:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0b4a6f011995244a95bff79a1298e83d230bc0aa22871a9c510745cafebec227`  
		Last Modified: Sun, 19 Nov 2023 03:18:53 GMT  
		Size: 62.6 MB (62641917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d619674e889e43b5933965519f238060b203fbf178c6982c91ea68fbbc6c8f7`  
		Last Modified: Tue, 21 Nov 2023 04:27:52 GMT  
		Size: 147.9 MB (147902758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9086744998e67d2cb56b53caef239ebfe68552758603fbfd89402aa0e987235a`  
		Last Modified: Tue, 21 Nov 2023 05:13:40 GMT  
		Size: 16.9 MB (16924351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec688218ad29fa7b2c6bf0338f9e3a0d10330985b8dfb6fc1be4b2bc32d1a10`  
		Last Modified: Tue, 21 Nov 2023 05:13:39 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1308bfb40af7a336cd660c7c69de4475415075ab3a0ff6e041ed0b83f080e15e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226415377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cb9ae2c76df1bd5355dc618b785c550d52b56c23b93cdfe7483b6d7d655002`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:57:53 GMT
ARG version=11.0.21.9-1
# Fri, 03 Nov 2023 22:58:11 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:58:13 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:58:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Nov 2023 23:42:27 GMT
ENV JETTY_VERSION=10.0.18
# Fri, 03 Nov 2023 23:42:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 03 Nov 2023 23:42:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 03 Nov 2023 23:42:27 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 03 Nov 2023 23:42:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Nov 2023 23:42:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.18/jetty-home-10.0.18.tar.gz
# Fri, 03 Nov 2023 23:42:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 03 Nov 2023 23:42:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 03 Nov 2023 23:42:42 GMT
WORKDIR /var/lib/jetty
# Fri, 03 Nov 2023 23:42:42 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 03 Nov 2023 23:42:42 GMT
USER jetty
# Fri, 03 Nov 2023 23:42:42 GMT
EXPOSE 8080
# Fri, 03 Nov 2023 23:42:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Nov 2023 23:42:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1caf17af52a0f5870773eff2466a3e46fd343129663aa68cfc416fa0dbd1ea`  
		Last Modified: Fri, 03 Nov 2023 23:08:27 GMT  
		Size: 145.0 MB (145033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992973199c02ab37233da0cce89950f130adc1d38b324d8f5084fe9f7bb07f67`  
		Last Modified: Fri, 03 Nov 2023 23:46:34 GMT  
		Size: 17.0 MB (17000280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753c9f915775b6abf9417e17ea37e93bae1107a74ee28a630f6caff7d2c5face`  
		Last Modified: Fri, 03 Nov 2023 23:46:32 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
