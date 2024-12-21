## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:2e3872bd7189a5d01e94ea600aa8cf22c752401c63937616280819e7ef7ff85f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6f075fa9484421285c16c6999910f42013ae4d89557d4e41d47f1800a9e40170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231227018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890cd74cabfc6f8783dbed1e861e3f3a1c81007798e469c12ba59b58a3572566`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 04 Dec 2024 01:30:10 GMT
COPY /rootfs/ / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Dec 2024 01:30:10 GMT
ARG version=17.0.13.11-1
# Wed, 04 Dec 2024 01:30:10 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=10.0.24
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.24/jetty-home-10.0.24.tar.gz
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Dec 2024 01:30:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
USER jetty
# Wed, 04 Dec 2024 01:30:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Dec 2024 01:30:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab261828f6d05146d337cb0cbf1b142becb434d0c55081fb828bba21c4236b30`  
		Last Modified: Fri, 20 Dec 2024 22:32:38 GMT  
		Size: 151.6 MB (151608423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49871f0e840a5ac30987c99b47b198f440d7a6f04844d2086bf527aef4042341`  
		Last Modified: Fri, 20 Dec 2024 23:16:11 GMT  
		Size: 16.9 MB (16939489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f099a342f35401fa51fa730401c2bfa512912764c195da028a3567d048cb28bc`  
		Last Modified: Fri, 20 Dec 2024 23:16:10 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ce34034176200c864a5106c48e14ff9fc5782828d34df6741af87b773cf3f7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5925904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec89c931becb4cb3258bab1120feabc6709e873d680aaa31a16edf5c5241cf`

```dockerfile
```

-	Layers:
	-	`sha256:99afda5a844ea726896b8d2f21804cf0934211ffc5fae739559d9a16663a3b81`  
		Last Modified: Fri, 20 Dec 2024 23:16:10 GMT  
		Size: 5.9 MB (5908503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8888ce54c121d683a7549aaaa0574fe79a11465af5c505a6ac5783df463bce`  
		Last Modified: Fri, 20 Dec 2024 23:16:10 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1fe4fbf02538e8748e2ad52cc4c023c23f95b017a164f944d7ec144ead1d07f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231859582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a82cc16db42f82d72797e3f65eeedb529433001bbec642a26e60fcdc548d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=10.0.24
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.24/jetty-home-10.0.24.tar.gz
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Dec 2024 01:30:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
USER jetty
# Wed, 04 Dec 2024 01:30:10 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Dec 2024 01:30:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737939e85848b34826899ab042c8aad6fc1fba8f7f661936f213981c4b20421e`  
		Last Modified: Sat, 16 Nov 2024 00:58:26 GMT  
		Size: 150.2 MB (150238943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a64d024c8ad648b753e8944b67b552cf44d71a2d1dbdcfe72616fd8fa940f2`  
		Last Modified: Wed, 04 Dec 2024 20:45:20 GMT  
		Size: 17.0 MB (17037086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dccacb425c3d68775340e0357fe8bdb9758d5e3800801be7065ddd025c664f2`  
		Last Modified: Wed, 04 Dec 2024 20:45:19 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9144153e2d881add73101cb71bc64b65b88aa78878377d0fb31b3bef716b307f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709e0b7d1fdf22a9eaa23931290ab224dbf752bfaa2f01db8b614b7f0dad8275`

```dockerfile
```

-	Layers:
	-	`sha256:a6029aa1bd1777b2e34260d6562e517156d3fb99a74c08642c86b1c1d1e0b943`  
		Last Modified: Wed, 04 Dec 2024 20:45:20 GMT  
		Size: 5.9 MB (5925504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc32bd1dee6776000e6a6afeea4a767fdd37060fcb83a5a83f3985d0dc3ddf0`  
		Last Modified: Wed, 04 Dec 2024 20:45:19 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
