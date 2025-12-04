## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:80aba3157623b6f87e0e10a07a98c457f8180dbc1e91684f808df4d3f586db4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:80c4f8ed8c37ed9e6566a8c208cc79cbb60307c7ba194d37ffa9281975fb2101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248969782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfb5dba0811e0d911c2155c616e24ffd62a8028ed043fd97374d90e6f600630`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:21 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:23:21 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:11:54 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 03 Dec 2025 21:11:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:11:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:11:54 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:11:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:11:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 03 Dec 2025 21:11:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:11:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:11:54 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:11:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:11:54 GMT
USER jetty
# Wed, 03 Dec 2025 21:11:54 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:11:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:11:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb2013f839dc1b3c014b823b3aac80d0e6d67fac06ba1b5ce16eef96069369`  
		Last Modified: Wed, 03 Dec 2025 21:11:38 GMT  
		Size: 165.5 MB (165496684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0379e18afab84d73e196bead4a0df863a0d023a7905ef16378a99a2031fb3d57`  
		Last Modified: Wed, 03 Dec 2025 21:12:12 GMT  
		Size: 20.5 MB (20540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f46098130b7e62be4f2ab95cedbdbded2471d2d35e20863857b4d34a174ae3`  
		Last Modified: Wed, 03 Dec 2025 21:12:10 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5deea982f6df9a194c7b5ec98c09e7f489712b593271e5978a5cc6a557928b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e21148d99949c3a8fe39eeec5c7901eaa50f3da861e7433df43afc29012b386`

```dockerfile
```

-	Layers:
	-	`sha256:e3168171aa4b14b372cf35160976fb70cc5e7d4cc025c392286b3af0923fad11`  
		Last Modified: Thu, 04 Dec 2025 00:16:30 GMT  
		Size: 5.9 MB (5929842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc982ceeed032f85dc8191fd2ee09e8d339e052231c87fed07e6aaf7dc280d31`  
		Last Modified: Thu, 04 Dec 2025 00:16:31 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9315085a454052d3f31fff670afad40fd7bd34b28184fa7ff1abf6188543de7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248967781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4651d8d56cb7ae6a6f99c5201e4668931ee7e5aa537524b9ba2d9937a271f5cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:26 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:26 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:26 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:14:24 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 03 Dec 2025 21:14:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:14:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:14:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:14:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:14:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 03 Dec 2025 21:14:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:14:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:14:24 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:14:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:14:24 GMT
USER jetty
# Wed, 03 Dec 2025 21:14:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:14:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:14:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba2b3f44053754feffb2ec7cfa45b66127e117d0d28e5607dbc6e1b6044b97`  
		Last Modified: Wed, 03 Dec 2025 21:41:24 GMT  
		Size: 163.6 MB (163582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c51a569f4e5599a33f629ada0a41b3309ebf3031cee4a9accc509ac59b57ddb`  
		Last Modified: Wed, 03 Dec 2025 21:14:44 GMT  
		Size: 20.6 MB (20590223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b54b26607350fc2007e70142776845a35346a99878e6ae7d4398c0b3939973`  
		Last Modified: Wed, 03 Dec 2025 21:14:42 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:33b3335cb8fcd275e08f6ff576d05a989c5d8a33825d2f8799cbab5a566f4ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636931686cfac31f31f0a9762ff19141eb5d872f9c69f6c39e0bdb06bd832eaf`

```dockerfile
```

-	Layers:
	-	`sha256:713cdbb78759b1b7a9c66944a3ccb4aeae80affdf68fd993915d82658ce1e381`  
		Last Modified: Thu, 04 Dec 2025 00:16:37 GMT  
		Size: 5.9 MB (5928507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:871e08c7f10524bcb523cb32a296bbcd915fa86dc0b0e6414bc3b4a50a1aa341`  
		Last Modified: Thu, 04 Dec 2025 00:16:38 GMT  
		Size: 18.5 KB (18453 bytes)  
		MIME: application/vnd.in-toto+json
