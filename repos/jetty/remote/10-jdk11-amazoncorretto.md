## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:1ca4185f16c5f22b5eefab883028432143069c240cc3d3c0e4c25691ebdaccc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:384269df8a91dbf2a454b11f2dc2fbe871dc9f7c76bb56be7dc8f77521ea4aa7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227651220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a504c3bd8e2246ef489f1ec4977ec6e84e91cfb979db85489d2a22113fea9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:44:02 GMT
ARG version=11.0.23.9-1
# Thu, 20 Jun 2024 17:44:26 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 17:44:27 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:44:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 20 Jun 2024 19:45:12 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 20 Jun 2024 19:45:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:45:13 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:45:13 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:45:13 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:45:13 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 20 Jun 2024 19:45:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:47:53 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:47:54 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:47:54 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:47:54 GMT
USER jetty
# Thu, 20 Jun 2024 19:47:54 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:47:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:47:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834abf49d00e2112eabd0d490f9af036a5d761960b0d3cc9d966ea5bb47a037`  
		Last Modified: Thu, 20 Jun 2024 18:19:01 GMT  
		Size: 148.1 MB (148105352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310828475010817b747bfabf93aa6b32d6ee0dea535c218794d8dfa910301bb`  
		Last Modified: Thu, 20 Jun 2024 19:54:43 GMT  
		Size: 16.9 MB (16897782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b537676934a7fca90935278740413b26a73ad3446388679a58cb60483e3205`  
		Last Modified: Thu, 20 Jun 2024 19:54:41 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:4b60bcc375d9e87958d39abc9cc57f6dd29d7b2199606b5d675b29b1ad75de82
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226821239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c903d939836dfef4cab9d85534f8f0d992fb425fde90167a27ece01c08acdd41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:30:29 GMT
ARG version=11.0.23.9-1
# Wed, 05 Jun 2024 02:30:47 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:30:49 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:30:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 05 Jun 2024 07:53:55 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 05 Jun 2024 07:53:55 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 05 Jun 2024 07:53:55 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 05 Jun 2024 07:53:55 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 05 Jun 2024 07:53:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:53:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 05 Jun 2024 07:53:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 05 Jun 2024 07:54:09 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 05 Jun 2024 07:54:10 GMT
WORKDIR /var/lib/jetty
# Wed, 05 Jun 2024 07:54:10 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 05 Jun 2024 07:54:10 GMT
USER jetty
# Wed, 05 Jun 2024 07:54:10 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 07:54:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:54:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a510556688a17b89b763674920ddcab88215d2e2a20215a11886a73170fe5520`  
		Last Modified: Wed, 05 Jun 2024 02:41:48 GMT  
		Size: 145.2 MB (145226640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f27ec8a44768aa3a3aabfecc3cfb686ece7bfba74fcea1359c02415161bcec7`  
		Last Modified: Wed, 05 Jun 2024 08:06:06 GMT  
		Size: 17.0 MB (17017525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130ab3d9455019e67012672a6d4424710cf3670e7cd92b4989d08e5669855426`  
		Last Modified: Wed, 05 Jun 2024 08:06:05 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
