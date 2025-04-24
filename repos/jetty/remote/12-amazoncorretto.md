## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:31a7e0da45a1af07aeb0d2306909464f5f99be347c0b9a99c4d464d75499d4d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:092cfd268d2f3a570931986d5bf1eb9552237ae7cb5a0545282ab9bb633a06a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268258907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79bfe2b581c7741ace9735866f380d7d1354eaecd612d65cb0a0789ec665b1d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 04 Apr 2025 01:30:23 GMT
COPY /rootfs/ / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["/bin/bash"]
# Fri, 04 Apr 2025 01:30:23 GMT
ARG version=21.0.7.6-1
# Fri, 04 Apr 2025 01:30:23 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=C.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21cc65f273105f38560a5eb91f93f77cb8ba129a46345ae0845e65aa97147`  
		Last Modified: Thu, 24 Apr 2025 20:08:27 GMT  
		Size: 164.9 MB (164888356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd273a05def45e80432fd7c1e2faf60d563c817bb6f0a1d95d318556fc30e8c`  
		Last Modified: Thu, 24 Apr 2025 21:08:41 GMT  
		Size: 40.6 MB (40607137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f13c37a59c066b14475989a167c52f1cfff08aec109e929aeb3e9cb6ddd0022`  
		Last Modified: Thu, 24 Apr 2025 21:08:37 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:84e6f2c0b1aeab18074f75aba12ab580c977df2ad575952d388be78c14231749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6046114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392022379e9d585c831d09e6ff98c9cfaa5df64427b1dffd7fa8e1583e1a36ca`

```dockerfile
```

-	Layers:
	-	`sha256:3d7c7274f936fce78ba94ca0d0b34b717f5002b2b42d2c56ff8aac4bb8727a16`  
		Last Modified: Thu, 24 Apr 2025 21:08:40 GMT  
		Size: 6.0 MB (6027747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016140c542b7c82cf4cc54a2639d68dfac712550041fe176f131b3ec642a5b7`  
		Last Modified: Thu, 24 Apr 2025 21:08:40 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:fb576007b9db49b81c0ff347fc5891a283be7ecc8ae05c304b9151f49ada3e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268125246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6b9d31c113cda0ca607f307ed65b86ee0221bca94f6d5139dfd95ced2f0671`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Fri, 04 Apr 2025 01:30:23 GMT
ARG version=21.0.7.6-1
# Fri, 04 Apr 2025 01:30:23 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
ENV LANG=C.UTF-8
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_VERSION=12.0.19
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Fri, 04 Apr 2025 01:30:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 04 Apr 2025 01:30:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
WORKDIR /var/lib/jetty
# Fri, 04 Apr 2025 01:30:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 04 Apr 2025 01:30:23 GMT
USER jetty
# Fri, 04 Apr 2025 01:30:23 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Apr 2025 01:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Apr 2025 01:30:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801f2d4c03ced6f3dd698c83d22a792997c6774ac7b281f577007cfc68d4b0d9`  
		Last Modified: Wed, 16 Apr 2025 00:15:56 GMT  
		Size: 162.9 MB (162922556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8b71d0d490f8275c8a63ff65a4ffb28c356edf18b07c28fa95318a65069eb9`  
		Last Modified: Wed, 16 Apr 2025 01:16:29 GMT  
		Size: 40.6 MB (40635176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b95e1dd3a5a3e9d0330b98406aeb68236b3f95702ef37ab39fbe76dbdc370b`  
		Last Modified: Wed, 16 Apr 2025 01:16:28 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:bd9f0730cad35d4402bd2cb8d2d1ea1e43867924eae28ffcd92d37e265c85709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8586f7987da2731b27bad2064b6e279b68844836054165fc6980e2fe1c15ebf9`

```dockerfile
```

-	Layers:
	-	`sha256:1107c28c2d8f6b9f9118045217e06170222b437726272cb5fee737eb76bdc553`  
		Last Modified: Wed, 16 Apr 2025 01:16:28 GMT  
		Size: 6.0 MB (6024534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352e179d5b8df95c0169ce5afa2a163d6aaee2b384a75d3e256c91afa8c04cb2`  
		Last Modified: Wed, 16 Apr 2025 01:16:27 GMT  
		Size: 18.5 KB (18497 bytes)  
		MIME: application/vnd.in-toto+json
