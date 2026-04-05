## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:4129902281e9911b06671777787d59bb7b7ad5f274eaf90bb57611c03ce5c04d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c2f9939d283d701bb437db46b400bb2e44a7d5afaeb82811b597dde0b333dee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267256098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193323fc103a69aec5e67afb217060bedf56a3e3e531116a32b9bcc6f25192a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:09 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:09 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:14:09 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:13:11 GMT
ENV JETTY_VERSION=12.1.8
# Fri, 03 Apr 2026 23:13:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 03 Apr 2026 23:13:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 03 Apr 2026 23:13:11 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 03 Apr 2026 23:13:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 23:13:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Fri, 03 Apr 2026 23:13:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 03 Apr 2026 23:13:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 03 Apr 2026 23:13:11 GMT
WORKDIR /var/lib/jetty
# Fri, 03 Apr 2026 23:13:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 03 Apr 2026 23:13:11 GMT
USER jetty
# Fri, 03 Apr 2026 23:13:11 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 23:13:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Apr 2026 23:13:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629127badbb34f2290251a80df183d34aa4ca03ca8cf38411493f3aeaca26cce`  
		Last Modified: Fri, 03 Apr 2026 22:14:28 GMT  
		Size: 152.5 MB (152455948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dc10c9cd2e13b09c0c512defcf85cd68b4330c5682ddaf25a2854997c0437e`  
		Last Modified: Fri, 03 Apr 2026 23:13:25 GMT  
		Size: 51.8 MB (51842973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece6e010b0ea6d6937942e3e011f581733efa9baa220257b8c810f2cfc6f0130`  
		Last Modified: Fri, 03 Apr 2026 23:13:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:575b0c37be776d444d0c8134a5cf99c87fcc963e1629065329bb958427985f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6166547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bef5a686f5b833fcb8c954b72f9128d0cfd0564062003fd8f8e45d93eccabea`

```dockerfile
```

-	Layers:
	-	`sha256:815a3db1210fe6262431435808da523f1fc8e70bd039272a2e04a96893ea8e5b`  
		Last Modified: Fri, 03 Apr 2026 23:13:24 GMT  
		Size: 6.1 MB (6149194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df920b5776037f565b1136f391fb76119edef847009fa257a6cdde377290013`  
		Last Modified: Fri, 03 Apr 2026 23:13:24 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:be448acc6757af00144913c5aa6718f05cd3585ddd23fc902dbb8521e05c6654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267673415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c594378341b633b54743c9cfaadb5b9e57a11557a1ffbf2c7f8509259311fa26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:41 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:13:41 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:13:41 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:13:43 GMT
ENV JETTY_VERSION=12.1.8
# Fri, 03 Apr 2026 23:13:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 03 Apr 2026 23:13:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 03 Apr 2026 23:13:43 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 03 Apr 2026 23:13:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 23:13:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Fri, 03 Apr 2026 23:13:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 03 Apr 2026 23:13:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 03 Apr 2026 23:13:43 GMT
WORKDIR /var/lib/jetty
# Fri, 03 Apr 2026 23:13:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 03 Apr 2026 23:13:43 GMT
USER jetty
# Fri, 03 Apr 2026 23:13:43 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 23:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Apr 2026 23:13:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1200879671d0b9b8f7eb006d486fe28538ebbeef1137aaadb6db419ae8d50b`  
		Last Modified: Fri, 03 Apr 2026 22:14:04 GMT  
		Size: 151.0 MB (150970895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c57c22aac2f8db1949aae1759bdd7455c456d7dc44d4e9bdce224948c9ecf7`  
		Last Modified: Fri, 03 Apr 2026 23:13:58 GMT  
		Size: 51.9 MB (51897805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af742070599436455d12be1b4d7db08b32a8a1d1c77de607148f756c5f8835`  
		Last Modified: Fri, 03 Apr 2026 23:13:57 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ae9b5de7afc648141c002b975633f3e13ea9174c4ab0c0fdd9f785db3ebd30b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6165267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e2f9e396b457a0928d099a35aaf4e3060279f2caa886abcf08fc50fa5f269c`

```dockerfile
```

-	Layers:
	-	`sha256:a2921d11d8b5e2d99e0b779504e4a1b83f333f2717840ecdada35e6e61c74489`  
		Last Modified: Fri, 03 Apr 2026 23:13:57 GMT  
		Size: 6.1 MB (6147823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd85a64e216eadc473da05c2ad5cce785b27730d11c4962412a4711749b0cb8`  
		Last Modified: Fri, 03 Apr 2026 23:13:57 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json
