## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:646aa0e2f28a5d4627daa4bb543bc1dd33c9367c4d52de8a27e44248e21ef812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3212c44bf934cd057c405686e22e6e4eefee167f3964f034196b2bd723875b4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234829241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6169d49d78a8b87316bceeb87cd4cf712ce5457e17b5761253f2d463dcc6c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 12 Jun 2023 19:20:12 GMT
COPY dir:fcef1a58ca6f7120ef8bf5af7158a168707c721bb2ebb75f4483ac8ec6174c3f in / 
# Mon, 12 Jun 2023 19:20:13 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:40:17 GMT
ARG version=17.0.7.7-1
# Mon, 12 Jun 2023 19:40:41 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:40:42 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:40:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 12 Jun 2023 20:48:07 GMT
ENV JETTY_VERSION=11.0.15
# Mon, 12 Jun 2023 20:48:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 12 Jun 2023 20:48:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 12 Jun 2023 20:48:07 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 12 Jun 2023 20:48:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 20:48:07 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Mon, 12 Jun 2023 20:48:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 12 Jun 2023 20:48:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 12 Jun 2023 20:48:26 GMT
WORKDIR /var/lib/jetty
# Mon, 12 Jun 2023 20:48:26 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 12 Jun 2023 20:48:26 GMT
USER jetty
# Mon, 12 Jun 2023 20:48:26 GMT
EXPOSE 8080
# Mon, 12 Jun 2023 20:48:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Jun 2023 20:48:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8c8d630364ddfad51ca27951f43586450b97e006740d3139ac1c7fc1fa1a48ab`  
		Last Modified: Wed, 07 Jun 2023 18:46:43 GMT  
		Size: 62.5 MB (62493283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4712d0fb6b42103525d76795bfc6a052a50adb039a6e7de559c47a05e2f36b78`  
		Last Modified: Mon, 12 Jun 2023 19:46:03 GMT  
		Size: 152.0 MB (151973843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ffea23aafab534ded91355ad8ab4505e52d933a2abd7431715c3f4166e38ad`  
		Last Modified: Mon, 12 Jun 2023 20:52:27 GMT  
		Size: 20.4 MB (20360502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eaa736a79dbd92e788b8aef10ae7f14bd284c7752e3d271704c1630f07cbc8`  
		Last Modified: Mon, 12 Jun 2023 20:52:25 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:3fa82f6e2f56217d3c71fc0e62ca01c8b14c542375ad38934f8c885f9d058cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235002100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d031747ef63d33389c51b20dd602b42f3d269978319a8458f1b7ed4a3609cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 12 Jun 2023 19:39:41 GMT
COPY dir:51df2295aa01017be94f36c53673ecd4aa152aa99ad3c20338f5409440ff57f7 in / 
# Mon, 12 Jun 2023 19:39:42 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:57:51 GMT
ARG version=17.0.7.7-1
# Mon, 12 Jun 2023 19:58:10 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:58:11 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 12 Jun 2023 20:42:28 GMT
ENV JETTY_VERSION=11.0.15
# Mon, 12 Jun 2023 20:42:28 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 12 Jun 2023 20:42:28 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 12 Jun 2023 20:42:29 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 12 Jun 2023 20:42:29 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 20:42:29 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Mon, 12 Jun 2023 20:42:29 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 12 Jun 2023 20:42:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 12 Jun 2023 20:42:44 GMT
WORKDIR /var/lib/jetty
# Mon, 12 Jun 2023 20:42:44 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 12 Jun 2023 20:42:44 GMT
USER jetty
# Mon, 12 Jun 2023 20:42:44 GMT
EXPOSE 8080
# Mon, 12 Jun 2023 20:42:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Jun 2023 20:42:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7943399bb3e529e35dfa651db084f8cbc0868d64a866e4cc4c88d2f0043943a8`  
		Last Modified: Wed, 07 Jun 2023 18:37:02 GMT  
		Size: 64.1 MB (64139660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646a9e09ff10513c3f197bdd57ba45acd9d119c8fd2abb9a7fe9c04f690c4dfa`  
		Last Modified: Mon, 12 Jun 2023 20:02:48 GMT  
		Size: 150.5 MB (150474072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1a407b4cab9b9abafe2f0efdc1b91cf97b5e0c6dcca02febcbc7745597113e`  
		Last Modified: Mon, 12 Jun 2023 20:45:35 GMT  
		Size: 20.4 MB (20386756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a199eeb72bf0903f87ff72359dee802b2e5cf4bc32739e62dc23724661dc94d`  
		Last Modified: Mon, 12 Jun 2023 20:45:33 GMT  
		Size: 1.6 KB (1612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
