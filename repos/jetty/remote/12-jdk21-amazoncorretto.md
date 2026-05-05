## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:fe53a061c9b6e03ae908a33d14d4e6f21f8e9bb29f9648f8e08fd32ab8ee70a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:078b1031abb813a44150b746277b6e5644c5de237da55935715736c5722e8760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280360587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfd95260b57fc4e6637c7207e65db85c42186d46fd9c2b47a2c2776ffb896f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:29 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:29 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:29 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 04 May 2026 20:43:01 GMT
ENV JETTY_VERSION=12.1.8
# Mon, 04 May 2026 20:43:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 04 May 2026 20:43:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 04 May 2026 20:43:01 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 04 May 2026 20:43:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:43:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Mon, 04 May 2026 20:43:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 04 May 2026 20:43:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 04 May 2026 20:43:01 GMT
WORKDIR /var/lib/jetty
# Mon, 04 May 2026 20:43:01 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 04 May 2026 20:43:01 GMT
USER jetty
# Mon, 04 May 2026 20:43:01 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 May 2026 20:43:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:43:01 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34427ac8245f2bc54ae2269830d743a78c73c94138af0501660e55c8b91be1ff`  
		Last Modified: Mon, 04 May 2026 20:12:51 GMT  
		Size: 165.7 MB (165695557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df377e6f610fd39c0440b82342a834f057a211cb7cf65d47eda8ca71e0d93120`  
		Last Modified: Mon, 04 May 2026 20:43:16 GMT  
		Size: 51.8 MB (51803145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bc72e7225bdea72080e9b703f62e57245707db416f9bed85e99934f5702d30`  
		Last Modified: Mon, 04 May 2026 20:43:14 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:41c85de50b2542d65c5fc8021eefb3c0629b441bc1237038c844e1eabe4f9f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6167264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674060989a0779b03f85a3f0bb5b54a1f1bbb23729825e551a7a1ec57c6eabd1`

```dockerfile
```

-	Layers:
	-	`sha256:eed29306e3f3b640078d1f02b0c01d27afe161cc9e797ff62bb3a46f407a2752`  
		Last Modified: Mon, 04 May 2026 20:43:14 GMT  
		Size: 6.1 MB (6149913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d032628a2dde9ca87432d7f4ae25acc2f76f9b8c267be33d05f8d408d7244dc`  
		Last Modified: Mon, 04 May 2026 20:43:14 GMT  
		Size: 17.4 KB (17351 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:7105163f0da19214f250df41388b5411b63fba8bb0f841223f2a7838807dd524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280596136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ecc1426757eb60d1947bee9cedb00a21b7f07f7d9fffbbf6bc5964872b2b2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:07 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:07 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 04 May 2026 20:43:20 GMT
ENV JETTY_VERSION=12.1.8
# Mon, 04 May 2026 20:43:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 04 May 2026 20:43:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 04 May 2026 20:43:20 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 04 May 2026 20:43:20 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:43:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Mon, 04 May 2026 20:43:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 04 May 2026 20:43:20 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 04 May 2026 20:43:20 GMT
WORKDIR /var/lib/jetty
# Mon, 04 May 2026 20:43:20 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 04 May 2026 20:43:20 GMT
USER jetty
# Mon, 04 May 2026 20:43:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 May 2026 20:43:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:43:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdfcdf3bd2c92c2567fd8412ee72fbd46db7b157b9d64a0f969635bd1431a4a`  
		Last Modified: Mon, 04 May 2026 20:12:31 GMT  
		Size: 163.9 MB (163902837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd98a4a43c0a751b3a4782db79ac4d7f5106f4fda05f81cbdb9d4832373516`  
		Last Modified: Mon, 04 May 2026 20:43:35 GMT  
		Size: 51.9 MB (51895892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d990aea4571699ff5692e8915691ec700761af414a74002046dcf8cdad3c1`  
		Last Modified: Mon, 04 May 2026 20:43:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9c783b103ae8ae282d388e24f3d6c8cabace0b75b1d63af7adc061e56c183df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6165987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880ee26aabf3a51c83588c995e84462a26962054e5eaa748c1f7f898a8770e01`

```dockerfile
```

-	Layers:
	-	`sha256:588087467a879745e0bcac5a5207c307ba776dcf3703a1b608a2e4d96479204a`  
		Last Modified: Mon, 04 May 2026 20:43:33 GMT  
		Size: 6.1 MB (6148542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9dfa7106be47401c7d98c72270289998d6b435a6818cb71c29af3ead4658f2`  
		Last Modified: Mon, 04 May 2026 20:43:33 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
