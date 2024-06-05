## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:85b7a6cedd3ab4f1f3c423f5b1f3d69a071c21a388ac8feb7946a3eade6373e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b64055c7067d568352899c639157e0414d5f976fedfc29add77e331f6acaa6ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231689747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafab1dbcbe512c6d994b184f2d6645c6adaba7655f49eaa0104cd1e72aee164`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:51 GMT
COPY dir:0754eb292d5814ae413cf45230cbfcb3aa86721e44b9e74852126d7313389c72 in / 
# Wed, 05 Jun 2024 00:26:51 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:41:13 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:41:36 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:41:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:41:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 05 Jun 2024 08:47:26 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 05 Jun 2024 08:47:26 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Jun 2024 08:47:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Jun 2024 08:47:26 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Jun 2024 08:47:26 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 08:47:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 05 Jun 2024 08:47:26 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Jun 2024 08:47:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 05 Jun 2024 08:47:44 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Jun 2024 08:47:44 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 05 Jun 2024 08:47:45 GMT
USER jetty
# Wed, 05 Jun 2024 08:47:45 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 08:47:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 08:47:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8a0995d2bf38a3ce742d376865782dab667a8fd7d3ded687b5775794788440be`  
		Last Modified: Fri, 31 May 2024 00:52:59 GMT  
		Size: 62.6 MB (62646348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd720c14c5c33474f61295a392a61ece0919dda8518ea7cbbc7be69f5e58942`  
		Last Modified: Wed, 05 Jun 2024 02:54:24 GMT  
		Size: 152.1 MB (152144890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b32a08e750fc18701d0c0ac10afc8b8c15f76d699d0a6f053448a7aa22fa8dc`  
		Last Modified: Wed, 05 Jun 2024 09:01:36 GMT  
		Size: 16.9 MB (16896876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87eb5261efa6f61d06053c6d02924b20241d6a5ae24f47c19a7cd3c7b6817`  
		Last Modified: Wed, 05 Jun 2024 09:01:35 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:3394a7b3b325bcc6b4b1ccd3a18996f58223938e602ee1dc5d2bc6d8887fa400
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232397238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1469c87eecdc7dc704b5f5a41a57b3965009c40ed6521c7faf6aa6c84b6c1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:33:01 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:33:19 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:33:21 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:33:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 05 Jun 2024 07:53:33 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 05 Jun 2024 07:53:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Jun 2024 07:53:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Jun 2024 07:53:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Jun 2024 07:53:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:53:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 05 Jun 2024 07:53:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Jun 2024 07:53:48 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 05 Jun 2024 07:53:48 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Jun 2024 07:53:48 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 05 Jun 2024 07:53:48 GMT
USER jetty
# Wed, 05 Jun 2024 07:53:48 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:53:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:53:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3c637a564c65c75ae813e2f950aa58a12afb7e860d4acd055a45c8698317c`  
		Last Modified: Wed, 05 Jun 2024 02:43:45 GMT  
		Size: 150.8 MB (150797207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3266e5382de4e24be8362725fc2ffea637609d8dfc56240ef93858efe8ffa1f`  
		Last Modified: Wed, 05 Jun 2024 08:05:54 GMT  
		Size: 17.0 MB (17022958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bd747fa3b935daa705505a88a50c9e8d70667fca1b2e8c4fafea6790e6dc23`  
		Last Modified: Wed, 05 Jun 2024 08:05:52 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
