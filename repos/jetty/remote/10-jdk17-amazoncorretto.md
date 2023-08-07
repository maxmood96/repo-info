## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:74d3a7c956abbff235d17d167e21b25120b4f6a2dfd5afa3f6c095dfa7135651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:5b96e08a53bf17f1802c76a40c2ad5296ff3d8cf123a8be262d45b254ac0d2a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231392796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34e1e89338cc9680778b6bcb91f7f09130e5ba5f92693d8f2ee8eb6aa71ef4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:18:57 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:19:22 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:19:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:19:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 26 Jul 2023 20:51:25 GMT
ENV JETTY_VERSION=10.0.15
# Wed, 26 Jul 2023 20:51:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jul 2023 20:51:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jul 2023 20:51:25 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jul 2023 20:51:26 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 20:51:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Wed, 26 Jul 2023 20:51:26 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 26 Jul 2023 20:51:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jul 2023 20:51:43 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jul 2023 20:51:43 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Wed, 26 Jul 2023 20:51:43 GMT
USER jetty
# Wed, 26 Jul 2023 20:51:44 GMT
EXPOSE 8080
# Wed, 26 Jul 2023 20:51:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jul 2023 20:51:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0331663fb7b989f09106c7cd829c15080f14aa2671e6219eaa7c6979548d1e48`  
		Last Modified: Wed, 26 Jul 2023 20:29:30 GMT  
		Size: 152.1 MB (152112347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d167dad343e0249df699c925245e6051f0eb02f29618fbf47a6e4305c4a9c8`  
		Last Modified: Wed, 26 Jul 2023 20:56:11 GMT  
		Size: 16.8 MB (16826916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60a4563e26814e0f9f73a641a9e3f9305c3ba54e51371a1c9b68cf79d12273d`  
		Last Modified: Wed, 26 Jul 2023 20:56:10 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:60f05aced4d3a6e66fa4895a5b55ac2b1fbf04b1338ba47a9576c5114158b502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231663978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6619d87a3f1c3f6ecd4645f55b14581003206a1472b5183238f982023e4e14c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 07 Aug 2023 19:40:56 GMT
COPY dir:95dabd7a234aac70a826a1e3c0eafa3928b0be72717af1dea469f66b7db891d5 in / 
# Mon, 07 Aug 2023 19:40:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:26:46 GMT
ARG version=17.0.8.7-1
# Mon, 07 Aug 2023 20:27:05 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:27:07 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:27:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 07 Aug 2023 21:34:08 GMT
ENV JETTY_VERSION=10.0.15
# Mon, 07 Aug 2023 21:34:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 07 Aug 2023 21:34:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 07 Aug 2023 21:34:09 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 07 Aug 2023 21:34:09 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 21:34:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Mon, 07 Aug 2023 21:34:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 07 Aug 2023 21:34:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 07 Aug 2023 21:34:23 GMT
WORKDIR /var/lib/jetty
# Mon, 07 Aug 2023 21:34:23 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 07 Aug 2023 21:34:23 GMT
USER jetty
# Mon, 07 Aug 2023 21:34:23 GMT
EXPOSE 8080
# Mon, 07 Aug 2023 21:34:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Aug 2023 21:34:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c3b5a1e75067e9d540ad8d844cad5a291a8cce89e1a3ed8e0f362a5736d3030c`  
		Last Modified: Wed, 02 Aug 2023 19:26:38 GMT  
		Size: 64.1 MB (64129548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c69eb4237f8f93689d48b1eb6408a260fd5bab441a8b8116e0f134821135e57`  
		Last Modified: Mon, 07 Aug 2023 20:41:11 GMT  
		Size: 150.7 MB (150657784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527ef05f31ff9f433355e68d5d987bf719b80fca2c5e613bf6996960f007c602`  
		Last Modified: Mon, 07 Aug 2023 21:37:49 GMT  
		Size: 16.9 MB (16875033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf66bed841bcf33c5caef2a34670350b2b1714d500cf715729b299d2089e3fc`  
		Last Modified: Mon, 07 Aug 2023 21:37:48 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
