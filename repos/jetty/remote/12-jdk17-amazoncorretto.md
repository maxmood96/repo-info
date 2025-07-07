## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:ec6f8d3473fc76ce6ecd4ebc9c1a8a6d797d785343efd53ea2f1186abf3c03d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a41e5d2394ecfa513efe1b821b1ce01ed8ee4e8974b94a7b12b49150621c2c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255365182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7107e76350aa1089f77bb48c3c2bd2a0a29adf1905c0883a4149e00bef911`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_VERSION=12.0.23
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.23/jetty-home-12.0.23.tar.gz
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Jul 2025 05:13:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Jul 2025 05:13:52 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Jul 2025 05:13:52 GMT
USER jetty
# Fri, 04 Jul 2025 05:13:52 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 05:13:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Jul 2025 05:13:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82300c0b516b05fd33e5ee80103c72571455470c886da1e8007c97667bd2b934`  
		Last Modified: Fri, 04 Jul 2025 00:15:23 GMT  
		Size: 151.7 MB (151747120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0cfe589b0a1afc903e49d7a28c4891ae1be6bfda8d7a1ac379e1b845965ded`  
		Last Modified: Mon, 07 Jul 2025 19:12:45 GMT  
		Size: 40.7 MB (40653516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5537117f24cb26eab4bd16209b457eb28e391053d297630e2fec251dd0ff50b4`  
		Last Modified: Mon, 07 Jul 2025 19:12:43 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1103ce3b92dc212c1a22cffb5b5351c796d5812be382680f7ce7d9611e739bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba08c66d95c6e4c3d4f5b7f986fb75709c88ca016d426f5ad4ae0b2de07d2d`

```dockerfile
```

-	Layers:
	-	`sha256:76f3ea9765bae975a1729c2c9e2dd396c8b8da5342090c699637def707512b97`  
		Last Modified: Mon, 07 Jul 2025 20:17:29 GMT  
		Size: 6.0 MB (6040789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e5f2e1ec52c87c67d97386eaa5d5103ebd4426ce8dd8c03cc05e59ba1d921f`  
		Last Modified: Mon, 07 Jul 2025 20:17:30 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:284b4902530db1554f76288a300070813da349db8daa9858e3731e0eba95f683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255856967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab629fb2070cfef6f354d5c9274473dcd0fd3022500332799f85443866ebb7ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_VERSION=12.0.23
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.23/jetty-home-12.0.23.tar.gz
# Fri, 04 Jul 2025 05:13:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Jul 2025 05:13:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Jul 2025 05:13:52 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Jul 2025 05:13:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Jul 2025 05:13:52 GMT
USER jetty
# Fri, 04 Jul 2025 05:13:52 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 05:13:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Jul 2025 05:13:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:409bf1beed8b3d18aa6739b3b654d78ea6e9842b177c58b3fde860845eae1b51`  
		Last Modified: Wed, 25 Jun 2025 19:30:21 GMT  
		Size: 64.8 MB (64794781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee2fa749893f0ce39dd63ca3a593cb0caf15b6f548f79d56d28fac7ec9a8d3`  
		Last Modified: Fri, 04 Jul 2025 03:17:04 GMT  
		Size: 150.4 MB (150391853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23663ba1e5a977e5f66dbd1755d98e2eb938c08af73c1c1165a197f5b6ba5ab`  
		Last Modified: Mon, 07 Jul 2025 19:20:34 GMT  
		Size: 40.7 MB (40668641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2b0c2f9cac35685201e7c5a16740d6cef9946fcd2259bf4415518af489be50`  
		Last Modified: Mon, 07 Jul 2025 19:20:32 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:55b471e45f75151d8988abb7f246cd3e23b441578cc0ca721bfad8e2b324c028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86e73e54d7c5ae430004af550ab328829bbfcf492ccbf4ac223c308a3062b2`

```dockerfile
```

-	Layers:
	-	`sha256:f36f3f8a8e5cd20d53e6aeab0079b06b2b0b6295de03c78e175db5500ee1691a`  
		Last Modified: Mon, 07 Jul 2025 20:17:35 GMT  
		Size: 6.0 MB (6039418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d19dfc403f185784d5b6fc2d3b204435589fd36c2f72d5b47a9461003034ca3c`  
		Last Modified: Mon, 07 Jul 2025 20:17:36 GMT  
		Size: 17.5 KB (17492 bytes)  
		MIME: application/vnd.in-toto+json
