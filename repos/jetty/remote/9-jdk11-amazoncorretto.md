## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:52486a84d77f818af385081b1f9b5f358c720bba0184c333d690f6f2fcc307c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c12db8d4d2b16fd74b33d6087131b94d4038dc8fe0626dd78c786357d5e5a809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227457053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96717bef850d089e13f6039c4678b85e0bfd805404a0816245d0fe19296fb47f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Aug 2025 04:54:08 GMT
COPY /rootfs/ / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["/bin/bash"]
# Fri, 15 Aug 2025 04:54:08 GMT
ARG version=11.0.28.6-1
# Fri, 15 Aug 2025 04:54:08 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
ENV LANG=C.UTF-8
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9b18b72b93cc14d31fcd5ae947987b35e6e81f265f08584038b95dc7093a`  
		Last Modified: Mon, 06 Oct 2025 22:12:29 GMT  
		Size: 148.3 MB (148297178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee8d2ef489698785849c34b0eb0d9a13fffafbeed0ea9d3c840f3f62f75fb1a`  
		Last Modified: Mon, 06 Oct 2025 22:13:02 GMT  
		Size: 16.2 MB (16217379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1d758b52e6e67c51d47524ae4405f6dfe47a85cb009673cb48256691e7063`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1f7f3fb01f90fc818c0a0d3ed26326d3691662a45d14d2b4b6a2af395da8ab9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a4875ea5718ccd316a973f4563f2de3ddb4ac59e705d775a8ca659514e6a3`

```dockerfile
```

-	Layers:
	-	`sha256:7f52615a722f5894712638e1dd67090e1758141b027abf8bed4e0c8744a36a65`  
		Last Modified: Mon, 06 Oct 2025 23:19:48 GMT  
		Size: 5.9 MB (5918758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6266da51f1f63b8914e82a6b09ccad5986a94afadf27c1a3a959d24216ec461`  
		Last Modified: Mon, 06 Oct 2025 23:19:48 GMT  
		Size: 17.4 KB (17431 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:761081c07a813437b0d064e69bebe62269a1be6853580f0b5731edc55c704ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226199213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fd32907af41a9faf25405e80a552d8a8cbd4c7e75949d5580b22b55b65946f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Aug 2025 04:54:08 GMT
COPY /rootfs/ / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["/bin/bash"]
# Fri, 15 Aug 2025 04:54:08 GMT
ARG version=11.0.29.7-1
# Fri, 15 Aug 2025 04:54:08 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
ENV LANG=C.UTF-8
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 15 Aug 2025 04:54:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Aug 2025 04:54:08 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Aug 2025 04:54:08 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Aug 2025 04:54:08 GMT
USER jetty
# Fri, 15 Aug 2025 04:54:08 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Aug 2025 04:54:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Aug 2025 04:54:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b8b12b7c5856e259b06bb3d673e93d1bea0809ad17d2d440d5f224e3e20fb7`  
		Last Modified: Tue, 21 Oct 2025 22:13:35 GMT  
		Size: 145.1 MB (145144638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cb462d28a220c67971da2827758e821925bf3f86bebc6901fb629add52b5da`  
		Last Modified: Tue, 21 Oct 2025 22:14:03 GMT  
		Size: 16.3 MB (16259492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55221c26c372c9c6deabfd2adfc8feff3e1ce1270b98effbead0c8ded41caa7c`  
		Last Modified: Tue, 21 Oct 2025 22:13:53 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:caaf2b213b1acb945766fe18d950316370534b006c628abe9a2742a0a60c920f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5938942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca4371b5d7e5f2eda8fb73b5a23616c23016f487597e2c527468fa437f0c1a4`

```dockerfile
```

-	Layers:
	-	`sha256:ff3c075eb80ab9297b85ac2760d9d40d4145bcf48e7d9e7326381d537ee897b5`  
		Last Modified: Tue, 21 Oct 2025 23:22:53 GMT  
		Size: 5.9 MB (5921419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecfad8d6dceb083a4e5fc1d0e1ead052c614209bad9d798e8503386c3c3b6d0`  
		Last Modified: Tue, 21 Oct 2025 23:22:54 GMT  
		Size: 17.5 KB (17523 bytes)  
		MIME: application/vnd.in-toto+json
