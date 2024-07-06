## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:977aa789dd4a05ee977f4565ac358acc459af4730c2374a0fa1ad75bf4ec19a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ccddef63537536048a665d9ba04ee9bbc85633f867528c680eefc72aad4c050c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255010075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff84b1089c33b98f53169e15b266585e7efcb5867977e38203d2b640a6be779d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0ce019b7b27729d4754008c4f426f161bb31458181f76946dfc3d8e418db80`  
		Last Modified: Fri, 05 Jul 2024 19:56:53 GMT  
		Size: 152.1 MB (152144730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc932e960b287d8e789cf50c3eced533f855c966075596254a291b462959b41`  
		Last Modified: Fri, 05 Jul 2024 20:52:08 GMT  
		Size: 40.2 MB (40217040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24668de818520f9e9760f7bbca4a66d90f5f93b0028dfe5a22aa59b9f25418`  
		Last Modified: Fri, 05 Jul 2024 20:51:51 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f7fc6a02ecfb5e0b0fe4286c54293f73d7225079a60cd08265f548cfcc9fcbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3f6486cf45304370641fccad5bdf420bd810ca0fdbba62d11a347085cda551`

```dockerfile
```

-	Layers:
	-	`sha256:40ad12c4d177bcc178e4708b904b66787c9bbcafef52aacf2bb4c14e13545c7f`  
		Last Modified: Fri, 05 Jul 2024 20:52:11 GMT  
		Size: 6.0 MB (5981518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f3e0cab748c0af516eed45e1cdb8eaf4e51e0ee8a7911f5fc41d27bd1d5ee3`  
		Last Modified: Fri, 05 Jul 2024 20:52:06 GMT  
		Size: 17.1 KB (17126 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:bb7a1e3dff9ab9be6d0285936afd65742f979811c2001d0437d6e41a84f8c0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255697008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e427339474d53c23e26549c6d2ac4d49075931729c6943f6b3ab61c4882421f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148beaaf5ef179ffe00e9048d05bb7fe674473d25c7902dd76e938135b1a72db`  
		Last Modified: Fri, 05 Jul 2024 20:11:28 GMT  
		Size: 150.8 MB (150790586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413954d57434541b1322f44b509a19ed6534d1f9762a07eb9f5c3704ded0001c`  
		Last Modified: Fri, 05 Jul 2024 21:01:29 GMT  
		Size: 40.3 MB (40335991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5bd1a88c9c1c31b4b725159ed0f50e308db775037cf4c486e7612dd4ecf91b`  
		Last Modified: Fri, 05 Jul 2024 21:01:27 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0ec0d72d71b387e7152c51d4fdbe7f66ccb42dc92a8a0066b0249efef28d882b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceff7741f0cbe91d75fb9067ccdd1b9be837b2655e6145be7d1f4dbe619cf5e1`

```dockerfile
```

-	Layers:
	-	`sha256:18fb7808a73a2da74b2f63f6863b38802c5925c801c1f435c0afd9181864666d`  
		Last Modified: Fri, 05 Jul 2024 21:01:28 GMT  
		Size: 6.0 MB (5980145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42b0630ff33d51941949036639defdccc37228d27aadd9cad2cedeb699ace04`  
		Last Modified: Fri, 05 Jul 2024 21:01:27 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json
