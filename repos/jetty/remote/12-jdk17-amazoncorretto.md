## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:55706e1c4605e5049398332b7e224ad7c374100f1f842e995a999462501855ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2d8d0cc963bb5641b8041c11b4e2b99502bddecebfeeab9c7c004ec3165c53f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267439438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2011adddc4abe14251fbf4345bb990e24387b2a25f10e8fa5a45854d1c54a2e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:15 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:15 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:19:33 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 21 Jan 2026 19:19:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:19:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:19:33 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:19:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jan 2026 19:19:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 21 Jan 2026 19:19:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:19:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:19:33 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:19:33 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:19:33 GMT
USER jetty
# Wed, 21 Jan 2026 19:19:33 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:19:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:19:33 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d09c36562c02e291fec0cd8d510ab0c206591e85dce9cebfe7fe6bd12f6006`  
		Last Modified: Wed, 21 Jan 2026 19:00:36 GMT  
		Size: 152.5 MB (152462935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcf774a21744b8958d52bd0ffcd5d01fcadc7eaf5a876af6fe462a5cb2f6d0`  
		Last Modified: Wed, 21 Jan 2026 19:19:47 GMT  
		Size: 52.0 MB (52034470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a17a3f103d5caacfb57effc1289f0b25c29a790b458ee2a4b71aad92fee99`  
		Last Modified: Wed, 21 Jan 2026 19:20:08 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:61fa9acb0f3e92a85f696cf6713f577636e782b0f23b5e9e258a4691b5366628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e9d5f80f059691e8cbdd1c77e849e02673e557ca937d4833035e5870c8f2b`

```dockerfile
```

-	Layers:
	-	`sha256:d79f8350f230d32fceaad04df66ecb51ea74e2c673c6117f3256b64dd5a98183`  
		Last Modified: Wed, 21 Jan 2026 21:19:08 GMT  
		Size: 6.2 MB (6151943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406eb4d9fd02d5474c08acba46c398ef6d3f48b99ab56d49e598abe92315e18f`  
		Last Modified: Wed, 21 Jan 2026 21:21:23 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c82052283c173c38819abfde36c0f68a8fcb6b0a664d96666d1791e425ae8fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267835464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef53c5dd01775284a4782f49ca333f841d01d4679ffe789c448303f27ce73c3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:19:24 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 21 Jan 2026 19:19:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:19:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:19:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:19:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Jan 2026 19:19:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 21 Jan 2026 19:19:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:19:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:19:24 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:19:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:19:24 GMT
USER jetty
# Wed, 21 Jan 2026 19:19:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:19:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:19:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da03988e890a2734422b08930678b55aacec1ee085bede5e1b18f8c3f898b33e`  
		Last Modified: Wed, 21 Jan 2026 19:00:37 GMT  
		Size: 151.0 MB (150985142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d7ed89c405ab6b94bee04d0a0f49de1de1815980e7c9b0497a84abf813c200`  
		Last Modified: Wed, 21 Jan 2026 19:19:39 GMT  
		Size: 52.1 MB (52078012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb18f030c436cd3a7ed82773e466ed8624f9ad78d028a114abb5b4f80f29670`  
		Last Modified: Wed, 21 Jan 2026 19:19:35 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e6836c98a31c4a853e31342073395f62993449df6478585943d79af132f20ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03d5b016bd8ee3e590368c4337b9a9e23d7dc9a1207be0082bf7023a8d80758`

```dockerfile
```

-	Layers:
	-	`sha256:789efcc1370ae990d3c9e75040fbad8ea6d9627c59bcdf4a2608267688e1305a`  
		Last Modified: Wed, 21 Jan 2026 19:19:38 GMT  
		Size: 6.2 MB (6150572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90fbeb5a9e5dff0859e02df05b7a909a9b2fd97357cff4d75ab5f3d4b2c501f0`  
		Last Modified: Wed, 21 Jan 2026 21:19:47 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json
