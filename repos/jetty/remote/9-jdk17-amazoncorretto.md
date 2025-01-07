## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:37022838b9127e0a1169c5fe9b82b122c8f04b3e492a6ceff284d799299266fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:23c8546cc941464d37fd76a3e07c14f2e179a0c9223b870c44cb475ceae440e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230385269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c14dfb4effe116b21e82188d205bcaacb40ae74197cb5de51e371f8b5853fb2`
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
ENV JETTY_VERSION=9.4.56.v20240826
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
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
	-	`sha256:8a5f5de3691ca636b1b640c27062a6f9a0abfd5fe0de5711031eb5f1523fb677`  
		Last Modified: Fri, 20 Dec 2024 23:14:40 GMT  
		Size: 16.1 MB (16097741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00046b12a514f29dbe4e79d05456dd317c81a53b76886b0ea6e06f9084744973`  
		Last Modified: Fri, 20 Dec 2024 23:14:39 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:32885894d55d68c7f7e128eaba74c45062ffaceb826b37dc34292c09c16dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5912707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f06458facca7028a8afa19d86e684a85cf0e021a9630974b62547101a14c66`

```dockerfile
```

-	Layers:
	-	`sha256:3800866d08e80f587fba34478e314d567207e3c56c892bb11c4419e8cb2020a9`  
		Last Modified: Fri, 20 Dec 2024 23:14:39 GMT  
		Size: 5.9 MB (5895277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6687c20edd5d9553a38e9488a94192025646420aa16180add2f6869051d38c1`  
		Last Modified: Fri, 20 Dec 2024 23:14:39 GMT  
		Size: 17.4 KB (17430 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d43c7aac62f7c06c5b5addcf4c574bba82ea0613ca718629245c0617b6b45776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231022173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291074cd76f5cb96cd112e6ce87934716639a0ee5453a90d216cf95736429a84`
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
ENV JETTY_VERSION=9.4.56.v20240826
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 04 Dec 2024 01:30:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 01:30:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.56.v20240826/jetty-home-9.4.56.v20240826.tar.gz
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
	-	`sha256:1286b98bd714a26fe96f8e5534493a65c854b959a4b44f28eb6a2e9ae883e380`  
		Last Modified: Sat, 21 Dec 2024 01:43:23 GMT  
		Size: 150.2 MB (150238978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e85d988f36f29f277612b245268f1a6951e3628d14d0c5cc2857be97951360`  
		Last Modified: Sat, 21 Dec 2024 04:40:48 GMT  
		Size: 16.2 MB (16199641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee557eae52d8fddbc455d33b83ddde7cd5009dd63caea1f32c745e8ce30b88d`  
		Last Modified: Sat, 21 Dec 2024 04:40:48 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d4550b1f246143d7f480c1d9addc56591a031550b6d3e94969cf1b6c87bf1d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5911429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f94ab7964f812d17967795fd2fbe24bf9e39a0ef1cb538168d941f99dd05f1`

```dockerfile
```

-	Layers:
	-	`sha256:6710bab01483dd655b50678c5e57da72d8ce854d21b0c056450e179c3532ad29`  
		Last Modified: Sat, 21 Dec 2024 04:40:48 GMT  
		Size: 5.9 MB (5893906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa16b2390a24ffbc49691095909764258855b597cf12090c7902338b75d58ee`  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json
