## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:c9e7273317f1dbd709441d5991854f9fd1db9d74d682b2cfb461a738d36f952c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:bf51fd253a4fd25afa6594fb5fe13c9a21fdaa8f2770eac7209fa9bb47d18dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232454841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1b611a5eed6544ee831b524274b12dc19ee98b9f41fd7ec5b0d44ae4a6b86e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:25 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:25 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:25 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Dec 2025 22:19:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Dec 2025 22:19:46 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Dec 2025 22:19:46 GMT
USER jetty
# Thu, 11 Dec 2025 22:19:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Dec 2025 22:19:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Dec 2025 22:19:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac57126ecd86ebc8bfbf2f8c72cef47008c2e2b42c706b3d2d81f5f916ccec5b`  
		Last Modified: Thu, 11 Dec 2025 22:13:15 GMT  
		Size: 152.4 MB (152417728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1694de6740a13396162756584b09690c50a082ee421de62a298556b3680010d`  
		Last Modified: Thu, 11 Dec 2025 22:20:12 GMT  
		Size: 17.1 MB (17094261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd500c89d4bbb580d245b7e9e4888297564a48aadb7b247cbf314026eaf6111f`  
		Last Modified: Thu, 11 Dec 2025 22:20:01 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:85be4af2728a4189567fa79545d5e0aba3a3aa3c76bbbd73e6d3370a49aaca2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994dec12160058ad79e08bcac71d478c15598328adad38fb20aa15d27e50807e`

```dockerfile
```

-	Layers:
	-	`sha256:c7b9db9410891cacc97cff8390aa7068fecbb476c5c6ad92f7795034662b0233`  
		Last Modified: Fri, 12 Dec 2025 00:15:39 GMT  
		Size: 5.9 MB (5928927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143c16efe2539e2109aded31ef15c92ebbe203880b46daa8dfe21508f6539805`  
		Last Modified: Fri, 12 Dec 2025 00:15:40 GMT  
		Size: 17.4 KB (17357 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ec9afbc1b176ecf7b261f837be00c1b1e8498381c85eaf7aa4d9513359da96fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232935963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617faa820489278ccf7e486d3ed5d3d62599a0b6e7ba25ffdd7dbccad92557c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:02 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:02 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:19:43 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 11 Dec 2025 22:19:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:43 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 11 Dec 2025 22:19:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Dec 2025 22:19:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Dec 2025 22:19:43 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Dec 2025 22:19:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Dec 2025 22:19:43 GMT
USER jetty
# Thu, 11 Dec 2025 22:19:43 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Dec 2025 22:19:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Dec 2025 22:19:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67bc37dbe272db9b7b10c3283dea952f31754f43ec167dae43bf6ef83012ea9`  
		Last Modified: Thu, 11 Dec 2025 22:12:56 GMT  
		Size: 151.0 MB (150989128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4508433cf0e079e7c9d0adbe32d439c7519aebb5da33f4f1a74406c298b7c2d`  
		Last Modified: Thu, 11 Dec 2025 22:20:01 GMT  
		Size: 17.1 MB (17149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d3358ec4040af086f6d054ab1c0be2b7a6eebfbe7e6163d097b3f009939f32`  
		Last Modified: Thu, 11 Dec 2025 22:19:59 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bab81446afb782db0e6792cf69f5517755f3aceb43f07db1e695e0beda2df6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7b7c9fd49a9a7e36d4bf984be876af94da93e520d9bc383d30f42db1335333`

```dockerfile
```

-	Layers:
	-	`sha256:73053d752dc410155dda9c77446cf2af5ec34aa83938d0983f68e7b59b454196`  
		Last Modified: Fri, 12 Dec 2025 00:15:46 GMT  
		Size: 5.9 MB (5927556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3955ad597ca9677a8f7647fb7774de40c39b3d8e62557c20e7332ab9cd27e03`  
		Last Modified: Fri, 12 Dec 2025 00:15:47 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
