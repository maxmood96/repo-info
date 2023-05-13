## `jetty:10-amazoncorretto`

```console
$ docker pull jetty@sha256:552951fdbaf62541a29ef985a511da46ee65d62dbaa7dd3ff254bdc3af0dca28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:143bb3e57ae20ed76a0bc815afed29fbf7bf1eb83c12f9a04a21a3b970276571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231337517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1c5c873ae47af2b97600900384c8e73a52b16f57180f87993cfc628ea032eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 13 May 2023 00:19:34 GMT
COPY dir:7a824a76678fb4ef17879dcecd9fac65df3d1efbef31a3b874da9f49f49b6814 in / 
# Sat, 13 May 2023 00:19:34 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 01:34:17 GMT
ARG version=17.0.7.7-1
# Sat, 13 May 2023 01:34:42 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 01:34:43 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 01:34:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 13 May 2023 03:49:01 GMT
ENV JETTY_VERSION=10.0.15
# Sat, 13 May 2023 03:49:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 May 2023 03:49:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 May 2023 03:49:01 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 May 2023 03:49:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 May 2023 03:49:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Sat, 13 May 2023 03:49:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 May 2023 03:49:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 May 2023 03:49:18 GMT
WORKDIR /var/lib/jetty
# Sat, 13 May 2023 03:49:18 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Sat, 13 May 2023 03:49:18 GMT
USER jetty
# Sat, 13 May 2023 03:49:18 GMT
EXPOSE 8080
# Sat, 13 May 2023 03:49:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 May 2023 03:49:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bf72c394abb748707ec4590d5017f36ad47098c9b92adc1b04c3ea3ba0b395f6`  
		Last Modified: Fri, 12 May 2023 00:07:44 GMT  
		Size: 62.5 MB (62494714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf64cf85c039184023bdfaa7e82e8a607c7f0a55286cce0c938431af0d83d3`  
		Last Modified: Sat, 13 May 2023 01:37:36 GMT  
		Size: 152.0 MB (151974038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c231df6aee90b82fe3221356a5eeb74675555c327454a1b7c098a3cf219ba7`  
		Last Modified: Sat, 13 May 2023 03:53:01 GMT  
		Size: 16.9 MB (16867152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4c188d8154ed7054567c0f1afba39f409f306e4815ec0e34170d30e9667733`  
		Last Modified: Sat, 13 May 2023 03:52:59 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c05e793e95b18a15a0d61525ab5200863a2807a523f35ffb96d7b166a9b117c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231487991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5a8254e7ae2d2e458c51d8b34e3606757131c1054cba88daef6b3cb7313f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:31:16 GMT
ARG version=17.0.7.7-1
# Sat, 13 May 2023 02:31:36 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:31:38 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:31:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 13 May 2023 04:21:14 GMT
ENV JETTY_VERSION=10.0.15
# Sat, 13 May 2023 04:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 May 2023 04:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 May 2023 04:21:15 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 May 2023 04:21:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 May 2023 04:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Sat, 13 May 2023 04:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 May 2023 04:21:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 May 2023 04:21:30 GMT
WORKDIR /var/lib/jetty
# Sat, 13 May 2023 04:21:30 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Sat, 13 May 2023 04:21:30 GMT
USER jetty
# Sat, 13 May 2023 04:21:30 GMT
EXPOSE 8080
# Sat, 13 May 2023 04:21:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 May 2023 04:21:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7ed20885ae48fa1760360e568c1aaba07f51cc6d418715514060ff0826a40c72`  
		Last Modified: Fri, 12 May 2023 19:28:02 GMT  
		Size: 64.1 MB (64134800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f531e2cf78efc9a3808075863cbac8998096d9d52e7683e55f2b9908762bd327`  
		Last Modified: Sat, 13 May 2023 02:34:01 GMT  
		Size: 150.5 MB (150466246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7090bd5be1e53c187aa599310aa7cd6481edeb85df40e164b26feaa394e68`  
		Last Modified: Sat, 13 May 2023 04:24:13 GMT  
		Size: 16.9 MB (16885334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6607f14960027581bba8db0acdc25c25b5d78050eb985d075717f9d878683539`  
		Last Modified: Sat, 13 May 2023 04:24:12 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
