## `jetty:9-amazoncorretto`

```console
$ docker pull jetty@sha256:4ed58e5e89edc57888a6df8f5d9456f0c9bd4e00562fdd316e7f3794d81a00f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:acc4933b742a9a50371a7b6eca6ca9d1baecee075b21b48a614977fa373d4e48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230291975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d82f173870a0bd9529ac7b3d5932637b2888fa138bfe00af8d1da733fc18b`
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
# Sat, 13 May 2023 03:47:20 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Sat, 13 May 2023 03:47:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 May 2023 03:47:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 May 2023 03:47:20 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 May 2023 03:47:20 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 May 2023 03:47:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Sat, 13 May 2023 03:47:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 May 2023 03:47:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 May 2023 03:47:38 GMT
WORKDIR /var/lib/jetty
# Sat, 13 May 2023 03:47:38 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Sat, 13 May 2023 03:47:38 GMT
USER jetty
# Sat, 13 May 2023 03:47:38 GMT
EXPOSE 8080
# Sat, 13 May 2023 03:47:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 May 2023 03:47:38 GMT
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
	-	`sha256:4ad6c2601f820f04ec30aba020a1e08a4ee2b37854a412cb02f2812ff93ae1d6`  
		Last Modified: Sat, 13 May 2023 03:52:03 GMT  
		Size: 15.8 MB (15821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7662e45ba61628bfad6bb52c577d4d24219417ea78e52d040c8c65c842f6cd7b`  
		Last Modified: Sat, 13 May 2023 03:52:01 GMT  
		Size: 1.6 KB (1612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6d8e2740d6d94006d4377ac72658f00f5b41383a1da2358f1fec57b4c77534a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230442698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b2c417436e162fa591473cbc5f9bc3e21a9abd9a72e7b7e3e36ab132cd1db9`
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
# Sat, 13 May 2023 04:19:54 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Sat, 13 May 2023 04:19:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 May 2023 04:19:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 May 2023 04:19:54 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 May 2023 04:19:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 May 2023 04:19:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Sat, 13 May 2023 04:19:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 May 2023 04:20:09 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 May 2023 04:20:09 GMT
WORKDIR /var/lib/jetty
# Sat, 13 May 2023 04:20:09 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Sat, 13 May 2023 04:20:09 GMT
USER jetty
# Sat, 13 May 2023 04:20:09 GMT
EXPOSE 8080
# Sat, 13 May 2023 04:20:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 May 2023 04:20:09 GMT
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
	-	`sha256:1a918db6f4d75c5b4f29849e7fea2d131296dc0287eda36943e8ca0d7c0b4682`  
		Last Modified: Sat, 13 May 2023 04:23:20 GMT  
		Size: 15.8 MB (15840042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f9942badaa07fb761d20fc80d4a60c7d0e19337243d3dff631d0512edb504c`  
		Last Modified: Sat, 13 May 2023 04:23:18 GMT  
		Size: 1.6 KB (1610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
