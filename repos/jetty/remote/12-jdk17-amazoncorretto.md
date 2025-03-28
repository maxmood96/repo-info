## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:e6bfdec7cc38dcb8e9bd176fc196669e6b096d64284105246d5dce41bbd4ce11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:319bdbc3904dd4fb12bdc9aa90305b8ea5d6e4fd0a34eb7cb581bfff1f451b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255017891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88c1e40ea6648668b0b82348a14722f87cbe6acbe464b23c6ffecbe50cce547`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=17.0.14.7-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=12.0.18
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.18/jetty-home-12.0.18.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ea6810da602f5c914128478327d94321883aee9b0c8a02cc20b8a8282c9c4`  
		Last Modified: Thu, 27 Mar 2025 23:58:41 GMT  
		Size: 151.7 MB (151687302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c65ff7fe9a50e9bef743741ec4d10ef51b23935324da05a2c1e88f5e7171ff`  
		Last Modified: Fri, 28 Mar 2025 00:08:37 GMT  
		Size: 40.6 MB (40576007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745dc79413e2ad9491cb71b2a734d29b7ce12615c2c6153a4b6d4868f83efed`  
		Last Modified: Fri, 28 Mar 2025 00:08:37 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0e9054103376559d73f9c868750886a6fee98b68346666872b61ad7d8f63d8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6041051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a269d55c9f5a06aceee6b1b2be982d6738dd496785e79750c0f3761cc7d941`

```dockerfile
```

-	Layers:
	-	`sha256:7dcd5009aa50a2e20fe0849418d96cfb8568fd462f6a288641f9cb8135f57dce`  
		Last Modified: Fri, 28 Mar 2025 00:08:37 GMT  
		Size: 6.0 MB (6023650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8587bfd1455225b6002aeaf0d471054f16af77dd2901b7cac42dc5d0e3fe5b5a`  
		Last Modified: Fri, 28 Mar 2025 00:08:37 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:3e3d92565becd79e72b18a598a83627dd099c011b3c3804ad17a42704d9bc148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255490650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18743c24969160217c169a55f4fc56bcba9b267403275c3f39eafec901daa74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 19 Mar 2025 00:38:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 00:38:43 GMT
ARG version=17.0.14.7-1
# Wed, 19 Mar 2025 00:38:43 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_VERSION=12.0.18
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.18/jetty-home-12.0.18.tar.gz
# Wed, 19 Mar 2025 00:38:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 19 Mar 2025 00:38:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
WORKDIR /var/lib/jetty
# Wed, 19 Mar 2025 00:38:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 19 Mar 2025 00:38:43 GMT
USER jetty
# Wed, 19 Mar 2025 00:38:43 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Mar 2025 00:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 Mar 2025 00:38:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb0a04e32045bea8a36477ff07d28428a7ae7e142505376782ccaa20b05e7b`  
		Last Modified: Fri, 28 Mar 2025 00:13:29 GMT  
		Size: 150.3 MB (150303064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040b22eaafaddc5c8a353cc1a12a4402ac1bb685b0d66a970f1e454001be12f9`  
		Last Modified: Fri, 28 Mar 2025 01:31:52 GMT  
		Size: 40.6 MB (40620072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e116b0aedefb3b134635516bbff0b1324a8638328af0d4b11ecc75f650e846f9`  
		Last Modified: Fri, 28 Mar 2025 01:31:50 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:11bf918afd1daa99d4aabc3153b92b6657b4a45cae9a44bdcfcd42f28c2c9652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6039772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312392764b3bdebb5cb83ecf8aaa4b70f1e23c8161fe1195e7a1550cf9504484`

```dockerfile
```

-	Layers:
	-	`sha256:6fff1684811c46252b4aecbabf5c914c3292810b8ada5977639301d68dd49cfb`  
		Last Modified: Fri, 28 Mar 2025 01:31:51 GMT  
		Size: 6.0 MB (6022279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d01ca7238fa18520b4b964f252f305685935261f826c92ae8c0b4ef698baf6b`  
		Last Modified: Fri, 28 Mar 2025 01:31:50 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
