## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:399641a94bf197b17f7c8a89ada3a518d9983e465326d2e182402e2954d2545c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8959ee1badf64f13e32220ea8f96ce6e17f08d7bc5bf8576edc195239171fe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228088631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07fa82c2e404426ef1cf783c306d10db16caba33d7c3400f8a514471da69abc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:15:32 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:15:32 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:15:32 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:15:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 18 Dec 2025 02:21:25 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 18 Dec 2025 02:21:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:21:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:21:25 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:21:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:21:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 18 Dec 2025 02:21:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:21:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:21:25 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:21:26 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:21:26 GMT
USER jetty
# Thu, 18 Dec 2025 02:21:26 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:21:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:21:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4f683ce2c9610d4a5cc89f4a3c26c0ce0688221e68fb73c40fa11f54463fc`  
		Last Modified: Thu, 18 Dec 2025 02:20:01 GMT  
		Size: 148.1 MB (148051302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435234b976aa795f61ec64287ee48dd5928a0a1f3635b178cedcb63a50e2f95`  
		Last Modified: Thu, 18 Dec 2025 02:21:45 GMT  
		Size: 17.1 MB (17094478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7749d33619507419d50501c6b5d55c6e9fe3c536f4b2c2d29819dc3fb0f088`  
		Last Modified: Thu, 18 Dec 2025 02:21:43 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4e5aa437ae3b53b946ca6cd3da62d2aa871f6f75b32e571631b5188f8e05ea43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619bee72b074a7e7fdde3a5a6f61573f88ccd7de7a1d464c712c6e12291c92e6`

```dockerfile
```

-	Layers:
	-	`sha256:d0c3d4baf151279f85760466e272bfc759032af994e885664ae42948d239d214`  
		Last Modified: Thu, 18 Dec 2025 06:15:34 GMT  
		Size: 5.9 MB (5936228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc493ca5466f96a8b8e9920d77704fe5dac43810e0cbfed9abb27ebb81c8b8a`  
		Last Modified: Thu, 18 Dec 2025 06:15:35 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4a6f7344da3f00da208fdf5685071452ee634d5aeb1d7e5f60975279bbe3d4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227082910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f5ceecdb61308951331da7a1f30ee3b2c06488d7b72ef38550525b128fdf19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:22 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:25:22 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:25:22 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 18 Dec 2025 02:21:42 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 18 Dec 2025 02:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 18 Dec 2025 02:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:21:42 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:21:42 GMT
USER jetty
# Thu, 18 Dec 2025 02:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5109e3d25f889e8daddd5fe4018cff5eb742c43e4eebb8d37a493f68a4628ad6`  
		Last Modified: Thu, 18 Dec 2025 02:20:42 GMT  
		Size: 145.1 MB (145144730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3559edba67832fb9910531095c26993f47456f25fe6d6bde2da99d994f45fb1`  
		Last Modified: Thu, 18 Dec 2025 02:22:04 GMT  
		Size: 17.1 MB (17140548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1601ec5516a7e1ae6993281a1c1c0e772b2c1545f9ac6a4f6c5b0805b57c1b1`  
		Last Modified: Thu, 18 Dec 2025 02:21:59 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:edf279f80515f4a7230976b3c1e96e6ac464321a37ce78d59d27ab717d049f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3664646be789db56295762885cb69e6a20df84c490d3d3eba58d7552128d8733`

```dockerfile
```

-	Layers:
	-	`sha256:8c627eddced04415ed427b0e9cede6d80aa58e2f118417ad54052904c6f3b10f`  
		Last Modified: Thu, 18 Dec 2025 06:15:44 GMT  
		Size: 5.9 MB (5935662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fbf3c221ca33d843c3d150e5895e1fce0a8b3668cda5341a39b77b7fc0b18a`  
		Last Modified: Thu, 18 Dec 2025 06:15:45 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json
