## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:aef1cb99744d99017ce18ee48e1e60bcc1ba007059ca7361fbf88ba6a1da6142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1343e437affa7b656e08b12de4c90c700ace4087c710ae22960de57cbd831af8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231720669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014e2793c20f89194e10ee2a6e8cda823ec2868329a11d822bfb8433014e95b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 05 Apr 2024 18:22:03 GMT
COPY dir:9acefc3d435d9504bd7fba575b2c4ee96a407449bf3ba0c2338d49d9a97b2a5a in / 
# Fri, 05 Apr 2024 18:22:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 23:59:36 GMT
ARG version=17.0.11.9-1
# Wed, 17 Apr 2024 00:00:01 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 17 Apr 2024 00:00:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:00:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 17 Apr 2024 01:09:31 GMT
ENV JETTY_VERSION=10.0.20
# Wed, 17 Apr 2024 01:09:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Apr 2024 01:09:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Apr 2024 01:09:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Apr 2024 01:09:32 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Apr 2024 01:09:32 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Wed, 17 Apr 2024 01:09:32 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 17 Apr 2024 01:09:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 17 Apr 2024 01:09:50 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Apr 2024 01:09:50 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 17 Apr 2024 01:09:50 GMT
USER jetty
# Wed, 17 Apr 2024 01:09:50 GMT
EXPOSE 8080
# Wed, 17 Apr 2024 01:09:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Apr 2024 01:09:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b48a4417297666404bb1459ef5f08938bfff21f2d5adb051db9f61fc54934d30`  
		Last Modified: Wed, 03 Apr 2024 01:52:33 GMT  
		Size: 62.7 MB (62667250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c368038eea2870b5580a7060ec5099ca9fedc1fd0a1c133608a62dab2bcd2d20`  
		Last Modified: Wed, 17 Apr 2024 00:19:11 GMT  
		Size: 152.2 MB (152184438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34171643a3aec35d9a7bdc76a9ec03cf657cff6a81bbfcb9c9877807c067ae01`  
		Last Modified: Wed, 17 Apr 2024 01:19:59 GMT  
		Size: 16.9 MB (16867347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ba7ec6dc4a6cccf196813c50e930bacc9e2602e627e498f037f0d5288dc10`  
		Last Modified: Wed, 17 Apr 2024 01:19:57 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5612066457fedb900110cd664ec2bbcd2b5e28461237f37a9aa1e0aaa2f995b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232310810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f03839b3fd692b4ab5281ab4b6ccf911c30f6b1cc710d7fe94039d25f81fe83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:46 GMT
COPY dir:2ba6ee739dafba609ebdf18f79a61867807b8e6e55204d714d3fea4ab910e739 in / 
# Fri, 19 Apr 2024 22:10:47 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:32:53 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:33:12 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 22:33:14 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:33:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 20 Apr 2024 00:02:29 GMT
ENV JETTY_VERSION=10.0.20
# Sat, 20 Apr 2024 00:02:29 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 20 Apr 2024 00:02:29 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 20 Apr 2024 00:02:29 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 20 Apr 2024 00:02:29 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Apr 2024 00:02:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.20/jetty-home-10.0.20.tar.gz
# Sat, 20 Apr 2024 00:02:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 20 Apr 2024 00:02:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Sat, 20 Apr 2024 00:02:45 GMT
WORKDIR /var/lib/jetty
# Sat, 20 Apr 2024 00:02:45 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Sat, 20 Apr 2024 00:02:45 GMT
USER jetty
# Sat, 20 Apr 2024 00:02:45 GMT
EXPOSE 8080
# Sat, 20 Apr 2024 00:02:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 20 Apr 2024 00:02:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:92f601831288d3f8f08bf8bcf02ba1eb90d12a4422c7b431f23ed0e92fc30b2f`  
		Last Modified: Thu, 18 Apr 2024 23:27:04 GMT  
		Size: 64.6 MB (64562444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831e7df34ecda740f9c245355a46199ef9bc38f34b5db0ae28ab0d4567376b5`  
		Last Modified: Fri, 19 Apr 2024 22:44:06 GMT  
		Size: 150.8 MB (150780226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419c4c7ae9c85a123127b281d07eda6ba56148a64def351adcda1bc42a30dca`  
		Last Modified: Sat, 20 Apr 2024 00:08:24 GMT  
		Size: 17.0 MB (16966508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b3fc3abac229982f1b63e6845c66bacf4e22bb7fbb9803610a5ea544dae444`  
		Last Modified: Sat, 20 Apr 2024 00:08:23 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
