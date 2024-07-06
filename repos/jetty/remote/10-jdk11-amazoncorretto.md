## `jetty:10-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:e1276d14525ff39ccc4c3f831949dca303216648c8fb15f7bc897c0818ff4033
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d18d4f36466ae74bae40df0b6a3116192280bf96b632bdc35a4fe2d924449f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227649920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a5fb14f9edd191751ef8518ecf4d7023dbd1570b5182a2880a0448b8e508e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=11.0.23.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Apr 2024 04:42:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
USER jetty
# Thu, 11 Apr 2024 04:42:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Apr 2024 04:42:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773bb01e826ce1f8c25d9da3686ec45a2167a1ae106e9f7ffed80ba96ecee9c9`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 148.1 MB (148105367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b98ccb3c374259f37929b50e65ee9dd1e8e5ab53a1d9c8f291b897cbfad022`  
		Last Modified: Fri, 05 Jul 2024 20:52:01 GMT  
		Size: 16.9 MB (16896248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24668de818520f9e9760f7bbca4a66d90f5f93b0028dfe5a22aa59b9f25418`  
		Last Modified: Fri, 05 Jul 2024 20:51:51 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2450f2a75eeb70f9775dc9a699a90fb8ce474676c2a8e1cc993a49012f719bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adfd7b3234e48976331bcf5913157f06001f496a8a3ca30c70cda75de209e6d`

```dockerfile
```

-	Layers:
	-	`sha256:c38d0fda95c9b9f336e47bb9fa06c9c94f462796c2abb03fb4bc71181b6f0fd5`  
		Last Modified: Fri, 05 Jul 2024 20:52:01 GMT  
		Size: 5.9 MB (5890661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7980bd1aa9c6d12fe8fa0ab5c6deb4b187bc10d67b755eb3e302ca80e41e37`  
		Last Modified: Fri, 05 Jul 2024 20:52:01 GMT  
		Size: 17.1 KB (17131 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:bfd0b2705d02794c9aa508c429de3603c811f07e60e0c4ae852fc7c090efa3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226810952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2420d4cb7c1f5379db32ec16c1aeaf9189c88fc6554be28bec5a5015a288619c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=11.0.23.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=10.0.20
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 11 Apr 2024 04:42:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
WORKDIR /var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
USER jetty
# Thu, 11 Apr 2024 04:42:46 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 11 Apr 2024 04:42:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3e7292128fc0b4b3aa0b80f12745c354576e9e6d548648d39ecd340991e0b1`  
		Last Modified: Fri, 05 Jul 2024 20:03:32 GMT  
		Size: 145.2 MB (145225632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7552e08c6c3af872223d77de1e7c3489f0bd9314cd38d7064a8ba380e67c9fdc`  
		Last Modified: Fri, 05 Jul 2024 21:08:52 GMT  
		Size: 17.0 MB (17014889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10ee5df88a08e96823661f6524cb1d9f14b245301dc88e74e67ca9167a8862a`  
		Last Modified: Fri, 05 Jul 2024 21:08:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:b75916d88f8134bd599012af95170a56aa6e0ecc011de3425a0087d6a82f48fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a378de2929959865c84360622a8319967dd3a803bcfe0884559bf1cb5a574011`

```dockerfile
```

-	Layers:
	-	`sha256:7e41f4dd0b9d8fdc443e07904500993f1bd506df8b08da42ec59d0c27d8213d9`  
		Last Modified: Fri, 05 Jul 2024 21:08:52 GMT  
		Size: 5.9 MB (5890094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfaede6c538c1e93ab8c8a62ced56ae96076ca8a88351b7d6e91d6752b02cc21`  
		Last Modified: Fri, 05 Jul 2024 21:08:51 GMT  
		Size: 17.5 KB (17528 bytes)  
		MIME: application/vnd.in-toto+json
