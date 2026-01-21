## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:40e74ecd1bac0e3ff3be141a44068632e2c7422b8c23948583ef49f7b21bb28c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0668c9c35fc2388dff6bcb3a809532fda5b4aa0284871970966a7467976cd577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227237281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d5c9b156f15f25eaf747f283cbe877c0b34493609b69dceff2b1579edbae96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:18 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:07:18 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:07:18 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:07:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:10:18 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 15 Jan 2026 23:10:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:10:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:10:18 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:10:18 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:18 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 15 Jan 2026 23:10:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:10:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:10:18 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:10:18 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:10:18 GMT
USER jetty
# Thu, 15 Jan 2026 23:10:18 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:10:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:10:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9521458adcf521dd7a9c6b42b4e553ccd70b13a33dc1ad4265a9df22b4de0`  
		Last Modified: Thu, 15 Jan 2026 22:07:37 GMT  
		Size: 148.1 MB (148064451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830dce4448cd6e5e9d4c305c58198b9bb00c3148601e0650c045d8e4902dfad3`  
		Last Modified: Thu, 15 Jan 2026 23:10:39 GMT  
		Size: 16.2 MB (16230798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6884d79eaac80aa7498de38ed67d709eee3102b3a65d59028b837761ff606b3`  
		Last Modified: Thu, 15 Jan 2026 23:10:34 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:66f381eedf967d910800ced984e749cda4797775c0abd460cbb36c2a3f0a2e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6d789e3c681949dcbcb1dfec009e2ad688313e5fd01a535e45540baacd827a`

```dockerfile
```

-	Layers:
	-	`sha256:9d48bf521979c02c39d522b71953a45dd7b7559515c4420158329aba8958880d`  
		Last Modified: Thu, 15 Jan 2026 23:10:28 GMT  
		Size: 5.9 MB (5921989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d022530bda1a23be5999a5121385bc38270101e453eba241c811d8513469e952`  
		Last Modified: Fri, 16 Jan 2026 00:20:39 GMT  
		Size: 17.4 KB (17388 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f92f8c295fb6c0a47aa91c437737063cd6b46750226b646fbaeee593a4990694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226196293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc712ce90642cb5458e8dda3717b8e3d93c24179bc86a6d50f508472eac55ec8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:47 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:06:47 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:06:47 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:06:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:17:20 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 15 Jan 2026 23:17:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:17:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:17:20 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:17:20 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:17:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 15 Jan 2026 23:17:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:17:20 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:17:20 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:17:20 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:17:20 GMT
USER jetty
# Thu, 15 Jan 2026 23:17:20 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:17:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6024b7b4e65480aa98d6c15d028da54111bf46413a4c558ce0fdc28ad5d6500b`  
		Last Modified: Thu, 15 Jan 2026 22:07:08 GMT  
		Size: 145.1 MB (145142605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19120c32826f102946e23aa159de208634767f20783f955deafc7754ce7f691c`  
		Last Modified: Thu, 15 Jan 2026 23:17:53 GMT  
		Size: 16.3 MB (16281378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf789bc47fdcb9964f7704e370ddcc96691654a41bd1c8b886db9733176f1e5`  
		Last Modified: Thu, 15 Jan 2026 23:17:31 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ed25e9ff40bb6faf33d0b813f614bea5ec2fdf3f6948b8f188dad8613f4d8b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5938903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfc53de5d3dd8d5930e56a6713653ad5df166bd22cf3578a4471a48d8fd9e7c`

```dockerfile
```

-	Layers:
	-	`sha256:ec6863605e7ee55bd082042c7bcbc424ba2620e201a39be6b3a44c76cd4e8761`  
		Last Modified: Fri, 16 Jan 2026 03:26:07 GMT  
		Size: 5.9 MB (5921423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda09f64e94d53a6af9c0cb2a8310ac0244ca590a7c4fb6158cd486d7fc0eded`  
		Last Modified: Fri, 16 Jan 2026 03:26:08 GMT  
		Size: 17.5 KB (17480 bytes)  
		MIME: application/vnd.in-toto+json
