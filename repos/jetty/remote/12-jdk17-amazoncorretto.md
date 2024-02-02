## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:c99f58ef0d2caa4753504ea663a02490c3f16765d1383f7bdaf6c870e18822b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:57955abc6ece777897e9546202e7d671681d16140fdf7759a1c622b0abc0e9aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254306571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f926af24695fc292cd7c010fdfed0c7bd66e058ce43d57ac5b99735cf18d5ca`
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
# Fri, 02 Feb 2024 12:03:05 GMT
ENV JETTY_VERSION=12.0.5
# Fri, 02 Feb 2024 12:03:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 12:03:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 12:03:05 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 12:03:05 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 12:03:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.5/jetty-home-12.0.5.tar.gz
# Fri, 02 Feb 2024 12:03:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 12:03:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 12:03:23 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 12:03:23 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 12:03:24 GMT
USER jetty
# Fri, 02 Feb 2024 12:03:24 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 12:03:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 12:03:24 GMT
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
	-	`sha256:394ef82b2cb7b52ea64664b7085087cde4deceb75d83aed8c747a17e7c03ba45`  
		Last Modified: Fri, 02 Feb 2024 12:19:35 GMT  
		Size: 39.7 MB (39677755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c360d16141aba70c56f0b7106d338b89430b14e3c98b93fceb3bb9ab4fa2fa37`  
		Last Modified: Fri, 02 Feb 2024 12:19:33 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:456e7cc2368507b872d3231f07e5cea983da5ed71abb6d86f2c021c047c94d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254768015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c0ea1bbb572b9ec09033766a91cf047a1b8a1c05e37600a12435bda357d8bc`
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
# Fri, 02 Feb 2024 19:52:27 GMT
ENV JETTY_VERSION=12.0.6
# Fri, 02 Feb 2024 19:52:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 19:52:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 19:52:27 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 19:52:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:52:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.6/jetty-home-12.0.6.tar.gz
# Fri, 02 Feb 2024 19:52:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 19:52:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 19:52:43 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 19:52:43 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 19:52:43 GMT
USER jetty
# Fri, 02 Feb 2024 19:52:43 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 19:52:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 19:52:43 GMT
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
	-	`sha256:41ba78c64686a112c1f690deeee6e6df89c6407e057477d321b6b45f637f2ffb`  
		Last Modified: Fri, 02 Feb 2024 20:05:21 GMT  
		Size: 39.8 MB (39760538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b23c06c8847f2912fb1ea791e5ea743f217bdfbf181d91ef8a264a94a95b119`  
		Last Modified: Fri, 02 Feb 2024 20:05:18 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
