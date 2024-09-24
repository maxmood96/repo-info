## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:d27efe249bd6a791598be1cb2a238caf5c52e6c92fe324d996655ab0263ce130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:f7bb2f7e15acc72a94e9795b1da8da0abd067dd1b0deaf9edce0c3f4834a5e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268956679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acef581934918eb67008574aa32e6592a067ac1210b90850bb1c30e172643987`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=12.0.13
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.13/jetty-home-12.0.13.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31392d7ddaaf1b0a5a2312e768716ba381912bc41f814ef2a3e7e3a0ea9f9f5`  
		Last Modified: Sat, 07 Sep 2024 01:05:55 GMT  
		Size: 165.8 MB (165819543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c630abd6ab976455f985dbbfec31546cdbc97b5962e3dac77e99d6c32f9e5`  
		Last Modified: Tue, 10 Sep 2024 21:58:08 GMT  
		Size: 40.4 MB (40439923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883da51654a339f732fa4fc48a3bea5849f47ebf0b2ef602746d63886b4deef`  
		Last Modified: Tue, 10 Sep 2024 21:58:05 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8f316389903ed29e9979fe60a72bb7d3a3166a2885bf7209e8fc6171f7d369aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1e099df5eed3a9850624c38c9957d1c786a8f9032a31ca28c30c3dfbe9174`

```dockerfile
```

-	Layers:
	-	`sha256:8049a8491727de105ad5372089193cd9b015af1d838fddd6bd184f140522ce59`  
		Last Modified: Tue, 10 Sep 2024 21:58:07 GMT  
		Size: 6.0 MB (6031092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44906cab097dc455449e137f07106c0f8d30b4c7f390c8046cbf4c0a60474e6d`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 18.1 KB (18099 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1924932fdf47f1467d2bddf90b5794e64c909d02d59ebc4f2371c60f223074ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268939837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47394b25f4d090845fc59986405c7bd1b62ed9566b025a8a03c5890ba625703a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 10 Sep 2024 00:22:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 00:22:25 GMT
ARG version=21.0.4.7-1
# Tue, 10 Sep 2024 00:22:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
ENV LANG=C.UTF-8
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_VERSION=12.0.13
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.13/jetty-home-12.0.13.tar.gz
# Tue, 10 Sep 2024 00:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Sep 2024 00:22:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Sep 2024 00:22:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Sep 2024 00:22:25 GMT
USER jetty
# Tue, 10 Sep 2024 00:22:25 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Sep 2024 00:22:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 00:22:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d21619c9feeafe24fc45c11645e23e593781a0a9acf5090729190d13af4a2b9`  
		Last Modified: Tue, 24 Sep 2024 02:42:43 GMT  
		Size: 163.8 MB (163820383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80eb3717dccd6baa7936d16cd2b8b90c667c0f91341c15bb136ddfc9fdd2433`  
		Last Modified: Tue, 24 Sep 2024 03:00:41 GMT  
		Size: 40.5 MB (40531241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befbdd0eb90f8427968c745edb32a510d44b3977e96cd55caf24b145fc62f8ab`  
		Last Modified: Tue, 24 Sep 2024 03:00:40 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8dbce14000967e6f78a976a0189268b7329a7847866e0439ef3ff025fe3ac3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4c3b031a48574c7a9bc41c69b917cb0cfa55840bdb11c28932202c0b120d8d`

```dockerfile
```

-	Layers:
	-	`sha256:69af995d66849bf1e14a3420ebb38e7974aa524e2fb784fcca979196f68eac7e`  
		Last Modified: Tue, 24 Sep 2024 03:00:40 GMT  
		Size: 6.0 MB (6029755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a7b97a9a3704d2d2f3f75b4b60e5c3b2336f782eb09b4860192aa22b93c38d`  
		Last Modified: Tue, 24 Sep 2024 03:00:39 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json
