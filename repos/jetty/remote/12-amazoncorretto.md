## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:397f3c6e7b6b51368e7e74f3a03d5b1c634cdfb2e23ec88016bfe9ad5b34b35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:44c0b4a3010197708152ebb2cdaa067e241e181851670ed984687b50ea37a203
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268061554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e7145a895041440bc1cea422c38f8dc50d0b0ec598cb54f367368f54c55584`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 20:53:01 GMT
ARG version=21.0.2.14-1
# Tue, 27 Feb 2024 20:53:26 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 27 Feb 2024 20:53:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 20:53:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Feb 2024 21:23:43 GMT
ENV JETTY_VERSION=12.0.6
# Tue, 27 Feb 2024 21:23:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 21:23:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 21:23:43 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 21:23:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 21:23:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.6/jetty-home-12.0.6.tar.gz
# Tue, 27 Feb 2024 21:23:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 21:24:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 21:24:02 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 21:24:02 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 21:24:02 GMT
USER jetty
# Tue, 27 Feb 2024 21:24:02 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:24:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 21:24:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65aa1d9db07ada9a2a5b4a0639f7f172d6455047e28e85f0820b2ecbab083f42`  
		Last Modified: Tue, 27 Feb 2024 20:57:24 GMT  
		Size: 165.7 MB (165693563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce340a065ed902dd1b596622559c459593bd87939da047a57d02e4df4e35a8c`  
		Last Modified: Tue, 27 Feb 2024 21:30:46 GMT  
		Size: 39.7 MB (39719627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2276a44b0d4d2b4b4f0a83b3893dee21358ad9256d28c3f8e704c5cedd489`  
		Last Modified: Tue, 27 Feb 2024 21:30:43 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:fa5554b00d089797a140115831925ecfe325ac5e462b5e70762b43f0d258d4c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267870234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39923dfb3421d2e2a64bfd1db782e4b9ef0f27c187faaea7f15b80f7d85e0eea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:29 GMT
COPY dir:ed6a811a4137d0b4591f2c9dabfdd849cb878c3501af91aa79c89a2e9f4479d5 in / 
# Mon, 26 Feb 2024 23:06:30 GMT
CMD ["/bin/bash"]
# Tue, 27 Feb 2024 21:07:28 GMT
ARG version=21.0.2.14-1
# Tue, 27 Feb 2024 21:07:50 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 27 Feb 2024 21:07:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Feb 2024 21:07:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Feb 2024 21:35:58 GMT
ENV JETTY_VERSION=12.0.6
# Tue, 27 Feb 2024 21:35:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Feb 2024 21:35:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Feb 2024 21:35:58 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Feb 2024 21:35:58 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 21:35:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.6/jetty-home-12.0.6.tar.gz
# Tue, 27 Feb 2024 21:35:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Feb 2024 21:36:14 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 27 Feb 2024 21:36:14 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Feb 2024 21:36:14 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 27 Feb 2024 21:36:14 GMT
USER jetty
# Tue, 27 Feb 2024 21:36:14 GMT
EXPOSE 8080
# Tue, 27 Feb 2024 21:36:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 21:36:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:53f483bd5fa48049d6551a641e547b302df82b17493915161f3f62020b3648fa`  
		Last Modified: Mon, 26 Feb 2024 23:07:06 GMT  
		Size: 64.4 MB (64445079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941afd9563243fdf387f8568f0c597eea409bf24c6eb89f386125dbf384f6087`  
		Last Modified: Tue, 27 Feb 2024 21:12:01 GMT  
		Size: 163.7 MB (163666566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5202712343fd72f26e7ce0a10be76571e37a384c59b4963cf8cc7130ea0afbf9`  
		Last Modified: Tue, 27 Feb 2024 21:40:51 GMT  
		Size: 39.8 MB (39756955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8d605739daab372fc8006ceef69cd6ac197565610f99f9d37a2d46aaf0083d`  
		Last Modified: Tue, 27 Feb 2024 21:40:49 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
