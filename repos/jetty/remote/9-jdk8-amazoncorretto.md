## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:8c7d30217379e2ea2e0f24e762eb226d06aa86eba0d51b415eb0b241f892d998
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c2712b51a47ad4e6b87abbabc6490ac13c12925d32948d52309fa9a3ad4b8dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155187984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e740c6dd93931859ab2ffc42cbe1be8645e7fce70318121388c9e64752998cb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:31 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:31 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:35 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 31 Oct 2025 01:12:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:12:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:12:35 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:12:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:12:35 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 31 Oct 2025 01:12:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:12:35 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:12:35 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:12:35 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:12:35 GMT
USER jetty
# Fri, 31 Oct 2025 01:12:35 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:12:35 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f169c4ab9c5b596302c6e78d09dc97ac1a459af646782f43c571ba613820`  
		Last Modified: Fri, 31 Oct 2025 00:11:11 GMT  
		Size: 76.0 MB (76043905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c965300eba54863a404dd40a220785c6ce4bd80123a7cb92fc601161ca0033`  
		Last Modified: Fri, 31 Oct 2025 01:12:54 GMT  
		Size: 16.2 MB (16208136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3957c3ae24a3af305d04083fd9acb1f298a18c7bda9726462459481ba18e1d`  
		Last Modified: Fri, 31 Oct 2025 01:12:51 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fadd6c5aae6bc4af26ad8060e0b44d17b3aa2c9f93a0411b6a3fec330d8f157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69433faeaf096a48891dde9443325c811ba487f9ed2baa9ff456090466d6afd`

```dockerfile
```

-	Layers:
	-	`sha256:c26d6d5649d59019850df79ece4287c6466644c24cc101f5ef01092192eaf34e`  
		Last Modified: Fri, 31 Oct 2025 02:20:05 GMT  
		Size: 5.8 MB (5756036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f7206e66ac6cad6698f7795f291b91f7acb9bf3d16ba0e7c1a5cb141e3442b`  
		Last Modified: Fri, 31 Oct 2025 02:20:06 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f9c554af0dde278ccd7c2427c1ad2b6bcdb5a3d976f57bdfd85c0bfb961cce43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141191889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b17479fdf8308d29466ce9036cb43955ac76bb88225d9c79fac91652408976`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:58 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:58 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:58 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:13:03 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 31 Oct 2025 01:13:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:03 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 31 Oct 2025 01:13:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:03 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:03 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:03 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d96ed5cf7cdd43c028ca3ffb2b3c794c53305e80d242b1a23649bd6d4c7ac`  
		Last Modified: Fri, 31 Oct 2025 00:11:39 GMT  
		Size: 60.1 MB (60118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b8c2ca8076d4989661d71a8f27c0305e73009ddf111ed443aedf6a4849192`  
		Last Modified: Fri, 31 Oct 2025 01:13:22 GMT  
		Size: 16.3 MB (16277638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559a3ad745f6a45ebd7f84d3bed2dd55ae63cf7dce5349312fcfc7b3d8ad142f`  
		Last Modified: Fri, 31 Oct 2025 01:13:21 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b96ee12b32acbcdc9a7289a06d0042234d1b35d730505ed2c39c4b27acf34beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bd8a85914db24e209e96e4a0a0bf87ef533bc7769460d853d4af6fc59512ea`

```dockerfile
```

-	Layers:
	-	`sha256:15dc59f52beb70fc89c72f351432be3eec8d1cfc84136d476732dd95a58c4713`  
		Last Modified: Fri, 31 Oct 2025 02:20:12 GMT  
		Size: 5.7 MB (5734463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6724344a4c079e1849b0ddb117e8622ee60d075e5044b920cef2cbb20f0ef04c`  
		Last Modified: Fri, 31 Oct 2025 02:20:13 GMT  
		Size: 17.5 KB (17469 bytes)  
		MIME: application/vnd.in-toto+json
