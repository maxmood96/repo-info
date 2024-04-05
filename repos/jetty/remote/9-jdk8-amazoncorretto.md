## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:784a65445dd39a8ec4840a947d2b276d4d37f8574eab12c247f47f8e07978af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8467592959671217e31548a99e1ac031e02d923ae50204cff75450803ccec640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153949740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766143ac81ebbf398879c46a1323250d3bddca3c2ef33f35c81ed063dd9d718f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:31:05 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 13:31:27 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:31:27 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:31:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 18 Mar 2024 18:45:29 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Mon, 18 Mar 2024 18:45:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 18 Mar 2024 18:45:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 18 Mar 2024 18:45:30 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 18 Mar 2024 18:45:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 18:45:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Mon, 18 Mar 2024 18:45:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 18 Mar 2024 18:45:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 18 Mar 2024 18:45:50 GMT
WORKDIR /var/lib/jetty
# Mon, 18 Mar 2024 18:45:50 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Mon, 18 Mar 2024 18:45:50 GMT
USER jetty
# Mon, 18 Mar 2024 18:45:50 GMT
EXPOSE 8080
# Mon, 18 Mar 2024 18:45:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 18:45:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8fb3e842b158f995b64b7e9c9b16fd7309e3efe721677a541055d89e9df989`  
		Last Modified: Sat, 16 Mar 2024 13:44:23 GMT  
		Size: 75.5 MB (75529612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd92288d0452d327295dea3c9fbaf32a668e0cd333534d4028d58ecd1fdcd5f`  
		Last Modified: Mon, 18 Mar 2024 19:02:20 GMT  
		Size: 15.8 MB (15767944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bedb0943de45017a49b394f70309ca218a6b8307e3d402de2aa1b0ecdffb473`  
		Last Modified: Mon, 18 Mar 2024 19:02:18 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a92875210177bb7c1b271678b3d4b9fee5842de7b169ee92f07bb04df86355fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140063235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ea2544e54e7bc1818ee2e0f85b48bf46406abf4709ba68ceaf409c6bd0b576`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:43:15 GMT
ARG version=1.8.0_402.b08-1
# Fri, 05 Apr 2024 18:43:31 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 18:43:32 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:43:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 05 Apr 2024 19:20:00 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 05 Apr 2024 19:20:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 05 Apr 2024 19:20:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 05 Apr 2024 19:20:00 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 05 Apr 2024 19:20:00 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 19:20:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 05 Apr 2024 19:20:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 05 Apr 2024 19:20:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 05 Apr 2024 19:20:17 GMT
WORKDIR /var/lib/jetty
# Fri, 05 Apr 2024 19:20:17 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 05 Apr 2024 19:20:17 GMT
USER jetty
# Fri, 05 Apr 2024 19:20:17 GMT
EXPOSE 8080
# Fri, 05 Apr 2024 19:20:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 05 Apr 2024 19:20:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa646d1af5c4bcd4cda7d1d93a5796974c96ea6fd6cd38c3d506fa9a9c1e1b0f`  
		Last Modified: Fri, 05 Apr 2024 18:55:17 GMT  
		Size: 59.6 MB (59628368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55345ddda8acb5ba68a2dbcbb58e9b6493f4bf8d23701690eee844393070de1a`  
		Last Modified: Fri, 05 Apr 2024 19:27:12 GMT  
		Size: 15.9 MB (15872624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb9feae5dae69b1f7aa90348bb051e750bd9b508a4aac8027cf7fc465f1daf1`  
		Last Modified: Fri, 05 Apr 2024 19:27:11 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
