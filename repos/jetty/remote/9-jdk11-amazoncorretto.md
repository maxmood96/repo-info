## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:5ae2a64acfa55218191d9b9b507b8442981f87c3936d2c5aa4dd7b29e56420f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:0715163dd8de5370a20fbca8e679f966334399af2c089f3120477aa531ff302f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226552067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87813c846c92307bc9e5216f7a1e996b83b33512dc3e378234d660b2e6fd06d8`
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
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:14bae2abfeeb4e1770f837d3ef3a42f0a787fa207ee9e48fa96311ca4c28ec2d`  
		Last Modified: Fri, 28 Jun 2024 01:21:21 GMT  
		Size: 148.1 MB (148105351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed933f387b3e6ffcbd2d17d39936a2c25fa7691d310b10c999ce62b13b3f23`  
		Last Modified: Fri, 28 Jun 2024 20:57:49 GMT  
		Size: 15.8 MB (15798413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6eefbe4d4b5fb1d001b0f236c4679249cb33ffbd5004902355f40db21668a2`  
		Last Modified: Fri, 28 Jun 2024 20:57:39 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c15214bb915d32d36599d7431c45a9cf02cca90e2bfb90507931ea5ebc328b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c86ffd6515dbf95fcbc26ba409063be2936075a34914cecd9d9ce53a09bbef`

```dockerfile
```

-	Layers:
	-	`sha256:5ab45cd4f997bb06f07e3f22b0d83088d95681ade380d57bc8c43582255643ae`  
		Last Modified: Fri, 28 Jun 2024 20:57:49 GMT  
		Size: 5.9 MB (5879341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61df07c24bcfb3e80314a25d70bd5bbcf850c40301d50a015d772cc5c1096bcf`  
		Last Modified: Fri, 28 Jun 2024 20:57:49 GMT  
		Size: 17.0 KB (17002 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1020050eaa107a2fe0e0719414aff85cdcf3d93a434dddec5e1214f71a8846c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225710744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4613559a84837e77ebef8d6b7c734b2b76a19d3c0e4a2761ae1366dab5526f`
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
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:54f05d4584bd775d90dfcdf0d33cbd2aa81836d3c79c27528081d4023dcef9e7`  
		Last Modified: Fri, 28 Jun 2024 01:26:57 GMT  
		Size: 145.2 MB (145225222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bdf4a4d7b4dbb8d88a6d5807a7570c5ddca27923716c6c61a9d9dacf45f838`  
		Last Modified: Fri, 28 Jun 2024 21:17:52 GMT  
		Size: 15.9 MB (15915091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6506251f56ada2d2fde2d4017a38f3c622f9d98b4233c9d6cac0ce61804fdc80`  
		Last Modified: Fri, 28 Jun 2024 21:17:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bfcc845a476a741ba6e07658365ca9c500c054edf780cfaaea53f3fb2af89b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cccc93bf240304511042b032634bfc38827a64a14fe85fdb96ebfb3d4e7b2a`

```dockerfile
```

-	Layers:
	-	`sha256:fceb5a1950a7396149a4195c9566c8e10bb3b9bc809e6fe832ebee96d942ee31`  
		Last Modified: Fri, 28 Jun 2024 21:17:51 GMT  
		Size: 5.9 MB (5878774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bb922368a4d53ea62d910568552d7ff17553fd2007027f9ef662657b21cbec`  
		Last Modified: Fri, 28 Jun 2024 21:17:51 GMT  
		Size: 17.3 KB (17298 bytes)  
		MIME: application/vnd.in-toto+json
