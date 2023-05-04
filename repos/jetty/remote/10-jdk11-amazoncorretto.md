## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:46e3090c0e1d1b5af824c327ea402f7c832ce48aba1792ac91c9f1cdfe39f3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:9c2c5cefde0c4b3ce249885614fce83e5f4c0dbbb6da7a67b7d929e5a103debd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227205387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdf8472dfa05e3a67ccdbfab6795424290d220591707c54a1a0388072c5f961`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:39:07 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 19:39:31 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 19:39:31 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:39:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 04 May 2023 20:26:20 GMT
ENV JETTY_VERSION=10.0.15
# Thu, 04 May 2023 20:26:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 04 May 2023 20:26:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 04 May 2023 20:26:21 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 04 May 2023 20:26:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 20:26:21 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Thu, 04 May 2023 20:26:21 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 04 May 2023 20:26:38 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 04 May 2023 20:26:39 GMT
WORKDIR /var/lib/jetty
# Thu, 04 May 2023 20:26:39 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Thu, 04 May 2023 20:26:39 GMT
USER jetty
# Thu, 04 May 2023 20:26:39 GMT
EXPOSE 8080
# Thu, 04 May 2023 20:26:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 May 2023 20:26:39 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba9a7b3f80b34f78a02e3b4893afa6a121c457d71db0cb2fe82057f656d538`  
		Last Modified: Thu, 04 May 2023 19:45:03 GMT  
		Size: 147.8 MB (147808136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a11b58426813885c4be66f2c10dc41cb344da777df9d0963c5c1c5aa0b6c22`  
		Last Modified: Thu, 04 May 2023 20:30:22 GMT  
		Size: 16.9 MB (16883371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86dcdcbfb2fa4d78c96faebb2744fbefda1e38e8356940be9c92391bc7d3ad0`  
		Last Modified: Thu, 04 May 2023 20:30:21 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:abdbb16ae7e8fcace9b498ac68b64f379760d3e1e9fb0333d7951a380bf4d9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225985697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc08ce00a3dacbe074178cfde039123ba7655b92315d8115ffb1b2d27cf67ee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 04 May 2023 20:02:54 GMT
COPY dir:dcba415a4a8d9f29c0f5914e2b9ce92b35bd4109c9cd4a8feba13044e94360bf in / 
# Thu, 04 May 2023 20:02:55 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:16:20 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 21:16:38 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 21:16:40 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 21:16:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 04 May 2023 21:44:59 GMT
ENV JETTY_VERSION=10.0.15
# Thu, 04 May 2023 21:44:59 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 04 May 2023 21:44:59 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 04 May 2023 21:44:59 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 04 May 2023 21:44:59 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 21:44:59 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Thu, 04 May 2023 21:44:59 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 04 May 2023 21:45:14 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 04 May 2023 21:45:14 GMT
WORKDIR /var/lib/jetty
# Thu, 04 May 2023 21:45:14 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Thu, 04 May 2023 21:45:14 GMT
USER jetty
# Thu, 04 May 2023 21:45:14 GMT
EXPOSE 8080
# Thu, 04 May 2023 21:45:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 May 2023 21:45:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7691241ca28307f278612dad94d3164926fb17e58a2302a47349e0d6e001249e`  
		Last Modified: Tue, 25 Apr 2023 06:49:36 GMT  
		Size: 64.1 MB (64130990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9410ea473ac2fdcf5a9f1c5e36b37c7693a3f37b9e2ea71d5e3fdd2bf25b8626`  
		Last Modified: Thu, 04 May 2023 21:21:16 GMT  
		Size: 145.0 MB (144954077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7cb31fdcf939275a49c1ba612ecdbdb3b8ea529569645ee13190e00d00bf5`  
		Last Modified: Thu, 04 May 2023 21:47:52 GMT  
		Size: 16.9 MB (16899081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56455667e9d292041d86190901c61117f97a0058202e174215376d927ca3585`  
		Last Modified: Thu, 04 May 2023 21:47:50 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
