## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:659edc3dab8312d9b7ca48208c86232700c7cbb30308e77485c0c43ea5a44ef6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6b37d3035cfc1964f03568e09ba2ebf64991ec8d4c9f7242ee48149d0d6fbcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235880865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde86e9b29d1a72ffcacda6e7014ea8770790d1e7c0fc7310d129805b6ca916a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:47 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:15:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:15:47 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:16:16 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 14 Nov 2025 03:16:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:16:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:16:16 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:16:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:16:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 14 Nov 2025 03:16:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:16:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:16:16 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:16:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:16:16 GMT
USER jetty
# Fri, 14 Nov 2025 03:16:16 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:16:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:16:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2eeedbb6c19345cead693cc54b4ab6b968c029966c1439c8e1b1921ecaed2c`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 152.4 MB (152415922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01298a74df2bac9d7d6ce6804bb7970ea1e6e6e2a45c96ef36c705586d7ff7d5`  
		Last Modified: Fri, 14 Nov 2025 03:16:35 GMT  
		Size: 20.5 MB (20532495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6f9cb4fe7bba0e0844ab4424c39566588907aeb4e2ef567f7cf6ad715da8f`  
		Last Modified: Fri, 14 Nov 2025 03:16:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:943a5d36565f62f6c937742039476fd9db554d7408de1222ce44a08201a6ce2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e10dee65317f3e6d9c80cbde5e89017f25e0abea3fcad596ea9d6b9de27bd`

```dockerfile
```

-	Layers:
	-	`sha256:3e7f6fa0c46c53d070d4938dbac4645b26d11a5db381acafacf645c0e91a9ac6`  
		Last Modified: Fri, 14 Nov 2025 06:16:53 GMT  
		Size: 5.9 MB (5928977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4920aaa0058126f5859951e92b55db39cf90bf123cf40cbda96ffea9eb4ceb44`  
		Last Modified: Fri, 14 Nov 2025 06:16:54 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:61cdfc0bca0a5fff9f63db359da67fc88c19dbc86d93f1674c0709e5ac868c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236376035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd110888f5e8e81d609893e2bce156d9c63a60a0c06700c7a0d2b89b10691f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:17 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:17 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:17:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:16:38 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 14 Nov 2025 03:16:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:16:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:16:38 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:16:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:16:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 14 Nov 2025 03:16:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:16:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:16:38 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:16:38 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:16:38 GMT
USER jetty
# Fri, 14 Nov 2025 03:16:38 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:16:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:16:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b8742846c34daad6dea6d70c9dbb64562941f5ec5c46f8d2eb1e6eb5241816`  
		Last Modified: Fri, 14 Nov 2025 03:15:35 GMT  
		Size: 151.0 MB (150987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aec94f76aaf68236663c4b78c2edb5232ce2bdffacc0182a190ea0d93239e7`  
		Last Modified: Fri, 14 Nov 2025 03:16:56 GMT  
		Size: 20.6 MB (20593366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f389f2a4a94daa441be0e9574f285b9a0209d5e650957032e02f589b27ef89e`  
		Last Modified: Fri, 14 Nov 2025 03:16:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f1299ca9e4f234d427e028a26bc51a7fd257bcc87a505e92be1301f0d6770428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6102508cbeecd8e1a6223b6829453c1ee663764d887c757064789ab68ccac98`

```dockerfile
```

-	Layers:
	-	`sha256:bb3cdbef44c66611c5998158b75a7d3928626b76b28ebfbc7bd71f426f8985d9`  
		Last Modified: Fri, 14 Nov 2025 06:16:59 GMT  
		Size: 5.9 MB (5927606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3b651867ee6306abfe6eef5c7e855262ebc4a369d271446afce5e7c97f3d86`  
		Last Modified: Fri, 14 Nov 2025 06:17:00 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
