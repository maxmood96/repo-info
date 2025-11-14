## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:838823a8d17c826398550942f04590bcb4146937dfdf291ede108a4263fedd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:11ecce270b5b23bff578c93695cf2f72e6d46920f4d17c66dee05717d94a9fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b21db1d84df1442100fdf6bc220ecf5e5fe63d270996713d7ecc8f9de6fe7ac`
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
# Fri, 14 Nov 2025 03:15:14 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 14 Nov 2025 03:15:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:15:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:15:14 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:15:14 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 14 Nov 2025 03:15:14 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:15:14 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:15:14 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:15:14 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:15:14 GMT
USER jetty
# Fri, 14 Nov 2025 03:15:14 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:15:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:15:14 GMT
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
	-	`sha256:fbef040fb7dbe0a57b57b3b111ae35d23abbce4f63d26bf4fc08019965649822`  
		Last Modified: Fri, 14 Nov 2025 03:15:32 GMT  
		Size: 16.2 MB (16208014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7eb46113e3080c7fe702ac2257ca4679aad939a45e975344fb8b5cd6a0b4be6`  
		Last Modified: Fri, 14 Nov 2025 03:15:30 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e63e345e12edb093682fd70e2235b16f032d4b789a023143f888aaf80b43d3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bff83586ac707d091946725ad274547aeca8cfb872f0db1f0d66a3edada379`

```dockerfile
```

-	Layers:
	-	`sha256:fc686fc45cd56f54cd5c9041328f1b1fb282b52bd1d6f66612ac6ec04bf528a8`  
		Last Modified: Fri, 14 Nov 2025 06:20:05 GMT  
		Size: 5.9 MB (5914688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad72e6ca37634d5cf11c2073f29b9aefc42b7460dcd77514dd8ddcdc9b48e61f`  
		Last Modified: Fri, 14 Nov 2025 06:20:06 GMT  
		Size: 17.4 KB (17387 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:99d9d8bfa28e67cf0a2ef101d0b3189fd576cc91dc1c7998f8811f59c263cff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232054340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c5a4e05c0a8cb3af5923e229abf9e452699f1653c4248e1053aa6327395cc4`
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
# Fri, 14 Nov 2025 03:15:54 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 14 Nov 2025 03:15:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:15:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:15:54 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:15:54 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:15:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 14 Nov 2025 03:15:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:15:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:15:54 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:15:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:15:54 GMT
USER jetty
# Fri, 14 Nov 2025 03:15:54 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:15:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:15:54 GMT
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
	-	`sha256:c5135925f54fc273f9924ab639181ca77817d3afa8e1551ad2e3bd05be15f888`  
		Last Modified: Fri, 14 Nov 2025 03:16:13 GMT  
		Size: 16.3 MB (16271671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b828146a4946ebfb5f1cea80748ccb19a15cd779ad2514903c4648d50d858`  
		Last Modified: Fri, 14 Nov 2025 03:16:11 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:08a96e5f982e862db936b313e91692ceda3e95758d9c1620bfeac85e38c9296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6dea4c02575d594e0df44b80fb502991a943fcc3b1c4d6cff799c1f69a4ed60`

```dockerfile
```

-	Layers:
	-	`sha256:3c9c7b75cba1b6a84459ec9810929a38d3d2cf77e939290d22693e3df685452c`  
		Last Modified: Fri, 14 Nov 2025 06:20:12 GMT  
		Size: 5.9 MB (5913317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949732d800cc7e95bcbab7e6406169db3b2e6edc34fce7a18837029afb805f58`  
		Last Modified: Fri, 14 Nov 2025 06:20:13 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json
