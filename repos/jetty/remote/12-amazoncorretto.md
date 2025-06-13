## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:1a1893e3675338a677eba9a5a40f0db9a45a5f079120167cf819a17d3b3bac31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c51510bd632be5a3cc96b40edf7d86cda13327b7eaa40724c7c30da84549066e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268475240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d8ddac9c42b2ad03595e1265cdc055018f9c7d0abe7bab853ed9ffc3a2ad95`
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
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f9e34af8ecbd84622c0fbc24a367b13e7e66d52134ec026aeb549f49fd8dbc`  
		Last Modified: Fri, 13 Jun 2025 17:15:21 GMT  
		Size: 164.9 MB (164854552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478d55202359b35cbe8f76d5bb41c92e8f2b899f711a2f953d04c51934a415ba`  
		Last Modified: Fri, 13 Jun 2025 17:16:45 GMT  
		Size: 40.7 MB (40656057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f99502c0a0ee057d99bb200b56551dc6603a563393688ab51cbf3315ca166b3`  
		Last Modified: Fri, 13 Jun 2025 17:16:43 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e3b2f545959f95ad59eb4a842771351b4bc5332873d0cdebf6bc2a36192dcd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ed32e8162856a6148f4ca87a3a5d818e327fbd095303fc8f542184a1665acf`

```dockerfile
```

-	Layers:
	-	`sha256:2ae8573a49f3799698fed8d52dfac989344f2a5efdc35788b8ddd445fdfa7318`  
		Last Modified: Fri, 13 Jun 2025 20:17:10 GMT  
		Size: 6.0 MB (6041654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8bdda6a3c370572ac999d1877b3670f0bdc37c2b5b0bfe753a2fba6ca392665`  
		Last Modified: Fri, 13 Jun 2025 20:17:11 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a978e2640e23d3ecca393be20879eea201bc8cc208190cb30538879299ebb430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268249410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02aea445a62d00b71aa8c1a6456aaeceb2d9e05a98bfc20a23bb38334b414ade`
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
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
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
	-	`sha256:85a9e5666d91b90ae8ad295371bbfab7de45473007f839e62582ac200cc4d4a3`  
		Last Modified: Thu, 05 Jun 2025 17:08:49 GMT  
		Size: 40.7 MB (40703363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55780f85c03a909ea7d913575ae58c81b26f96b8bc086494c9d4961588a3f922`  
		Last Modified: Thu, 05 Jun 2025 17:08:39 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e30b83eed266b42371fa1e5df906501d9a0417ef5a6d924ee7c35616fb547f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a654f389d03178728d9b42e9c758a3f24aed0cbe0a5cf88b622e5dc960d5d`

```dockerfile
```

-	Layers:
	-	`sha256:800d033652c4ea1200e0d0955445ae1855a57af582d34daec00c60d46505062d`  
		Last Modified: Thu, 05 Jun 2025 20:17:06 GMT  
		Size: 6.0 MB (6035885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42495912cd68dfd2f438900d2812d9a7fa44017272ec90d56e0697f7b8a1c770`  
		Last Modified: Thu, 05 Jun 2025 20:17:07 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
