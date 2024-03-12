## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:e99362345692d985678f9b49421cef1aa348b7be16dbce366a6eb2ff0455f326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4d56a1e33db7bd9082318bf3b2fb490df760a971f68fd9917553c826a95be2b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235011269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da4914d831de8331e191cfce2b121717c18b116dd5d81aebc7bc77ae6a06f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:14:50 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:15:16 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:15:17 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:15:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Feb 2024 00:11:21 GMT
ENV JETTY_VERSION=11.0.20
# Tue, 27 Feb 2024 00:11:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 00:11:21 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 00:11:21 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 00:11:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 00:11:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Tue, 27 Feb 2024 00:11:21 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 00:11:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 00:11:38 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 00:11:39 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 00:11:39 GMT
USER jetty
# Tue, 27 Feb 2024 00:11:39 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 00:11:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:11:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974e4a3de7d41c914b0b9ba5df50e9c076fca509c8de9c1e6acf5112cae2ffd5`  
		Last Modified: Mon, 26 Feb 2024 23:27:18 GMT  
		Size: 152.0 MB (151993838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ccd7356e2b0d684caadfd7c8d4f687b85f13d6d441e621614b7497915e39f4`  
		Last Modified: Tue, 27 Feb 2024 00:19:36 GMT  
		Size: 20.4 MB (20369067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d8410e2c7ead98adda1067443a06cfe3fc108aeeacdf9b5c066eb6629ff2c`  
		Last Modified: Tue, 27 Feb 2024 00:19:34 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:59cd473fab09da78f5903fc884c90190a0d47c13dc47ee0d1508025b45f575f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235583169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78f3258723073bfe9da1d03a068211392d5949a8cf286428130ffb67ef28190`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:58 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Mon, 11 Mar 2024 22:39:59 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:14:27 GMT
ARG version=17.0.10.7-1
# Mon, 11 Mar 2024 23:14:45 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 11 Mar 2024 23:14:47 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:14:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 12 Mar 2024 00:25:11 GMT
ENV JETTY_VERSION=11.0.20
# Tue, 12 Mar 2024 00:25:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Mar 2024 00:25:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Mar 2024 00:25:12 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Mar 2024 00:25:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 00:25:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.20/jetty-home-11.0.20.tar.gz
# Tue, 12 Mar 2024 00:25:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Mar 2024 00:25:26 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 12 Mar 2024 00:25:27 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Mar 2024 00:25:27 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 12 Mar 2024 00:25:27 GMT
USER jetty
# Tue, 12 Mar 2024 00:25:27 GMT
EXPOSE 8080
# Tue, 12 Mar 2024 00:25:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 00:25:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d08b4648c019c286307953327f1386a50e2b199831d1433be794eeb494a0b3`  
		Last Modified: Mon, 11 Mar 2024 23:23:54 GMT  
		Size: 150.6 MB (150578296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581caa667500e83ae4b70d4355764500d9e7520870db6e985da3826046ca56ac`  
		Last Modified: Tue, 12 Mar 2024 00:31:13 GMT  
		Size: 20.4 MB (20426865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663f4a20f656abab15e2cac0698192288bfa30d0abbf4e020aa3b14f6bb9f98`  
		Last Modified: Tue, 12 Mar 2024 00:31:11 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
