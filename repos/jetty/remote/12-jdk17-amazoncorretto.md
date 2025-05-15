## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:f7a4c46b3014a1f7d41c957cbd82bb20ac1cd0eabd9970430232b95cee266267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:68ac2bb0588731f2cb23354331b7254e4edf2be2ddbd0f9e75272147cb2c7c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255133405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d3d2bbd3478eaccf34960c9944369107c8f78ab74deb1df94764b2a9a3dc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 01 May 2025 13:44:39 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7644a5b45425fc2fbfa8e6bb1a403f455554900a76632970cb35ea38247c2354`  
		Last Modified: Thu, 01 May 2025 21:08:04 GMT  
		Size: 151.8 MB (151763434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b8275bf5051b790fe2b0cb73b8b860023777b87e877554a30d08617c83e81b`  
		Last Modified: Wed, 14 May 2025 19:01:34 GMT  
		Size: 40.6 MB (40608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71ee8732f0b7dcc0e52d912f82f63805b3d9d18b33beab6c410607801c82e9c`  
		Last Modified: Wed, 14 May 2025 19:01:34 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7258499bcaf9f3a99ea2278217fcbf5b0aeb76dc3bf540cd85ce7cca071a3c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6045497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a250c5e6b438cf8f9c1bc9bd3417117ab264604cd68dc818102b495095bcdc43`

```dockerfile
```

-	Layers:
	-	`sha256:63b0946fe7eefedee6f35f9326b0e29815fc1144a623634c6537fd2bebb6398f`  
		Last Modified: Wed, 14 May 2025 19:01:34 GMT  
		Size: 6.0 MB (6028096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e306068638ac1a4b53428e517e73af7bfa5a5ee58f37909858927fd0a524a5`  
		Last Modified: Wed, 14 May 2025 19:01:34 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:03e39456002fb3b7f2a8b53b3ea58d6d0d3aaf00ddb095ec61c6611cee4c8180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255618216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a927731bd677100a1452abd376bd358ba13adc39af3ff54e8d9f5a8f687ed25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 01 May 2025 13:44:52 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42101b5e9c297f73effd5de79bf61ca74d0240232f5a85af7bf4dd89bbaa448c`  
		Last Modified: Thu, 01 May 2025 21:15:57 GMT  
		Size: 150.4 MB (150375851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a1ae432e901e1785ffda9f8ecfe27af4dc182aa9a3e464a9e2e855be75336`  
		Last Modified: Wed, 14 May 2025 19:28:58 GMT  
		Size: 40.6 MB (40645946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fbe9735f4fda9da0d55cc17b56b139b35a0f146d4a05a8fcdb8c676a000369`  
		Last Modified: Wed, 14 May 2025 19:28:57 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:24d1b73c7644caf6730cf94f4ce5f0b5a7958ed844eeb994708bdf4bc6420a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6044218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96942228bb3eda396cc86ba92539d19f0b0823946cd0ff19369dab483fad63f8`

```dockerfile
```

-	Layers:
	-	`sha256:bdeb820f5afd48be1689d0e0eb5e4f1c0f8a5e1ec2b863e039daffe7d4dee8de`  
		Last Modified: Wed, 14 May 2025 19:28:57 GMT  
		Size: 6.0 MB (6026725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa256d13bde447433ee3cd97daa45a96abe7c78d2310798bcab429076e0def14`  
		Last Modified: Wed, 14 May 2025 19:28:57 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
