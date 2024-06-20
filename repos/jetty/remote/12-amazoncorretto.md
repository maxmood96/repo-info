## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:aec07945638c3f94dcebf342d4ba9bce5ac2fffd20fa84d9e1cd1e6aded045a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:53488a6f80382834fa4cd588ee5850def123b1ea09fcff5222411fae452ee68e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a670f5bd5dcfea98f165021d7d58badd02d498b0638de35e70710947ec12e824`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:51:24 GMT
ARG version=21.0.3.9-1
# Thu, 20 Jun 2024 17:51:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 17:51:49 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:51:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 20 Jun 2024 19:20:44 GMT
ENV JETTY_VERSION=12.0.9
# Thu, 20 Jun 2024 19:20:44 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:20:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:20:45 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:20:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:20:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Thu, 20 Jun 2024 19:20:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:21:05 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:21:05 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:21:05 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:21:05 GMT
USER jetty
# Thu, 20 Jun 2024 19:21:05 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:21:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:21:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6587bf502e0fddfa3d71e42fc5be22a5dada226ab4e30f31f4c34ed43581b965`  
		Last Modified: Thu, 20 Jun 2024 18:23:58 GMT  
		Size: 165.7 MB (165682272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5a5131ccc8ed1951a57977b490973848a17f6ce441ee2f99a576e32c7eb494`  
		Last Modified: Thu, 20 Jun 2024 19:52:57 GMT  
		Size: 40.2 MB (40216633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13944dd4ebdeb8fc9d0496c3207169e3c3757e714a41cbf2b86c92e03914e41`  
		Last Modified: Thu, 20 Jun 2024 19:52:54 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:aa1e6fb8357ec2f1542e0f56745a7a5715cb9864c4f433393b2dd77a85270321
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268665859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046e5d60cb62696c2266efc3add91e49840eaed5cc667dc65b203f6c321a1ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:36:03 GMT
ARG version=21.0.3.9-1
# Wed, 05 Jun 2024 02:36:22 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:36:24 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:36:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Jun 2024 07:51:26 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 05 Jun 2024 07:51:26 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Jun 2024 07:51:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Jun 2024 07:51:26 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Jun 2024 07:51:26 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:51:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 05 Jun 2024 07:51:26 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Jun 2024 07:51:41 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 05 Jun 2024 07:51:42 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Jun 2024 07:51:42 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 05 Jun 2024 07:51:42 GMT
USER jetty
# Wed, 05 Jun 2024 07:51:42 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:51:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:51:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22eb46e585a9749ebf27644a669f43b430553a5e83c39e1f6219d51b8a62684a`  
		Last Modified: Wed, 05 Jun 2024 02:45:58 GMT  
		Size: 163.7 MB (163748486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da18537ad06b4274f835659c27b827678525af4e89cf484076279628461035ae`  
		Last Modified: Wed, 05 Jun 2024 08:04:20 GMT  
		Size: 40.3 MB (40340298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190428c4e295944ef288e636b7ede250ae4ebf87db4fda6b435b8e9d13ce4a30`  
		Last Modified: Wed, 05 Jun 2024 08:04:17 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
