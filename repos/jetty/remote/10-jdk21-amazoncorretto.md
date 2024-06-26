## `jetty:10-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:e597506eabb951f0945085bc8ddc34f533b78d1093007341b97d633f8cbd0c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5b6e5fd1c804b9e738608af1ac98f8aab75473922460afb71d90f4272ccdb6ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245227364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e605e8f213cc2aefd9e66b273f2f3e7825fcbb98fd5767862d89c7f1e1be880d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:51:24 GMT
ARG version=21.0.3.9-1
# Thu, 20 Jun 2024 17:51:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 17:51:49 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:51:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 20 Jun 2024 19:37:12 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 20 Jun 2024 19:37:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:37:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:37:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:37:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:37:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 20 Jun 2024 19:37:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:42:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:42:16 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:42:16 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:42:16 GMT
USER jetty
# Thu, 20 Jun 2024 19:42:16 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:42:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:42:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6587bf502e0fddfa3d71e42fc5be22a5dada226ab4e30f31f4c34ed43581b965`  
		Last Modified: Thu, 20 Jun 2024 18:23:58 GMT  
		Size: 165.7 MB (165682272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dbf354a5789b77cae516778e2d6f5a3db08271208c1eb2aa2674fd5a464e3a`  
		Last Modified: Thu, 20 Jun 2024 19:54:12 GMT  
		Size: 16.9 MB (16897007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9ebc15df292031efcf08dfc0ac565922b532c45e2a3603b13ea0dcd98689f2`  
		Last Modified: Thu, 20 Jun 2024 19:54:11 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1e158e8eb16158f72565ccf1ba088c5728deb0bb8189f22ba01ebd3e509fcb8b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245329167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a0d733e7f9996ea927b41e5b777cd61d590312157770e4fe53d4a8a4c73084`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:45 GMT
COPY dir:23934f7f3a9c4ad2c0f7afe64c708fe8194f94cafce3bfbba33d3cd60b2fc65e in / 
# Thu, 20 Jun 2024 17:39:47 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:27:17 GMT
ARG version=21.0.3.9-1
# Thu, 20 Jun 2024 18:27:36 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 18:27:38 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:27:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 26 Jun 2024 17:23:01 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 26 Jun 2024 17:23:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jun 2024 17:23:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jun 2024 17:23:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jun 2024 17:23:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:23:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 26 Jun 2024 17:23:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 26 Jun 2024 17:23:16 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jun 2024 17:23:17 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jun 2024 17:23:17 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 26 Jun 2024 17:23:17 GMT
USER jetty
# Wed, 26 Jun 2024 17:23:17 GMT
EXPOSE 8080
# Wed, 26 Jun 2024 17:23:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:23:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b964e874adca881e086a1062b2772882d2bcb2401e15ce21606f20d7a58e7de`  
		Last Modified: Thu, 13 Jun 2024 01:57:59 GMT  
		Size: 64.6 MB (64568709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a0ab3ae31a54931e74a64c95205fed2b9ef2e2b72157455064e05fd1fd523`  
		Last Modified: Wed, 26 Jun 2024 16:52:41 GMT  
		Size: 163.7 MB (163740143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8a6c23ba55b357f4572193ff56c4ce21f04f541dcf83ed3469393413e9d935`  
		Last Modified: Wed, 26 Jun 2024 17:29:59 GMT  
		Size: 17.0 MB (17018681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca541807ec2a22a6fa44615875df6bf8a430753195c5a13858ded440373545`  
		Last Modified: Wed, 26 Jun 2024 17:29:58 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
