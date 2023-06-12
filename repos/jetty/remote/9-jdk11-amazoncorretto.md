## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:a881511253f965a67e8d9c35f9b3226efb4b92b98d194f1aa38f2258be07419c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:dba86bd2b7c48339371a5ea66c8c09150885aea9558082a382d88818630ae220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226105109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b8eabbb2b5cba0fe642f35cb02eaf2a44772b45fa9cefc477a7c1d262ee347`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 12 Jun 2023 19:20:12 GMT
COPY dir:fcef1a58ca6f7120ef8bf5af7158a168707c721bb2ebb75f4483ac8ec6174c3f in / 
# Mon, 12 Jun 2023 19:20:13 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:38:41 GMT
ARG version=11.0.19.7-1
# Mon, 12 Jun 2023 19:39:05 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:39:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 12 Jun 2023 20:47:40 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Mon, 12 Jun 2023 20:47:41 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 12 Jun 2023 20:47:41 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 12 Jun 2023 20:47:41 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 12 Jun 2023 20:47:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 20:47:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Mon, 12 Jun 2023 20:47:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 12 Jun 2023 20:47:59 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 12 Jun 2023 20:47:59 GMT
WORKDIR /var/lib/jetty
# Mon, 12 Jun 2023 20:47:59 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 12 Jun 2023 20:47:59 GMT
USER jetty
# Mon, 12 Jun 2023 20:47:59 GMT
EXPOSE 8080
# Mon, 12 Jun 2023 20:47:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Jun 2023 20:47:59 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8c8d630364ddfad51ca27951f43586450b97e006740d3139ac1c7fc1fa1a48ab`  
		Last Modified: Wed, 07 Jun 2023 18:46:43 GMT  
		Size: 62.5 MB (62493283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480bf58f72b4bbe5678732504474d092d31d21283abd2db6fb6640d698c4b2ab`  
		Last Modified: Mon, 12 Jun 2023 19:44:39 GMT  
		Size: 147.8 MB (147786810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fee1c129cc83d1574ae63cf567b090475ede42222eae651506ca7277a033cfc`  
		Last Modified: Mon, 12 Jun 2023 20:52:16 GMT  
		Size: 15.8 MB (15823403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285dd6bf5cc4a5bbe103f8bab3d224009104c77f162ab59517c2196e98c7e292`  
		Last Modified: Mon, 12 Jun 2023 20:52:14 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:27356f66e6df9d26a5a11711eba495bbda7fd174c1b52147d97f8cef94a5084d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224942676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab08aec55d12d5446c6511b514a94242897d1465b73d5ec0bf9cff56d33fb078`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 12 Jun 2023 19:39:41 GMT
COPY dir:51df2295aa01017be94f36c53673ecd4aa152aa99ad3c20338f5409440ff57f7 in / 
# Mon, 12 Jun 2023 19:39:42 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:56:22 GMT
ARG version=11.0.19.7-1
# Mon, 12 Jun 2023 19:56:43 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:56:45 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:56:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 12 Jun 2023 20:42:09 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Mon, 12 Jun 2023 20:42:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 12 Jun 2023 20:42:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 12 Jun 2023 20:42:09 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 12 Jun 2023 20:42:09 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 20:42:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Mon, 12 Jun 2023 20:42:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 12 Jun 2023 20:42:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 12 Jun 2023 20:42:25 GMT
WORKDIR /var/lib/jetty
# Mon, 12 Jun 2023 20:42:25 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 12 Jun 2023 20:42:25 GMT
USER jetty
# Mon, 12 Jun 2023 20:42:25 GMT
EXPOSE 8080
# Mon, 12 Jun 2023 20:42:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 Jun 2023 20:42:25 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7943399bb3e529e35dfa651db084f8cbc0868d64a866e4cc4c88d2f0043943a8`  
		Last Modified: Wed, 07 Jun 2023 18:37:02 GMT  
		Size: 64.1 MB (64139660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230810294aeb4c5e07869834731892493ac7269c38f064f575c4543fb500e6e`  
		Last Modified: Mon, 12 Jun 2023 20:01:30 GMT  
		Size: 144.9 MB (144941516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5a820c726dd0b89efb6fe52516fb99af4b47d4f5b51a9c40c1632d342b2735`  
		Last Modified: Mon, 12 Jun 2023 20:45:24 GMT  
		Size: 15.9 MB (15859888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59346447ce6f31301635f792cb3c2f12d35c94431b5158ffede8db4237b5f761`  
		Last Modified: Mon, 12 Jun 2023 20:45:23 GMT  
		Size: 1.6 KB (1612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
