## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:cae5fc96505d7151debace5a248cba88090e0b7226beedf19b4a8ff87a56e32b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:75ad3704125a6ed80b161bd2f3eb8467463f6d37d7757ecf97cc8cd477cdb2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e17ae05c13ee68c13b02d9cc6b6defe7514aa455f563f9c4844d06136cae839`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:39 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:17:39 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:17:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:20:09 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 18 Dec 2025 02:20:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:20:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:20:09 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:20:09 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:20:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 18 Dec 2025 02:20:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:20:09 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:20:09 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:20:09 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:20:09 GMT
USER jetty
# Thu, 18 Dec 2025 02:20:09 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:20:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:20:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa664a9e63598be7c33de82039c1906be50b20b21fe7be4ce3e48358cd8c570`  
		Last Modified: Thu, 18 Dec 2025 01:18:25 GMT  
		Size: 152.4 MB (152417666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f5968a7df58467ce7ac3c2582097793516d7c22c34f73fb379063ec2dc7ec`  
		Last Modified: Thu, 18 Dec 2025 02:20:27 GMT  
		Size: 16.2 MB (16215602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067f4d4562423d752c04236d3e3a149673de076f681f58712272e475e7af7c2`  
		Last Modified: Thu, 18 Dec 2025 02:20:25 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:be2f7e1ca49b9c7da25c5d3ce8d5cd10947275ca1e4076000940282cfd7e6a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e6a577597a498e104a18ff6a60d583ddc363be15272d7bc01d28cb4d13907`

```dockerfile
```

-	Layers:
	-	`sha256:989314b6cd39f7451c41f74d848d9ab53aeaa76ef769fac312e43ebb0b50dbd5`  
		Last Modified: Thu, 18 Dec 2025 06:20:00 GMT  
		Size: 5.9 MB (5914688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53b50611afbda95b4f89412cdbe5b3c59b996e33ab2f328cb308dfcee435b89`  
		Last Modified: Thu, 18 Dec 2025 06:20:01 GMT  
		Size: 17.4 KB (17388 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:70330ccb47bcab860aecf01456415cfae47c6220aac400c66e02ecba8e9e1de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232057246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fb8d89d548b4d1e461d0d9308d0950d0d9fafa8f4fb48c04fbc50a50d216f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:04 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:04 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:26:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:20:25 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 18 Dec 2025 02:20:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:20:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:20:25 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:20:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:20:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 18 Dec 2025 02:20:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:20:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:20:25 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:20:25 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:20:25 GMT
USER jetty
# Thu, 18 Dec 2025 02:20:25 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:20:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:20:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca0a28db4df858f849233729de0ecf5383aff275c42bd9cf1d62bacb519c2c1`  
		Last Modified: Thu, 18 Dec 2025 01:26:46 GMT  
		Size: 151.0 MB (150989199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ef563cf2df0783e568ed1c6d9c60cae08e69eb89acf205fade396e614cd0f0`  
		Last Modified: Thu, 18 Dec 2025 02:20:44 GMT  
		Size: 16.3 MB (16270416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3c5ffda6970a02d63ccb9a1a6bd730bb370fc8c007a23081d787e1105e6585`  
		Last Modified: Thu, 18 Dec 2025 02:20:43 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a45944fac8eaaeec330a73d0bf73237bbafc6e862f7a3a14ea3a77656be1d137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e4e9782392bbb4f6f060ffd9c3d9617cd7214c52410ac8d053939f75a3f9ab`

```dockerfile
```

-	Layers:
	-	`sha256:2b26227ee7f926907eebceddb2a9d227b237c66f7b69838e12d99e7cc13ed8d3`  
		Last Modified: Thu, 18 Dec 2025 03:17:46 GMT  
		Size: 5.9 MB (5913317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f1423f80ef729fec2550a1547f116d8f20728444f45a3534cf17ddcb0b725f`  
		Last Modified: Thu, 18 Dec 2025 03:17:47 GMT  
		Size: 17.5 KB (17480 bytes)  
		MIME: application/vnd.in-toto+json
