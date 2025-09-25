## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:fb4e7cf663ed6d54c474ee10e3ceac685c01ba65c4de14b8edba3b3d3da919b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d47147d077a4de9643c1eac9e608d2652b4de8e4cd3eb82948a406fcb37efeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235448300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260e21b97895f22194c1cf848e536fd36688d84a6c4192d777f867b61fa4b823`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9366c5e7bd5a6d2a9b3c3bd58e67cb4e92dc15ea766d757f065f39f426a045`  
		Last Modified: Fri, 12 Sep 2025 02:10:25 GMT  
		Size: 151.9 MB (151889560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6419859afb8042b2934c55c54e5e3fb0eec7014d10eb76e502c8007f861a8674`  
		Last Modified: Fri, 12 Sep 2025 02:11:28 GMT  
		Size: 20.6 MB (20573577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f971ad87d11c08751ec85d51a1c8e6854df43b0fc57c80290a19552d0c4ee8e`  
		Last Modified: Fri, 12 Sep 2025 02:11:22 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f1529164b379621b9d012afde2e53a04d1e9de1b0fdfc2ea493a0b976fdecdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0810afa9b0efcb21ada4eee891f4cc86df22aa88b0aee4f83be4aec5803578`

```dockerfile
```

-	Layers:
	-	`sha256:ca1ddfc278491b7156e9c3a6e41b771d5982ef60e6db7f449bc2844dc2d0e1b7`  
		Last Modified: Fri, 12 Sep 2025 05:16:51 GMT  
		Size: 5.9 MB (5925742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e7729dbc6e5d4dedc5e269aa9b4aa8dffec816e756740eadab796e2bb80298`  
		Last Modified: Fri, 12 Sep 2025 05:16:52 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ab715924c068f4f805ae458cc158824c69388a6be2aa728b1d309fd19412e919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235764352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75e2678c70a227027c6078ceb5130443edca05618a56b5572d96f1473b6f6de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 19 Aug 2025 02:05:55 GMT
COPY /rootfs/ / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 02:05:55 GMT
ARG version=17.0.16.8-1
# Tue, 19 Aug 2025 02:05:55 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5799c11fcb9bea8c5f9b4a5d739394e37910fc3fdaeef7102c5e1f03bf0c50`  
		Last Modified: Wed, 24 Sep 2025 22:13:02 GMT  
		Size: 150.4 MB (150393249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4437671a97f1444c67c37c44a7efb70de6e89b2c5d9501231bc59e92fd0131`  
		Last Modified: Wed, 24 Sep 2025 22:14:09 GMT  
		Size: 20.6 MB (20576080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad15c7f5f99b9cdb16cb74c17bc7c7cd1928c1117407beb668f92b3d2997cb11`  
		Last Modified: Wed, 24 Sep 2025 22:14:07 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d6a10d6c4b4d483dcc05bf7fbfe1c54004cac692f040c4ed8786b29944e8a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5941864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80450dca03af5b98ee12ecc72adbb23ad6a77ce235d3b7b38847641e8439bcfc`

```dockerfile
```

-	Layers:
	-	`sha256:8dac098623b632e4aa0ac3a99d7b14f0a2a76649bf10d72d0a4cead0c7316588`  
		Last Modified: Thu, 25 Sep 2025 02:16:52 GMT  
		Size: 5.9 MB (5924371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c1f071732ed6c874b296be42d467c615eaf33276780e8bf4222eaec9bda4a4`  
		Last Modified: Thu, 25 Sep 2025 02:16:54 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
