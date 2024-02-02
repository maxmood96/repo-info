## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:906f317283e88761566275ad6c255918735fb33372ab2357fb922e1ecd96cb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c35f18b98857ef3b065ad48db22af1205eaee0671a196bca1d4f39fc479bde8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230502846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729dd09f234cba15724ba45ee7c02c9dd51ea885ba93465e887cc7c7b72b448b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:46:50 GMT
ARG version=17.0.10.7-1
# Wed, 17 Jan 2024 23:47:13 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 17 Jan 2024 23:47:14 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:47:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Jan 2024 01:09:41 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Thu, 18 Jan 2024 01:09:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Jan 2024 01:09:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Jan 2024 01:09:42 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Jan 2024 01:09:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 01:09:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Thu, 18 Jan 2024 01:09:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Jan 2024 01:09:59 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 18 Jan 2024 01:09:59 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Jan 2024 01:09:59 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 18 Jan 2024 01:09:59 GMT
USER jetty
# Thu, 18 Jan 2024 01:10:00 GMT
EXPOSE 8080
# Thu, 18 Jan 2024 01:10:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Jan 2024 01:10:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83abe90dca8aa1836d536330c592a7e215ec1926ce6a85fbaa1c595427323`  
		Last Modified: Thu, 18 Jan 2024 00:04:14 GMT  
		Size: 152.0 MB (151996967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe49b28b27ecab6920086c763165b0adfafda46a297df71fcd0c03cef39d7d`  
		Last Modified: Thu, 18 Jan 2024 01:21:09 GMT  
		Size: 15.8 MB (15843246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3c8f39e5f7634a4f3a9f615b32662abea2c651a1b807afa53ce1cbd0fb9beb`  
		Last Modified: Thu, 18 Jan 2024 01:21:07 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:11449ac8bb9c987fdee0bbceb7af501379aa8c7b735ee99e4c05e817ef0eae69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230883255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4368b65dbf63d2825531450b755d9ec56b956fff6e182711bec921297243e1c`
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
# Fri, 02 Feb 2024 04:34:31 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Fri, 02 Feb 2024 04:34:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 04:34:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 04:34:31 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 04:34:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 04:34:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Fri, 02 Feb 2024 04:34:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 04:34:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 04:34:47 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 04:34:47 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 04:34:47 GMT
USER jetty
# Fri, 02 Feb 2024 04:34:47 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 04:34:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 04:34:47 GMT
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
	-	`sha256:35ee8462e4e12c3fcedf41294d54c7a47cff74df7173d2b70a4be46a789755f4`  
		Last Modified: Fri, 02 Feb 2024 04:48:14 GMT  
		Size: 15.9 MB (15875779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c73dfc43701127a74a1425dd170fa8103236355f0912d2816b1381d7cb9a3c`  
		Last Modified: Fri, 02 Feb 2024 04:48:12 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
