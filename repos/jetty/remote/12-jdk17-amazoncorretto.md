## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:302465e60e92b37a8935350aa2275a7b768fc23b3c3c46d44562e1c1b6d60d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:625437d2d8bda380d18a0511fdc1d1e40e4e299221345da987b1df611aae8337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267274632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e176237f7e68bbd3ccc0a322ff43045b9ddab87c6c22329771d51a39b9d41`
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
# Mon, 04 May 2026 20:43:16 GMT
ENV JETTY_VERSION=12.1.8
# Mon, 04 May 2026 20:43:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 04 May 2026 20:43:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 04 May 2026 20:43:16 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 04 May 2026 20:43:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:43:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Mon, 04 May 2026 20:43:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 04 May 2026 20:43:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 04 May 2026 20:43:16 GMT
WORKDIR /var/lib/jetty
# Mon, 04 May 2026 20:43:16 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 04 May 2026 20:43:16 GMT
USER jetty
# Mon, 04 May 2026 20:43:16 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 May 2026 20:43:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:43:16 GMT
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
	-	`sha256:4f399c587f3a34996d8475b04b58d59e6d9b5b38e96096f6809575b5af68abcc`  
		Last Modified: Mon, 04 May 2026 20:43:31 GMT  
		Size: 51.8 MB (51803101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696d2b0afb78d05e1369b552b7f5003a502dc6c8988e5ccbfd8efbc1184e464`  
		Last Modified: Mon, 04 May 2026 20:43:29 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fd72c31ced0affe1f7dfb42e90757592c1d159eb3809ab1cbc267133f255da62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6167363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71b35db5666ed23389fc2ef0fecabd11620d8407a551ec37e007b6a7b8a44e`

```dockerfile
```

-	Layers:
	-	`sha256:0839193ae65e5127303053fcb253f530e178751acdfbb069e8bc28370ffa6ac1`  
		Last Modified: Mon, 04 May 2026 20:43:30 GMT  
		Size: 6.2 MB (6150010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73bcdb78105000736c1efbf977ea9bcda33966a22a5d57df22b4217401d0130`  
		Last Modified: Mon, 04 May 2026 20:43:29 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d538177219116ddeeb94219c5b8f6dd9183c3be2138363907f574d306471f030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268009700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eced0622fa7b32f53176827b643a6448b9b7cf0e255181e8deb379e540708d7`
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
# Mon, 04 May 2026 20:43:23 GMT
ENV JETTY_VERSION=12.1.8
# Mon, 04 May 2026 20:43:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 04 May 2026 20:43:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 04 May 2026 20:43:23 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 04 May 2026 20:43:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 20:43:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Mon, 04 May 2026 20:43:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 04 May 2026 20:43:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 04 May 2026 20:43:23 GMT
WORKDIR /var/lib/jetty
# Mon, 04 May 2026 20:43:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 04 May 2026 20:43:23 GMT
USER jetty
# Mon, 04 May 2026 20:43:23 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 04 May 2026 20:43:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 May 2026 20:43:23 GMT
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
	-	`sha256:53a1a0ca5e8ab16f41d9d833b7cd1474eb07079b81bba136fb1bf3415ae6e79c`  
		Last Modified: Mon, 04 May 2026 20:43:38 GMT  
		Size: 51.9 MB (51895546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2d0501a725b18c5d739d41f3becc5682e85c900674c30d566ec7e89415e0b9`  
		Last Modified: Mon, 04 May 2026 20:43:36 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3a7c13a2d40d0c07d93ffe37b0e2f616c7f6e90cdad88c1e9e1e790c00b2d721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6166084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324414cd74b1ad2ca5abc06261e1e678f0af01632c7895e7b395a7d4a30937c`

```dockerfile
```

-	Layers:
	-	`sha256:340d9d638cb4d88e6ea70a896f58fb60daf6486f0afffccd69c56a49a77ecbd2`  
		Last Modified: Mon, 04 May 2026 20:43:37 GMT  
		Size: 6.1 MB (6148639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299e317f05873c52fbd612888fa8b3a21f7b0cc9d5066210b783b95dd9aa06c7`  
		Last Modified: Mon, 04 May 2026 20:43:36 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
