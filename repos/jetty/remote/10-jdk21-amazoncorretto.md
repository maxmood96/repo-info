## `jetty:10-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:b4f1f38a0c967f94c5e58cdeb6d4bcda175793586775d0167200a5e43c184959
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:70c0e95768003373c11a185e576c7b14c461c45731c1fdfd887c99dabc5f5a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245506973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ab6f61e574fd8d86814d5a694fcca8b82b39a8758064cda84202bf2b99bc9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:25 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:25 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:13:47 GMT
ENV JETTY_VERSION=10.0.26
# Fri, 31 Oct 2025 01:13:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:47 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Fri, 31 Oct 2025 01:13:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:47 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:47 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:47 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b8bf1a2d41e5961e041978e350f514e0b16151864da2fa18fedc6f348e6f0f`  
		Last Modified: Fri, 31 Oct 2025 01:11:23 GMT  
		Size: 165.5 MB (165482592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1d62e9fd763541381a7b69cf420e75f71d0e0f128023afe6e3861b1cb2c2c3`  
		Last Modified: Fri, 31 Oct 2025 01:14:05 GMT  
		Size: 17.1 MB (17088437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3a6c3f320c2f783be3d1ab451c218a81a3b5d0a68e3bf8081e552098214182`  
		Last Modified: Fri, 31 Oct 2025 01:13:58 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1d783bf1ada18d011a39811525eb5fc0efdcdb759885860b2c2eb5dca871c029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2457b9b8d947b7f8f29d6a12155e948cb11e3ca037efce05415e0f38da079c22`

```dockerfile
```

-	Layers:
	-	`sha256:32dd0a04486643d9fb3809edfe06b1b1408c126cee69a2a188763ce3f6d906e5`  
		Last Modified: Fri, 31 Oct 2025 02:15:20 GMT  
		Size: 5.9 MB (5929788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cfd0e473405bd194dd137224e6a14d419015451b1313b99349028ccae4526c4`  
		Last Modified: Fri, 31 Oct 2025 02:15:20 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:16c2194cca169a9bcbd6e06b74669cebe4ac83179c14a0c320bb0a2fa78640fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245533705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de57dde83b6067bb8db1f0e7eece20b31aa789d4c2391437eb705e738ed747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:14:02 GMT
ENV JETTY_VERSION=10.0.26
# Fri, 31 Oct 2025 01:14:02 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:14:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:14:02 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:14:02 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:14:02 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Fri, 31 Oct 2025 01:14:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:14:02 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:14:02 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:14:02 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:14:02 GMT
USER jetty
# Fri, 31 Oct 2025 01:14:02 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:14:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd1baf4e91e00d7b9956781f2599d36622339644d5c2a7ec70735ba3ae40162`  
		Last Modified: Fri, 31 Oct 2025 01:13:02 GMT  
		Size: 163.6 MB (163587405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750d5024809d6bfa30da61ed9a033d606444aa2842c76bd0eb17edaafc90133c`  
		Last Modified: Fri, 31 Oct 2025 01:14:23 GMT  
		Size: 17.2 MB (17150966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e794de0da49d66311baeaf3b6f0811169e7ad0610b3291df5abb0da44aaaf6`  
		Last Modified: Fri, 31 Oct 2025 01:14:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b04c1b8a42894ee3936b1f9c9df525eaaa998bec8da4fea723674cdcaf58a645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9aa7697d1f34492f22ca968d0a526fcf6752f969a9ad5e707a434059edc590`

```dockerfile
```

-	Layers:
	-	`sha256:ff768514a9a49d420104cd988a2d4f99eb2e1d9cb0d828e8b79656e07f448c92`  
		Last Modified: Fri, 31 Oct 2025 02:15:26 GMT  
		Size: 5.9 MB (5928453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f040c1e02c3b2ad50c5104822f6a328b05f233dc7e017913a0642bf3db0c58`  
		Last Modified: Fri, 31 Oct 2025 02:15:26 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json
