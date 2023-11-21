## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:cac4f02cacc3c2ae7091800c497dba8aa81b51676a0c8a2bada8359012f26719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:fe22dea92156d950c7cb04bcef47705f9b4d6791ec45887a70c42df15ae5354d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253948671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aead0ebadbf5527cb8e665f65a590c8707fb6c54998b4dae6e5dea81b46bef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 21 Nov 2023 03:21:54 GMT
COPY dir:ddf8ce4c235ebf92718d40c0041035b283a61cbd94b49610e57999ebc78d3ec6 in / 
# Tue, 21 Nov 2023 03:21:55 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 04:19:06 GMT
ARG version=17.0.9.8-1
# Tue, 21 Nov 2023 04:19:30 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 21 Nov 2023 04:19:31 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:19:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 21 Nov 2023 05:06:35 GMT
ENV JETTY_VERSION=12.0.3
# Tue, 21 Nov 2023 05:06:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 21 Nov 2023 05:06:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 21 Nov 2023 05:06:35 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 21 Nov 2023 05:06:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 05:06:36 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.3/jetty-home-12.0.3.tar.gz
# Tue, 21 Nov 2023 05:06:36 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 21 Nov 2023 05:06:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 21 Nov 2023 05:06:54 GMT
WORKDIR /var/lib/jetty
# Tue, 21 Nov 2023 05:06:54 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Tue, 21 Nov 2023 05:06:54 GMT
USER jetty
# Tue, 21 Nov 2023 05:06:54 GMT
EXPOSE 8080
# Tue, 21 Nov 2023 05:06:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 05:06:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0b4a6f011995244a95bff79a1298e83d230bc0aa22871a9c510745cafebec227`  
		Last Modified: Sun, 19 Nov 2023 03:18:53 GMT  
		Size: 62.6 MB (62641917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274aefe2866ac25d07f65db25903ae25536d5f231eeb28ddd6df3aaed855857c`  
		Last Modified: Tue, 21 Nov 2023 04:30:06 GMT  
		Size: 151.9 MB (151939996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ee0d3154b4b6da8dfebe8b10a4ccbd2302691ee9bfe55fd7eeb4bf75060081`  
		Last Modified: Tue, 21 Nov 2023 05:12:33 GMT  
		Size: 39.4 MB (39365124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c2e1359a51217d9ffa49d95e6a5a69ad5b4216205dd254a2f6536cdc57e2c`  
		Last Modified: Tue, 21 Nov 2023 05:12:30 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5c0ccc47fb32599dc1aef5d88e82425c25aadbabeb37d0d40a381b478aa233f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254346868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54b81848ea7a57d8e805c484d0707998cb70277650283122cfe1b5b28cdfc70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:00:26 GMT
ARG version=17.0.9.8-1
# Fri, 03 Nov 2023 23:00:49 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 23:00:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:00:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Nov 2023 23:41:02 GMT
ENV JETTY_VERSION=12.0.3
# Fri, 03 Nov 2023 23:41:02 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 03 Nov 2023 23:41:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 03 Nov 2023 23:41:02 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 03 Nov 2023 23:41:02 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Nov 2023 23:41:02 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.3/jetty-home-12.0.3.tar.gz
# Fri, 03 Nov 2023 23:41:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 03 Nov 2023 23:41:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 03 Nov 2023 23:41:18 GMT
WORKDIR /var/lib/jetty
# Fri, 03 Nov 2023 23:41:18 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Fri, 03 Nov 2023 23:41:18 GMT
USER jetty
# Fri, 03 Nov 2023 23:41:19 GMT
EXPOSE 8080
# Fri, 03 Nov 2023 23:41:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 Nov 2023 23:41:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509fd1e1b089d93af373eb5127ffbef3bd59dd121a8e1aeafdff2fd334d34418`  
		Last Modified: Fri, 03 Nov 2023 23:10:36 GMT  
		Size: 150.5 MB (150521753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edadfa78afd86407403d3d8a9c7b20681f1a286b6cc790605e67ba94e05e0430`  
		Last Modified: Fri, 03 Nov 2023 23:45:26 GMT  
		Size: 39.4 MB (39443278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16cc5e089ff86ea276e9adbb4ae997a06935a3bcd8644ea83511cb633644249`  
		Last Modified: Fri, 03 Nov 2023 23:45:24 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
