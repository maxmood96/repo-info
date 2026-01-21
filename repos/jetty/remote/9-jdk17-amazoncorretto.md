## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:a0a00ac6c93e185f6550e2efb35d263813b37b1a7183233b4c2251277c9eb1d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:11e0babec858d8bc609a017459e6518781aca518cba78317dbe78f03bcc3fe82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231593451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13d189294a36809bf8eba2607910d86cd918d7dbdefe70795e603637e55d1da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:07 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:09:07 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:09:07 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 15 Jan 2026 23:10:06 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 15 Jan 2026 23:10:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:10:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:10:06 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:10:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 15 Jan 2026 23:10:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:10:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:10:06 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:10:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:10:06 GMT
USER jetty
# Thu, 15 Jan 2026 23:10:06 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:10:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:10:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b2373aa952072c4a2f4627407327ebe36b371e8477839d8f30e5669d37509`  
		Last Modified: Thu, 15 Jan 2026 22:49:20 GMT  
		Size: 152.4 MB (152425245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c8ccacb30b53255d02c9b9a84bba15fc5621a2be4254cd7d7523cf8e3185ad`  
		Last Modified: Thu, 15 Jan 2026 23:10:26 GMT  
		Size: 16.2 MB (16226174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d177c3f314bba4ab92beb8f99cfa6f1d5c9e25f44c5cccf11a87b272b24919`  
		Last Modified: Thu, 15 Jan 2026 23:10:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3d4cde5cc8a919d37d76e0d7769904128bcf65785a2e992120f9d196542cf6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a1d0dc6b6cd6562e15741c9d1c572da5536b588206ba695ce19584be20778e`

```dockerfile
```

-	Layers:
	-	`sha256:01258cabbb34288c9c0f5341595e7670d0cb319be785eef272bb36dda6cdc690`  
		Last Modified: Fri, 16 Jan 2026 00:20:43 GMT  
		Size: 5.9 MB (5914688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2c000b53f5a22bbb4496eb485f6150441e5606358f6f0ad36d379c9ae3d30e`  
		Last Modified: Fri, 16 Jan 2026 00:20:44 GMT  
		Size: 17.4 KB (17388 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:94f3d3028f709ef088e0d52b9a3ff5add8063b181b2e84e310b4946dd0dc1c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232025549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3580fbc685697e342c42ac2e112fa6858e4004f6155ca2ec99add3c61964792c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:09 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:08:09 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:08:09 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 15 Jan 2026 23:16:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Thu, 15 Jan 2026 23:16:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 15 Jan 2026 23:16:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 15 Jan 2026 23:16:37 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 15 Jan 2026 23:16:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:16:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Thu, 15 Jan 2026 23:16:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 15 Jan 2026 23:16:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 15 Jan 2026 23:16:37 GMT
WORKDIR /var/lib/jetty
# Thu, 15 Jan 2026 23:16:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 15 Jan 2026 23:16:37 GMT
USER jetty
# Thu, 15 Jan 2026 23:16:37 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:16:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b7da1ac0542372ade529b0109964dae17b785436e8afabb79539d076a5733`  
		Last Modified: Thu, 15 Jan 2026 22:09:02 GMT  
		Size: 151.0 MB (150976986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342bbbf7865298d84ef75939248f8b460e065430723a83572bac925ea95d3f81`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 16.3 MB (16276253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a43165b4b5a1f7dceafc7f983929f6de9e417ff3c686d8b994cb8994f097871`  
		Last Modified: Thu, 15 Jan 2026 23:16:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5996cda082115c3802874c980a3597bc6ee915f2a9e28f9fd97a6993538691cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03810244a5e731d261d1c68df30630b17b7b0bb6d6034b9449bf36cd616e037`

```dockerfile
```

-	Layers:
	-	`sha256:428852e9dc4233cd17820275ff30c6eb90ef11c885afbee99a0ee697e004d3fa`  
		Last Modified: Fri, 16 Jan 2026 00:21:20 GMT  
		Size: 5.9 MB (5913317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50af66a462687e53e6c7d02914c0b3716d126072e49eddefcaea522858b8868c`  
		Last Modified: Fri, 16 Jan 2026 00:21:21 GMT  
		Size: 17.5 KB (17480 bytes)  
		MIME: application/vnd.in-toto+json
