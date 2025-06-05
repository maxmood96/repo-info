## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:413de70e9bf7a6a21406909acb14d49acea7168c21bc8dbe64749861076af49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:789b486eadff6874a2eedbd5f7914a2d016241b57826c238b2ba97f48cf33bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255148032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4473e5035d4b755559d1058eb6e99b59f1566f7ecfc630fb090d77e527e18f32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5e8e7a00da5e54199b818ce7941f270d97472be3e2f3676fb333e1a3869ddf`  
		Last Modified: Mon, 19 May 2025 23:46:10 GMT  
		Size: 151.7 MB (151734253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0857b0fb3cefdcbe262a6907add36c415ec828480f5b2488bb4da100356aeb5c`  
		Last Modified: Thu, 05 Jun 2025 17:00:26 GMT  
		Size: 40.7 MB (40652101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fae38d456ec105cd36a55490c6a603e4c813dc8f31393393da86ebe5cf32ee`  
		Last Modified: Thu, 05 Jun 2025 17:00:02 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fd538b0217061615efc2917c90f991651d49dd109880e917d24aae53ced88ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6053756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279ab071ed7848fd1007a9a88d11533a2358d93d3e70e3f7aff1971e9258d18`

```dockerfile
```

-	Layers:
	-	`sha256:c420125a0d3d684e083951091c03ca53e544a160ac3030a269637c672533a2b2`  
		Last Modified: Thu, 05 Jun 2025 17:18:01 GMT  
		Size: 6.0 MB (6036355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2d21fc4cd36caab000ac1148dbb9d7a35dd2a257515be80426dcf0dba3360f`  
		Last Modified: Thu, 05 Jun 2025 17:18:02 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:7c51a621bb36917caececfad50f932c86f0810a02e42f44075c93488fb7e765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255719195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6809663bafe422a5c226cc2154ea46c42b425294a6840b68a0b689299d90c5a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_VERSION=12.0.22
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.22/jetty-home-12.0.22.tar.gz
# Wed, 04 Jun 2025 15:07:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 04 Jun 2025 15:07:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
WORKDIR /var/lib/jetty
# Wed, 04 Jun 2025 15:07:15 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 04 Jun 2025 15:07:15 GMT
USER jetty
# Wed, 04 Jun 2025 15:07:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 04 Jun 2025 15:07:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Jun 2025 15:07:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee6e95ea36d89af4f4cd7e8f243672db44afdd48ed329c3637ac24e8cf28ee`  
		Last Modified: Tue, 20 May 2025 00:16:49 GMT  
		Size: 150.4 MB (150399232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408fabb0dcc2781c00212aac1fb9264c5769087f38d9fc71f0779d226e63a2c2`  
		Last Modified: Thu, 05 Jun 2025 17:10:48 GMT  
		Size: 40.7 MB (40710790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8c8c76c2c0412749428bda0c66ba6a936944abd1df894400603405d512820`  
		Last Modified: Thu, 05 Jun 2025 17:17:45 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:51d59003880a38a523a3b6a4f4163e40265b651c08bb704573b81a1d756461fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35f43a957c1e8c77f3ded7cb4fb773c2878ad95bdba9343592a17e6a48aaef4`

```dockerfile
```

-	Layers:
	-	`sha256:d54a508b4e4076aed5547f3756b3691e1c9d681caf31d35e8cdbc179a9f8e538`  
		Last Modified: Thu, 05 Jun 2025 20:16:56 GMT  
		Size: 6.0 MB (6034984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eead79983b563de27596b174bb7a2c4006d56b2d7ef3991ee85db84055d2cb5d`  
		Last Modified: Thu, 05 Jun 2025 20:16:57 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
