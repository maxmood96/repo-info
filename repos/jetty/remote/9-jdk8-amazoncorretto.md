## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:e4089dcf920b6b58349992d655a6111808c1701b8494d88c7cd57077a73ff1bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1caea35e225d05227a758daa24b80fd100e79b0161390f57c55b5b38010c5551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155221047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6174051ae4db07d8017534ff7b6d7e9eacf1fbeff3a7c202a8f1ae597505086`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:15 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:15 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:08:15 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 15 Jan 2026 23:09:21 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 15 Jan 2026 23:09:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:09:21 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:09:21 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:09:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:09:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 15 Jan 2026 23:09:21 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:09:21 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:09:21 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:09:21 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:09:21 GMT
USER jetty
# Thu, 15 Jan 2026 23:09:21 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:09:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:09:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95512b2044a8f80c577659eead5e19c14c6cec9a57545ced886f0055475bb3a1`  
		Last Modified: Thu, 15 Jan 2026 22:08:55 GMT  
		Size: 76.0 MB (76044822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7800fa31dd19a8858b2e67a83fa1936735e4056ce891d7e6df399e6a234a3`  
		Last Modified: Thu, 15 Jan 2026 23:09:41 GMT  
		Size: 16.2 MB (16234193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac175e48400e2c3e601fa7540e411d49c3e836c630f1cbef0672410a0c7ae83c`  
		Last Modified: Thu, 15 Jan 2026 23:09:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ea2b054caa80bcebaf1171f14f16f2ca14bb384eb1a2a44a125f4e36aca3e203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001e43ee50c14f4401e2c64990f245822404eea15c22cb991cd0c0f8f6f315b0`

```dockerfile
```

-	Layers:
	-	`sha256:a0d8be851366d19b47b3e68d45dafc721b46227d80441630bf3c5e5f54785007`  
		Last Modified: Fri, 16 Jan 2026 00:21:21 GMT  
		Size: 5.8 MB (5756040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8093fab617a578240a6812f60d38726f6e2a8139896c422972abd2c72cbd5c`  
		Last Modified: Fri, 16 Jan 2026 00:21:24 GMT  
		Size: 17.4 KB (17376 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:befbcabfb97aa0ea408093d08172e1196975a356d4f8cdb60efdab07af5d7584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141192231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f8d2312418fb737f25ab153621d9866ecb936be43d726203333fb9b44e64b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:24:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:24:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:24:25 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:20:22 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 18 Dec 2025 02:20:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:20:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:20:22 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:20:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:20:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 18 Dec 2025 02:20:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:20:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:20:22 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:20:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:20:22 GMT
USER jetty
# Thu, 18 Dec 2025 02:20:22 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:20:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:20:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909fe2bc51d4f2e9dc917f97ac6bb1a9aea7b2afc8fdc287ac788a885c135dd7`  
		Last Modified: Thu, 18 Dec 2025 01:24:53 GMT  
		Size: 60.1 MB (60118031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f1e10b1b279679cfc9591eb19f7e7253cd94b8eccac6f4dc7d0586b42eab89`  
		Last Modified: Thu, 18 Dec 2025 02:20:40 GMT  
		Size: 16.3 MB (16276568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30441f2df24f72b610da36df9e86ea4e100901b7781c86a3c80fd02ba77a9866`  
		Last Modified: Thu, 18 Dec 2025 02:20:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1405d5a6f3d7e57b8964da2f041da3cfdfc5209fe2d1b22e52a75675e4a20bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeb2940e19e77c8e71bfc37a6261381f9f63a3b2ae01a5ae5596c0b37bfb2c4`

```dockerfile
```

-	Layers:
	-	`sha256:c58bb268403d86b56276fd007e2da27e44c1f020a9d849525ccd6aba33685507`  
		Last Modified: Thu, 18 Dec 2025 06:20:20 GMT  
		Size: 5.7 MB (5734467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cb13e4009146cc70ec7f39557b71d69de62f6cc75e746695aa918f980d194a`  
		Last Modified: Thu, 18 Dec 2025 06:20:21 GMT  
		Size: 17.5 KB (17469 bytes)  
		MIME: application/vnd.in-toto+json
