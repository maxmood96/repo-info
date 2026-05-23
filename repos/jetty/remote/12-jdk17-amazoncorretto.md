## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:b83c81c074cf7699fbd771d902f435837b9046424832a93c021a8f3b8a854697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:98752efec113505f13e99a061188263aa05f04cfc75ddc1fa218c83404b3063b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267438442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c54f954d76c61b853320d6b7db0cb07cc3cab42c44ba950166482d70722926`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:37 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:37 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:07:52 GMT
ENV JETTY_VERSION=12.1.9
# Fri, 22 May 2026 22:07:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 22 May 2026 22:07:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 22 May 2026 22:07:52 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 22 May 2026 22:07:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 22:07:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Fri, 22 May 2026 22:07:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 22 May 2026 22:07:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 22 May 2026 22:07:52 GMT
WORKDIR /var/lib/jetty
# Fri, 22 May 2026 22:07:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 22 May 2026 22:07:52 GMT
USER jetty
# Fri, 22 May 2026 22:07:52 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 22 May 2026 22:07:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 22:07:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c70d1c6953a128a159df107482ccf05c002cb93693078cb9080127ce0eeff`  
		Last Modified: Fri, 22 May 2026 21:12:00 GMT  
		Size: 152.7 MB (152670549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ec31ab0deb898aa8c9eafe2e42df183f51f0b71e1b6038b940ccf9e9d634c`  
		Last Modified: Fri, 22 May 2026 22:08:06 GMT  
		Size: 51.8 MB (51814041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fdc2f54a4e5e3eb01e3de1705eb24eecd04afab4a307320d60beea8da353e7`  
		Last Modified: Fri, 22 May 2026 22:08:04 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fbba05f6f679fd0674efc8432bbfa8ff9676d469484d7ffd5685b7ddd04d2eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7b7218fadf2a3f025befa53f6d0f55859597c213a7a7fdb45bd85ab7321da9`

```dockerfile
```

-	Layers:
	-	`sha256:5e6b01d4f76dc2d410f8acf07e3774e555744639fcf8d70d38d4751244e30cbe`  
		Last Modified: Fri, 22 May 2026 22:08:04 GMT  
		Size: 6.1 MB (6119644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c68001c7b888b370bf58f3c1f8ea27d1cdadc7bf6cf6b666359883f708f4a84`  
		Last Modified: Fri, 22 May 2026 22:08:04 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0da737ccb62f1990550c6e93a91585d4b8e8aec3676ee475632a5e36cadc78d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267995488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e25c54472c32fbf433579b330498c46016e62468eda7d380888f37750baee46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:04 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:04 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:04 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:08:06 GMT
ENV JETTY_VERSION=12.1.9
# Fri, 22 May 2026 22:08:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 22 May 2026 22:08:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 22 May 2026 22:08:06 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 22 May 2026 22:08:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 22:08:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Fri, 22 May 2026 22:08:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 22 May 2026 22:08:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 22 May 2026 22:08:06 GMT
WORKDIR /var/lib/jetty
# Fri, 22 May 2026 22:08:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 22 May 2026 22:08:06 GMT
USER jetty
# Fri, 22 May 2026 22:08:06 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 22 May 2026 22:08:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 22:08:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d876074273e0cd4b6cf1c24604ff033565872c6d506da1298267fccc360c96`  
		Last Modified: Fri, 22 May 2026 21:11:25 GMT  
		Size: 151.3 MB (151318380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6251a6b4c7c21c074e701f0446f1f07df5c3515db11898580ac3e2fadfd48264`  
		Last Modified: Fri, 22 May 2026 22:08:20 GMT  
		Size: 51.9 MB (51885214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e1bf7d193e7f32240ac50c800b34a136d536711477259dc262ada06ec50be`  
		Last Modified: Fri, 22 May 2026 22:08:19 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:99b17d9f15ed8b2dd54079b96f3c5f19bc97ff3f89009a17c0a93e80a574cef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe6d35655ab70da1fa37641d0d3ec08ba615c5eee227f89135aa4f3bfa0ab22`

```dockerfile
```

-	Layers:
	-	`sha256:e2db173cbbb688371ab75f4abd3846630b2f56e9ecf8335a3c72304031fae62d`  
		Last Modified: Fri, 22 May 2026 22:08:19 GMT  
		Size: 6.1 MB (6118273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0d3c5873916860576bae78226e81cee0a009e46e88eaa4c3db21fb527f11ec`  
		Last Modified: Fri, 22 May 2026 22:08:19 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
