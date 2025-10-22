## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:707140ccad0b0bf4cdb3b2484a497438b29edc55ee8e0ed413f86de63294366e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:ac35cb12fa4af8073a3cf523a518180edf2914a9f3b885fcdb8910634c446a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228334971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a620e9799cab51923d1eb15a6cee4a2df60e776cc9aed45d83f9a2bf62108e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 19 Aug 2025 02:05:55 GMT
COPY /rootfs/ / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 02:05:55 GMT
ARG version=11.0.28.6-1
# Tue, 19 Aug 2025 02:05:55 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9b18b72b93cc14d31fcd5ae947987b35e6e81f265f08584038b95dc7093a`  
		Last Modified: Mon, 06 Oct 2025 22:12:29 GMT  
		Size: 148.3 MB (148297178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bf925b9f33b687c67905f38878d97bfc4c92cedf0a48fe17925f5dfcf0701f`  
		Last Modified: Mon, 06 Oct 2025 22:14:07 GMT  
		Size: 17.1 MB (17095298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd0eba0f500fcad5b60fe8712ba55992dee994f9e6d42008b7bb8e3e40917`  
		Last Modified: Mon, 06 Oct 2025 22:14:02 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bd148f4032e1505294dbea71449512b11c09e2a30998edef2e0a4e4e5660cfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5950397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21086a877b97097708ac12a4c092a2c0b7bf559c2bea3c76bd0a255ac384ec5a`

```dockerfile
```

-	Layers:
	-	`sha256:34ecddbeb590469a6341743615ff45a4b0eb94cc1f6864ed483546445abbf530`  
		Last Modified: Mon, 06 Oct 2025 23:15:30 GMT  
		Size: 5.9 MB (5932997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd288cc04bbb105864a48474216263a34f20061d6d58c7862ab04f05d8680c8`  
		Last Modified: Mon, 06 Oct 2025 23:15:30 GMT  
		Size: 17.4 KB (17400 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5cebb0a93bae54aa1f6dd4c239fd87f66b5ed0ac7af5b4082a18f14cbf1fe871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227077807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a0a1a1c119a740d395b1762e4d15002adf4f512ec4d26e41a881afdf66e4ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 19 Aug 2025 02:05:55 GMT
COPY /rootfs/ / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 02:05:55 GMT
ARG version=11.0.29.7-1
# Tue, 19 Aug 2025 02:05:55 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 19 Aug 2025 02:05:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 19 Aug 2025 02:05:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
WORKDIR /var/lib/jetty
# Tue, 19 Aug 2025 02:05:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 19 Aug 2025 02:05:55 GMT
USER jetty
# Tue, 19 Aug 2025 02:05:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 19 Aug 2025 02:05:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 02:05:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b8b12b7c5856e259b06bb3d673e93d1bea0809ad17d2d440d5f224e3e20fb7`  
		Last Modified: Tue, 21 Oct 2025 22:13:35 GMT  
		Size: 145.1 MB (145144638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810eb844aaa6d55253dd4004f508808845db0168d46bf8f5741c07b43bec5804`  
		Last Modified: Tue, 21 Oct 2025 22:15:30 GMT  
		Size: 17.1 MB (17138085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa4c4ec70b9de78dcc0cfb93941b8d02202b2771c216b745a80272cd996913`  
		Last Modified: Tue, 21 Oct 2025 22:15:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:18cd86cf95071248b170a55215f135904a8d391bd5c9b04c8696ba7189f690b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82f571428efec4e55ab5488ee2aaf585a1fded4cbc363a3664c142794d40a8e`

```dockerfile
```

-	Layers:
	-	`sha256:afd6fce9151fd52b869af2f91f0f363cc9a4076c866868794106becb4c58e3a1`  
		Last Modified: Tue, 21 Oct 2025 23:15:59 GMT  
		Size: 5.9 MB (5935658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0506d31ae4d23214e9918ce2f698b82d03c1605a68542a29e885ce65ede8fa8`  
		Last Modified: Tue, 21 Oct 2025 23:15:59 GMT  
		Size: 17.5 KB (17492 bytes)  
		MIME: application/vnd.in-toto+json
