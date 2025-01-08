## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:03128a0659a1f8c7f753a8f1b941d770635c5f3188fc94bffc4d48d468a21de5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d8180dc8cb47eeaeed2031b948972fd8aa1b5b58cc9d4e7d50386a3064b8d744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254787442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b141226bba994bcdd2cbe807f7dc6409b5fcf0b98579edd1408097424cb1220`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab261828f6d05146d337cb0cbf1b142becb434d0c55081fb828bba21c4236b30`  
		Last Modified: Fri, 20 Dec 2024 22:32:38 GMT  
		Size: 151.6 MB (151608423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd739dd8660f279fe4b40eb5073ac753321bb293ab8d6488a86da053f31ebe`  
		Last Modified: Thu, 02 Jan 2025 19:29:16 GMT  
		Size: 40.5 MB (40499914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bca0e9006191d127e8515dded592f0bdb10d1c6c853fab0daabdf6434136eb`  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:cfb29a2d795ba1145289c7933e021b06be3c216e53493f663414916689c6c5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6039768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f803421df469d5ff7ac64c3ba71df79cd4ab3abae0055b7c3fea6638d8da21`

```dockerfile
```

-	Layers:
	-	`sha256:7a1ab38165eb588d22fa6cac8b7f86f3d6edf4bc42465c9ff282761dcdc5ce3c`  
		Last Modified: Thu, 02 Jan 2025 19:29:16 GMT  
		Size: 6.0 MB (6022367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d00a1a3c2c39854b2f8112e1f3bae4dede7f1a47deaca3b779d64d465086778`  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6f0af59e70bc0f4b15078a63d757e94652e0d5e20a2f1833f530bae4e7e4ca7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255422113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febce7c72d00fd305fe96125c9cc0ebf4ea1a893d171d5a1f493efdfcf1e5031`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1286b98bd714a26fe96f8e5534493a65c854b959a4b44f28eb6a2e9ae883e380`  
		Last Modified: Sat, 21 Dec 2024 01:43:23 GMT  
		Size: 150.2 MB (150238978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f0bc0836f115adaf035de63ce76302af60a33bfbafebbe4a454c4aede1124`  
		Last Modified: Thu, 02 Jan 2025 19:59:23 GMT  
		Size: 40.6 MB (40599582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645696e2fa596869a7b924327a60236146e690035acc8384eae1c6bef43cfb6`  
		Last Modified: Thu, 02 Jan 2025 19:59:22 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:42551aeeccc139b37b0373c2755e8fde73128ca2b202db8bf49e670e9a8b4946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e240ca1485cb7e033d89ce6cda023319f4f89897f6330d019bb89b04f057d464`

```dockerfile
```

-	Layers:
	-	`sha256:c754167dc0bf7a0a6f591575741d3b8495485f5ad82e2e3666c5eb812d1749a3`  
		Last Modified: Thu, 02 Jan 2025 19:59:22 GMT  
		Size: 6.0 MB (6020996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6175f164dca5146e4b37716508947cbc9e2aec64798a2fdfb6b2efa23875c06`  
		Size: 17.5 KB (17493 bytes)  
		MIME: application/vnd.in-toto+json
