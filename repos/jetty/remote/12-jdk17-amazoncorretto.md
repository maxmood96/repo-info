## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:66e2cde80de41e13e35cba4c79ed358927bcb5268f09984977a59f26578cd7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c2e853e7de38069502855afac7f19aee2816670e0487f8e4fb1687fce90e19f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255010034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6d4061038e89d12405091d314b4ed791d16ec1506fc910925088f23bcfddb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:47:22 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 17:47:47 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 17:47:47 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:47:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 20 Jun 2024 19:21:11 GMT
ENV JETTY_VERSION=12.0.9
# Thu, 20 Jun 2024 19:21:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:26:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:26:15 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:26:16 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:26:16 GMT
USER jetty
# Thu, 20 Jun 2024 19:26:16 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:26:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:26:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122220135d78584f57387e7ed3c95af6a688def4b291d8e18a3e77cb35441cd`  
		Last Modified: Thu, 20 Jun 2024 18:21:17 GMT  
		Size: 152.1 MB (152144847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2969b613bb6d6fd41be26ee6c76129b6928252a8c14f464ed0f354a43b8ce8`  
		Last Modified: Thu, 20 Jun 2024 19:53:17 GMT  
		Size: 40.2 MB (40217101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b2d9bf24a4669a3af3733275400f9068b4d0528170281c653f5e7f97ad064`  
		Last Modified: Thu, 20 Jun 2024 19:53:14 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:067ac44d6ea9e9efcd9485f5e410588ec0d86152f9328e60159cc238f5a59eb6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255714105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e386a1ec4536d08148d18bb00b9d68f59104b942349f719bd51ec0515c02fae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:33:01 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:33:19 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:33:21 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:33:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 05 Jun 2024 07:51:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 05 Jun 2024 07:51:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Jun 2024 07:51:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Jun 2024 07:51:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Jun 2024 07:51:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:51:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 05 Jun 2024 07:51:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Jun 2024 07:52:02 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 05 Jun 2024 07:52:03 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Jun 2024 07:52:03 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 05 Jun 2024 07:52:03 GMT
USER jetty
# Wed, 05 Jun 2024 07:52:03 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:52:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:52:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3c637a564c65c75ae813e2f950aa58a12afb7e860d4acd055a45c8698317c`  
		Last Modified: Wed, 05 Jun 2024 02:43:45 GMT  
		Size: 150.8 MB (150797207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1b4d5ffc63c22270485066ce0ae1869be8a2a52ad8c4ab20eb46ecdd78e83a`  
		Last Modified: Wed, 05 Jun 2024 08:04:37 GMT  
		Size: 40.3 MB (40339823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2104fb969599de3f72abca1d4017b71a11b01fc892b19b6955dc7cb114f662`  
		Last Modified: Wed, 05 Jun 2024 08:04:35 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
