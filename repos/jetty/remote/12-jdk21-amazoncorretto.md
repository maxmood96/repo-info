## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:857f2764cd415059bd41c1937f01c47ef77c14f5da2556a0db61c237bb824042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6d1d1e261b1f1cbe0f2fe4d26cc4b71db094209d90fbcb74beaebd0e2c2e6599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280384746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5020d08bedbcc7366f3b4e3ef777b3196f707a045de7e0af21eeaa78d3e61d03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Oct 2025 00:53:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
USER jetty
# Wed, 22 Oct 2025 00:53:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Oct 2025 00:53:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Oct 2025 00:53:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d592fe075709c62638ad9b0b8b67157100093faaa06408e582bdceb37cb6083`  
		Last Modified: Wed, 22 Oct 2025 00:36:57 GMT  
		Size: 165.5 MB (165487938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d0d6aab01315dcf28d92c70f9a36da0e4587fd1c8fa3d4ef5d238f6cdb6c7`  
		Last Modified: Wed, 22 Oct 2025 17:46:21 GMT  
		Size: 52.0 MB (51954312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a7ca5952310593a3acbfd23ec6e22e6e2addcc8490d1a7240eeedefcd20b28`  
		Last Modified: Wed, 22 Oct 2025 17:46:17 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b9baa772176054c8807cc41f0c288a3972fbac6042a07af4d20c26e0ffc9c43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6171192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ac2e53039ab004e8401f4f82c2c9a6c97cfa122be5908a57006bf814830194`

```dockerfile
```

-	Layers:
	-	`sha256:495afcec98dfa489caaee592c2b7dbbe80fc4b14aa86c580dcb64cee245fc184`  
		Last Modified: Wed, 22 Oct 2025 20:16:41 GMT  
		Size: 6.2 MB (6152830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f52b1cc150729c6fa7cc637e4271e09ecf959bfcec758c1d0f67eb1b7e600e`  
		Last Modified: Wed, 22 Oct 2025 20:16:42 GMT  
		Size: 18.4 KB (18362 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c5773aaa3fb8639a6aee4e7c4ee08b6e50878e9bc4a7dcd4bd40dfeb3606ac7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280391425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101ab18d3d98e41dab8adbe53829e69e8cf57e6c06dfc46ace363efe77b32042`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_VERSION=12.1.3
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.3/jetty-home-12.1.3.tar.gz
# Wed, 22 Oct 2025 00:53:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Oct 2025 00:53:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Oct 2025 00:53:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Oct 2025 00:53:34 GMT
USER jetty
# Wed, 22 Oct 2025 00:53:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Oct 2025 00:53:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Oct 2025 00:53:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c99654ecaa79d9c18ade13301c62620d4fd6ffa16a1f4b1d2b9003f55592d`  
		Last Modified: Tue, 21 Oct 2025 22:13:26 GMT  
		Size: 163.6 MB (163587188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce55505204a5f89c7f28ce55bae392cd46e9dfa7d4e054bb0ee9e74dab654687`  
		Last Modified: Wed, 22 Oct 2025 17:46:48 GMT  
		Size: 52.0 MB (52009153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74b660e026b4433fbc662f5ac6a2ec92909ca6ae1bdcb167b8a6491826f5235`  
		Last Modified: Wed, 22 Oct 2025 17:46:43 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:763f7f363a050a9d3a4de04cd3c2b2b76df4ce6b8cce892c3b0c93095d41fb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b711402de9db2da64c5d3e33599013f5b0270dc12a4e40b50c141e0295a91f`

```dockerfile
```

-	Layers:
	-	`sha256:e4577f102ec4419c55aea0ecc25624228206bb401ddc7a347061f692ac7de925`  
		Last Modified: Wed, 22 Oct 2025 20:16:48 GMT  
		Size: 6.2 MB (6151495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:addbe1b7891f028adf2dbc25af70003aeb7bbe51aebd1558f7b1e5079e09dabd`  
		Last Modified: Wed, 22 Oct 2025 20:16:49 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json
