## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:0d51971a025979feef13f05137052649f6022f9bacce15d202180c20ed891ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c2e853e7de38069502855afac7f19aee2816670e0487f8e4fb1687fce90e19f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255010034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6d4061038e89d12405091d314b4ed791d16ec1506fc910925088f23bcfddb3`
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
# Thu, 20 Jun 2024 19:21:11 GMT
ENV JETTY_VERSION=12.0.9
# Thu, 20 Jun 2024 19:21:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Jun 2024 19:21:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Thu, 20 Jun 2024 19:21:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Jun 2024 19:26:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Jun 2024 19:26:15 GMT
WORKDIR /var/lib/jetty
# Thu, 20 Jun 2024 19:26:16 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Thu, 20 Jun 2024 19:26:16 GMT
USER jetty
# Thu, 20 Jun 2024 19:26:16 GMT
EXPOSE 8080
# Thu, 20 Jun 2024 19:26:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:26:16 GMT
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
	-	`sha256:5c2969b613bb6d6fd41be26ee6c76129b6928252a8c14f464ed0f354a43b8ce8`  
		Last Modified: Thu, 20 Jun 2024 19:53:17 GMT  
		Size: 40.2 MB (40217101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b2d9bf24a4669a3af3733275400f9068b4d0528170281c653f5e7f97ad064`  
		Last Modified: Thu, 20 Jun 2024 19:53:14 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ae785bdef4f71e7b70d82b2380a0618eaa64eed6aa5414d810843eb4943d4b06
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255697699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01eade8342e35b3164c640f1cd596b6bca10095198d02759a94f71a2e68b46`
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
# Wed, 26 Jun 2024 17:21:05 GMT
ENV JETTY_VERSION=12.0.9
# Wed, 26 Jun 2024 17:21:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 26 Jun 2024 17:21:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 26 Jun 2024 17:21:05 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 26 Jun 2024 17:21:05 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:21:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.9/jetty-home-12.0.9.tar.gz
# Wed, 26 Jun 2024 17:21:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 26 Jun 2024 17:21:21 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip which && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 26 Jun 2024 17:21:22 GMT
WORKDIR /var/lib/jetty
# Wed, 26 Jun 2024 17:21:22 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 26 Jun 2024 17:21:22 GMT
USER jetty
# Wed, 26 Jun 2024 17:21:22 GMT
EXPOSE 8080
# Wed, 26 Jun 2024 17:21:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:21:22 GMT
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
	-	`sha256:91438e47ae976105b6468b6743cbd070e3bc3cacec383ce35937cb73bf2b2009`  
		Last Modified: Wed, 26 Jun 2024 17:28:38 GMT  
		Size: 40.3 MB (40337350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b3669271997474a4d4fd633aa639aa7a4600a7ce71c2adbd2dc2361ed03b4b`  
		Last Modified: Wed, 26 Jun 2024 17:28:36 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
