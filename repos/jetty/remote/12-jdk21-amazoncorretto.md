## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:9aa63f2fe572f384d04f595709ae2348f43573ce61506cc4c891f894e99d2715
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:9c6c44480ad3600590f696c7bc5c0f20c033bacdc0c5cdaff62a5207c896e7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267962508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098d3b0817cca6b1a0c1d0a6078342cd0aa82857a549d4e197b9612c74efe02f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:7cf02143f4772415f4bc4b1e97ab9cd6cb0a41ac9a2b7602816db88b5c2317d1`  
		Last Modified: Fri, 20 Dec 2024 22:33:10 GMT  
		Size: 164.8 MB (164787402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bddee02a95321efa3f17fd446c2f90b0ed9ac0f89e33ddef0e895db5abc44ea`  
		Last Modified: Thu, 02 Jan 2025 19:29:12 GMT  
		Size: 40.5 MB (40496003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49d657af1c6971efe29ff3262cd58beaf9676072f4df4df2c6afdacd36c2842`  
		Last Modified: Thu, 02 Jan 2025 19:29:12 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:d448dff99700201c1cc46e47857350adc5e4d9f317678e1c4df07c07c6feae82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6041600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a1c4bff49efee81cf6b2deef316bf6c527567f1736c4a6708890a255368f3e`

```dockerfile
```

-	Layers:
	-	`sha256:6048a1ebc10dd5ec5bb782a57717deb52dedc21c87f6ff9c4f41187d2aa04656`  
		Last Modified: Thu, 02 Jan 2025 19:29:12 GMT  
		Size: 6.0 MB (6023232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b93c4946459f30ff5166c6d8a9b2c397d097d55972fd0e795380fe1a2bdba46`  
		Last Modified: Thu, 02 Jan 2025 19:29:12 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:b7babac90c3cd56c95ffbac308411233866f57a59316fd18feaf289c0c548ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268030736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6528e2e91e14de97baaeb5ab64a14120021d61d484d232a3d36ffed8e8363d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c520393dae5bcb364385e9b1b7b5f017fd81834b93db884937ea2f00d247ab7c`  
		Last Modified: Sat, 21 Dec 2024 01:49:30 GMT  
		Size: 162.8 MB (162839630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bfeb03fd5dc10893e87a46fbef9666dabedb5e0b781fe95b35932c6e37cc24`  
		Last Modified: Thu, 02 Jan 2025 19:56:59 GMT  
		Size: 40.6 MB (40607553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c392e011ebca0c691d5daed5271db5b78224097180a437ee3d7d5cdccb25ad0`  
		Last Modified: Thu, 02 Jan 2025 19:56:58 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bd13e4f9eea03625aa61ac67a56660a67b440e1730404f1d4beed424cbac670b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e79fe611113ad821ff962b198b8e4b0864c6ccf73932c887f5b0482fc34b0a9`

```dockerfile
```

-	Layers:
	-	`sha256:9238760d3333fa11279e81c34054348d092491dfb08bb3681c1aa9400f5a5ee0`  
		Last Modified: Thu, 02 Jan 2025 19:56:58 GMT  
		Size: 6.0 MB (6021897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f175bd7ce23dc14992281cb8f9bc9b7eaa25d00ca31dc256dda4f9c7916bf0e1`  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
