## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:15a27dc14f3fee278cf5665d5fef89850ff4ad44ed1a67206606e50308d2558e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a811644ed27f690f599e948944b43e895ebd3df53ae79b3ee4b94475fc85217c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267315104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16014be1e9d7b7f083d09c9cac2b6425aae0c823b5473514a2a16bc536baa158`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:25 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:25 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:25 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:19:07 GMT
ENV JETTY_VERSION=12.1.3
# Thu, 11 Dec 2025 22:19:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:07 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:07 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Thu, 11 Dec 2025 22:19:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Dec 2025 22:19:07 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Dec 2025 22:19:07 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Dec 2025 22:19:07 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Dec 2025 22:19:07 GMT
USER jetty
# Thu, 11 Dec 2025 22:19:07 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Dec 2025 22:19:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Dec 2025 22:19:07 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac57126ecd86ebc8bfbf2f8c72cef47008c2e2b42c706b3d2d81f5f916ccec5b`  
		Last Modified: Thu, 11 Dec 2025 22:13:15 GMT  
		Size: 152.4 MB (152417728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304f4264b2fb32016de4b9d9379c2f8f1dd726c42ad692cf0ce30f5bd344481`  
		Last Modified: Thu, 11 Dec 2025 22:19:33 GMT  
		Size: 52.0 MB (51954527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397ee38aac5ab0bc6e3dbb32a0f4af0add2bae004621d94c883b60386b9b849`  
		Last Modified: Thu, 11 Dec 2025 22:19:28 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2ba3da1addeaefa0744c093a5379e55fb019142f0e745834a36474094d1f1eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6055e1e03123342e59f01ac0dae68a0b48a16c29380bfc7cba86394a9a84316e`

```dockerfile
```

-	Layers:
	-	`sha256:9be42c004c9ee51581e12cff667a21b96784b7584af7010a19de755feef745ec`  
		Last Modified: Fri, 12 Dec 2025 00:18:03 GMT  
		Size: 6.2 MB (6151971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79998b0808980c73139fd64303708636d0c21bf27b23f03f7b10934f3aab7335`  
		Last Modified: Fri, 12 Dec 2025 00:18:04 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:83cd0a5f77df7f0987504b8f37ee12e5d55d1882d87d7304592f5c44d1ac6b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267796412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1ae3daab5600fcfa45e01b75fdf82f6e52031a053894377ec8e7fc88c6ff88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:02 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:02 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Dec 2025 22:19:02 GMT
ENV JETTY_VERSION=12.1.3
# Thu, 11 Dec 2025 22:19:02 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Dec 2025 22:19:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Dec 2025 22:19:02 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Dec 2025 22:19:02 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:19:02 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Thu, 11 Dec 2025 22:19:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Dec 2025 22:19:02 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Dec 2025 22:19:02 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Dec 2025 22:19:02 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Dec 2025 22:19:02 GMT
USER jetty
# Thu, 11 Dec 2025 22:19:02 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Dec 2025 22:19:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Dec 2025 22:19:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67bc37dbe272db9b7b10c3283dea952f31754f43ec167dae43bf6ef83012ea9`  
		Last Modified: Thu, 11 Dec 2025 22:12:56 GMT  
		Size: 151.0 MB (150989128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63dcb1ee8b34dfbe744cacdf38586daa2d98204603922eb6822fd785e4dc696`  
		Last Modified: Thu, 11 Dec 2025 22:19:30 GMT  
		Size: 52.0 MB (52009653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5051bd6cb4256dee17ea813afdc1f0ae9ada6dc2ca91cec5eceefeab48e51bc3`  
		Last Modified: Thu, 11 Dec 2025 22:19:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a0cb08f337d2ff308f0fd384d87db49b54be1612254534fb23d9ee3cdd0c6260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c85313c30e567499dd00228755912ba3ca6d38dcbdb413615e777fdaf3ac1e4`

```dockerfile
```

-	Layers:
	-	`sha256:01caa0dd729baae3cb031bbf30a678d8fdd7eb56288bd1edfa81439bb75936dd`  
		Last Modified: Fri, 12 Dec 2025 00:18:10 GMT  
		Size: 6.2 MB (6150600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99e720c88e38098e2d255739530180bcb8a51425017c275b543ce8d0a3f7b2d`  
		Last Modified: Fri, 12 Dec 2025 00:18:12 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
