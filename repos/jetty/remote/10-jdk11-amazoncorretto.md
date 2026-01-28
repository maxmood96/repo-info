## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:d6a4be9360c270da110febb157072e04a214c215e601618998ad4af4486b0ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a8759361b224fdfd250e6eb196e3827f2dd666a4ba29d249cfa1cf15fa35b7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228221745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b116cba31bbaaca90860352e0d12ba0faf83811b7e5f35870066c535ff8c5f8b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:41 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:12:41 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:41 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:11:35 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 27 Jan 2026 23:11:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:11:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:11:35 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:11:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:11:35 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 27 Jan 2026 23:11:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:11:35 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:11:35 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:11:35 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:11:35 GMT
USER jetty
# Tue, 27 Jan 2026 23:11:35 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:11:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:11:35 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab537c006158cb59c0f5895965cca6f481a368f6abb61f4e81c796777a9eed5`  
		Last Modified: Tue, 27 Jan 2026 22:13:02 GMT  
		Size: 148.1 MB (148131195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53f2d99266d0e47f40937874ab776aa6c33f099e2b3ad5755ef7be543d8ec23`  
		Last Modified: Tue, 27 Jan 2026 23:11:47 GMT  
		Size: 17.1 MB (17124965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4780cc753436c2cb4949082a37ead3b1499080e94dfccf09fdbe363f852b0d0c`  
		Last Modified: Tue, 27 Jan 2026 23:11:46 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7b33ee813f76353b5275e0646bafc6b96a37ee33b41afcce0c632c0f7287ac1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af373cf61a36f0cf1e81a15f2bf04d70d6a64162c7a5555a8eb475a2790030cd`

```dockerfile
```

-	Layers:
	-	`sha256:50c51e36cf4e716994ec0551f46b332d8c8fc6033c5a38b11df0b262465f84d0`  
		Last Modified: Tue, 27 Jan 2026 23:11:47 GMT  
		Size: 5.9 MB (5936228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aa7110da6bb1e7735f79e7e09011fc1eb9df8ab0cbe02787da079100f8574f`  
		Last Modified: Tue, 27 Jan 2026 23:11:47 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:095b618754b2e8a4f91c5a3336eb9493f17ba5ba1c7d02a2f6ac493d33622a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227182687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec56bd654646ce154013d7077b83e6616996349c86967bd595bbd7bb06bd83b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:39 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:11:39 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:11:39 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:14:04 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 27 Jan 2026 23:14:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:14:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:14:04 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:14:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:14:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 27 Jan 2026 23:14:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:14:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:14:04 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:14:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:14:04 GMT
USER jetty
# Tue, 27 Jan 2026 23:14:04 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:14:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb2c67e2d580b2ad17d6de4766ea5018821f410e94f6e448143ef2823d1e4c8`  
		Last Modified: Tue, 27 Jan 2026 22:12:00 GMT  
		Size: 145.2 MB (145224244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeca41b0d9193f1d9d6711c0dbc565be9fd006523eefd989403d77bd9fdde46`  
		Last Modified: Tue, 27 Jan 2026 23:14:15 GMT  
		Size: 17.2 MB (17157680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a07ee74e93e33d8da9b0057aefcc0b3dccc6ee4c17afa99a6b7bf4a4e1b1e`  
		Last Modified: Tue, 27 Jan 2026 23:14:10 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:33e308eb8428c302b7b518ef154269ffa59c42871ebb5472255c2112ac95b9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5571be6448f8fded56229e567c2f0bc02cfd2935cbde04ca5653c480a7eaaa30`

```dockerfile
```

-	Layers:
	-	`sha256:1cc72decb20defe47e85820092437f32968dc7b8bb74549f51e2cf6a30804cb5`  
		Last Modified: Tue, 27 Jan 2026 23:14:15 GMT  
		Size: 5.9 MB (5935662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391efbb1cd9a0e545930ae3c48b0e5f7aa4e404e7cfe5e51a1b28dd601397cc9`  
		Last Modified: Tue, 27 Jan 2026 23:14:14 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
