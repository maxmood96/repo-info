## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:7b157d65c58dc38ee345fdaa966bbaace35b0ab6c5971ce740f3ae4921fee662
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4f8b59e3856c4260ce674654bdb9b9ef74be98ca5930f83ab6bf61db69c3cf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248946217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45227ce3ec8a813edc3eba81996fb2577858a24c80477e489bc92fcd414caf52`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:08 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 05 Nov 2025 01:06:08 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Nov 2025 04:51:57 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 05 Nov 2025 04:51:57 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Nov 2025 04:51:57 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Nov 2025 04:51:57 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Nov 2025 04:51:57 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 04:51:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 05 Nov 2025 04:51:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Nov 2025 04:51:57 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 05 Nov 2025 04:51:57 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Nov 2025 04:51:57 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 05 Nov 2025 04:51:57 GMT
USER jetty
# Wed, 05 Nov 2025 04:51:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 05 Nov 2025 04:51:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Nov 2025 04:51:57 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb82af62a77255279f1c497851a6fe8f80f84cef1425a841bf7348ca44f3fa`  
		Last Modified: Wed, 05 Nov 2025 02:35:06 GMT  
		Size: 165.5 MB (165485971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da741b05429da6c00c672ef4d7b5ce5765a6f84e554f12ae4b45784f7c216436`  
		Last Modified: Wed, 05 Nov 2025 04:52:22 GMT  
		Size: 20.5 MB (20524302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c45bcf05ae0c23eb10925883b19f08f68c2232c09e74b1a8c916a27c2d0d63c`  
		Last Modified: Wed, 05 Nov 2025 04:52:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:67fb1bacb879f5af043818b55bb1c2759c5efec41b1d1acd5f135ed6dcb79313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad82d94e62cc1d422f4a15a5fcf4c1575c12bddb2bd2d0380217b0731ab04e6`

```dockerfile
```

-	Layers:
	-	`sha256:116dd3816ac6f68c727a5a2368ad6cc37511be07515f0afb6bb3df22a17ed073`  
		Last Modified: Wed, 05 Nov 2025 06:16:15 GMT  
		Size: 5.9 MB (5929838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1e6bfcf7f53da1dfc9f55dc52b61b5a9af697cd1925276ded943031a4a638f`  
		Last Modified: Wed, 05 Nov 2025 06:16:15 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fdb8da560e7253f59f6d0e8759e8b6e576f943fc8ca4043f358d2566ef18065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248968634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1eb388bdc4b928d78fe6ca23583bfd1457f2d0d1206381ff0c0208ff415b3a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:12:18 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:12:18 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 04 Nov 2025 23:12:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Nov 2025 23:26:46 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 04 Nov 2025 23:26:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 04 Nov 2025 23:26:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 04 Nov 2025 23:26:46 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 04 Nov 2025 23:26:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:26:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 04 Nov 2025 23:26:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 04 Nov 2025 23:26:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 04 Nov 2025 23:26:46 GMT
WORKDIR /var/lib/jetty
# Tue, 04 Nov 2025 23:26:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 04 Nov 2025 23:26:46 GMT
USER jetty
# Tue, 04 Nov 2025 23:26:46 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 04 Nov 2025 23:26:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 23:26:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad0d1fcc61302619a93c14ea37d679d5cc2a8f138552caa19924202526997b`  
		Last Modified: Tue, 04 Nov 2025 23:26:04 GMT  
		Size: 163.6 MB (163582941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61ba8342573e2313598dad079c832780d0b4ebade0ef0a1c121e738d5361b41`  
		Last Modified: Tue, 04 Nov 2025 23:27:05 GMT  
		Size: 20.6 MB (20590359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f576cb1f4eaddd8ddc3b1d4ccad0bfa71cb38c16613562e08416b8c8d018f`  
		Last Modified: Tue, 04 Nov 2025 23:27:04 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:78a44a997f6ed646d8fe2e8530744e94815357f8aa98a90f169279772c5c6d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588c05abfc30f682e505ac8d32d2e09b773e3d34ec780175dbfb8b77d7dff9c2`

```dockerfile
```

-	Layers:
	-	`sha256:2b5c4cd99c440596f1b61bb522e5eeb69fd751c8d9845d1ee361887455717b00`  
		Last Modified: Wed, 05 Nov 2025 00:16:44 GMT  
		Size: 5.9 MB (5928503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05c7ea33c1eb38abf15d2fc558c253ffc4b8b57085f5d1ab3784a69ea6f440a`  
		Last Modified: Wed, 05 Nov 2025 00:16:45 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json
