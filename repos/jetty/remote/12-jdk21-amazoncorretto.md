## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:1afde5d4a7685b91d77f71832ae98a3289f1bb3db0f2008b4aec7aaf072cb67e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5beb956a3401c8e58e87f8dcf6fa86a453463783b5329731da866566c3dd568c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280359396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c6d6ea195a7eec51f02cff4243617b7832ab97add372a361ee8f1af0db76f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:05 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:15:05 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:15:05 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:13:16 GMT
ENV JETTY_VERSION=12.1.3
# Thu, 06 Nov 2025 23:13:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:13:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:13:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:13:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Thu, 06 Nov 2025 23:13:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:13:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:13:16 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:13:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:13:17 GMT
USER jetty
# Thu, 06 Nov 2025 23:13:17 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:13:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:13:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b6e807c1a7c53af4ccdd4780bf792c6494ade14902f1c503d47c104f25cfd`  
		Last Modified: Thu, 06 Nov 2025 23:11:15 GMT  
		Size: 165.5 MB (165485950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472ed9e3c76afbceea6009a4df3b8b0e8c66e028c535b08787ff0652448da159`  
		Last Modified: Thu, 06 Nov 2025 23:13:43 GMT  
		Size: 51.9 MB (51937436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8856e94e2a64e0374268f2310348eb80381550a378777a41524654192a584a4`  
		Last Modified: Thu, 06 Nov 2025 23:13:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c609cd2d3ed3d39835bbd63544c59379caadb422cd7b9d1ab9d2099e295ae156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6a6ced0ffd6fc653fcb90b159bad7a8098570c27b606a5ef3a0eca1aef626a`

```dockerfile
```

-	Layers:
	-	`sha256:c2ae6c2bca26064b2ef3c3b4245ec40bb1e4e4cbb6e8379db0fe92f42a74100b`  
		Last Modified: Fri, 07 Nov 2025 00:17:50 GMT  
		Size: 6.2 MB (6152830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342dc75f97dcc66ea1c3c9549d8076882e80a0df8f71b8d76b59a7f53b4d751d`  
		Last Modified: Fri, 07 Nov 2025 00:17:51 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0583c18dd0f0af9c92c4e834742664c09d2186448ef8474b251dfb1ebe13938b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280384539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2af0d0fbbf429f1b4179cb463d3be8366cefec37e53bfabd8d2dcc70ae4c27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:08 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:14:08 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:13:45 GMT
ENV JETTY_VERSION=12.1.3
# Thu, 06 Nov 2025 23:13:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:13:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:13:45 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:13:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:13:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Thu, 06 Nov 2025 23:13:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:13:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:13:45 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:13:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:13:45 GMT
USER jetty
# Thu, 06 Nov 2025 23:13:45 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:13:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:13:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50fcdfedf41173aea97496be730854d377fdf96be58c639f421a2d1bff774e7`  
		Last Modified: Thu, 06 Nov 2025 23:13:01 GMT  
		Size: 163.6 MB (163582959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be61f1543be92e62ce889a1e5a61a606deb1ee76911f52dc9101d9180323f2c`  
		Last Modified: Thu, 06 Nov 2025 23:14:20 GMT  
		Size: 52.0 MB (52006407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af44a2ed82fedf269697a52bee3ebbd06ce86e371c4d998e52b96e568641b0e5`  
		Last Modified: Thu, 06 Nov 2025 23:14:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b5e443a7e1d0a8ae01b44ff71a44c07e1e6d46427e6d64aede5ee7fa7a3d49fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4e864e977e702532b13f7047a6034a3cee22db46957bdcd64f61f2d9b263d8`

```dockerfile
```

-	Layers:
	-	`sha256:08dc52f8e145866430d202032aba516dea89c326883de6d59eca754d82fcaeb5`  
		Last Modified: Fri, 07 Nov 2025 00:17:58 GMT  
		Size: 6.2 MB (6151495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f230f20e1803b02a0cd36a7f9da0c9f87722f2d611858756a94d6b149514fb42`  
		Last Modified: Fri, 07 Nov 2025 00:17:59 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
