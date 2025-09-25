## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:7ac7c7309e32727d5e6748b91c474fa924bc3a509eea8592de7c27896f1f0ec1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c941893add212a821e8c5aa0adbee6f6f7ea93a0bf51aa2213a9f5404480597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279915045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4104fb722ab5f17aeb6185ca45e91e9d6e88e588941c85fb143dee2349ba967e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Sep 2025 00:35:55 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 00:35:55 GMT
ARG version=21.0.8.9-1
# Tue, 09 Sep 2025 00:35:55 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e750caf8f1aace6b2a40b4d03ac34238ad41147f9852aea71ac3fd0f305ecc01`  
		Last Modified: Thu, 25 Sep 2025 03:16:04 GMT  
		Size: 165.0 MB (165044322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c418cc90645c0d34518cfd546306f7dd9ce715c6ee37b5078abfb18f2acb613`  
		Last Modified: Thu, 25 Sep 2025 03:17:08 GMT  
		Size: 51.9 MB (51935006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5daf61f5b68a07fd9e2e20da988d4d5cef8579d8439775a249232b9fcd74b4a`  
		Last Modified: Thu, 25 Sep 2025 03:17:01 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f15d0e3c854c9c0bbaaebb14df2c9266fa069114b9471900d9e440fa8652ab07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6167961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a14f5a2c17dc47b714cef4704def64d589b35eab36ca3014549ef0f75fbd999`

```dockerfile
```

-	Layers:
	-	`sha256:5db67ccd3fa69a5fb0e9c2bd4723173f424d835626017473544c4a26a3f269ff`  
		Last Modified: Thu, 25 Sep 2025 05:18:52 GMT  
		Size: 6.1 MB (6149599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b3d01ac352de93328347070bab04cf4e8f912b4203b403e3a22f115cecf5a3`  
		Last Modified: Thu, 25 Sep 2025 05:18:53 GMT  
		Size: 18.4 KB (18362 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:dad22a178698dc6131b9a7ec3700911806a20bd5189f6a80eef4b28342efeb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279882353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eabf1839844bcac5df3dd65cb512d14c37dd3a2102e1a21bdc7945c48ca7377`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Sep 2025 00:35:55 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 00:35:55 GMT
ARG version=21.0.8.9-1
# Tue, 09 Sep 2025 00:35:55 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_VERSION=12.1.1
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.1/jetty-home-12.1.1.tar.gz
# Tue, 09 Sep 2025 00:35:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Sep 2025 00:35:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Sep 2025 00:35:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Sep 2025 00:35:55 GMT
USER jetty
# Tue, 09 Sep 2025 00:35:55 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Sep 2025 00:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Sep 2025 00:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c868e5c107db6ab89ab40ef0c51c4a502a10ecc34ea2109f2dd64bd446a85`  
		Last Modified: Wed, 24 Sep 2025 22:12:58 GMT  
		Size: 163.1 MB (163112265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f5d041e236c00d051594e11a21b7a88c1e3692c6ee906621bc560fbbdd3723`  
		Last Modified: Wed, 24 Sep 2025 22:13:59 GMT  
		Size: 52.0 MB (51975065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c5ec005d905c476d54526b9f1b61ece28c32494302e48f9a1964d9c4350cd`  
		Last Modified: Wed, 24 Sep 2025 22:13:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9e0ddc390777c65eb579d91f44193f5d49cfa9c6a7fb880aa7647768b27814da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6166754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf98f9eef38583ead7fb81d0d45760a2f6c182e523cffe23e6794213851b4398`

```dockerfile
```

-	Layers:
	-	`sha256:52c953b36edfaacadda0ccc99abe55ca249e1d1d22d9c7c029fcc7dfac1d2720`  
		Last Modified: Thu, 25 Sep 2025 02:17:35 GMT  
		Size: 6.1 MB (6148264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7638d08ccaa56386bf96bc4c510d8e7abb029b25dbc6b9752fdf53a340f9a68`  
		Last Modified: Thu, 25 Sep 2025 02:17:36 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json
