## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:9f04d690874e3902a8848dd971fd466ede7e2da8f9250d718aadbb3814ddfbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c5a11037e76eff1c1a8d6edbeb8cc77d757a9f63800a5a37ef507decef10fd08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254741663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a714877d10d892c6efaf1ca9ecf5f755ce7aa7914a092ccd9fbe3b4175a552`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:25:44 GMT
ARG version=17.0.10.7-1
# Fri, 05 Apr 2024 19:26:11 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 19:26:11 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:26:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 08 Apr 2024 19:58:16 GMT
ENV JETTY_VERSION=12.0.8
# Mon, 08 Apr 2024 19:58:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Apr 2024 19:58:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Apr 2024 19:58:16 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Apr 2024 19:58:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Apr 2024 19:58:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.8/jetty-home-12.0.8.tar.gz
# Mon, 08 Apr 2024 19:58:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Apr 2024 19:58:35 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 08 Apr 2024 19:58:36 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Apr 2024 19:58:36 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Mon, 08 Apr 2024 19:58:36 GMT
USER jetty
# Mon, 08 Apr 2024 19:58:36 GMT
EXPOSE 8080
# Mon, 08 Apr 2024 19:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Apr 2024 19:58:36 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72ca54c75fd50984d32961a3ed7ca68cfbffb3ea07022ebc3aad34cb5da7742`  
		Last Modified: Fri, 05 Apr 2024 19:39:52 GMT  
		Size: 152.0 MB (151960513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188766752df04c436ed1f736264addc40a927b82204c29c504481c3217328b3d`  
		Last Modified: Mon, 08 Apr 2024 20:07:41 GMT  
		Size: 40.1 MB (40112267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf0177c88151cd01ec31292cbdaafac76f5146a467438832edbb090884f73c8`  
		Last Modified: Mon, 08 Apr 2024 20:07:38 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a21bc5382d091ab36efa34caacc19509fafe84745888d4ce4962c627bfd2b14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255348098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f46a17392ae79944dfd03ce82fa05afafb8ca46d49e86974babf4ae25af4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:47:30 GMT
ARG version=17.0.10.7-1
# Fri, 05 Apr 2024 18:47:51 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 18:47:53 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:47:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 08 Apr 2024 20:09:29 GMT
ENV JETTY_VERSION=12.0.8
# Mon, 08 Apr 2024 20:09:29 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 08 Apr 2024 20:09:29 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 08 Apr 2024 20:09:29 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 08 Apr 2024 20:09:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Apr 2024 20:09:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.8/jetty-home-12.0.8.tar.gz
# Mon, 08 Apr 2024 20:09:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 08 Apr 2024 20:09:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 08 Apr 2024 20:09:46 GMT
WORKDIR /var/lib/jetty
# Mon, 08 Apr 2024 20:09:46 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Mon, 08 Apr 2024 20:09:46 GMT
USER jetty
# Mon, 08 Apr 2024 20:09:46 GMT
EXPOSE 8080
# Mon, 08 Apr 2024 20:09:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Apr 2024 20:09:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c5a38cf733c789b5a6260fff0d81dedc82aa35425ac61c276c1665f3f7cac`  
		Last Modified: Fri, 05 Apr 2024 18:58:50 GMT  
		Size: 150.6 MB (150572609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c465d5251a0be59a6b028e2392b9d2141b58ce0058ab4de8fe95e3b04a7978b3`  
		Last Modified: Mon, 08 Apr 2024 20:15:25 GMT  
		Size: 40.2 MB (40213247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0de7d213b1bd4762585a60a41d9a1ffa223e057ccf2372bb43b4a1b5db1b4`  
		Last Modified: Mon, 08 Apr 2024 20:15:22 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
