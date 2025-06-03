## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:7e8ddadbe21a2cd0f7d6189695947a7728882fc1d41a5d2a42ce9c6bf7c65223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d3f18c046fc69c9b7ec5c081f4f6f40030123465f67861e59f0dbe83bc66719f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268222315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67c6bd65503e5703269873390734bd101433d8cc912478ebed473572f5f96d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4096a50338e29bd24ebb9cc31e05a0687dcd0600d2b083c44af8d15708a07f`  
		Last Modified: Mon, 19 May 2025 23:46:13 GMT  
		Size: 164.8 MB (164842240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61355033926d231894d5a3659d7d615a1f92466f51661975bd62b5e3b7f3cb1`  
		Last Modified: Mon, 19 May 2025 23:47:16 GMT  
		Size: 40.6 MB (40618398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e25f60a896019e07fc08c41aa7c043956ea6a0c9169d6cd888f4a9a8784089`  
		Last Modified: Mon, 19 May 2025 23:47:04 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5922d3a1eb9c0deaff7c627a081a003a827e6d2d91f8c25cd926de1c565559e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fadcabea909d47d61da147544e82088d84e5fd0422daa6aba99bf1b39114496`

```dockerfile
```

-	Layers:
	-	`sha256:4d28149a3e74a94e967317928c42e0e5212b8570ad2f0364c7be84062110c278`  
		Last Modified: Tue, 20 May 2025 02:17:24 GMT  
		Size: 6.0 MB (6037254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac466febfcfce3b9eb48c181fd171c094dd7976b20adf3f9cfdb91d352a996a`  
		Last Modified: Tue, 20 May 2025 02:17:24 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a698dfb977d286fa86748b903aa3487f5d1095404e8e5427d8262e5ce9fe7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268216921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa194f2fd9532bfeaadcae17e2d862dbfcc4ec51265e78f975892daeb878988`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5767f014b050afc587e9ad7bd97300c4413147067eec529f41a8051ad29ffd6`  
		Last Modified: Tue, 20 May 2025 00:49:43 GMT  
		Size: 162.9 MB (162936873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d651bbbd7252ddd05bb8a36f9d9d330e26d05358d6c95756bf6cd09cd9dde53b`  
		Last Modified: Tue, 20 May 2025 00:41:52 GMT  
		Size: 40.7 MB (40670875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2985ef3ea58ae2272189c2b9e2a57a7835a0bbd697999a2abd4bcc26feeb967`  
		Last Modified: Tue, 20 May 2025 00:41:40 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0ff8f3a84656d0f14fe32afbf111c556fb935f9298b09c5bc8265a65872270ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bc88f908743d9931a9bc4cb7bb9f5d5d0ecc0bfbe77d36c5397238742df8be`

```dockerfile
```

-	Layers:
	-	`sha256:0dffe306be5494f927e3a3595883b17f766dc3edfc7bdb3482e10fe14a28388d`  
		Last Modified: Tue, 20 May 2025 02:17:28 GMT  
		Size: 6.0 MB (6035919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54599c3351f4a13898bf75dce0258f42ce9443bb66308611e54ab9ecebf2dab`  
		Last Modified: Tue, 20 May 2025 02:17:28 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
