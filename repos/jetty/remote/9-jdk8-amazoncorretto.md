## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:2208a6971d068e7c9f47987969a23444a94f50333c0ff9caa3fb33f939b529d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a54f0725ecb15491545ef3b9ae1c297839fe29c3dbb4ddb5dc05a6bdf0450592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153871963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3afdde244e78d2eb9049b8912f18707c3891e6a735789553c408d2b0ae1fc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:39:03 GMT
ARG version=1.8.0_382.b05-1
# Tue, 29 Aug 2023 19:39:23 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:39:24 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:39:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 29 Aug 2023 20:34:47 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Tue, 29 Aug 2023 20:34:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 20:34:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 20:34:47 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 20:34:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 20:34:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Tue, 29 Aug 2023 20:34:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 20:35:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 20:35:06 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 20:35:06 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 20:35:06 GMT
USER jetty
# Tue, 29 Aug 2023 20:35:06 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 20:35:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 20:35:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2777c08acd60bdc608943c816f90f481bd66683594a52f6a9338c94fb0dd386`  
		Last Modified: Tue, 29 Aug 2023 19:52:03 GMT  
		Size: 75.6 MB (75579654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f4a53963353f8f2ce3fd68fd4449723fdb1ac41fd5c84da4e2017d941313ac`  
		Last Modified: Tue, 29 Aug 2023 20:40:42 GMT  
		Size: 15.8 MB (15813413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d1dfd79bd8b6b5e78c74faa0f110958d215eb75047c97e4eb9c85bed5e2908`  
		Last Modified: Tue, 29 Aug 2023 20:40:41 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f1cd326ec416f9d9593ab5d6f29b8de9fb5a87ef8b29df12e4a1c4968d26f702
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139615948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f2bbb342162f3bdfd5c220da179847cf73d83a1afb1cbbd982d6f3a04cbbc5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:06:26 GMT
ARG version=1.8.0_382.b05-1
# Tue, 29 Aug 2023 19:06:42 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:06:43 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:06:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 12 Sep 2023 22:47:15 GMT
ENV JETTY_VERSION=9.4.52.v20230823
# Tue, 12 Sep 2023 22:47:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Sep 2023 22:47:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Sep 2023 22:47:15 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Sep 2023 22:47:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Sep 2023 22:47:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.52.v20230823/jetty-home-9.4.52.v20230823.tar.gz
# Tue, 12 Sep 2023 22:47:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Sep 2023 22:47:32 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 12 Sep 2023 22:47:32 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Sep 2023 22:47:32 GMT
COPY multi:04e96d62b43d0ed55ad32900f133ff3fa46502048db2c67b0ea7a783ed3acc37 in / 
# Tue, 12 Sep 2023 22:47:32 GMT
USER jetty
# Tue, 12 Sep 2023 22:47:32 GMT
EXPOSE 8080
# Tue, 12 Sep 2023 22:47:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Sep 2023 22:47:33 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fa55c5082bb206f57cd8989ecad654c6a065d7edbc3380b023251441fc467f`  
		Last Modified: Tue, 29 Aug 2023 19:16:21 GMT  
		Size: 59.6 MB (59622084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e14cc176c1ea4a387f37c52ba7d6f2952de08db86b3ac3be03f1b29740c0502`  
		Last Modified: Tue, 12 Sep 2023 22:57:22 GMT  
		Size: 15.9 MB (15862249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fead8f584e525a6b0999eb31bb52389363b8c553fe2e08b3c25d7f55e487e552`  
		Last Modified: Tue, 12 Sep 2023 22:57:21 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
