## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:06ef52d5d13ff2314107352a241ac235014ed1a2ecf014858c6f12f541a226c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8454c479de3355e65dd464fa4bf14abc4a394e9e896489f006b67f2d5cef50c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231687364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53aaf1237687a6d4ffa7643d727ab647b58181a8ad9e5f8a83b91f9ee2324f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=17.0.11.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Apr 2024 04:42:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
USER jetty
# Thu, 11 Apr 2024 04:42:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Apr 2024 04:42:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Apr 2024 04:42:46 GMT
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
	-	`sha256:7575395465faa7caa986195e558e346d905d9641aae813edee401d7ccdbd1946`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 16.9 MB (16894330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24e5810829bd8e8e9d1ee94e65735c6a8b92aab5a7ac472181fb690c384ba46`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:234d2367be0d161d1245ff2e48a65184d28c9adbb95ddfc82add29e975a038f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2f49d436eb9eb3dfe4231efa597cbc78b19c1d631cdde3b5836fcfdfa4d302`

```dockerfile
```

-	Layers:
	-	`sha256:25848781c17b67701d534ffdaeea2a968135f5c0cda42d2dc40dfd3c74a2dc15`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 5.9 MB (5882526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5158c1722b344f44f68119178fd5aa9db54e81872cbad356b1a1d96348b41da`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:26835b753d38299b3fee6d8c937dd39e1fa8de934ab1787ba310febe68c6a0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232378029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6c7b064442d7b6116095e76ff47e8fada36f9e2c73df88a7ac2c3aa10f6ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=17.0.11.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Apr 2024 04:42:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
USER jetty
# Thu, 11 Apr 2024 04:42:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Apr 2024 04:42:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Apr 2024 04:42:46 GMT
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
	-	`sha256:377ccfe3b2136f66b810cfd2d5959fcd799e4708574f6ae6adfc146570521f07`  
		Last Modified: Fri, 05 Jul 2024 21:07:40 GMT  
		Size: 17.0 MB (17017014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbc8108f2da802832b26c315577d59ff06acdf1efd9fc85ae7e1f3e3f1e6015`  
		Last Modified: Fri, 05 Jul 2024 21:07:40 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0b09898f508e028ff6c724f1624e29c7c362878b6a88ae1ec5443ee3443e53be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada7ea62d3e1f459a55c1e35be8444bd9c3536f5c4e4fefda0128d1c04f2f9b2`

```dockerfile
```

-	Layers:
	-	`sha256:bfee42113e536d9d7f7b2020bc6500b737b1af3df030c4ab725070db5a2da59d`  
		Last Modified: Fri, 05 Jul 2024 21:07:40 GMT  
		Size: 5.9 MB (5881153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ebda11dfecfdd25ca57a7a64798a3b7c85d85bbe9fbe57a618dea8495e1a0d`  
		Last Modified: Fri, 05 Jul 2024 21:07:40 GMT  
		Size: 17.5 KB (17528 bytes)  
		MIME: application/vnd.in-toto+json
