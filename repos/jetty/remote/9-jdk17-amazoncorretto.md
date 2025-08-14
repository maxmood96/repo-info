## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:816f2e94f1b80fe2a71dffc7d5c27664e0ff104ce46d615ae77e17dbf09a893f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:deec06b0b676c0e67a687fafa4e93c158be73dccdde2e88e8a1578a3fbb0f607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230995729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6640786d9aa50a07bc5b20f5edd3fc29fcd151fc67a5e3f0a2979e920f798d11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Aug 2025 07:13:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
USER jetty
# Tue, 12 Aug 2025 07:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 Aug 2025 07:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 07:13:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0609072df14ca55d332f8e3c224846b0b7eead95460c9ece0cfefd122f064`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 151.9 MB (151874859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b940fe56155c85d4ec78fa440cb96ab9033b629637fba48e17c9106fac76e52`  
		Last Modified: Wed, 13 Aug 2025 23:11:50 GMT  
		Size: 16.2 MB (16159622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5260bfb30f6517987f4b2f5ae308296e6e49e9502ea2dda205bfedc43d13b8e3`  
		Last Modified: Wed, 13 Aug 2025 23:11:47 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a4cbf55ab10f2cf46ad8ef7eb801c63dd119b7a9265cb98cdeeea4ab63f83362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5928884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809936d23d8ef89ee38d6b8c8b50471a03924ff11da1c144a769947303ee4b24`

```dockerfile
```

-	Layers:
	-	`sha256:5aa4e006e7890bd1aef91fd09c3b0b9a5548ac52002ed69c88c783e803a464f6`  
		Last Modified: Thu, 14 Aug 2025 02:18:30 GMT  
		Size: 5.9 MB (5911453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c56756d4c3f6b6000030bd1986c693f6b541f8bc6149532e8fa7eac9be4352`  
		Last Modified: Thu, 14 Aug 2025 02:18:31 GMT  
		Size: 17.4 KB (17431 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0d75e5255fe186dde9fbb6bfb814548b9a1e6cdbb5ff36995bd5dd7ee7cea2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231370267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e41e5786b8c0e5d21318e20f26142f8809d9a459577873fe4a8b8c9ffa1a2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 12 Aug 2025 07:13:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 12 Aug 2025 07:13:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
WORKDIR /var/lib/jetty
# Tue, 12 Aug 2025 07:13:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 12 Aug 2025 07:13:40 GMT
USER jetty
# Tue, 12 Aug 2025 07:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 Aug 2025 07:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 07:13:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cd4aced99c35e8bc24c9f8f76de4c6384d08e38ee655cb9bdcb8b655f87e74`  
		Last Modified: Thu, 14 Aug 2025 09:14:46 GMT  
		Size: 150.4 MB (150397839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2bde2960598b07ef15e21911b62fb2c05c97addd28879871548c1f451032f`  
		Last Modified: Thu, 14 Aug 2025 17:29:53 GMT  
		Size: 16.2 MB (16176188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa680ca2cc858db298eb6e53b9e609e652bc155cbfc7486ab4bd112ae2a21bd8`  
		Last Modified: Thu, 14 Aug 2025 17:29:52 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:dd8e1b2b8ec34365dce8600b25a7de1dbf90ccbeb99dd75e7e6717fde5cd2027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc59a6366cc0cabd518c808379e41dfe80093dd235bbd081e63a255b24ab4037`

```dockerfile
```

-	Layers:
	-	`sha256:423ca89abda0f45b7af55a4f01d475bd0b3a9fdb3aa4b3a35ac7243d8b77487b`  
		Last Modified: Thu, 14 Aug 2025 20:18:49 GMT  
		Size: 5.9 MB (5910082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0192fbd0c15698f997581ad7fa1c4e30e9c95bafbd771730e2ed8faee7f74e53`  
		Last Modified: Thu, 14 Aug 2025 20:18:50 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json
