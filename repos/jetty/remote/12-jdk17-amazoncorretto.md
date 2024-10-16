## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:f3a80301abcea15e3b02143b8163167f8d06590bf1edef288521fe67597f7ffb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a7ae1e1492dd1997669c2394135403b3d9bdd5ff23fbd2a58c17033770f25e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254729068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d05771bddc20d4f48668d5a310aa8a4e6b920626399457f620e0e748c41f309`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 02 Oct 2024 21:05:31 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 21:05:31 GMT
ARG version=17.0.13.11-1
# Wed, 02 Oct 2024 21:05:31 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=C.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_VERSION=12.0.14
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
WORKDIR /var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
USER jetty
# Wed, 02 Oct 2024 21:05:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca355396aebf98936fe82454d6efbaa1bc21150c55e00a00c4b49f6c82762`  
		Last Modified: Wed, 16 Oct 2024 17:56:35 GMT  
		Size: 151.6 MB (151613285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc78314773fd3f95bfd26c226ef4d8b1f314aa57da9e95d8c926ed416160b762`  
		Last Modified: Wed, 16 Oct 2024 19:00:52 GMT  
		Size: 40.4 MB (40435961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf63de406e0529d1dcb985f97656914501b2c4f0ac0c191a273d37afa882cdc`  
		Last Modified: Wed, 16 Oct 2024 19:00:50 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:eda420b7d79f69ac6419f59132246a237cd6dc7667e9fe1f283abc3ff8deb818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6047413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea0963d6c6e74bbcd3883f08e05ceccec7c8edc59d4fe6f6badbbe70e49bebd`

```dockerfile
```

-	Layers:
	-	`sha256:6f53d92d958f44385a11e4213e08cac685643074aa38400022829955f98a51e1`  
		Last Modified: Wed, 16 Oct 2024 19:00:52 GMT  
		Size: 6.0 MB (6030244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132bed00202dd61c7cf23cc02c02b16f0327cc05a13ff07afb78156b094c6ac1`  
		Last Modified: Wed, 16 Oct 2024 19:00:50 GMT  
		Size: 17.2 KB (17169 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:642b46be4243f4b6796714b0f2dfa2ef1c63ca472ae2ef529c2f5746ee40cc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255378467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745d4c523bf1293ff7d2d47b18b583a9cb3e37ae1dbbbabe6b07bb6f104afd51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 02 Oct 2024 21:05:31 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 21:05:31 GMT
ARG version=17.0.13.11-1
# Wed, 02 Oct 2024 21:05:31 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=C.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_VERSION=12.0.14
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
WORKDIR /var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
USER jetty
# Wed, 02 Oct 2024 21:05:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1838150d7adba5669a255ff6f5d5072e4b6b849ddfb9fa3b51929eb6fd4b9d6`  
		Last Modified: Wed, 16 Oct 2024 18:20:20 GMT  
		Size: 150.2 MB (150244887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d80ac460c37480b64fb2434161b06c4d0827a1d937dfe2911b0599187415d2`  
		Last Modified: Wed, 16 Oct 2024 20:03:40 GMT  
		Size: 40.5 MB (40539255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce8e9ddb0139e96211bc583608524c12adf265bf7322218b8e7575b513235f1`  
		Last Modified: Wed, 16 Oct 2024 20:03:39 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f46e546c5a1d9119e929132902dd83c9d781421028e5c08e01414b0bfa30ae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6046132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c234b92cbcb640d16b150143103239ae7c4718c1b531faa1f7538c536ce1f8`

```dockerfile
```

-	Layers:
	-	`sha256:c3e1d6a9393d6073d16736fd4820d23b8de67c3983ab2d8873602d50660399bd`  
		Last Modified: Wed, 16 Oct 2024 20:03:39 GMT  
		Size: 6.0 MB (6028871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea7af0223d623e1997c83c1d0c3933ff02fb3eca300613ff93d15d0deb8102d`  
		Last Modified: Wed, 16 Oct 2024 20:03:39 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json
