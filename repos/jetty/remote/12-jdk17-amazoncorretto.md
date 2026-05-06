## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:27b213a9b2f56fe21019963ef3741799032bf83dbc85fa4d72070c4a3ac80025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:246d002a33df9888afe680c0fe6735d3248788dc3467da49da332588d4ca20bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267255535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb00edb6d255a79d4de34c3b4e2adc095f1f4c9baa0d16e0fdf4630b309115a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:24 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:24 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:24 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 06 May 2026 17:08:11 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:08:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:08:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:08:11 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:08:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:08:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:08:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:08:11 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:08:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:08:11 GMT
USER jetty
# Wed, 06 May 2026 17:08:11 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:08:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:08:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032cabcbac193a16c2253875c88ae2e3f74dab118518bde463f31531ad16461d`  
		Last Modified: Mon, 04 May 2026 20:11:45 GMT  
		Size: 152.6 MB (152609646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86e07077be756dba342d1f14efe1334b95ead3340b4c59ee437e8267e537367`  
		Last Modified: Wed, 06 May 2026 17:08:24 GMT  
		Size: 51.8 MB (51784004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63f6d9a5636dc7cce074b13b120155aaf72b7652bca5c20d2ac7e075576400f`  
		Last Modified: Wed, 06 May 2026 17:08:23 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9d6795de3dd79966fca511a7b21e10f37b49953155ac04f5f7c05545a25d4ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965fa171a676f6bf02ed6fb0bb174726c5d8b92a86641997dc7c0184c6a08440`

```dockerfile
```

-	Layers:
	-	`sha256:991ba6b792d730626512f2a156631e5fa669e8109b010ddeee62cd0c9074187a`  
		Last Modified: Wed, 06 May 2026 17:08:23 GMT  
		Size: 6.1 MB (6119644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3ca532a6f0ec220adae0b8f066ad1be9ee66676e36602132528997490a4755`  
		Last Modified: Wed, 06 May 2026 17:08:23 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9c70c0ba5e91fbee1037a1e980e0065d799d9062a5ce9fe6d84710c900eefab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267984702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba4e0e4e9eb1fb5da2c173809d392f0e55ebae74daa12b3b243bb42059144e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:41 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:41 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:41 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 06 May 2026 17:07:52 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:07:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:07:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:07:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:07:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:07:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:07:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:07:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:07:52 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:07:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:07:52 GMT
USER jetty
# Wed, 06 May 2026 17:07:52 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:07:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:07:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04cd62a6e78a94f951948f9a5bd7a651c4178ddc92f9efa3473eab2c4fdbe9`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 151.3 MB (151316746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc73bbe898be66386a989bb5a8b2e02141766d1b0e387d8acd4d34337ad651`  
		Last Modified: Wed, 06 May 2026 17:08:06 GMT  
		Size: 51.9 MB (51870549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff03d2acf2cfbef4cfdc7dae61f27d95a5b84540c585603342d6f1990191aeda`  
		Last Modified: Wed, 06 May 2026 17:08:04 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a17b1e9887a85c1ae7649f5f41b60930ef065a7319affc1d7e29d23d00131e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cf079c620a7fbc4f4c8ef626d2a3a37cbdca4198b98ed73b59474a4cbcc543`

```dockerfile
```

-	Layers:
	-	`sha256:6c3c391ccad20718dd2686bbe9d45ae1244944ef61c27cdbb2acbf86e92b1da6`  
		Last Modified: Wed, 06 May 2026 17:08:04 GMT  
		Size: 6.1 MB (6118273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedda8ded975f1556b1d9ba3493d19d18c126b992ba9cef5a8b595f826473029`  
		Last Modified: Wed, 06 May 2026 17:08:04 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
