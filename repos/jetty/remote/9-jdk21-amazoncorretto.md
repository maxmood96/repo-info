## `jetty:9-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:2524fa7d9f14424e463df9e0bd6ceb267bf3856503f8bd6fa1cd497a7457bd9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:db6d5791e425b9726c571bdac64c29d2af46e30a0be378ae6250092e08cfd937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244626305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a5db081bd03e446a885506ea69f0cce0fce5c2d705b5b90af6473d42b830b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 08 Jul 2024 06:35:54 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 06:35:54 GMT
ARG version=21.0.4.7-1
# Mon, 08 Jul 2024 06:35:54 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
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
	-	`sha256:ec5aa352e5e798908f4002feb10e2247696b6b1c61528d1f0c363963bab84785`  
		Last Modified: Sat, 07 Sep 2024 01:56:20 GMT  
		Size: 16.1 MB (16109549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196bccaa7fbb36bc553716e26a4e801c9724a53f4520daa42b4c4afc3fe6cbd`  
		Last Modified: Sat, 07 Sep 2024 01:56:20 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4cf4e275c2df88b53923b7dc1156d71688756f9bbb3e603a95038cadc52c7a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93eaf4e9470ca7c83644c603f43cc1b1a92cb6c67a2b760868b039e7236fe458`

```dockerfile
```

-	Layers:
	-	`sha256:0c8111fdec08ac325497eba2b2a999dcc71cca93458598879e39c735b8c5f496`  
		Last Modified: Sat, 07 Sep 2024 01:56:20 GMT  
		Size: 5.9 MB (5906271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97700e1a8909b267b405bcdf8f20d7c6d5587a0f971a67bcc0c792fd7b096bd3`  
		Last Modified: Sat, 07 Sep 2024 01:56:19 GMT  
		Size: 18.1 KB (18123 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1a608b899771e174d4b08355b95510eeb1d160a3df8b316178e6e193c8e07865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244615071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ec33d977efc483587c1d4d2236da9925e00a3a8884b229e60f66e4e6013d9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 08 Jul 2024 06:35:54 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["/bin/bash"]
# Mon, 08 Jul 2024 06:35:54 GMT
ARG version=21.0.4.7-1
# Mon, 08 Jul 2024 06:35:54 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Mon, 08 Jul 2024 06:35:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Jul 2024 06:35:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Jul 2024 06:35:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 08 Jul 2024 06:35:54 GMT
USER jetty
# Mon, 08 Jul 2024 06:35:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Jul 2024 06:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Jul 2024 06:35:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccb17f585e623ab3c6d7898c58a94c2ecc6aac965f9d369b9389bfafa591557`  
		Last Modified: Sat, 07 Sep 2024 13:26:49 GMT  
		Size: 163.8 MB (163820593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba0d84e57be597a5063b072082f9d4aa9e6fd30c96498db8263e12470ba00d`  
		Last Modified: Sat, 07 Sep 2024 14:39:21 GMT  
		Size: 16.2 MB (16206468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37824e5616ddb42d879e4a0dfaf00e3e16f39ab173de12e8ef6a165d6c7eb6`  
		Last Modified: Sat, 07 Sep 2024 14:39:20 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0d569441614f05a16b4d93eb02ae3950c1237b35c1463c112dd48aa8d75e9977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc1b457fc40d6b0fbbca04967dbb1af83a9db05a4a990ff379dbdc1ef89b4e6`

```dockerfile
```

-	Layers:
	-	`sha256:246a546a062a9e7c22f2c74c0da0a4ff8e93c65d90240dfa72f796cc7a65d115`  
		Last Modified: Sat, 07 Sep 2024 14:39:21 GMT  
		Size: 5.9 MB (5904934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168a4b6b68612eeebd116918fa81ac419090e45252c5d190445e867713e975cd`  
		Last Modified: Sat, 07 Sep 2024 14:39:20 GMT  
		Size: 18.5 KB (18532 bytes)  
		MIME: application/vnd.in-toto+json
