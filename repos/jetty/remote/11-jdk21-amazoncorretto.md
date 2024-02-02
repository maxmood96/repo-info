## `jetty:11-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:f6647113d3be3a7e5306c6519775f32e87b282dacd5cd752ec2322f12f172bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:87493a13fa8aff54bf59ceedb9562a32a0e4c499d10ad8dd3355386d2232539d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248727411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7e3201c478826a58056ba31c6839af3425bab790bc19d557c3682b7fb39ce5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:51:16 GMT
ARG version=21.0.2.13-1
# Wed, 17 Jan 2024 23:51:40 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 17 Jan 2024 23:51:41 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:51:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Jan 2024 01:12:18 GMT
ENV JETTY_VERSION=11.0.19
# Thu, 18 Jan 2024 01:12:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 18 Jan 2024 01:12:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 18 Jan 2024 01:12:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 18 Jan 2024 01:12:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 01:12:19 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.19/jetty-home-11.0.19.tar.gz
# Thu, 18 Jan 2024 01:12:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 18 Jan 2024 01:12:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 18 Jan 2024 01:12:37 GMT
WORKDIR /var/lib/jetty
# Thu, 18 Jan 2024 01:12:37 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 18 Jan 2024 01:12:37 GMT
USER jetty
# Thu, 18 Jan 2024 01:12:37 GMT
EXPOSE 8080
# Thu, 18 Jan 2024 01:12:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Jan 2024 01:12:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f84241f2bb59ffb93ded1f8d01c552d2f92bd89c24ce5f633002c7c618aa32`  
		Last Modified: Thu, 18 Jan 2024 00:08:42 GMT  
		Size: 165.7 MB (165696333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b29e28591843aadff5ad6e07d50af6bdea8f660cd2ed538f9db2daf96f9b65`  
		Last Modified: Thu, 18 Jan 2024 01:22:54 GMT  
		Size: 20.4 MB (20368443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8958835c5ea90428f4cbaf8145ec4853fb3c6499fee55dab513b11d4ea83b3a`  
		Last Modified: Thu, 18 Jan 2024 01:22:52 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:51bba259911ac8ef7c4130207da95f021e68b492878078cab4fb894622b0fbbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248527659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1526b749badd75b101b7f34299c6fbf8c0f0b944a2e48c45f241cbf42eacb5bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:50 GMT
COPY dir:9aa2a0617061f7d0def778dac1581f965a33bb26f84a69dab1fef189d1a60261 in / 
# Thu, 01 Feb 2024 23:30:51 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:54:58 GMT
ARG version=21.0.2.13-1
# Thu, 01 Feb 2024 23:55:19 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 01 Feb 2024 23:55:21 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:55:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 02 Feb 2024 04:35:56 GMT
ENV JETTY_VERSION=11.0.19
# Fri, 02 Feb 2024 04:35:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 02 Feb 2024 04:35:56 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 02 Feb 2024 04:35:56 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 02 Feb 2024 04:35:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 04:35:56 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.19/jetty-home-11.0.19.tar.gz
# Fri, 02 Feb 2024 04:35:56 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 02 Feb 2024 04:36:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 02 Feb 2024 04:36:12 GMT
WORKDIR /var/lib/jetty
# Fri, 02 Feb 2024 04:36:12 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 02 Feb 2024 04:36:12 GMT
USER jetty
# Fri, 02 Feb 2024 04:36:12 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 04:36:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 04:36:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:47443cfd9c92429d14dc57cc7a23137f39c4c124ae6551bb1f992c8dfbaee707`  
		Last Modified: Thu, 01 Feb 2024 08:21:29 GMT  
		Size: 64.5 MB (64453219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb59fe6197271a3523b658a82372cedfb8effaade5362f27392bad6f702f4a6a`  
		Last Modified: Fri, 02 Feb 2024 00:04:15 GMT  
		Size: 163.7 MB (163663602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed1e281c6fcc602e02551f1cd93b2bb054fd6bb71fcdc9da7a7199535807115`  
		Last Modified: Fri, 02 Feb 2024 04:49:11 GMT  
		Size: 20.4 MB (20409207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a763663020b5534116786ef932c340c71d22f4e7016f576ce28975ee307e22e3`  
		Last Modified: Fri, 02 Feb 2024 04:49:09 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
