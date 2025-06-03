## `jetty:11-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:6ba25aa078cf0408a6dfbd5cb576c8bc38c20eb4180d2ce0ce8a8b0aa79f16b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0e5da07bf75000f669b50ab96b5e15f2dc458e8c9f0807e97ae802b192edca92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248051192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed954f0b39fc8c285cbdb89ae255bfde41f759363264d4dbc117ae4bd83676b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=21.0.7.6-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=11.0.25
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.25/jetty-home-11.0.25.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4096a50338e29bd24ebb9cc31e05a0687dcd0600d2b083c44af8d15708a07f`  
		Last Modified: Mon, 19 May 2025 23:46:13 GMT  
		Size: 164.8 MB (164842240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0071be37620889c3ce89317e3866c36456579ef15f2d75bff5a1ceefac2cc19`  
		Last Modified: Mon, 19 May 2025 23:47:28 GMT  
		Size: 20.4 MB (20447278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1735166beb6abce1a778689d0eddd5e829105101720036f5bf7cf23b909e3be2`  
		Last Modified: Mon, 19 May 2025 23:47:10 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:86b72f7e83b4a9b1e36c84b849c6377393d2207f260609b7a4ca45910435226a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a007aec5239b4136eae75a8971cb7ee51d5042457d7c694a17086b5dd78163`

```dockerfile
```

-	Layers:
	-	`sha256:3ed32b2c55d095cb9450313240cd5519e279426d37baa17ba805a569748d4da3`  
		Last Modified: Tue, 20 May 2025 02:16:23 GMT  
		Size: 5.9 MB (5920858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed280414e16f7ddc749f647ef19f793261c7a3f321d0f62afdbfb81ca415607`  
		Last Modified: Tue, 20 May 2025 02:16:24 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:306ab71e505a1838df80fc9d0ad9aa9dc71129d8e7a25ccfb71a31f8c83d3eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248046043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c603da4e4f42772b0ec60024fffdff9c48875883c4b409d74a2ea92fab43ecd7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=21.0.7.6-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=11.0.25
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.25/jetty-home-11.0.25.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5767f014b050afc587e9ad7bd97300c4413147067eec529f41a8051ad29ffd6`  
		Last Modified: Tue, 20 May 2025 00:49:43 GMT  
		Size: 162.9 MB (162936873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de885ce63f9da4c92f508cb67b4b0ab8cc1573f3075e82b80d88d11d027c4d62`  
		Last Modified: Tue, 20 May 2025 00:44:01 GMT  
		Size: 20.5 MB (20499998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d69bc49f2a4a1f3cf7bd42790a926884b874bd0e39b3d9034fbf3cc6c27f74`  
		Last Modified: Tue, 20 May 2025 00:43:56 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f17cf4e77d762e179277d3298090f69bfa725cffa501ce6f41b8ef0f74749b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5938020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9decca55d8a20772a3963288061c1f323308dd69dd14c9ee3b1a463b6ac1861b`

```dockerfile
```

-	Layers:
	-	`sha256:37d6ab605af162ea965a2c1d9e060dade7d61b87d36a95a74f515e2a62dfcdb5`  
		Last Modified: Tue, 20 May 2025 02:16:28 GMT  
		Size: 5.9 MB (5919523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfe9f6f827abf0e2a6431ed2cf0a485ea12fe8c0436a1b9dd6be2fed7aa25be`  
		Last Modified: Tue, 20 May 2025 02:16:28 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
