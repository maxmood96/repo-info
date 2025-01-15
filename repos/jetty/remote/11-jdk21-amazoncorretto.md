## `jetty:11-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:a13da1b66fe1cb260412f9b03a0d09da68c83a1a0d0e0a26ed4df45af0a3e83a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e16c61e4b51dc7e2d60c3769045712315250a959be6d157691644b1536acc79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247781695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71077e0a763ae39bb5eb7d19db2ac7ff72d646d641a26607be84b243d19c245c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 04 Dec 2024 01:30:10 GMT
COPY /rootfs/ / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Dec 2024 01:30:10 GMT
ARG version=21.0.5.11-1
# Wed, 04 Dec 2024 01:30:10 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=11.0.24
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.24/jetty-home-11.0.24.tar.gz
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba40bee579293bea80d8fd5bf17d1160fb8b86b90eb6dc7c12a0774bb9c5df2a`  
		Last Modified: Sat, 11 Jan 2025 02:29:40 GMT  
		Size: 164.8 MB (164774059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f48d3b8da37aafd5197b16b9ea88ebf1b042fc6e4194ab791f9e41a3e85b02`  
		Last Modified: Sat, 11 Jan 2025 03:08:51 GMT  
		Size: 20.4 MB (20370140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffabd341c71c6539515ab7491ca2050bb4985dc7566395e4440af9a64575bb65`  
		Last Modified: Sat, 11 Jan 2025 03:08:49 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:219dd044a92322d9642e040de9a7907dd0f2af30e6a89746fe9f3498a6a39213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad4850dc2205122211b282f4313388c61c036385f86d363b722a9446d9c7622`

```dockerfile
```

-	Layers:
	-	`sha256:5be30477051abf21559414cecd847784780cf7f97602b69838bffa90863c4360`  
		Last Modified: Sat, 11 Jan 2025 03:08:50 GMT  
		Size: 5.9 MB (5909418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a5ce88d249d1ff283739971fac060f738236af4644ffb820cb4dbe62f38429`  
		Last Modified: Sat, 11 Jan 2025 03:08:50 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6d27d92b6989249b499f9a1480e102fa47fc84c3e5f972b732e7a6754f5dc35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247935504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083ac6803b0d5a37278887455dc86ed303cc7bcda9ebc7f9a2652e3757bc6e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 04 Dec 2024 01:30:10 GMT
COPY /rootfs/ / # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Dec 2024 01:30:10 GMT
ARG version=21.0.5.11-1
# Wed, 04 Dec 2024 01:30:10 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 04 Dec 2024 01:30:10 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_VERSION=11.0.24
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.24/jetty-home-11.0.24.tar.gz
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Tue, 14 Jan 2025 20:35:27 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48854f99fd7ce00ff7770349e5c1ecba06bdce170ca9ed4983d3f4dc6481d497`  
		Last Modified: Sat, 11 Jan 2025 03:09:29 GMT  
		Size: 162.9 MB (162850542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42cc1f9e4f4d10f5750bd45178bf772e99c69f66746fdf18075498a952fd2b1`  
		Last Modified: Sat, 11 Jan 2025 04:14:10 GMT  
		Size: 20.5 MB (20492992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02725708fd3c898dc9853e83539bb35f3bb2b2b191777e6b40432002db456f0a`  
		Last Modified: Sat, 11 Jan 2025 04:14:09 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:07d140f261bda2b7f990f25603796aaa41eeaf024bf608b5a4d946212ccab9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11ae507dcd8f6ab6df07030cdab8508393f85d1635ade16ecfe553e033dfd47`

```dockerfile
```

-	Layers:
	-	`sha256:65dbb70f27c4b0504dc8f8a69fc98a3ef8f9074ef61ef3da07846e7ca9843355`  
		Last Modified: Sat, 11 Jan 2025 04:14:10 GMT  
		Size: 5.9 MB (5908083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccde5d8dbb55a4d1a9a75069be1da6dee9a4cce1009cb29ba0b1cc99416bae43`  
		Last Modified: Sat, 11 Jan 2025 04:14:09 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
