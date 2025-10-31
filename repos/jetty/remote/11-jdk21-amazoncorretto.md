## `jetty:11-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:6958725948cc28d090a3d78947cb40fa7c90a0e4a361b1b14318b02704b4a1bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5bcaebde25edb4c3a29830eafd23037b5b3efa5d1042633cd825e601ec7ee647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248952268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d11feb7a1bb4b95497d9878f660744300df96dd1d9e725bc28170b352b41b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:25 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:25 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:13:34 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 31 Oct 2025 01:13:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 31 Oct 2025 01:13:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:34 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:34 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b8bf1a2d41e5961e041978e350f514e0b16151864da2fa18fedc6f348e6f0f`  
		Last Modified: Fri, 31 Oct 2025 01:11:23 GMT  
		Size: 165.5 MB (165482592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0693f8c24c66ad7cac1457b3841bfaa1c0d774f93809e7b0bc4df66ebc08d6`  
		Last Modified: Fri, 31 Oct 2025 01:13:51 GMT  
		Size: 20.5 MB (20533732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f6a8e8236d5517725fd22875e443f96641a09adca6dd55b454fbe8aa32959`  
		Last Modified: Fri, 31 Oct 2025 01:13:48 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b8e22a8e4539173b7b6eacc1ffea53268b915aab6c396d65f7b3ba877fde16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96546500d04f566ba32012e321a0947a2c3ce896fe867db8db12b8e4d609dec`

```dockerfile
```

-	Layers:
	-	`sha256:29028eaa7936ef157bf8cb38a0b76e4152e032549ed04a7539cc82bfbf9fc231`  
		Last Modified: Fri, 31 Oct 2025 02:16:31 GMT  
		Size: 5.9 MB (5929838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1720f72a0b1c56867ee2b0f449541d9e797917e6268d5311a464a4d8cd21e288`  
		Last Modified: Fri, 31 Oct 2025 02:16:32 GMT  
		Size: 18.3 KB (18325 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:11430f984dc188e202ceaf1338fdcbea2f2c71713c1f61a9ac438c3d5b09404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248975882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed26f5435b8b8e7964d7693123ad9b9880938b9a4baa09ebfc8824109bb040df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:14:06 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 31 Oct 2025 01:14:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:14:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:14:06 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:14:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:14:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 31 Oct 2025 01:14:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:14:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:14:06 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:14:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:14:06 GMT
USER jetty
# Fri, 31 Oct 2025 01:14:06 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:14:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd1baf4e91e00d7b9956781f2599d36622339644d5c2a7ec70735ba3ae40162`  
		Last Modified: Fri, 31 Oct 2025 01:13:02 GMT  
		Size: 163.6 MB (163587405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938e8126e37d80ddddc5e0a448efc80d9867dbfcc82f1bab70107c6da1c9263`  
		Last Modified: Fri, 31 Oct 2025 01:14:24 GMT  
		Size: 20.6 MB (20593143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86943bd45aa07b71d2bd95acf79f88790c49b7a22af7ec234b6fa10ed3a7dcd`  
		Last Modified: Fri, 31 Oct 2025 01:14:21 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f6a9efe810271bfac3cbda09fa79be641f1953878e2564df0dce791da4699321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f1b1a289f1c8df20afac7ce9c04f3529607aa578708081996a63a0c91d8330`

```dockerfile
```

-	Layers:
	-	`sha256:3f9af2a46c739c126defad6c8c06f2b8057ea0f83cbec0f4c1e13d814736a23b`  
		Last Modified: Fri, 31 Oct 2025 02:16:37 GMT  
		Size: 5.9 MB (5928503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b94fe8f61af6b79d8fdde8cb5d8894e2a4ed0b95a6f5052feb38606e462e5b`  
		Last Modified: Fri, 31 Oct 2025 02:16:38 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json
