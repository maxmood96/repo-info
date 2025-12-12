## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:2b84d634a8cb521ea0e76e1f6582ad357db8cf7ae55b8f6413c95b723a501cd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4abb141b8c60077839c6425b3d0530a114c02301dec129ec41d0d80c80b8ec4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235899965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcef53e479c5048fedaec3ae0fd336d02af361f5b72efdd09d9152a4dccf56f`
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
ENV JETTY_VERSION=11.0.26
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
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
	-	`sha256:5b5234720a5b5ef1c60d4cd5a5b8d7648011cf6dd6828fd236501b284da16333`  
		Last Modified: Thu, 11 Dec 2025 22:20:04 GMT  
		Size: 20.5 MB (20539389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad644efc02feae058d013392067204df988eae0d31138ae97e9befa0447e4b1a`  
		Last Modified: Thu, 11 Dec 2025 22:20:01 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:26909f7a691aea83618848af2a83f95d726427e79e7426999d788c5fcb205dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b676b758abab27e19cd91b1b8c785cf808691b48c9ce77336d241c89ba6abc`

```dockerfile
```

-	Layers:
	-	`sha256:4811e769661eafa0a989ab8c0f6ab411761936372abdb3262677f373cee58f8f`  
		Last Modified: Fri, 12 Dec 2025 00:16:53 GMT  
		Size: 5.9 MB (5928977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437fef164057da4796af73204d0c092bdaf6f9a49b5795d24c51a862ba11ea69`  
		Last Modified: Fri, 12 Dec 2025 00:16:54 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d5f3ba75da8bfa9beb30fad4bb6829ee80f906da720d0e7d536fddf3c562a2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236378004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4ca0ff4174cd6d9848dcc7f6fa17d1878bca088dfc9d3b973348c03feeb1ef`
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
# Thu, 11 Dec 2025 22:19:30 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 11 Dec 2025 22:19:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:30 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 11 Dec 2025 22:19:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Dec 2025 22:19:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Dec 2025 22:19:30 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Dec 2025 22:19:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Dec 2025 22:19:30 GMT
USER jetty
# Thu, 11 Dec 2025 22:19:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Dec 2025 22:19:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Dec 2025 22:19:30 GMT
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
	-	`sha256:3a55a919ba31543c9d800205714444b9a416459b269b89dc9e27b3749057bacc`  
		Last Modified: Thu, 11 Dec 2025 22:19:49 GMT  
		Size: 20.6 MB (20591244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e663d836a32a903fdf4283300f68cadb543808b59d13449359a67523172cdc3`  
		Last Modified: Thu, 11 Dec 2025 22:19:47 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ac569f7bdb9076380f5bcc3b86d6d09132afba1b0b3fd70e0b07795e7fd080a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cc027053fbee1f6f87641237e1d5cef860c38be7186d909c8103a0f23df6b3`

```dockerfile
```

-	Layers:
	-	`sha256:799604341c850124df236e3707c7818a7fda15dde97f146d411ace4c467b4d60`  
		Last Modified: Fri, 12 Dec 2025 00:17:00 GMT  
		Size: 5.9 MB (5927606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfe638ef5ca1036bb0d1c3ba47e19f54ad6e8f4a27d036c64370cfcb828f182`  
		Last Modified: Fri, 12 Dec 2025 00:17:01 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
