## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:dcfafa4a4dd7becd67085dfb587ce3bdbe435dd6941666fcf811b6b5d1cc037e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2404004667e84e69a7fc5dcdc1ad84e8d88467e3871668971b0bf979c1efa5a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154100121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775a5e8b189e383200fc0e7091944179f2f7bcaa26267a46acf3b433447cc73f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:14:35 GMT
ARG version=1.8.0_392.b08-1
# Fri, 12 Jan 2024 22:14:57 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:14:57 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:14:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 13 Jan 2024 00:57:30 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Sat, 13 Jan 2024 00:57:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 Jan 2024 00:57:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 Jan 2024 00:57:30 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 Jan 2024 00:57:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 00:57:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Sat, 13 Jan 2024 00:57:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 Jan 2024 00:57:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 Jan 2024 00:57:50 GMT
WORKDIR /var/lib/jetty
# Sat, 13 Jan 2024 00:57:50 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 13 Jan 2024 00:57:50 GMT
USER jetty
# Sat, 13 Jan 2024 00:57:50 GMT
EXPOSE 8080
# Sat, 13 Jan 2024 00:57:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 00:57:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6cabfc44baf04764162d5ccf437d05c5ed37327513a9a4edc6cbaeade6d739`  
		Last Modified: Fri, 12 Jan 2024 22:27:45 GMT  
		Size: 75.6 MB (75599003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e18a7bbf13e80e37a0ef37133f09838dccb0d87aa83902165d972b221f718c`  
		Last Modified: Sat, 13 Jan 2024 01:07:04 GMT  
		Size: 15.8 MB (15838484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae387a7b8d8e8626006aae4bf7490d864f53f687e36cb7336a3ae77a5ccb902`  
		Last Modified: Sat, 13 Jan 2024 01:07:02 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9890c815b0906e2b555da0d932af4f868d24697f128edc13de64116399146f95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139950686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94c88ea49a44192fc470917d05b9d1fe91c8864298e915d1c9afd38a44e8678`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:23 GMT
COPY dir:eb2de4474e28d9fde9bbe1ffb630978f47dae30856e760ca73ebb5d0cb75efd7 in / 
# Fri, 12 Jan 2024 21:49:24 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:29:30 GMT
ARG version=1.8.0_392.b08-1
# Fri, 12 Jan 2024 22:29:46 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:29:46 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:29:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 12 Jan 2024 23:40:23 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Fri, 12 Jan 2024 23:40:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 12 Jan 2024 23:40:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 12 Jan 2024 23:40:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 12 Jan 2024 23:40:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 23:40:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Fri, 12 Jan 2024 23:40:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 12 Jan 2024 23:40:39 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 12 Jan 2024 23:40:39 GMT
WORKDIR /var/lib/jetty
# Fri, 12 Jan 2024 23:40:39 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 12 Jan 2024 23:40:39 GMT
USER jetty
# Fri, 12 Jan 2024 23:40:39 GMT
EXPOSE 8080
# Fri, 12 Jan 2024 23:40:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 23:40:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9620bfd6832ce2ca50093b819c4f62fd86c4b96a997fd5da88afa856b28cb1a0`  
		Last Modified: Fri, 12 Jan 2024 19:03:15 GMT  
		Size: 64.5 MB (64462448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50909be413c3460ab9a71b817b9f8d6bb20f2335ec1c36a06e21ce537e413ce8`  
		Last Modified: Fri, 12 Jan 2024 22:39:05 GMT  
		Size: 59.6 MB (59609616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28633b91350cb380b240cf6303e3db2739fd8ce6ea7eb11d92d27e02b7b73288`  
		Last Modified: Fri, 12 Jan 2024 23:54:27 GMT  
		Size: 15.9 MB (15876989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4679c67e2ad497bdc36bdd079273ae7405e21889749750063d0eaf0c57913a`  
		Last Modified: Fri, 12 Jan 2024 23:54:26 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
