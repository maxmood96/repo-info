## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:c020c3d82d4876c6de110a669a15ff41c763429615bcf1b96df3d6e6ccbf0c10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3c23decb649d50b1cbe8ad78a4dc3abda7e5107d63ee402744a266d0f26bbe76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155346974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8c180b7d80284ac95ef029ff15da130c386181952d586747b922efb21e6029`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:33 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:06:33 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:06:33 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 28 Jan 2026 04:56:55 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 28 Jan 2026 04:56:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:56:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:56:55 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:56:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:56:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 28 Jan 2026 04:56:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:56:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:56:55 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:56:55 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:56:55 GMT
USER jetty
# Wed, 28 Jan 2026 04:56:55 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:56:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:56:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1384bd83b644d74563e674c31f1fac8876e53e1eea823021dbbd470c29551a`  
		Last Modified: Wed, 28 Jan 2026 04:06:49 GMT  
		Size: 76.1 MB (76147006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28bd027c05a8e31e0acc5fb7d770cdaa6b0a160f3734ceb3bc540f0e8d44da`  
		Last Modified: Wed, 28 Jan 2026 04:57:05 GMT  
		Size: 16.2 MB (16234382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00cc2deb2ccce6179afadf5dfe7da830c259da794d75663eb016c9adf31952`  
		Last Modified: Wed, 28 Jan 2026 04:57:05 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1080469106a5eb1c2a765c418e3d581115dc1d472723f1fe5f0d8e55f07fc7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91069f4d81e022f0b630b57e7ddc29ef9bcbd2a1cb8f3c600a88045670cde895`

```dockerfile
```

-	Layers:
	-	`sha256:ae0c58923278d02e7550f90fe7d67f5460bbffe2433b195c94ba828337c98654`  
		Last Modified: Wed, 28 Jan 2026 04:57:05 GMT  
		Size: 5.8 MB (5756040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f92bafcb7b6f814fbcea61202ddd0b5c68c4132cacb1f903587724275a5d8a`  
		Last Modified: Wed, 28 Jan 2026 04:57:04 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a040e63914dc5c77af248962e1f06e56e106a9f2870141060384161b734707df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140998323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0716e2a5f4d2b9b5df345212f52efeb03fbe6d1eb1160db3690cf4d7c292e7ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:26:04 GMT
ARG version=1.8.0_482.b08-1
# Wed, 28 Jan 2026 04:26:04 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:26:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:26:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 28 Jan 2026 05:39:01 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 28 Jan 2026 05:39:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 05:39:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 05:39:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 05:39:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:39:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 28 Jan 2026 05:39:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 05:39:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 05:39:02 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 05:39:02 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 05:39:02 GMT
USER jetty
# Wed, 28 Jan 2026 05:39:02 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 05:39:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 05:39:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538fab718541c9ad1d9ba20d118b7be1cf135a612d5791981045db60d09262d`  
		Last Modified: Wed, 28 Jan 2026 04:26:20 GMT  
		Size: 59.9 MB (59920527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4a33866bf4fb2e2e2ae7a3713d38722439ef3b3b21fd40887490902a70802`  
		Last Modified: Wed, 28 Jan 2026 05:39:13 GMT  
		Size: 16.3 MB (16277030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b524479663a38e9171b3494d15e6b7dc04455a984d9db64f49bdd89e84351ff7`  
		Last Modified: Wed, 28 Jan 2026 05:39:13 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:51a256f6ad73bf72e14c17beacbf0ff5752d512ee6ff524957e4c9759128f3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377465f332554060f241db92fa0a4aa25a499f78e63ed8d3ae348e6f490beae`

```dockerfile
```

-	Layers:
	-	`sha256:e2c382eef6707234b7efabc14895278c1124918eb7f7a1ef616f8e5f8d399012`  
		Last Modified: Wed, 28 Jan 2026 05:39:13 GMT  
		Size: 5.7 MB (5734467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21510b523e5a6cdf75106cdaac557a925a056470af11f0742512066e23dfe46`  
		Last Modified: Wed, 28 Jan 2026 05:39:13 GMT  
		Size: 17.5 KB (17469 bytes)  
		MIME: application/vnd.in-toto+json
