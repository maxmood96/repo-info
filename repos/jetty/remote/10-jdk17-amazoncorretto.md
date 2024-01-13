## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:4aa6123f0bcb08b43bce3ca2594d4bf9e2b997f57bb7744bde5011cbdf5c404a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c3e9e074025dcb2f5487972592d9e5aca1de573eb9c8bcef2426e1d1f70a427e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231547428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb10dca2eeff819e46021d59e26406c5686e3dfc6ba35c3b536f7bf0dc1d4317`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:20:47 GMT
ARG version=17.0.9.8-1
# Fri, 12 Jan 2024 22:21:11 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:21:11 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:21:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 13 Jan 2024 01:01:59 GMT
ENV JETTY_VERSION=10.0.19
# Sat, 13 Jan 2024 01:01:59 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 13 Jan 2024 01:01:59 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 13 Jan 2024 01:01:59 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 13 Jan 2024 01:02:00 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:02:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Sat, 13 Jan 2024 01:02:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 13 Jan 2024 01:02:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 13 Jan 2024 01:02:17 GMT
WORKDIR /var/lib/jetty
# Sat, 13 Jan 2024 01:02:18 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 13 Jan 2024 01:02:18 GMT
USER jetty
# Sat, 13 Jan 2024 01:02:18 GMT
EXPOSE 8080
# Sat, 13 Jan 2024 01:02:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:02:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804a5c0be154d9be5ec18b320260870f1cdbcbd23f6293e89b7b03788361f4d`  
		Last Modified: Fri, 12 Jan 2024 22:32:01 GMT  
		Size: 152.0 MB (151964148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4919be9cc1b2e439550f68f4324e69d49f8d93820304b8e0a6201019c491694`  
		Last Modified: Sat, 13 Jan 2024 01:09:37 GMT  
		Size: 16.9 MB (16920646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5799160aadb31cfcb4543a4fce06a8d2b47f756e2ad3959bf9e3f4b5ec5e97f`  
		Last Modified: Sat, 13 Jan 2024 01:09:36 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:dc7f147849237dfe1a0f47951ecb8636198a0354106b8ebc01194d8ab8979280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231938728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34a9423126224f6a74fc34bdd5727fb5c7282e4e0a3bcfe1b5400eb8cb20d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:23 GMT
COPY dir:eb2de4474e28d9fde9bbe1ffb630978f47dae30856e760ca73ebb5d0cb75efd7 in / 
# Fri, 12 Jan 2024 21:49:24 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:33:37 GMT
ARG version=17.0.9.8-1
# Fri, 12 Jan 2024 22:33:56 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:33:57 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:33:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 12 Jan 2024 23:43:54 GMT
ENV JETTY_VERSION=10.0.19
# Fri, 12 Jan 2024 23:43:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 12 Jan 2024 23:43:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 12 Jan 2024 23:43:54 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 12 Jan 2024 23:43:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 23:43:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.19/jetty-home-10.0.19.tar.gz
# Fri, 12 Jan 2024 23:43:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 12 Jan 2024 23:44:09 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 12 Jan 2024 23:44:09 GMT
WORKDIR /var/lib/jetty
# Fri, 12 Jan 2024 23:44:09 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 12 Jan 2024 23:44:09 GMT
USER jetty
# Fri, 12 Jan 2024 23:44:09 GMT
EXPOSE 8080
# Fri, 12 Jan 2024 23:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 23:44:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9620bfd6832ce2ca50093b819c4f62fd86c4b96a997fd5da88afa856b28cb1a0`  
		Last Modified: Fri, 12 Jan 2024 19:03:15 GMT  
		Size: 64.5 MB (64462448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc468c97e95c424fa8d0d51bc53ca6d85ba872a1a1cbde8f3e8bcf22bed76ab`  
		Last Modified: Fri, 12 Jan 2024 22:42:33 GMT  
		Size: 150.5 MB (150509588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3210d62694ffb618f8ae1ae6d2738849e29310e05d55158daa4ddd51ed1e3a9`  
		Last Modified: Sat, 13 Jan 2024 00:01:41 GMT  
		Size: 17.0 MB (16965058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08130afa67596122c711b2f649ff24ea528a403aa3477c11d67257edc56d2c57`  
		Last Modified: Sat, 13 Jan 2024 00:01:39 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
