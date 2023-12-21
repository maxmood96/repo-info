## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:2c6588f2991d81987a7ad3e40874b898c7b49408c60ea68a4fe24b0cc6c03d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4c4a87e19035734cb2a7cbe0f5266133eafd79df6c0acfaf131798a19b3ef404
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267807826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac16fc4a19dd7cfcd8c759e35464b229a5682d7790ac6a51453941ea58d595b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:40 GMT
COPY dir:7964ac201a93d838933b1631de52186ab9a9c98f572a75fd024299ea94e621fa in / 
# Wed, 20 Dec 2023 08:49:41 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:34:16 GMT
ARG version=21.0.1.12-1
# Wed, 20 Dec 2023 09:34:42 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 09:34:42 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:34:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 21 Dec 2023 18:48:04 GMT
ENV JETTY_VERSION=12.0.5
# Thu, 21 Dec 2023 18:48:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 21 Dec 2023 18:48:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 21 Dec 2023 18:48:04 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 21 Dec 2023 18:48:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Dec 2023 18:48:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.5/jetty-home-12.0.5.tar.gz
# Thu, 21 Dec 2023 18:48:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 21 Dec 2023 18:48:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 21 Dec 2023 18:48:25 GMT
WORKDIR /var/lib/jetty
# Thu, 21 Dec 2023 18:48:25 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 21 Dec 2023 18:48:25 GMT
USER jetty
# Thu, 21 Dec 2023 18:48:25 GMT
EXPOSE 8080
# Thu, 21 Dec 2023 18:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Dec 2023 18:48:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:99e9b04a7dc206f4a47a0937a2039102066a5273ce57a11fa6894d90fe3957bc`  
		Last Modified: Wed, 20 Dec 2023 08:50:39 GMT  
		Size: 62.6 MB (62645506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d69575b1919324e459c53eb060a89444609036d59e675ac3d43b37d16fb5c`  
		Last Modified: Wed, 20 Dec 2023 09:44:22 GMT  
		Size: 165.5 MB (165482992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988cc2109df90236890d5969b33c8a5b4b7516066bffb622556dab0af7deb40`  
		Last Modified: Thu, 21 Dec 2023 19:13:08 GMT  
		Size: 39.7 MB (39677694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38fbd1befcb11bc92efe1d45c610c707f6288e12ba430d7843d03648d47045`  
		Last Modified: Thu, 21 Dec 2023 19:13:03 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c03de9b3232bb952a5944f1f1b8ba49b11448884d2a00dc30d8c0199f7da66ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267602405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b3b007aaebf869985a93251a4a4f2596142a948ea7b686b77d51e382b535f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:23 GMT
COPY dir:380956fd469c5bff2cfd19545c66184d8301b431f1a3cd9c8338b2680a7f7a2b in / 
# Wed, 20 Dec 2023 01:32:24 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 02:03:17 GMT
ARG version=21.0.1.12-1
# Wed, 20 Dec 2023 02:03:36 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 02:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:03:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 21 Dec 2023 17:49:40 GMT
ENV JETTY_VERSION=12.0.5
# Thu, 21 Dec 2023 17:49:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 21 Dec 2023 17:49:41 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 21 Dec 2023 17:49:41 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 21 Dec 2023 17:49:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Dec 2023 17:49:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.5/jetty-home-12.0.5.tar.gz
# Thu, 21 Dec 2023 17:49:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 21 Dec 2023 17:49:58 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 21 Dec 2023 17:49:58 GMT
WORKDIR /var/lib/jetty
# Thu, 21 Dec 2023 17:49:58 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 21 Dec 2023 17:49:58 GMT
USER jetty
# Thu, 21 Dec 2023 17:49:58 GMT
EXPOSE 8080
# Thu, 21 Dec 2023 17:49:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Dec 2023 17:49:58 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1cdee3d784afc8dc3a31863ea6b75bfb24c3394d454dd5ca221d29fbd4c3f130`  
		Last Modified: Wed, 20 Dec 2023 01:32:56 GMT  
		Size: 64.4 MB (64445029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e5cc04f4f8dfd375c063dcc6d958a6dc857009c80ea17f993b7d7531f2a4d3`  
		Last Modified: Wed, 20 Dec 2023 02:11:53 GMT  
		Size: 163.5 MB (163453040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb972271ab7c7b37563bc7805fa58868634575fffb7a019861eba07186a371dd`  
		Last Modified: Thu, 21 Dec 2023 18:04:58 GMT  
		Size: 39.7 MB (39702703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abb3f8ca265c3ce94186dbc6b5842b8a0a39c98c857773c618e10144b94b26d`  
		Last Modified: Thu, 21 Dec 2023 18:04:55 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
