## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:6fd4f281f50df3f607896440088d3d608fa3cc0e115ee8d97d3c5b10f74fa202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b723bc779b348dba9647500036559f682d7f03273481f24098c1d46e1371bb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232475095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b078a069781a47e281b0df2418961ddd7e4a27a444f985a0bef92ff177ccab8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:07 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:09:07 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:09:07 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 15 Jan 2026 23:15:18 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 15 Jan 2026 23:15:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:15:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:15:18 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:15:18 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:15:18 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 15 Jan 2026 23:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:15:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:15:18 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:15:18 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:15:18 GMT
USER jetty
# Thu, 15 Jan 2026 23:15:18 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:15:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:15:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b2373aa952072c4a2f4627407327ebe36b371e8477839d8f30e5669d37509`  
		Last Modified: Thu, 15 Jan 2026 22:49:20 GMT  
		Size: 152.4 MB (152425245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110efa453dc891e75e4f401ba4f477708a5c086e1e7530aa9c708d22f62b2b2`  
		Last Modified: Thu, 15 Jan 2026 23:15:37 GMT  
		Size: 17.1 MB (17107817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3d175325fd6bba187f48866b86bf53ebb1aaa0c1b0456ca99e54d1ba4be8f1`  
		Last Modified: Thu, 15 Jan 2026 23:15:36 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:38fafe9da97880de53ac6a1e3116dd5da61e926745ce20f49bbf1825d1c2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b12401ec8b8b3652e548498e3f48ef9c72957f702142f0f3bf89d4f73153f5`

```dockerfile
```

-	Layers:
	-	`sha256:cfdf20dc503f6a4c2459cfaa1e8dc08b3ecdf106011bcdc4a25217cfc86fe3ce`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 5.9 MB (5928927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74550d99bd10b30cfe9ee6fc54d1b048c592749568239dea3adce4a3b5d698b8`  
		Last Modified: Thu, 15 Jan 2026 23:15:30 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:68ade907d287629bdcc55d01fce19ad626f43a064a44fbb354902b3ee1748ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232900812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8bc954d00bc7631014d42c600bd7d0484eec86196f0598f7b4a574f3664123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:09 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:08:09 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:08:09 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 15 Jan 2026 23:20:50 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 15 Jan 2026 23:20:50 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:20:50 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:20:50 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:20:50 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:20:50 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 15 Jan 2026 23:20:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:20:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:20:50 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:20:50 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:20:50 GMT
USER jetty
# Thu, 15 Jan 2026 23:20:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:20:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:20:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b7da1ac0542372ade529b0109964dae17b785436e8afabb79539d076a5733`  
		Last Modified: Thu, 15 Jan 2026 22:09:02 GMT  
		Size: 151.0 MB (150976986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdb774ba1a4a55ae1388a2e29f9581856a22c327ca48a91e1c6e29d63583dec`  
		Last Modified: Thu, 15 Jan 2026 23:21:07 GMT  
		Size: 17.2 MB (17151516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d363c50ad6fd6c2aa628ff30763537b358c0465c1129e1a041dc30dcc8deaec`  
		Last Modified: Thu, 15 Jan 2026 23:21:06 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1084bd05d0a846531496cc01fab85f4a004df9d403c2c5c2026eb00c9114c521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fed5245fd5884539325c5dcd5abe2d3e5c23adc3392c4837ec5fd0f469b822`

```dockerfile
```

-	Layers:
	-	`sha256:74954c21c0eecd51ea56b85723f0c67ab95757c04029c01217154537591993f4`  
		Last Modified: Fri, 16 Jan 2026 03:16:59 GMT  
		Size: 5.9 MB (5927556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e466c28f357aeb0623dfc27323cf74235a4881310c2b9ab8f236e55865513cc5`  
		Last Modified: Thu, 15 Jan 2026 23:20:59 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
