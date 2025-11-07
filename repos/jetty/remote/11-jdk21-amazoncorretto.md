## `jetty:11-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:f71ac176e3fcc9ddd29507e2179103c859085432667180e17893766a7081ab24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4c92e76c52f7e43755758082a9bdf6c013005b66be79222afa73e9225a4b977b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248946174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e517b4771d4a3512200e8d49ba6d23f2bc54ce8c4803537fddfb7b85a7cfab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:05 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:15:05 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:15:05 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:13:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:13:30 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:13:30 GMT
USER jetty
# Thu, 06 Nov 2025 23:13:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:13:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:13:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b6e807c1a7c53af4ccdd4780bf792c6494ade14902f1c503d47c104f25cfd`  
		Last Modified: Thu, 06 Nov 2025 23:11:15 GMT  
		Size: 165.5 MB (165485950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d291604b49b3a2f273d6013a87f3684ecd64ca2847d1671365bf9db311476`  
		Last Modified: Thu, 06 Nov 2025 23:13:53 GMT  
		Size: 20.5 MB (20524214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8c5d728931f74d1e50efc321db03bd10d30a7d6cdd08782d9fb33452fe175`  
		Last Modified: Thu, 06 Nov 2025 23:13:50 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6964d60c144984d62ffcb7c332b32c6ad884e5e5168ce9aa0a74865c8b399faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66059f2094e56f3eb666a681b7a4a7fa4a1f406841ff77a9b1afc1a4663af22c`

```dockerfile
```

-	Layers:
	-	`sha256:a491392641d8029a5da2200a9c2fcc9d22b49544ba85bf76732990516696b4f6`  
		Last Modified: Fri, 07 Nov 2025 00:16:37 GMT  
		Size: 5.9 MB (5929838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccade865eaced8c26078c4846795155c1dfaa710dd7bd577d4e3d05f82b35aa3`  
		Last Modified: Fri, 07 Nov 2025 00:16:38 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a6532eca3b42114db6fd42cbe046fc86dbcddb05e09cd5a8b48cd46609c3093d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248968223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dc9a7f3f28a63c24459dbbd2a3d3025e44e9e4ccbd5bc20c29feb4ed052d37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:08 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:14:08 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:14:16 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 06 Nov 2025 23:14:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:14:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:14:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:14:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:14:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 06 Nov 2025 23:14:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:14:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:14:16 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:14:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:14:16 GMT
USER jetty
# Thu, 06 Nov 2025 23:14:16 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:14:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:14:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50fcdfedf41173aea97496be730854d377fdf96be58c639f421a2d1bff774e7`  
		Last Modified: Thu, 06 Nov 2025 23:13:01 GMT  
		Size: 163.6 MB (163582959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c47ccc6fe5364b24eade9056fe9a8955a3aceafd6dc8c5115776eadd3c26c9d`  
		Last Modified: Thu, 06 Nov 2025 23:14:38 GMT  
		Size: 20.6 MB (20590092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818f5e1b9124ded46bd43a3a419fa9017d382f83a9adb19b8c6a4aebdd5f9b01`  
		Last Modified: Thu, 06 Nov 2025 23:14:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:62ed5d1cb8d5d4609763c7c26a59239a12709f167dd6b31373ccdedbd9310c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cb21fb98978deda9c108940c67b4e77a3ed27997be3e67fab241abfd919546`

```dockerfile
```

-	Layers:
	-	`sha256:c49be2b10af59847da24e2e0b402fd4c1493aaf49cd9b429e76a8fc8d141da50`  
		Last Modified: Fri, 07 Nov 2025 00:16:44 GMT  
		Size: 5.9 MB (5928503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9cfb36873afb73bc776483733065b8d8334fa78e64424c14c363f822562e8e`  
		Last Modified: Fri, 07 Nov 2025 00:16:45 GMT  
		Size: 18.5 KB (18453 bytes)  
		MIME: application/vnd.in-toto+json
