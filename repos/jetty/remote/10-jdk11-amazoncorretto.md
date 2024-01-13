## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:1b7d1ac662720affd22fe84f6e9a78de597aba841cbea3e926a16757e871955a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8acb447dfeba1614dff64555e5d5cdcd0d826f4bbba7fe0ac0b9293dabc51e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227527967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0833e7c5921e0e853622f64df6ac58da4e50f1f8c0b44067bd1522c2f327d8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:17:31 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:17:55 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:17:56 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:17:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 13 Jan 2024 01:02:26 GMT
ENV JETTY_VERSION=10.0.19
# Sat, 13 Jan 2024 01:02:26 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 Jan 2024 01:02:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 Jan 2024 01:02:26 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 Jan 2024 01:02:26 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:02:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Sat, 13 Jan 2024 01:02:26 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 Jan 2024 01:02:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 Jan 2024 01:02:44 GMT
WORKDIR /var/lib/jetty
# Sat, 13 Jan 2024 01:02:44 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 13 Jan 2024 01:02:45 GMT
USER jetty
# Sat, 13 Jan 2024 01:02:45 GMT
EXPOSE 8080
# Sat, 13 Jan 2024 01:02:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:02:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb88a83adf24aa3bf320f79f5d513a8ea3664c3ff9f904cd63321278f57bbd8`  
		Last Modified: Fri, 12 Jan 2024 22:29:46 GMT  
		Size: 147.9 MB (147939933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b44a1ce9fab8eb3cf39153a13276ddf2f601f67c4ab78cc2fbfbac448df449`  
		Last Modified: Sat, 13 Jan 2024 01:09:50 GMT  
		Size: 16.9 MB (16925399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5004935b2bb4c57fcef8e8bd16b7e0a710928970195d04a8c5bf2ffdd3e28c`  
		Last Modified: Sat, 13 Jan 2024 01:09:48 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:3a32efd2f6df4ed68999d7ec5e4b5760a3df6172acd6bd0d0e5fc1d08caf253c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226456648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c161ccbd8368a521689e459e98b4ea8d4a29c62493ec904011251dc2bf7700`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:23 GMT
COPY dir:eb2de4474e28d9fde9bbe1ffb630978f47dae30856e760ca73ebb5d0cb75efd7 in / 
# Fri, 12 Jan 2024 21:49:24 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:31:05 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:31:23 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:31:25 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 12 Jan 2024 23:44:15 GMT
ENV JETTY_VERSION=10.0.19
# Fri, 12 Jan 2024 23:44:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 12 Jan 2024 23:44:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 12 Jan 2024 23:44:15 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 12 Jan 2024 23:44:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 23:44:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Fri, 12 Jan 2024 23:44:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 12 Jan 2024 23:44:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 12 Jan 2024 23:44:30 GMT
WORKDIR /var/lib/jetty
# Fri, 12 Jan 2024 23:44:30 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 12 Jan 2024 23:44:30 GMT
USER jetty
# Fri, 12 Jan 2024 23:44:30 GMT
EXPOSE 8080
# Fri, 12 Jan 2024 23:44:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 23:44:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9620bfd6832ce2ca50093b819c4f62fd86c4b96a997fd5da88afa856b28cb1a0`  
		Last Modified: Fri, 12 Jan 2024 19:03:15 GMT  
		Size: 64.5 MB (64462448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5002b70eeec43fc3f2d8b5badf3186a1c37fa50b81ba6a1fa19811be65f8c92f`  
		Last Modified: Fri, 12 Jan 2024 22:40:31 GMT  
		Size: 145.0 MB (145030569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f311c470559cf25224fa5e3875026ead43c5ae9ad22c5b12f02de4adc5940a4`  
		Last Modified: Sat, 13 Jan 2024 00:02:17 GMT  
		Size: 17.0 MB (16961997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a3cfd894f4ef555136fc6a435524fe49b7db5aa1aefc8df877dbeab3a318ca`  
		Last Modified: Sat, 13 Jan 2024 00:02:16 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
