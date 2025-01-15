## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:e56d8d97270db4863afa9ade928e754be7b2eb00cf8647d431ccd70706235c2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:feea79789130431ac051db06448ff9c5c6769a11facb49fa748d99e1a0f84958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254741602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6011989f7c932b351ac0884b1471e14090f854803007f18cd79b7f5c8e31764d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff001010b923a0181362a7f37e350a3085467a2b774e124a0214de57212325`  
		Last Modified: Tue, 14 Jan 2025 20:34:19 GMT  
		Size: 151.6 MB (151604378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84d1049e56aeb8127c43cd9055c747684a06f62da51693ba11cce1f50a67b5d`  
		Last Modified: Sat, 11 Jan 2025 03:08:53 GMT  
		Size: 40.5 MB (40499728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8373aa80891fcbad9f9ad84af7b2fd2bbef70cbb52b837e0f630faab9c04518e`  
		Last Modified: Sat, 11 Jan 2025 03:08:50 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1d60147cf5634783aac4cd5aef1a00d60bccfd4395e8cb8a075c1f74cbc5a664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6039768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a339a54cf7abc6e6f99946f3b0e98c85702c52e60f1eb698033399f8ae7bae4`

```dockerfile
```

-	Layers:
	-	`sha256:e3b1135e6bccfb5c0daf6fe9e71fe2016cb12fe8983aaf0b49716c73ca3ace3a`  
		Last Modified: Sat, 11 Jan 2025 03:08:52 GMT  
		Size: 6.0 MB (6022367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d1cc6aea49ab4e95cc61d36c3f122a6b8f9e76cf52f3127852d107eace9b5c`  
		Last Modified: Sat, 11 Jan 2025 03:08:52 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f4b196c7db3725a6f85748f297bbbefc63d254a0d2c33144d330d2be6c4fa845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255445530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142cc7cc171b75b99d21651ff5d74e6849c63446aa973058b07935d7fbeb118c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3c3d5e7dd2769ec34c8a6782da13cd2fb91d9f2b7326bd873b4ffb1120d5f`  
		Last Modified: Tue, 14 Jan 2025 20:38:32 GMT  
		Size: 150.2 MB (150244756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b844d1e17d8f0fedccb8348dfe14311dcc1a25c6426f4c8a6c070cbbac297d`  
		Last Modified: Sat, 11 Jan 2025 03:50:51 GMT  
		Size: 40.6 MB (40608802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bed6d272e23a87fd48d9087f023b82348cea24f49a0e43973b8506ea9d1be3`  
		Last Modified: Sat, 11 Jan 2025 03:50:50 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3838b158e36df91f00f883719a674008bd1f2ed81fcff691956f13239cb9c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ff1cd7c98670772c40ff23a0a3c99e5df8d1a93f0c4eeacd21550525002ec`

```dockerfile
```

-	Layers:
	-	`sha256:d8c8a1c17a14189659abab0b37b4bf52d4a9c468492743a3b547b26ec3e16fe3`  
		Last Modified: Sat, 11 Jan 2025 03:50:50 GMT  
		Size: 6.0 MB (6020996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84e6efa8854a77ec4518a764a7fb4b983e10e1b4ecaca3603529f96c6ee451d`  
		Last Modified: Sat, 11 Jan 2025 03:50:50 GMT  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
