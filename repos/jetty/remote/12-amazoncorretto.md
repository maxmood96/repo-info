## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:a96da9621c17cb227a145abca0e68e7eea5d98256ecfa044e1551818cd6d4af4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e42388760cb2e05118c7c5621ccb380af8806482578abc8d572f8616ae9ad33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4d3e44d205191f56d9706be8f7dc1427711d3b5a021dd234daaf9994548080`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/bash"]
# Wed, 08 May 2024 22:29:47 GMT
ARG version=21.0.3.9-1
# Wed, 08 May 2024 22:29:47 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 08 May 2024 22:29:47 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2024 22:29:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5468c58a0b4174503bfa5010bd340e5c763a988b59086b50b190a585a4e7f`  
		Last Modified: Fri, 28 Jun 2024 01:26:00 GMT  
		Size: 165.7 MB (165682231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e8c933a2d90ab4fa2adc763ccad4123db26f4131c76b2df4ee69efade2a99`  
		Last Modified: Fri, 28 Jun 2024 20:58:03 GMT  
		Size: 40.2 MB (40216461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bf40f36806d62edafff78b02a1c647841a7f37c3ca29e3045d5ccef50f3689`  
		Last Modified: Fri, 28 Jun 2024 20:57:48 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:9934a12a610fb8ba9519373fe97333a0a55ccfe4fcce3c8000f43abc4f25d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6001137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b91b279e835d14c77eae2bc4b57a5dfb2597f9f4232476d15ad057148d8a27`

```dockerfile
```

-	Layers:
	-	`sha256:7a4d96543a81f9e71ecd270f385fedbc6d97fab8991c7cbb3effe600445c72b1`  
		Last Modified: Fri, 28 Jun 2024 20:58:02 GMT  
		Size: 6.0 MB (5983202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e653f4ba52b008d62eefb04a7b53488a42f8b5d29fcbed6272581189bae8c21`  
		Last Modified: Fri, 28 Jun 2024 20:58:01 GMT  
		Size: 17.9 KB (17935 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d6443516e155a36b3ee0eb062823f3073bd085da641dc0ab382d321880caf64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268646974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508048bccf3efd622c3edf11d99735e4eb7ffa67b9b7969a706c77c62c10bc83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2024 22:29:47 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Wed, 08 May 2024 22:29:47 GMT
CMD ["/bin/bash"]
# Wed, 08 May 2024 22:29:47 GMT
ARG version=21.0.3.9-1
# Wed, 08 May 2024 22:29:47 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 08 May 2024 22:29:47 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2024 22:29:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2024 22:29:47 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 08 May 2024 22:29:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 08 May 2024 22:29:47 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 08 May 2024 22:29:47 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2024 22:29:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 08 May 2024 22:29:47 GMT
USER jetty
# Wed, 08 May 2024 22:29:47 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 08 May 2024 22:29:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2024 22:29:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da42e6374082caa54e1c7189b0ec27bbdc8f3cebce37dd533779f5708b3aa6c6`  
		Last Modified: Fri, 28 Jun 2024 01:31:00 GMT  
		Size: 163.7 MB (163740247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc00d03e5cba3453c2854b86c8902ac39ddb49b93ed16430da89da1cca90aafe`  
		Last Modified: Fri, 28 Jun 2024 21:19:08 GMT  
		Size: 40.3 MB (40336295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9002cede9d611cb57d45980cb60a91121923e40c76ae7fbeb7bebec23945c3`  
		Last Modified: Fri, 28 Jun 2024 21:19:06 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8d9dc98a32aef5204f61d6a617d26eba46276328a6c4d9266870ebc7370bcf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6000130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acf933f94b405221a76ec4658670019278acccae2d596a8fa5c49bf6598aad6`

```dockerfile
```

-	Layers:
	-	`sha256:a196946edfecb0db27fb774e98d59bdc09b72500ed2b4df89de353eb33c15670`  
		Last Modified: Fri, 28 Jun 2024 21:19:06 GMT  
		Size: 6.0 MB (5981865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1dd66670a8a154c3923d631834cbb4e42d9dd536609df16ce9f73950bf0b4e`  
		Last Modified: Fri, 28 Jun 2024 21:19:06 GMT  
		Size: 18.3 KB (18265 bytes)  
		MIME: application/vnd.in-toto+json
