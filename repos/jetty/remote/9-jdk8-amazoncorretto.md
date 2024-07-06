## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:e9990130c8fe367ca02b3ea3549f1fe632c96d4544d4f643f67bab586167741a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8ab4bc9d20e8e01ef84afc1402a975ef824ad9929a0031acfc5bab1f4ef17cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153975501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a2dffe127f9b8227101a372748a5ea33284e746d6e9191f41fc2d1a940ed27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=1.8.0_412.b08-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:ed49dd100acfe5974f64f71d47c63e45352073ed0cb7a6c0cff1a0efd58a8e18`  
		Last Modified: Fri, 05 Jul 2024 19:56:14 GMT  
		Size: 75.5 MB (75539815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8f8e315a310d449bff13bca02fa17603a677b51f9d0070e91021d1440b8863`  
		Last Modified: Fri, 05 Jul 2024 20:51:54 GMT  
		Size: 15.8 MB (15787382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7975efde23548440cadd06798d32075129f7ebb21e61fe9aa3487177053ff309`  
		Last Modified: Fri, 05 Jul 2024 20:51:54 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:61fddffaef4b30469762cc26f513625dc1083838099129b11d9a3cc3b274cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5727893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232fea8f6591faec3cdf63a9cc8cdd5e41e001c4f2a4d019659db088d0479da2`

```dockerfile
```

-	Layers:
	-	`sha256:e6c872cf0d8dd8b21c37c08066e93ed94c2c119478e5a7b9ff78489b3f0a46bb`  
		Last Modified: Fri, 05 Jul 2024 20:51:54 GMT  
		Size: 5.7 MB (5710743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cf30683e444cc32cbd174ca60d6e5c79f50c3a43af2593650bc162c940473c`  
		Last Modified: Fri, 05 Jul 2024 20:51:54 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c0d832964d26a279ee1415e41bf0fdcac9a7125f44575cd1a1e5bac8f051c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140140299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ca16d0478d68e265bd934f76967d874cb5e2901e3eba3062ffe33deb77bb5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 11 Apr 2024 04:42:46 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 11 Apr 2024 04:42:46 GMT
CMD ["/bin/bash"]
# Thu, 11 Apr 2024 04:42:46 GMT
ARG version=1.8.0_412.b08-1
# Thu, 11 Apr 2024 04:42:46 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Apr 2024 04:42:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Apr 2024 04:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:cada1bd9b04a15210b907122920931347f196d760f887d499c8ee0bec8c67b10`  
		Last Modified: Fri, 05 Jul 2024 19:56:18 GMT  
		Size: 59.7 MB (59650249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632ea086f73c387ab0bdd83d70a33ef27b61ef7c20a0dcbb17f653763586f450`  
		Last Modified: Fri, 05 Jul 2024 20:54:55 GMT  
		Size: 15.9 MB (15919619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d55834a906a617793a37734e31e5baaa7fe04fc93ba4e07e410dfff1bf468e`  
		Last Modified: Fri, 05 Jul 2024 20:54:54 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk8-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:67a4d6c3d4c24105798bc956eb9798b1a4738eba9ef844ba42a964ef218bbeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5707479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c59a7b265b119a7976dd1ef7c2afffe8b11dcb2472227c35a0c61fa8d8a470`

```dockerfile
```

-	Layers:
	-	`sha256:785f19dd850f64e7f5e330178108f44bb75c0d7e419ad907dccfaec5191768d2`  
		Last Modified: Fri, 05 Jul 2024 20:54:55 GMT  
		Size: 5.7 MB (5689933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67033423026d4dae3bf9f98a4f8e6fbc5284dc049521ed3abcf8515c1d19b9e7`  
		Last Modified: Fri, 05 Jul 2024 20:54:54 GMT  
		Size: 17.5 KB (17546 bytes)  
		MIME: application/vnd.in-toto+json
