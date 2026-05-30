## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:33279ecdf3228f1f99807313d6d0e29a6b30b192fe027ca0fe54abdee6f8e37c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:270856aac3cd8f1f5383961a90b98f384ae022520474a447432d11a69d022bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280525502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d7b9ffdd4926d9c54e47eb47edf9d989cc4fa947fc6e02839b26094197bdd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:12 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:12 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:12:12 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:13:11 GMT
ENV JETTY_VERSION=12.1.9
# Sat, 30 May 2026 02:13:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 30 May 2026 02:13:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 30 May 2026 02:13:11 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 30 May 2026 02:13:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 May 2026 02:13:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Sat, 30 May 2026 02:13:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 30 May 2026 02:13:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 30 May 2026 02:13:11 GMT
WORKDIR /var/lib/jetty
# Sat, 30 May 2026 02:13:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 30 May 2026 02:13:11 GMT
USER jetty
# Sat, 30 May 2026 02:13:11 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 30 May 2026 02:13:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 May 2026 02:13:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c385119c2f2941b8af70a64eacbaf2f0ddf73bcef9afe5084b40aca94bccda`  
		Last Modified: Sat, 30 May 2026 01:12:32 GMT  
		Size: 165.8 MB (165760940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25e2e2b64bf8e7549d91cd1d75ca26c42a5077d0307a704ceaf5948009c663a`  
		Last Modified: Sat, 30 May 2026 02:13:25 GMT  
		Size: 51.8 MB (51820736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05bb496a5cfa479668f36aaf7c73bea75827c12faf6fca09890b1c841bd4c86`  
		Last Modified: Sat, 30 May 2026 02:13:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:adb16b205bb43f19817c48dfa9f2a94a9dea5775de8542e8d66d57a6bc2815ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d312440ed985ae4a40d40cace7a933063d430050e428e7ed9ffe47b6625c435`

```dockerfile
```

-	Layers:
	-	`sha256:15eecd57df60e116348ac710528cde48639aaa448c135ba2183685c6e07ddd83`  
		Last Modified: Sat, 30 May 2026 02:13:24 GMT  
		Size: 6.1 MB (6119547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b98544b845dd42ff600d8bbfe7e16491313640b1bf6a416b249cad78a73ad83`  
		Last Modified: Sat, 30 May 2026 02:13:23 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:411c419871d2a81858b85021d016f3ac49b24e2c24c04f60e09c50f79d58c0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280582091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e4d6ede648d94549e559fdff5f7381350339bcdd96fe7c0c9dc8047fb1f021`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:12 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:12 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:12:12 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:13:04 GMT
ENV JETTY_VERSION=12.1.9
# Sat, 30 May 2026 02:13:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 30 May 2026 02:13:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 30 May 2026 02:13:04 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 30 May 2026 02:13:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 May 2026 02:13:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Sat, 30 May 2026 02:13:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 30 May 2026 02:13:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 30 May 2026 02:13:04 GMT
WORKDIR /var/lib/jetty
# Sat, 30 May 2026 02:13:04 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 30 May 2026 02:13:04 GMT
USER jetty
# Sat, 30 May 2026 02:13:04 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 30 May 2026 02:13:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 May 2026 02:13:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c908ecabd64b5f3b79616b6d1005e436e80ea25c80a15abfc8cf5fd74147060`  
		Last Modified: Sat, 30 May 2026 01:12:35 GMT  
		Size: 163.9 MB (163903189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774ff6091f365418f948bf27317395e490631d9f2cd5b2bf22278c7b20e6a81`  
		Last Modified: Sat, 30 May 2026 02:13:18 GMT  
		Size: 51.9 MB (51886317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29b6c61d2b944121ad231ab1101c900592bb86e1d3e7ac09467e22b4dffc511`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7683bd0b38015d7327ae24c205389eb44f71ef61ebb0b33e37ded24c1eb00433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394527225caef052fda73738ae2733c432f39689c7f7754676e41e3f20cf4961`

```dockerfile
```

-	Layers:
	-	`sha256:ea626b996856a2e5ebacada75716be9d98f63f5aa4e451356b89bdd532686a0f`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 6.1 MB (6118176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0fd2c6700648dce48a483b8dabf039c3fa09dc017bddd95f50a88ef2239dcd`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
