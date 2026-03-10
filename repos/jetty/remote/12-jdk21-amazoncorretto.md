## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:9e2f519bedff3a42d4bbdc063f1e3061c3e97533dbe15b831b7e3d0be6fd3a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c9dc0b95a8f5477ce0408cfe3e33673972397c4f32a9282ab899e75e46ee28c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280598232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef94f4f96247b3523076a46c6cb2541fb5f1e53e1d6c8e52606a2ac755b5cfa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:29 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:29 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:15:29 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 10 Mar 2026 16:40:28 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:40:28 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:40:28 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:40:28 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:40:28 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 16:40:28 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:40:28 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:40:28 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:40:28 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:40:28 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:40:28 GMT
USER jetty
# Tue, 10 Mar 2026 16:40:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:40:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:40:28 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bda24a0a1972d7430848f2e9c53e25d2db55ca3537798a384329ba70f9db98`  
		Last Modified: Mon, 02 Mar 2026 23:15:50 GMT  
		Size: 165.5 MB (165548489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59729e035d9f25206e76424b1bba1f168959621a50643996a1527289cf1ae82`  
		Last Modified: Tue, 10 Mar 2026 16:40:43 GMT  
		Size: 52.1 MB (52087638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9962e3a49e9a1772cea19a92833bf2901866ec7866d34a649bf7b5c6bf5a3c92`  
		Last Modified: Tue, 10 Mar 2026 16:40:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8c62d9a3ade6628c7ce599c4bbe0705391b5b2467ce4c51723a740e19ba173e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b7dbf4252ed102f3fac5550ffe49c46c671ea92acf51e8116db8fc6ff70e7e`

```dockerfile
```

-	Layers:
	-	`sha256:73a9d21bfdbc3c94a57b1730110a9fc6c9137eb5678b422a5067ee4a68218bb1`  
		Last Modified: Tue, 10 Mar 2026 16:40:40 GMT  
		Size: 6.2 MB (6151902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab451bd9bd2f8f2d77778d5d5d0a899674df7fc1f7b70fc35bcb663f2ed3f631`  
		Last Modified: Tue, 10 Mar 2026 16:40:40 GMT  
		Size: 17.4 KB (17352 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4ae9f998019ee218aa78b40a6935b887f1482f63e17cacab8246902594f1a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280570841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55947f8bb80f96235ec43f5ce4dae253a554ac5407dfc2a1fe1833f473d59c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:44 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:14:44 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:44 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 10 Mar 2026 16:39:48 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:39:48 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:39:48 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:39:48 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:39:48 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 16:39:48 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:39:48 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:39:48 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:39:48 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:39:48 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:39:48 GMT
USER jetty
# Tue, 10 Mar 2026 16:39:48 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:39:48 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa780b6d9640895d00c1754835e9116ebd6059e626cc1a1618dde104a8dedd`  
		Last Modified: Mon, 02 Mar 2026 23:15:05 GMT  
		Size: 163.6 MB (163606125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cc7cbe01d0b04f89dec57d9c3a07f6d5fdc52a3ef39ecde8891e5a81bd6c35`  
		Last Modified: Tue, 10 Mar 2026 16:40:02 GMT  
		Size: 52.2 MB (52151429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6871aa944910f7e539f99645d0953466ce9006d75443fe9e462ac219a8fd24f3`  
		Last Modified: Tue, 10 Mar 2026 16:40:01 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c6f8913f7acaa61d98898ee4ae6deb9163d78ee1b371be4ab0493d4c366cd11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6167975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc381691c217122b8bd08ff785a91f426fb045b3b6ee8d002406f680e32526e`

```dockerfile
```

-	Layers:
	-	`sha256:4dcad9e0dda4936962a275a952499d35a1454a8abce3b62e4620363b4b920c75`  
		Last Modified: Tue, 10 Mar 2026 16:40:01 GMT  
		Size: 6.2 MB (6150531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8824b53fe4e5b273ace6f9bc505593e7c173787f0c8e3897cf13d6ae4b2975`  
		Last Modified: Tue, 10 Mar 2026 16:40:01 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json
