## `jetty:9-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:2bc87af49248bd40fd046360e601b786076e1983a38502bbb8ea22e298e47582
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3c85dd701e4da631667318b44f4ff90db4c7839001dc4b1a82ad721f6ebd2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244629636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130b6b4d1aec50829e41d1023f17ed273d8207373dbf5e48b404fc98a06e1169`
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
# Fri, 31 Oct 2025 01:12:40 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 31 Oct 2025 01:12:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:12:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:12:40 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:12:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:12:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 31 Oct 2025 01:12:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:12:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:12:40 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:12:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:12:40 GMT
USER jetty
# Fri, 31 Oct 2025 01:12:40 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:12:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:12:40 GMT
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
	-	`sha256:06482a1cb770edbadc34b6d65421564a5e9469e2733695b23acba92cbbb969ee`  
		Last Modified: Fri, 31 Oct 2025 01:12:58 GMT  
		Size: 16.2 MB (16211100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb64a9a6bd109f73598dd7c6e68c53390ee3fbeb1420d0436c6dec04787bd42a`  
		Last Modified: Fri, 31 Oct 2025 01:12:57 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:a38d1eba7d8c24b3bee8eb24a9551bc8d08d4c758a513a932840ffc6eefd9055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5933893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688679d37a00d157f0b7324ec522aebe7f2144b23a051f17996685331bf0ab35`

```dockerfile
```

-	Layers:
	-	`sha256:e33031ae7d7f4c4602ff73bd79322d96fae97233dc34edfadb871725a1ae9c17`  
		Last Modified: Fri, 31 Oct 2025 02:19:36 GMT  
		Size: 5.9 MB (5915543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a550c0beef6f7e051036465672cf61ef55f098a5b507ebe8be240322bdf6765a`  
		Last Modified: Fri, 31 Oct 2025 02:19:37 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:65cfe733086fd69eff5dbfb3a1a73b8628e1a460cb61ac10a57023b032682e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244654632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e020061f4f4cc31f22e0aa0a22a81e8266fcef075d90d5f59f6c029f79c60a`
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
# Fri, 31 Oct 2025 01:13:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Fri, 31 Oct 2025 01:13:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 31 Oct 2025 01:13:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 31 Oct 2025 01:13:17 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 31 Oct 2025 01:13:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 01:13:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Fri, 31 Oct 2025 01:13:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 31 Oct 2025 01:13:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 31 Oct 2025 01:13:17 GMT
WORKDIR /var/lib/jetty
# Fri, 31 Oct 2025 01:13:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 31 Oct 2025 01:13:17 GMT
USER jetty
# Fri, 31 Oct 2025 01:13:17 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 31 Oct 2025 01:13:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Oct 2025 01:13:17 GMT
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
	-	`sha256:e72f947b51386318873f21f1ef8833d7fbf06b24c390bafde49ff9757a0e1d04`  
		Last Modified: Fri, 31 Oct 2025 01:13:36 GMT  
		Size: 16.3 MB (16271893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb14d82c2fa234087880a7b1a802d9ce564f4d84ecf3adef453d70675c1acf5`  
		Last Modified: Fri, 31 Oct 2025 01:13:34 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8f2a2e0c58840bc10f35b6b6946b9fbb9bbbc143e0274e8ba25fb697dcd3204f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e13a2fe5ababb4dd214fd2546cfab70149b36ea0bf6b1e5b2706a2b555978e`

```dockerfile
```

-	Layers:
	-	`sha256:01db6071dc85b2eef638ba9e027e40a89f72b7443eb8df807bbe694a7d8892d5`  
		Last Modified: Fri, 31 Oct 2025 02:19:43 GMT  
		Size: 5.9 MB (5914208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab183f40a2db731403160062b911941964a59f9a5163276de57b720358b813f`  
		Last Modified: Fri, 31 Oct 2025 02:19:44 GMT  
		Size: 18.5 KB (18478 bytes)  
		MIME: application/vnd.in-toto+json
