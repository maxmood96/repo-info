## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:79dd473d2af1a38c6e8eab4b0ce8c053904fc63c6c322c63f0c69a9f8072cd25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:2bf88918ba1e21bf38d9110d5a1d802eec6c36a61b9968822797593217c230d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267264857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f540442e49ba16177148c361ef233069ebe174242690637e261e7222e5d6b181`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:53 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:25:53 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:25:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:25:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 22:19:11 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 22:19:11 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 22:19:11 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 22:19:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 22:19:11 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 22:19:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 22:19:11 GMT
USER jetty
# Wed, 15 Apr 2026 22:19:11 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d44d1181044bb18183f3b8756628e252dfebb612bbd5f528fd1b45de56d3ca2`  
		Last Modified: Wed, 15 Apr 2026 21:26:13 GMT  
		Size: 152.5 MB (152455220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599be072aebc228de13c311f82c1ab05df9418cf2001968fe36aaa955ee496f8`  
		Last Modified: Wed, 15 Apr 2026 22:19:30 GMT  
		Size: 51.9 MB (51852497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d66e4d8902ca757bb0b9d81b2ab2a0f88ff0f8b856343719591c0b95a43618d`  
		Last Modified: Wed, 15 Apr 2026 22:19:29 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ab8505dfab968d64e5811b8348b13df66c137f4db3afc38a4a1867bd19cabe47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6166547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f834bbe70b3bb2320f556459950656413cdf03f92b72580d626366598fae6ff1`

```dockerfile
```

-	Layers:
	-	`sha256:3b368bc1da07bb53dbd42e8ac5efae17f745a8b128e2b4b0fb2d06d821c8ec78`  
		Last Modified: Wed, 15 Apr 2026 22:19:29 GMT  
		Size: 6.1 MB (6149194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930d0117d94e462606797e73678555ab381bac3efcae2c1852107ef79480e3b7`  
		Last Modified: Wed, 15 Apr 2026 22:19:29 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:25325cb8b38505b44d5e69e31c731a2332438fbbb2f46785f91c8aaeaff7a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267664090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200754fd52259f68ca010fdff106a42d7fa50fac3c41f46aaebb0682dfa78fe1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:45 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:38:45 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:38:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:31:31 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 22:31:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 22:31:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 22:31:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 22:31:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:31:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 22:31:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 22:31:31 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 22:31:32 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 22:31:32 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 22:31:32 GMT
USER jetty
# Wed, 15 Apr 2026 22:31:32 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:31:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:31:32 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60529fabbe409bc96b29d5c1281965124bdc6ce7f59780f6fe0ed404356e0094`  
		Last Modified: Wed, 15 Apr 2026 21:39:08 GMT  
		Size: 151.0 MB (150971651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18397ca40b0067babd2e16d935a14a27ad9ec6e115d587420198046ece007bdf`  
		Last Modified: Wed, 15 Apr 2026 22:31:50 GMT  
		Size: 51.9 MB (51887589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dbafd0bf3624a624fd312375c78a592f1d3d94ae262b2846a002398ed9b237`  
		Last Modified: Wed, 15 Apr 2026 22:31:48 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:730751c559eeb52c1f93f709c611d05981c69f7a9369fda4567864c822b29bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6165268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11dead9f0c1119d34d2fbfa0398ac4a612c61ca1ab2e3605a1baa4621b8c382`

```dockerfile
```

-	Layers:
	-	`sha256:d969370ab515a06fa3a98f5591ff6dda2a678c636ea6719115e8d7e97caa43fe`  
		Last Modified: Wed, 15 Apr 2026 22:31:49 GMT  
		Size: 6.1 MB (6147823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9fed59c6adaa753550279b3b822729750f2935d58aa65303305dbe251bfd25`  
		Last Modified: Wed, 15 Apr 2026 22:31:48 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
