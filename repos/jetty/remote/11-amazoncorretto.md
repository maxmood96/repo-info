## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:4d09459e01e82147cbdc4a028dcb4fef5d7b046966ce3060f57226de6696f1f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:34c0fdbf3ae7a0556d6daf286b2d6a6052fe00f7555ae097ce3a0eef105db2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248268760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440a9044daffd05bd35f6aadb1c18dd8a015d78cd7de94e761eab03684e8299f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=21.0.7.6-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=11.0.25
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.25/jetty-home-11.0.25.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a647cad6a9d7741a8b6d89acd10ca8a895dafb6f992d813e5bbe76031169d`  
		Last Modified: Fri, 04 Jul 2025 00:15:29 GMT  
		Size: 164.9 MB (164854461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ace799459aa0ba10544fd84c2599df205927bd6335dcdaa1983020535e2ca`  
		Last Modified: Fri, 04 Jul 2025 00:15:57 GMT  
		Size: 20.4 MB (20449752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ce207b250cd7dec8c4a0e3ca2a4b293ca5aede2fa25af726a468c7d8ef38f`  
		Last Modified: Fri, 04 Jul 2025 00:15:56 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9b3af8135dc06e11df4e167c91176e853c02530326ed58d3931589ea11888fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2659d25a514164329b8a3bee3f0d5b04a8d152b1699cb64e96655ad2570dc9`

```dockerfile
```

-	Layers:
	-	`sha256:0d1e38936758753e1856129cc5b33211a32ae016d5091c3ce5748fc8b4cdc63e`  
		Last Modified: Fri, 04 Jul 2025 02:16:13 GMT  
		Size: 5.9 MB (5925292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f0300f9594b5984a667273fd54f8c915c934df347c90b35130bbd4371f12cf`  
		Last Modified: Fri, 04 Jul 2025 02:16:14 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:46a41af1c43a38b2038a8d5565e252693562bcb916793da58aebf1fffe0c8764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248180325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c383985599388a453c58632035524fd8b3b8ab909f14dcc5817c77cdb17849ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=21.0.7.6-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=11.0.25
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.25/jetty-home-11.0.25.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43964a7b36c19d8d08d18253a187b8d9786e92144f40e02ae62a91f72c8c9f73`  
		Last Modified: Fri, 13 Jun 2025 21:49:08 GMT  
		Size: 162.9 MB (162923005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c07a9946321beef1a106a9e104f4802407af08bed22c19e0acc148f67c473d`  
		Last Modified: Fri, 13 Jun 2025 21:14:46 GMT  
		Size: 20.5 MB (20464883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf0459806e005c250ce8aaeea824e94e1d29d9fc595aa039b7ffd92805eed9`  
		Last Modified: Fri, 13 Jun 2025 21:14:45 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0698779222bf10963ed8012f920fa3c0a8172a52efc00e134d603721336af6d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990bd7e8fda2569796e82e43ac7b236e8af885e7ac9c6144e4f8d6e70b9daeb1`

```dockerfile
```

-	Layers:
	-	`sha256:c6fe4ff5b4015f45e7634bdf23b128460351f17da1136d6c57fe35aabb788638`  
		Last Modified: Fri, 13 Jun 2025 23:16:16 GMT  
		Size: 5.9 MB (5923957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4601319316d33e371c6af3c1a24c79aad5b8f8ce8640f7ac7a6f5280b06285d6`  
		Last Modified: Fri, 13 Jun 2025 23:16:17 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
