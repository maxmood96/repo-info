## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:7b5445e0dca1db0fafc3a44b43875d636d4ff1b14585a85619cc8d60a8e68a84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:31989ed4a675e96c7a99dcaa1855c04b9a2d14681d6581ac3101b178ad8cd4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231511484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae95bba6c159ef9b832c9106ce440131caa69e1816e8a6d0e085c56ca63a6a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:43 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:11:43 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:11:43 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 06 Nov 2025 23:13:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:13:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:13:30 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:13:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:13:30 GMT
USER jetty
# Thu, 06 Nov 2025 23:13:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:13:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:13:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d698af529dfc04b48b4625b22e044bbbbde679eaff562a9eac50396c1bb0c1b7`  
		Last Modified: Thu, 06 Nov 2025 23:13:03 GMT  
		Size: 148.0 MB (148044753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a06d3c838a158bfb8e0f7b1f0a3a63baccb0eb4c96b8d2fc6b1ddf6f975c44`  
		Last Modified: Thu, 06 Nov 2025 23:13:52 GMT  
		Size: 20.5 MB (20530721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67806efa7720f7ffd935e3c37f61501c90b458c2e37e9a44606291136ba39a93`  
		Last Modified: Thu, 06 Nov 2025 23:13:50 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:fdf5011951c6ab9c6fe7a7bd327c5e465814b62702ace6f5b4523dcc8a960be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ba77cc3daed8f2f4277e304d1cc5dbd0fa4bea7cf009fc24221a3305895dd0`

```dockerfile
```

-	Layers:
	-	`sha256:2bed95845b71fa5d4a6209bcc81f84153666e3005e4942093f858c124f561f70`  
		Last Modified: Fri, 07 Nov 2025 00:16:43 GMT  
		Size: 5.9 MB (5936274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6bb768b61e2646100a2b4c5918c6a808e69b6b9294f0bb8d08ce974b2f811c`  
		Last Modified: Fri, 07 Nov 2025 00:16:44 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:b82b0fb4856702f2febb811689183c18f1714ad79c89975a6146c0c245412924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230522083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a71a0748bb549b494c10b23ba288f5ce0df838519bdea2102fde529a1e0334`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:09 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:13:09 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:13:09 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 06 Nov 2025 23:14:19 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 06 Nov 2025 23:14:19 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 06 Nov 2025 23:14:19 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 06 Nov 2025 23:14:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 06 Nov 2025 23:14:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 23:14:19 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 06 Nov 2025 23:14:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 06 Nov 2025 23:14:19 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 06 Nov 2025 23:14:19 GMT
WORKDIR /var/lib/jetty
# Thu, 06 Nov 2025 23:14:19 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 06 Nov 2025 23:14:19 GMT
USER jetty
# Thu, 06 Nov 2025 23:14:19 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 06 Nov 2025 23:14:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 06 Nov 2025 23:14:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b3dbbf9942d831705af842b5b4d8637f885aef547dbffbb26a5f48f413b10f`  
		Last Modified: Thu, 06 Nov 2025 23:11:18 GMT  
		Size: 145.1 MB (145144507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84fe73554c999049926e88ccff8bfac0b96074bf2b1e6a64e2532db27c2389d`  
		Last Modified: Thu, 06 Nov 2025 23:14:37 GMT  
		Size: 20.6 MB (20582403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e05965438f3d3b7d8b8d516ffc9d115a3239acaf3ffed6f4a7176383c0067d8`  
		Last Modified: Thu, 06 Nov 2025 23:14:35 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk11-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c3df6f26b16f8a07afaf1061eb19dac241526888cf68ff095faf5e14c10571e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5481d97ff35f9bd2fdd250b250a49e52fb2e71a48c78345620671db56bc481b6`

```dockerfile
```

-	Layers:
	-	`sha256:acee6212282c726fd1bac9d61e48aa38021a85b74885864af97ee489da0e8324`  
		Last Modified: Fri, 07 Nov 2025 00:16:50 GMT  
		Size: 5.9 MB (5935708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8ba4aed83ef61431c2262e97feaad9fa7a7140621c2b5cb0e68584baecb2b8`  
		Last Modified: Fri, 07 Nov 2025 00:16:51 GMT  
		Size: 17.4 KB (17448 bytes)  
		MIME: application/vnd.in-toto+json
