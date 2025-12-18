## `jetty:10-amazoncorretto`

```console
$ docker pull jetty@sha256:2f1a703c497902b4c9c77542b2a4e491d8b15bb1d636fa309cfacce9e96e98fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a43f953fb7ef44d54a27b251a428974e53fe2fdebe1f6dbad5cd93eab1154dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245525041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85db41f3863d40883e7a9734bf20e1312b21a1c7c0dfd7d2dd046c7ae94878c2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:24 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:18:24 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:18:24 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Dec 2025 02:21:14 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 18 Dec 2025 02:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:21:14 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 18 Dec 2025 02:21:14 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:21:14 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:21:14 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:21:14 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:21:14 GMT
USER jetty
# Thu, 18 Dec 2025 02:21:14 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:21:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:21:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2339f32e6c9020ba0afbae3e3cd1b564466fed84dba76f72548ebcaf5947e3ef`  
		Last Modified: Thu, 18 Dec 2025 01:19:15 GMT  
		Size: 165.5 MB (165492330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c482c97ea0f4fe72eb5d6e1a7f820189ff2a3f445dbed6c94f6506b72bdc101`  
		Last Modified: Thu, 18 Dec 2025 02:21:35 GMT  
		Size: 17.1 MB (17089860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3b926d37a395fe325c13ab8c0c4acf66bd70d76e8c54b1b4a078bc00d6e63`  
		Last Modified: Thu, 18 Dec 2025 02:21:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2aae4379e385eab22575071e0bee929022034379775976f072f85410f4a15b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602a03438624dc08e526e59e6aea5c6a3f41a73b9af49525c799f5170b849e33`

```dockerfile
```

-	Layers:
	-	`sha256:b649b63c40210254866f7245b4bd96ebafbfda4cd82eeff73101b2c0de6f4976`  
		Last Modified: Thu, 18 Dec 2025 06:15:24 GMT  
		Size: 5.9 MB (5929792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1c4538ba9b3ec7e975e21b3c96d737cbe799c189c89f6ca13ccf1ad434ab79`  
		Last Modified: Thu, 18 Dec 2025 06:15:25 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e5e2a0edc91c5fbb4b75afc70b85cf33380c3e7b3cd792400b5aa798bd4d9781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245524165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203d69dc1e5d867bcfcd2efc258ec5a147b26b665d2644ccd3be43e7bc53071b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:49 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:26:49 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:26:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Dec 2025 02:21:37 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 18 Dec 2025 02:21:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Dec 2025 02:21:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Dec 2025 02:21:37 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Dec 2025 02:21:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:21:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 18 Dec 2025 02:21:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Dec 2025 02:21:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 18 Dec 2025 02:21:38 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Dec 2025 02:21:38 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 18 Dec 2025 02:21:38 GMT
USER jetty
# Thu, 18 Dec 2025 02:21:38 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 18 Dec 2025 02:21:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 02:21:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22bdf99b000252028c87652a8573d46452c5cb60b7d624b1036ae366a0cefc4`  
		Last Modified: Thu, 18 Dec 2025 02:20:19 GMT  
		Size: 163.6 MB (163581031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c482f83ee84154178b9fe0eeb2f66f1f6982648c8efbf5c3ead3db813f4b2def`  
		Last Modified: Thu, 18 Dec 2025 02:21:57 GMT  
		Size: 17.1 MB (17145502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6340809a0418458e7844925767159b2022a95ff72f062c9e82daab506147`  
		Last Modified: Thu, 18 Dec 2025 02:21:50 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5944a1944feeb7189c2d34140aaea25b7728c2ec401a7dd05012e8368dfb7394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3bfe898a5a8d9bf8b468c7f718f8ad55ad304525a4d77b01bef84433f83792`

```dockerfile
```

-	Layers:
	-	`sha256:7cdc19a6a45390acf9f6aa1c4a2f81d232979ced884dc358dcc3946117575359`  
		Last Modified: Thu, 18 Dec 2025 06:15:31 GMT  
		Size: 5.9 MB (5928457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63ae1a23a663a19afb00c9945b4ffdf6008ebe4b8c48afb7e2b9fa1bcab1869`  
		Last Modified: Thu, 18 Dec 2025 06:15:31 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json
