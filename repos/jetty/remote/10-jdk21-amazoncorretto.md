## `jetty:10-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:f20b1fabc1be4bd440deb330495e705527c2bdd7a9316635e3ee8dda3d3fa8fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c7ada3f6f46b3773e653f3ada588d9012b91bbbe3ac9a50e0b13ef45b6be8c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245501563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bbb98064ae3159a362674d9822ba1b82f5a5a5579769f9d9a1abc0cb893789`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:08 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 05 Nov 2025 01:06:08 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Nov 2025 04:52:03 GMT
ENV JETTY_VERSION=10.0.26
# Wed, 05 Nov 2025 04:52:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Nov 2025 04:52:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Nov 2025 04:52:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Nov 2025 04:52:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 04:52:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Wed, 05 Nov 2025 04:52:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Nov 2025 04:52:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 05 Nov 2025 04:52:04 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Nov 2025 04:52:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 05 Nov 2025 04:52:04 GMT
USER jetty
# Wed, 05 Nov 2025 04:52:04 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 05 Nov 2025 04:52:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Nov 2025 04:52:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb82af62a77255279f1c497851a6fe8f80f84cef1425a841bf7348ca44f3fa`  
		Last Modified: Wed, 05 Nov 2025 02:35:06 GMT  
		Size: 165.5 MB (165485971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b949187b4e81dec910494960cae6b14f017f48e03a17cb351fa7fa5840735c3e`  
		Last Modified: Wed, 05 Nov 2025 04:52:27 GMT  
		Size: 17.1 MB (17079648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507b73e7d32f9301385b1f29c50ee6313ff9e98576817bd1fa115abc03aaddd`  
		Last Modified: Wed, 05 Nov 2025 04:52:26 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b65b05581e0596d202403ba8886da877fd49a682b2fe308de3fbe8d08bc7e0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ed5178ec709b932dbb54fafd999e9c4cd214125ad8c9894a4f7a1f6d445d0`

```dockerfile
```

-	Layers:
	-	`sha256:15f1a598fae6a09be9ff797c15689a74cbb7cfa65c6117f8378a2a6e87d97f2c`  
		Last Modified: Wed, 05 Nov 2025 06:15:18 GMT  
		Size: 5.9 MB (5929788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836a6e9d48de76ec54fd3483a85772dcf96ad02a4b3c4f7c98973bef422c8ee2`  
		Last Modified: Wed, 05 Nov 2025 06:15:19 GMT  
		Size: 18.3 KB (18326 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:18ed17d7832727449836b5bc02e034e8a37da135ecb45f5273f9fc2b2c5bf632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245524894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56133d21de4b671beaf0228e1002981df038101632f34122395e238783be1252`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:12:18 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:12:18 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 04 Nov 2025 23:12:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Nov 2025 23:27:00 GMT
ENV JETTY_VERSION=10.0.26
# Tue, 04 Nov 2025 23:27:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 04 Nov 2025 23:27:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 04 Nov 2025 23:27:00 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 04 Nov 2025 23:27:00 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:27:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Tue, 04 Nov 2025 23:27:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 04 Nov 2025 23:27:00 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 04 Nov 2025 23:27:00 GMT
WORKDIR /var/lib/jetty
# Tue, 04 Nov 2025 23:27:00 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 04 Nov 2025 23:27:00 GMT
USER jetty
# Tue, 04 Nov 2025 23:27:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 04 Nov 2025 23:27:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 23:27:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad0d1fcc61302619a93c14ea37d679d5cc2a8f138552caa19924202526997b`  
		Last Modified: Tue, 04 Nov 2025 23:26:04 GMT  
		Size: 163.6 MB (163582941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e570ab115f7069c9c9118ff2edf469c57653bbdc3c8472165d1e120d2bb5182e`  
		Last Modified: Tue, 04 Nov 2025 23:27:20 GMT  
		Size: 17.1 MB (17146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b4a8fafa07784fa3d7d0d9bc92c6d491b2730a2d248a1750fd3223724cee9`  
		Last Modified: Tue, 04 Nov 2025 23:27:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0cb61002aa382314e5b24ab426ed90c9c3bd2dad00b0722caef50a3b7b93b68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8988f6bce60fdd9e447b9e6a849b072d23387b925286d68dbe2b28efd2eabdba`

```dockerfile
```

-	Layers:
	-	`sha256:924a3ba5dccf56a6d1949739a7702e2944d8473030d0e76d68122d7d4fa7cd65`  
		Last Modified: Wed, 05 Nov 2025 00:15:39 GMT  
		Size: 5.9 MB (5928453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61584a9260486706e4c598d251b1d91ca3fbe71c3f50b9038478d9f57f8b45b`  
		Last Modified: Wed, 05 Nov 2025 00:15:39 GMT  
		Size: 18.5 KB (18453 bytes)  
		MIME: application/vnd.in-toto+json
