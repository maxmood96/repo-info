## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:856639a74a0c375c9695f281b8fbbab3d603b5b83f0ac165bab242b3dcad8497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a2b2759400aa399bb47c04c81dd508e59847072619d8c2c0252b9ba31a29a66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235878455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a96d8f64c00841b0de3585588b180499000e282b67ce9a5da12fdc85d99fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:47 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:11:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:47 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:13:40 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 31 Oct 2025 01:13:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:40 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 31 Oct 2025 01:13:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:40 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:40 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:40 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cee90354531f4ca16570052264d74542e465a82e38fdafa8b2ffb35f381810`  
		Last Modified: Fri, 31 Oct 2025 01:12:54 GMT  
		Size: 152.4 MB (152409108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100afb05b386ea754718a566ffe29616debf564c15a971f3394a919c3c84e669`  
		Last Modified: Fri, 31 Oct 2025 01:13:55 GMT  
		Size: 20.5 MB (20533402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522579bb603f0ef22ad4c362e2b4676f4af1b18943f91247ff792da40eba002`  
		Last Modified: Fri, 31 Oct 2025 01:13:52 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:39744aad9f89f637aa398f9d960fa0e942d91ae0fa327560b02379580e614aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d438d9b946511b88d8cad6f97f0f65ec894293de2d9c386fbf6c9f08c1dde583`

```dockerfile
```

-	Layers:
	-	`sha256:87fb1f74f28699a430842ef62afde96e29fe20bec23e507f10abd3f9c3e177b1`  
		Last Modified: Fri, 31 Oct 2025 02:16:52 GMT  
		Size: 5.9 MB (5928973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5425329412a2cb993a66155896242ec0eda662d0fe8ff23ab02ae4494bbe858`  
		Last Modified: Fri, 31 Oct 2025 02:16:53 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:9c34aeb9509a81e9034378ca2a649485fd3dd22836813a7445b3eca743bc21ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236376916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5f957581a19f7c4a3a8bcefa7b48c5e55a9acd9c91291327fd4c9bcdf6db44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:09 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:09 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:09 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:14:01 GMT
ENV JETTY_VERSION=11.0.26
# Fri, 31 Oct 2025 01:14:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:14:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:14:01 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:14:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:14:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Fri, 31 Oct 2025 01:14:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:14:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:14:01 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:14:01 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:14:01 GMT
USER jetty
# Fri, 31 Oct 2025 01:14:01 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:14:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:01 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe77ddb74850a2a8eb934a6793b84365d9be75189f7d257ddd3bf0519b0fb0`  
		Last Modified: Fri, 31 Oct 2025 01:13:14 GMT  
		Size: 151.0 MB (150988225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1648c761692a86d6b25d5a01e8234d2f4e9bb66e22359c23d860fe1cb11d86b6`  
		Last Modified: Fri, 31 Oct 2025 01:14:23 GMT  
		Size: 20.6 MB (20593358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858ec48311596967755f01f1243bfdc1789a9715883248a842454d2fdf7063f`  
		Last Modified: Fri, 31 Oct 2025 01:14:21 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0735fd599a940067adc53e0658138491e395de15bf036619c5a3c408f8ea6a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5865c1c6ce32c8688a6fa033afca528268ed1b897e0affb8afbb682dcd7b852`

```dockerfile
```

-	Layers:
	-	`sha256:399b203732c37e459fdd619766e100168fcd629ceecbcef94f5c08f6652bc054`  
		Last Modified: Fri, 31 Oct 2025 02:17:02 GMT  
		Size: 5.9 MB (5927602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfaffddd0092675f7aeb08fa3912214ef39b5a2fdbaa8bf72e4bfa67fe4c3e46`  
		Last Modified: Fri, 31 Oct 2025 02:17:03 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
