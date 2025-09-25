## `jetty:9-amazoncorretto`

```console
$ docker pull jetty@sha256:8edee5eccbbcfc86643d4e162cf74d056dbe3dc2a324101dc664c69a21778d37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a1f2932b08e57938337bcb2066c031265dcc77d9eb437a9778ab69e8c4f71b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244188068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450825a073421c353784a898a29585b6bade28a7c6cb91590a66732c49a8b3cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Aug 2025 04:54:08 GMT
COPY /rootfs/ / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["/bin/bash"]
# Fri, 15 Aug 2025 04:54:08 GMT
ARG version=21.0.8.9-1
# Fri, 15 Aug 2025 04:54:08 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
ENV LANG=C.UTF-8
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e750caf8f1aace6b2a40b4d03ac34238ad41147f9852aea71ac3fd0f305ecc01`  
		Last Modified: Thu, 25 Sep 2025 03:16:04 GMT  
		Size: 165.0 MB (165044322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfa6042ab1a0bec665d4f687de21fac7ce8d4835985ea94c05636f5b78a75e7`  
		Last Modified: Thu, 25 Sep 2025 03:16:54 GMT  
		Size: 16.2 MB (16208029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3bc6a5f3cd9e2cd8aa53598e958c9954856f9ee9cc9906d887d4abde2b972`  
		Last Modified: Thu, 25 Sep 2025 03:16:50 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d63acad8a49f461e703f83d2a56afac23de886beced085cc5b6064ef405c75bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbb3c83c0945d0e0247b66cd275bcfd68dd06b719c6e7d8dd266ff938b631cd`

```dockerfile
```

-	Layers:
	-	`sha256:11dbaae22322b7a6ca74c1e594a6295ecd066282f9acadd5321c0ef6136d8682`  
		Last Modified: Thu, 25 Sep 2025 05:19:33 GMT  
		Size: 5.9 MB (5912312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79a14c571d17e6b2360cd686a1cf591c9b37caf9fefa6e84cbd0fc0113aaf32`  
		Last Modified: Thu, 25 Sep 2025 05:19:34 GMT  
		Size: 18.4 KB (18393 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:53564a5e41fa2ee054d54e34e3784fc4bae6f64ce7649bc49beb1cd7c0e1d6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244156984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80afeb60d9c4a296138a9c5868b398bb1bd417b50835236eee2dfdbe64108b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Aug 2025 04:54:08 GMT
COPY /rootfs/ / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["/bin/bash"]
# Fri, 15 Aug 2025 04:54:08 GMT
ARG version=21.0.8.9-1
# Fri, 15 Aug 2025 04:54:08 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
ENV LANG=C.UTF-8
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c868e5c107db6ab89ab40ef0c51c4a502a10ecc34ea2109f2dd64bd446a85`  
		Last Modified: Wed, 24 Sep 2025 22:12:58 GMT  
		Size: 163.1 MB (163112265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53678da23bfabe8ea8d931b0955aa650589ac48a2cdbd04f6cad238bb238abe7`  
		Last Modified: Wed, 24 Sep 2025 22:14:11 GMT  
		Size: 16.2 MB (16249696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7ce7557f4bd51000ac91588984f7faff8ed0c3cb1af6f317c56f90454980d5`  
		Last Modified: Wed, 24 Sep 2025 22:13:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:123b3bce0a61c8d22b072114156166da9e15ffb792ee5117afbe9c32862a0602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5929498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db6e8d19f8559672186c73bfc159b54955f24e65cd504fea10d8d34dc213672`

```dockerfile
```

-	Layers:
	-	`sha256:9b0d42c1bd489510d4bb93d2a43426a6ac5d2a47d6002811d7be3d5ac2913628`  
		Last Modified: Thu, 25 Sep 2025 02:19:10 GMT  
		Size: 5.9 MB (5910977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:609429cbad73b9b5fcff6bb174e2c6eec657bf578db700517b40f38f40b6b342`  
		Last Modified: Thu, 25 Sep 2025 02:19:11 GMT  
		Size: 18.5 KB (18521 bytes)  
		MIME: application/vnd.in-toto+json
