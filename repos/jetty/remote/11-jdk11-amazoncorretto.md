## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:c4e4cec5f7717ccd86feef9b3e04244b6333811c2f8d37f141c9efee17b41695
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:dfd998994fbf8821e95ac16e1ef2129ad8cf91c74558abad6804dca653438612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231516173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff2384eaeb5ed6a930e28ada235c57927cce76eef8edf888bb8ca73d045f64d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:47 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:14:47 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:47 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:43fb62205c806751bb98d48643e1aa992f329848298980df7d635af114aa7a9a`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 148.0 MB (148046029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6401ba4994f74de05dc4315ea77a4c92184863312b5008d2e780905016ee93d`  
		Last Modified: Fri, 14 Nov 2025 03:16:34 GMT  
		Size: 20.5 MB (20537696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f73b6de05d9e5de81b93463adc647d929bbbec2492bda50ed6cd3a8e50f767`  
		Last Modified: Fri, 14 Nov 2025 03:16:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9a4405f5997575d9492b01975a4957fe8a57be25c7ead40b08f2fbacebf6b062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9520069697f27883238feb8695ba779ebd7ebc8ffa88fca0d6eabcc052eba14c`

```dockerfile
```

-	Layers:
	-	`sha256:a3fd8fa3619357add95dd466bf2fd059a08494da762401f327ac34f7e6cb08f3`  
		Last Modified: Fri, 14 Nov 2025 06:16:44 GMT  
		Size: 5.9 MB (5936278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9c83e59b6eefd62c4d8a45c498d4af1fb4627fff281a68a817d963ba8d01e9`  
		Last Modified: Fri, 14 Nov 2025 06:16:45 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5a71fa7072ccb7fa1c3c740d81ff47d5785112cb705df36f875e7388dc67e5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230522009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab847d7bc3e8bd7b90e987cc6d756c4198c60734569b649e13665b0ae118bc71`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:26 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:15:26 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:15:26 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 03:16:53 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 14 Nov 2025 03:16:53 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 14 Nov 2025 03:16:53 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 14 Nov 2025 03:16:53 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 14 Nov 2025 03:16:53 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 03:16:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 14 Nov 2025 03:16:53 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 14 Nov 2025 03:16:53 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 14 Nov 2025 03:16:53 GMT
WORKDIR /var/lib/jetty
# Fri, 14 Nov 2025 03:16:53 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 14 Nov 2025 03:16:53 GMT
USER jetty
# Fri, 14 Nov 2025 03:16:53 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 03:16:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 03:16:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9edde79542b8043f205bea08ae238c30a1ca98123823ddf3b2f089a63d8ee`  
		Last Modified: Fri, 14 Nov 2025 03:16:38 GMT  
		Size: 145.1 MB (145144926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2127e3dfea01cae45279aead5386c9dd8b03144cf47d9725cd63822d484fe9ae`  
		Last Modified: Fri, 14 Nov 2025 03:17:14 GMT  
		Size: 20.6 MB (20582406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1949a89b5899622d30322fb9be3bc3814a8d462ace0d41729fa84f5819a644`  
		Last Modified: Fri, 14 Nov 2025 03:17:11 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:becb5f4a2a55fe14a7f78ce0dd42d741df6d25aeab22d65fe9e9ba3da5da58f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a91a27fae135e764ea330a879dd00416af04686661dc7c39fd3ec2ba18b414`

```dockerfile
```

-	Layers:
	-	`sha256:ec8e70edf3aceb1bb9b3f166c1f0cf84ccf2f70c51aecde31f24256527fd3c4f`  
		Last Modified: Fri, 14 Nov 2025 06:16:51 GMT  
		Size: 5.9 MB (5935712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f0647f3c7e52ba29be746cbc03a96f025699116e028f034a8d14e06799648d`  
		Last Modified: Fri, 14 Nov 2025 06:16:52 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
