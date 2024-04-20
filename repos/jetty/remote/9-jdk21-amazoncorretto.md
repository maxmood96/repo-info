## `jetty:9-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:864f3a5a41764e8d779d7ec127752eda72b546a18f4364b8dbc21bc5e3e3784e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:bc516cde838ef3b4ff28ab72d2a575dbf649f6be8c83bf4631b0f856ffa4a5db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244158244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20e898a658eb6ad9a25f74021b8d1dfb8c2e65ba952333ef6e6a79d69f216bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:04:08 GMT
ARG version=21.0.3.9-1
# Wed, 17 Apr 2024 00:04:34 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 17 Apr 2024 00:04:35 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:04:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 17 Apr 2024 01:03:43 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Wed, 17 Apr 2024 01:03:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Apr 2024 01:03:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Apr 2024 01:03:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Apr 2024 01:03:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Apr 2024 01:03:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Wed, 17 Apr 2024 01:03:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 17 Apr 2024 01:04:01 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 17 Apr 2024 01:04:01 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Apr 2024 01:04:02 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 17 Apr 2024 01:04:02 GMT
USER jetty
# Wed, 17 Apr 2024 01:04:02 GMT
EXPOSE 8080
# Wed, 17 Apr 2024 01:04:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Apr 2024 01:04:02 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0b3b191aca20792b9feac2b30c67d5206e0594d7306d11eb716b456b3dfdc`  
		Last Modified: Wed, 17 Apr 2024 00:23:36 GMT  
		Size: 165.7 MB (165705336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46fc8707503f60bfc34b55f8b6df34d6c08cd5aeb661a41600df2232f5bed7d0`  
		Last Modified: Wed, 17 Apr 2024 01:15:52 GMT  
		Size: 15.8 MB (15784025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a52190329582d6334fb65ccc9bede3a8128440ac184fbb3d8a79eebfbf30f86`  
		Last Modified: Wed, 17 Apr 2024 01:15:51 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:083acb0d9b183039a6bb082b56f258493506605d6b4a4f15aa9b29c97211a5c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244160891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c7d7b396ec9023c84d0b49502c488affdf59fabef8f1de402c57bf9439ae7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:46 GMT
COPY dir:2ba6ee739dafba609ebdf18f79a61867807b8e6e55204d714d3fea4ab910e739 in / 
# Fri, 19 Apr 2024 22:10:47 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:36:09 GMT
ARG version=21.0.3.9-1
# Fri, 19 Apr 2024 22:36:29 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 22:36:31 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:36:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 19 Apr 2024 23:59:07 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 19 Apr 2024 23:59:08 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 19 Apr 2024 23:59:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 19 Apr 2024 23:59:08 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 19 Apr 2024 23:59:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Apr 2024 23:59:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 19 Apr 2024 23:59:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 19 Apr 2024 23:59:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 19 Apr 2024 23:59:24 GMT
WORKDIR /var/lib/jetty
# Fri, 19 Apr 2024 23:59:24 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 19 Apr 2024 23:59:24 GMT
USER jetty
# Fri, 19 Apr 2024 23:59:24 GMT
EXPOSE 8080
# Fri, 19 Apr 2024 23:59:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Apr 2024 23:59:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:92f601831288d3f8f08bf8bcf02ba1eb90d12a4422c7b431f23ed0e92fc30b2f`  
		Last Modified: Thu, 18 Apr 2024 23:27:04 GMT  
		Size: 64.6 MB (64562444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a033d75f284d4e448fd202676bcc810611980191616634bcbec8b8e6a1eba3f`  
		Last Modified: Fri, 19 Apr 2024 22:46:29 GMT  
		Size: 163.7 MB (163729737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b1f8a841fcbaec3c160e04810a866f10387465e20dd1bff466a154d68ec5c8`  
		Last Modified: Sat, 20 Apr 2024 00:06:03 GMT  
		Size: 15.9 MB (15867077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065cd438a2f90997b31ac8a5cec9aa3206046b5634e8673643182e1225fcd784`  
		Last Modified: Sat, 20 Apr 2024 00:06:01 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
