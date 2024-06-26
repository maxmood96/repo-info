## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:0310b969650afc8f357c882be3ffffe5aeb56b0d51bd716a96f70a90a2a78232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:be5735048681d52a3777441527706f04af9c081c6eac20db9074da9e22210222
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230591911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643b3cb1c91cbe6ba1e11f9cd25c260aa5d32cf9926c0217b757ccfbd33127a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:29 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Thu, 20 Jun 2024 17:20:29 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:47:22 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 17:47:47 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 17:47:47 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:47:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 20 Jun 2024 19:10:22 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Thu, 20 Jun 2024 19:10:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:10:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:10:22 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:10:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:10:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Thu, 20 Jun 2024 19:10:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:15:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:15:25 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:15:25 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:15:25 GMT
USER jetty
# Thu, 20 Jun 2024 19:15:25 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:15:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:15:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122220135d78584f57387e7ed3c95af6a688def4b291d8e18a3e77cb35441cd`  
		Last Modified: Thu, 20 Jun 2024 18:21:17 GMT  
		Size: 152.1 MB (152144847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e932d504ee934c7e14bed4fcee125a4dfb92f08c27a2f8f306e08cf9a69dd4bc`  
		Last Modified: Thu, 20 Jun 2024 19:52:31 GMT  
		Size: 15.8 MB (15798979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0518c725fb19c317d8d5278ece248771f1e5664c853da45c224cc8f1020a3d`  
		Last Modified: Thu, 20 Jun 2024 19:52:30 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c487b67c819ca28e482cb194e7511119750862dfbc0fe3c14a2f23fcf1c2f53d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231279101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fdc552dd62ecaf22167419e773ecdb78059f68fa96a742a14c3bec1d7f3b5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:45 GMT
COPY dir:23934f7f3a9c4ad2c0f7afe64c708fe8194f94cafce3bfbba33d3cd60b2fc65e in / 
# Thu, 20 Jun 2024 17:39:47 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:23:37 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 18:23:57 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Jun 2024 18:23:59 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 26 Jun 2024 17:19:39 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Wed, 26 Jun 2024 17:19:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jun 2024 17:19:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jun 2024 17:19:40 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jun 2024 17:19:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:19:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Wed, 26 Jun 2024 17:19:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 26 Jun 2024 17:19:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jun 2024 17:19:56 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jun 2024 17:19:56 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 26 Jun 2024 17:19:56 GMT
USER jetty
# Wed, 26 Jun 2024 17:19:56 GMT
EXPOSE 8080
# Wed, 26 Jun 2024 17:19:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:19:56 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6b964e874adca881e086a1062b2772882d2bcb2401e15ce21606f20d7a58e7de`  
		Last Modified: Thu, 13 Jun 2024 01:57:59 GMT  
		Size: 64.6 MB (64568709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d7068a47d0ed30b3b3c624262d1d44e1a48c54bfb60a353b15bc654b9d80cf`  
		Last Modified: Wed, 26 Jun 2024 16:49:16 GMT  
		Size: 150.8 MB (150790006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9b194420e58ae81462422c296320120bb1cedd2c54de09574c44ab58c85f15`  
		Last Modified: Wed, 26 Jun 2024 17:27:33 GMT  
		Size: 15.9 MB (15918752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd775c797f9055c8d89efb11cce6bc7c767ffb9dc8abd0fa6a994de3a2baff40`  
		Last Modified: Wed, 26 Jun 2024 17:27:32 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
