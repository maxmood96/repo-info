## `jetty:9-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:02a6e5bd45b8c10828168f8cf71dfd74e487e2a88c7f8b18ed9189aacb44a709
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:60dfeeb39e0588ebf2bae362607b1658a6fb2113befa481731439cb808861cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244129888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3ae5d7d68062520f64ed524837b0c3005f7031cd08560d4294019da9606c42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=21.0.3.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
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
	-	`sha256:25d89ce34f31bbf0c736abd2c5850a89a70a63c183300873b63c89b857f2347a`  
		Last Modified: Fri, 05 Jul 2024 19:56:48 GMT  
		Size: 165.7 MB (165682730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c184ea17a2e4ea56874baa08755f5b833c5ddce75f563cee25066c88228ddcb9`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 15.8 MB (15798854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24e5810829bd8e8e9d1ee94e65735c6a8b92aab5a7ac472181fb690c384ba46`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f73b59a4b7d87fdaf818fd493f69288062cb9081234d4af925008adef6a80bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf835b0a6453448b79249afdc6a862a9c51134f40dc07b9d88b4857778665083`

```dockerfile
```

-	Layers:
	-	`sha256:3e654376eb09281799352510bac0b05e77ff675cd4c58cd25d6a260e2d870d0d`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 5.9 MB (5872886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd2a96a6418e6f73182face5bcbf9084f604a13842676a661955b93d4684a20`  
		Last Modified: Fri, 05 Jul 2024 20:51:59 GMT  
		Size: 18.1 KB (18123 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6bd4b10d4343973d16c984034c4373f87d3d5927828838771e00bbfb29053525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244226960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b7b7ea15fd07cf8d478be8613e768df01cba16aa24dc932084d5cb1177cd24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=21.0.3.9-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 11 Apr 2024 04:42:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
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
	-	`sha256:4656569e1791b9a2fca54650735b260b09155d4ae7d843f41c8223a93b62836e`  
		Last Modified: Fri, 05 Jul 2024 20:20:44 GMT  
		Size: 163.7 MB (163739172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38d422ef0da75773230eaa0dba96b83de5eef86d26497481c2bd515aa22da2`  
		Last Modified: Fri, 05 Jul 2024 20:56:10 GMT  
		Size: 15.9 MB (15917357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692002e1450eb0a841ccaf15800eb8291517f992de5df193e114e2b77fcdae45`  
		Last Modified: Fri, 05 Jul 2024 20:56:09 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0b06223e13d5b3e5ef0bdbb3a1259146b1621e06b700c75e966ab94aa514af49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070f73e3d04c348005e6f19bce9a43b6120504fae9875e46d3bf913991855c5b`

```dockerfile
```

-	Layers:
	-	`sha256:e10db6c320504d477aea73ea343537b41ae2748921c4623d4dfbf15ee581ebaf`  
		Last Modified: Fri, 05 Jul 2024 20:56:10 GMT  
		Size: 5.9 MB (5871549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cd1c92c929aafa264fc7342ae663810edea79a705abdd5dbd1494f0a1ae62d`  
		Last Modified: Fri, 05 Jul 2024 20:56:09 GMT  
		Size: 18.6 KB (18556 bytes)  
		MIME: application/vnd.in-toto+json
