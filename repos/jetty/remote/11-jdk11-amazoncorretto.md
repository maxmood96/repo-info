## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:e0a95d7b86589333d468bba705a8adddef688dec1de490a4b4abeccb8d5b7a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:cbe985e1fda43350a9ab62cb6e01cbb1253964eb6fb0f434b4ae77bb239e7778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231091171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd09c36cfcd7e296ec6315c099106fb10a66387ec90b6e28f59407db55fa3b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:31 GMT
COPY dir:5f2d6af17649be50804cc4384ca7f8357e947a564ca83834a31e4d94723f7f1e in / 
# Fri, 19 Apr 2024 22:25:31 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:52:26 GMT
ARG version=11.0.23.9-1
# Fri, 19 Apr 2024 22:52:50 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 22:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:52:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 20 Apr 2024 00:41:53 GMT
ENV JETTY_VERSION=11.0.20
# Sat, 20 Apr 2024 00:41:53 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 20 Apr 2024 00:41:53 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 20 Apr 2024 00:41:53 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 20 Apr 2024 00:41:53 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Apr 2024 00:41:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Sat, 20 Apr 2024 00:41:53 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 20 Apr 2024 00:42:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 20 Apr 2024 00:42:11 GMT
WORKDIR /var/lib/jetty
# Sat, 20 Apr 2024 00:42:11 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 20 Apr 2024 00:42:12 GMT
USER jetty
# Sat, 20 Apr 2024 00:42:12 GMT
EXPOSE 8080
# Sat, 20 Apr 2024 00:42:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 20 Apr 2024 00:42:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0b2952a75473f303233bc1034d63689122b90aa8b8fd5ebd0dced887e1c294e9`  
		Last Modified: Thu, 18 Apr 2024 23:27:02 GMT  
		Size: 62.7 MB (62650735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1476ce3593235b55da110d2f0fb96d5ac170362bebae3a9335bcde34af904efd`  
		Last Modified: Fri, 19 Apr 2024 23:06:49 GMT  
		Size: 148.1 MB (148126964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d09768ab92e340f06545c37c8b1361a48ff04a14678031447ea38672738a6f9`  
		Last Modified: Sat, 20 Apr 2024 00:49:51 GMT  
		Size: 20.3 MB (20311838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17539fffd1e7add8457896e5f66489c0f7f101b5f319594b6fd8752ef09b54f1`  
		Last Modified: Sat, 20 Apr 2024 00:49:49 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d00fef27eb5bb2a116d3877906a064717051a09d5043d87e9e8a74cf32544d15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230212791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543ece9abe321867eb32b7b52baa310f4e5a128913d891529135ac87beb3c7ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:46 GMT
COPY dir:2ba6ee739dafba609ebdf18f79a61867807b8e6e55204d714d3fea4ab910e739 in / 
# Fri, 19 Apr 2024 22:10:47 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:30:04 GMT
ARG version=11.0.23.9-1
# Fri, 19 Apr 2024 22:30:24 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 22:30:25 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:30:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 20 Apr 2024 00:01:46 GMT
ENV JETTY_VERSION=11.0.20
# Sat, 20 Apr 2024 00:01:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 20 Apr 2024 00:01:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 20 Apr 2024 00:01:46 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 20 Apr 2024 00:01:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Apr 2024 00:01:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Sat, 20 Apr 2024 00:01:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 20 Apr 2024 00:02:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 20 Apr 2024 00:02:01 GMT
WORKDIR /var/lib/jetty
# Sat, 20 Apr 2024 00:02:02 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 20 Apr 2024 00:02:02 GMT
USER jetty
# Sat, 20 Apr 2024 00:02:02 GMT
EXPOSE 8080
# Sat, 20 Apr 2024 00:02:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 20 Apr 2024 00:02:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:92f601831288d3f8f08bf8bcf02ba1eb90d12a4422c7b431f23ed0e92fc30b2f`  
		Last Modified: Thu, 18 Apr 2024 23:27:04 GMT  
		Size: 64.6 MB (64562444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ce561f0e449d5d9e976e40cdcd89f8656aaf3aa2f36fec8ab5b6156757eea8`  
		Last Modified: Fri, 19 Apr 2024 22:42:00 GMT  
		Size: 145.2 MB (145226584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6641b7f4636939934f8da599df7879bb2d6d400b25c439e7b667ee69160e0b13`  
		Last Modified: Sat, 20 Apr 2024 00:07:53 GMT  
		Size: 20.4 MB (20422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46b4977f090a74eabc95b9c31266554e2836e0ed0afb2f3edc25ac750536fcf`  
		Last Modified: Sat, 20 Apr 2024 00:07:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
