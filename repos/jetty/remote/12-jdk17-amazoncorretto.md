## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:f19a2723b5f27696d461c08855dd18752b4255d0dcc3453f28277029afb62c1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:35aec0c95273bf1b5b1fc0453da63afc249b6fc99ec25b87cd7978f4a8b156ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267254895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fab49fb256978171793d41604a2decd816e0fd04b4d47038ef71556068509ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:17:57 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:17:57 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:17:57 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:17:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 09 May 2026 01:22:06 GMT
ENV JETTY_VERSION=12.1.9
# Sat, 09 May 2026 01:22:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 09 May 2026 01:22:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 09 May 2026 01:22:06 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 09 May 2026 01:22:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 01:22:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Sat, 09 May 2026 01:22:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 09 May 2026 01:22:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 09 May 2026 01:22:06 GMT
WORKDIR /var/lib/jetty
# Sat, 09 May 2026 01:22:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 09 May 2026 01:22:06 GMT
USER jetty
# Sat, 09 May 2026 01:22:06 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 09 May 2026 01:22:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 09 May 2026 01:22:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c2b88010711c77950915c6572f377f9489e6d24e1215ea3505d74e89f9c008`  
		Last Modified: Sat, 09 May 2026 00:18:18 GMT  
		Size: 152.6 MB (152609374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954f2c6c03f0c8712cd7b6b74b080913c210a30c7394fd04e246542bf693f4c5`  
		Last Modified: Sat, 09 May 2026 01:22:21 GMT  
		Size: 51.8 MB (51783907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d682804ae2dba2ce9eb327b50bcf7473e57329f62e7ae5219fbd4100de3ceb`  
		Last Modified: Sat, 09 May 2026 01:22:19 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:4f3088cd3184e163ca9213b6ff35e91a92080c424d65be239f75d9eaec0b6c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022b4c984bd70719dc92685fd1ca430d45c29aeae9942cb2029bf7187c8a1a5b`

```dockerfile
```

-	Layers:
	-	`sha256:10ae45d242469b35cafc6eadc12bf2c36a42566d3ac1eda6f658f7e2719fdcbb`  
		Last Modified: Sat, 09 May 2026 01:22:19 GMT  
		Size: 6.1 MB (6119644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd3396d4dff0a35201389544da27d9eb3ae2c919534ccbfd8367057a2a86fff`  
		Last Modified: Sat, 09 May 2026 01:22:19 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:47059350a261b6f29c7f5f4b6a3505d3f112228c0b4f76b775c2b348915559ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268018155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf82c90415ffefb3fded37b1edf46e0ed956975744853473deda5cf2879f65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:36 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:15:36 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:15:36 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 09 May 2026 01:47:32 GMT
ENV JETTY_VERSION=12.1.9
# Sat, 09 May 2026 01:47:32 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 09 May 2026 01:47:32 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 09 May 2026 01:47:32 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 09 May 2026 01:47:32 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 01:47:32 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Sat, 09 May 2026 01:47:32 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 09 May 2026 01:47:32 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 09 May 2026 01:47:32 GMT
WORKDIR /var/lib/jetty
# Sat, 09 May 2026 01:47:32 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 09 May 2026 01:47:32 GMT
USER jetty
# Sat, 09 May 2026 01:47:32 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 09 May 2026 01:47:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 09 May 2026 01:47:32 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5a373cc394dd589400a17753c0e3a74546136c286b1faca8494832a0c9dfce`  
		Last Modified: Sat, 09 May 2026 00:15:58 GMT  
		Size: 151.3 MB (151324879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54714f09d5d97f9e586101260b782605cde7584079ea4c2eec4ea984856651a`  
		Last Modified: Sat, 09 May 2026 01:47:47 GMT  
		Size: 51.9 MB (51882485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0d531adc67b0ecc48429ef3e963aa794a0805d30afdaca5e2933b0d3975568`  
		Last Modified: Sat, 09 May 2026 01:47:45 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3934628e4a95444f37a819f36aa90449414d45513d3172e878e3596522aa4897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4cc253ae4da6fd2886f3aa3fe78d1356ffb2439b7448b36f1b5b2b6f4793b5`

```dockerfile
```

-	Layers:
	-	`sha256:7154023d18c9e49f7ab3177cd158d48bd960da9c1b26f8f76eb68b14f61b45a9`  
		Last Modified: Sat, 09 May 2026 01:47:46 GMT  
		Size: 6.1 MB (6118273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eae6ee6dad8ebca799f01c22ba1136a25585f702948b26233ecad81d73d8660`  
		Last Modified: Sat, 09 May 2026 01:47:45 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
