## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:b77b81467a54a97752ba1e8260b9674c8dc2e88d545055903458eed6cd647910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4bb44dfb23755e2c6af5de6e846875b3f66a1d88ebc3678aa470636e726ea8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267292111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94966910dbdfcc407c5277abcc9ebe7e356cb63a62bb73ba345692e65a2a077`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:47 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:15:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:15:47 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:15:33 GMT
ENV JETTY_VERSION=12.1.3
# Fri, 14 Nov 2025 03:15:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:15:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:15:33 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:15:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:15:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Fri, 14 Nov 2025 03:15:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:15:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:15:33 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:15:33 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:15:33 GMT
USER jetty
# Fri, 14 Nov 2025 03:15:33 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:15:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:15:33 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2eeedbb6c19345cead693cc54b4ab6b968c029966c1439c8e1b1921ecaed2c`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 152.4 MB (152415922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c40952ae0f3431bfe83be27c76175640a6613ea041f28d31037ae6499b761f`  
		Last Modified: Fri, 14 Nov 2025 03:15:58 GMT  
		Size: 51.9 MB (51943741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1db5287a0b1fefca34299c9d0b268948a73bebfb86c5e909c8024f6391ab31`  
		Last Modified: Fri, 14 Nov 2025 03:15:51 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3cf38526c5ea75ee2ce9ce0a3281454a2050d7feb19712d3b4a8789056215832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b707fb155ec1d440a0cbb1a8e6350bc53b19b6bd51251c25e5253fd17ff9a3`

```dockerfile
```

-	Layers:
	-	`sha256:c7d6446060757e16410fe86c550783d433adac9419539d8861f7ad024ba82ed3`  
		Last Modified: Fri, 14 Nov 2025 06:18:02 GMT  
		Size: 6.2 MB (6151971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477bb17b42b0d08f8d74ff655b8208142f3fe8b8fcc5c241daf6cb6b71f86d1a`  
		Last Modified: Fri, 14 Nov 2025 06:18:03 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9a4bffb86606f947027fec407abbcb54550661d1dff02b2aa65a5b945fc3a7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267791891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5703fc5dcf6dc68155c717330cf8f2bd73a1d4c11cc7ec6dc9bd4f3da9fc7e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:17 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:17 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:17:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:16:06 GMT
ENV JETTY_VERSION=12.1.3
# Fri, 14 Nov 2025 03:16:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:16:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:16:06 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:16:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:16:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Fri, 14 Nov 2025 03:16:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:16:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:16:06 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:16:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:16:06 GMT
USER jetty
# Fri, 14 Nov 2025 03:16:06 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:16:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:16:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b8742846c34daad6dea6d70c9dbb64562941f5ec5c46f8d2eb1e6eb5241816`  
		Last Modified: Fri, 14 Nov 2025 03:15:35 GMT  
		Size: 151.0 MB (150987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10126074e7492baa715937355185dbd97a482a2b21ef3e316f0872ceca11726b`  
		Last Modified: Fri, 14 Nov 2025 03:16:34 GMT  
		Size: 52.0 MB (52009222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0c45431afb1b49bc752e0d0e146f5657b7d6b2c0360f77a69ffb550ff0d1d7`  
		Last Modified: Fri, 14 Nov 2025 03:16:16 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fbd35a4b0e6fae35d0986bd332921fa88d0e4f3d4ef4b233113ed620563f4ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6f4db11fb2d13e7ccaa17227868df70df7a6aac594a6cb4d0e5958581af3e5`

```dockerfile
```

-	Layers:
	-	`sha256:01277a0976c66a54836195ac8289f57d5765d38bcc2a721103922f0516f92f3a`  
		Last Modified: Fri, 14 Nov 2025 06:18:08 GMT  
		Size: 6.2 MB (6150600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5cb66906cb60eb3335ff0810349c680413540db520fe0e3abbc45c0ff04ccc`  
		Last Modified: Fri, 14 Nov 2025 06:18:09 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
