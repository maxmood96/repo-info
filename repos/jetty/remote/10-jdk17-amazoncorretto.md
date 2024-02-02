## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:49b17c743ecd0c5ca6b28a324eb17c2f294f081096a9ab87645106aca9666c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:178246b5043d35ccf402ff3123e4b6bfd2e1c3eb29628f4841a0203f43de3598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231540570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9509851dcc48ab19c6b50e2634b3acf5582ee7d1017ca5512d942c65909a5a24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 01 Feb 2024 23:54:01 GMT
COPY dir:2df8955a095aec5442eb78c5eb2b2d5ec8efe73514e149ef530142d09c10ab53 in / 
# Thu, 01 Feb 2024 23:54:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:41:33 GMT
ARG version=17.0.10.7-1
# Fri, 02 Feb 2024 00:41:57 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 02 Feb 2024 00:41:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:41:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 02 Feb 2024 12:05:18 GMT
ENV JETTY_VERSION=10.0.19
# Fri, 02 Feb 2024 12:05:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 12:05:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 12:05:18 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 12:05:18 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 12:05:19 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Fri, 02 Feb 2024 12:05:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 12:05:36 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 12:05:36 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 12:05:36 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 12:05:36 GMT
USER jetty
# Fri, 02 Feb 2024 12:05:36 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 12:05:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 12:05:36 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7c46e61fc0317cccadde1288fd50789f5fcc06bddf47082f5ba5894613f35b38`  
		Last Modified: Thu, 01 Feb 2024 03:07:26 GMT  
		Size: 62.6 MB (62646486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a5b4b3ba0577d3a5abe5d2151f49b917f2b765af4eba45d781c0750c35041a`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 152.0 MB (151980697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bebebb9df21236adce104018f525984a8af6e69c8109ad49b5c11be89248d9`  
		Last Modified: Fri, 02 Feb 2024 12:21:00 GMT  
		Size: 16.9 MB (16911754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7498a6b196ff74cb0eab6de3d183b175555dfc80894c47531fc8237be0f0d626`  
		Last Modified: Fri, 02 Feb 2024 12:20:59 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5c766688a757277ba1b9ca44d0840a109671d61e3096cdf00cd26fd2621a571d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231969193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc537ce49bc43c6d657bdc78d1cb6e3797a05a35bc3c07c964e183fa3b7b25ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:50 GMT
COPY dir:9aa2a0617061f7d0def778dac1581f965a33bb26f84a69dab1fef189d1a60261 in / 
# Thu, 01 Feb 2024 23:30:51 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:51:43 GMT
ARG version=17.0.10.7-1
# Thu, 01 Feb 2024 23:52:02 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 01 Feb 2024 23:52:04 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:52:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 02 Feb 2024 19:55:11 GMT
ENV JETTY_VERSION=10.0.20
# Fri, 02 Feb 2024 19:55:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 19:55:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 19:55:11 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 19:55:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:55:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Fri, 02 Feb 2024 19:55:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 19:55:26 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 19:55:26 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 19:55:26 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 19:55:26 GMT
USER jetty
# Fri, 02 Feb 2024 19:55:26 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 19:55:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:55:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:47443cfd9c92429d14dc57cc7a23137f39c4c124ae6551bb1f992c8dfbaee707`  
		Last Modified: Thu, 01 Feb 2024 08:21:29 GMT  
		Size: 64.5 MB (64453219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc9a1a8335d60be2724428ee2f6a031fbb6649441064dbdd470a3d4be58e66`  
		Last Modified: Fri, 02 Feb 2024 00:01:31 GMT  
		Size: 150.6 MB (150552624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff7b341518136d8398e07abad4ec613a86302d6359a35163282cfeb24a17024`  
		Last Modified: Fri, 02 Feb 2024 20:07:43 GMT  
		Size: 17.0 MB (16961716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc2d81b05c1793b4ba80e8987d2f7c80720793ddda1702dd94556f7a940919d`  
		Last Modified: Fri, 02 Feb 2024 20:07:41 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
