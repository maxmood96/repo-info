## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:2c3f53b6ff5c07fedb5ef8b7447ccb5f3f54f811d7cc71cbc5a12702f727074d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:73b50bedba5f731b7afa741d374a8390d1b0428988f7e2da5a2af1248074ebb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad2b119b6d023846f67eb913541c1098b363427a6d73689e42a7c23ab31cfb6`
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
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
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
	-	`sha256:178316f11fc4fdc43f8843c0e5dd97162ac1bb60f078588ff0fe2754caec177a`  
		Last Modified: Fri, 12 Sep 2025 02:11:37 GMT  
		Size: 52.0 MB (51975181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f18ab90006899df1095cc103c974b6bd38486fd72d89f7ab7cb289bfd17fc5d`  
		Last Modified: Fri, 12 Sep 2025 02:11:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:62842623fc6e86b2bbb62f80fa29629c9837d16f92329d0c91e7ba6f29073386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6166131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fa3e848b8ed80c6cc9b897eb8f23c6b40b9dcf6b7f31ec1b582ca902623599`

```dockerfile
```

-	Layers:
	-	`sha256:6e98898c82b1d185f13a75a54f8f71aea425eb1869e3f1f115ee656f15037213`  
		Last Modified: Fri, 12 Sep 2025 05:17:57 GMT  
		Size: 6.1 MB (6148736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c72523ff8a84b33e77cc11bec946d00dea0bc5ba007ed1bc73872e25369734e`  
		Last Modified: Fri, 12 Sep 2025 05:17:57 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d3de45b76e4f490846a1c1616db0d728c2336e6e8a5433ca28eafaa7a1b138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267167875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eaa01d11684501401da0fae0cbd3a029c4637b31d42c400ef66fb68b15ba22`
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
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91b5238a9fe3179ab0c01e037bb1cee69661fce54f0a324c0ba14edb32c5934`  
		Last Modified: Fri, 12 Sep 2025 02:12:53 GMT  
		Size: 150.4 MB (150394241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f849079da8aa908843e75482ef42e498c1d4d331d8ee17cd92e6b8b655e6afd`  
		Last Modified: Fri, 12 Sep 2025 02:13:48 GMT  
		Size: 52.0 MB (51980035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc90bf942e8f7c4bab56f02a9aa2fef54cb0554b1e5bbe215a04ffcea51d789f`  
		Last Modified: Fri, 12 Sep 2025 02:13:42 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d161437343e26a14ee9fc2890f6849124f2c0fb00420e05e8fadabd584fd3d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12d57fddb47213f8e7cf7e46951ecb2007b509a99d98db5c4100c4a263809b2`

```dockerfile
```

-	Layers:
	-	`sha256:e1fe3d017e2e6816ece2e64dcff6b9c4280a512af9dcf8556a85ea5ff1fa5a58`  
		Last Modified: Fri, 12 Sep 2025 05:18:02 GMT  
		Size: 6.1 MB (6147365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a2765af266444d145a651b46440c11e5206ef09dd03fa020e6caf167e414bf`  
		Last Modified: Fri, 12 Sep 2025 05:18:03 GMT  
		Size: 17.5 KB (17488 bytes)  
		MIME: application/vnd.in-toto+json
