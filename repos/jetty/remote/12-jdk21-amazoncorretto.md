## `jetty:12-jdk21-amazoncorretto`

```console
$ docker pull jetty@sha256:70caaff54eb2e44f8075315653a3db46fc1c5f158ccb8bd4d0a0726175a9c03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:61c5943cb0f662ed89eb0a22da8654ffcdf5693dbbbe74ca61c61e920a547d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280342140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2e4977dce93e6ab183d08b4ebffa3204f57db03db6703f6e6b8174f102dd15`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:29 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:29 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:29 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 06 May 2026 17:07:57 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:07:57 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:07:57 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:07:57 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:07:57 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:07:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:07:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:07:57 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:07:57 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:07:57 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:07:57 GMT
USER jetty
# Wed, 06 May 2026 17:07:57 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:07:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:07:57 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34427ac8245f2bc54ae2269830d743a78c73c94138af0501660e55c8b91be1ff`  
		Last Modified: Mon, 04 May 2026 20:12:51 GMT  
		Size: 165.7 MB (165695557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8400836c0fee0d4e88b20b7547db90c7dd95843a3cac0986b40996ca6a6025d`  
		Last Modified: Wed, 06 May 2026 17:08:10 GMT  
		Size: 51.8 MB (51784697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf93192fef1ba3f26904feaab3336cffaf70404ebf30f9a401c6414f6dfa7c6`  
		Last Modified: Wed, 06 May 2026 17:08:09 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8df1dd3bad53471a87661782625ed41750f0bd1a4698b8a865c0275bb3382087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f368c196f52a1ce1b93e02f940826be5e2be760b65f7e6accb338bc5174f421`

```dockerfile
```

-	Layers:
	-	`sha256:83d403c88665cf2b47e33f4430edb8b61b1f66e1507375984be53eeced55bd9c`  
		Last Modified: Wed, 06 May 2026 17:08:09 GMT  
		Size: 6.1 MB (6119547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd4931e585cd187b7a6c06f65498698ca7fb69ae762b312b1dd07b4603b4c18`  
		Last Modified: Wed, 06 May 2026 17:08:08 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0fde0ab5b612c6d5bb9f304a8c763ce77cd38f24f32ef05ea59d23cf9fa99b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280571262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe1e99ef881985dd448447de2f2c68341de3127d4b07c0c6308cdd979e8d3d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:07 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:07 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 06 May 2026 17:07:50 GMT
ENV JETTY_VERSION=12.1.9
# Wed, 06 May 2026 17:07:50 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 06 May 2026 17:07:50 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 06 May 2026 17:07:50 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 06 May 2026 17:07:50 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:07:50 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.9/jetty-home-12.1.9.tar.gz
# Wed, 06 May 2026 17:07:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 06 May 2026 17:07:50 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 06 May 2026 17:07:50 GMT
WORKDIR /var/lib/jetty
# Wed, 06 May 2026 17:07:50 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 06 May 2026 17:07:50 GMT
USER jetty
# Wed, 06 May 2026 17:07:50 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 May 2026 17:07:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 May 2026 17:07:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdfcdf3bd2c92c2567fd8412ee72fbd46db7b157b9d64a0f969635bd1431a4a`  
		Last Modified: Mon, 04 May 2026 20:12:31 GMT  
		Size: 163.9 MB (163902837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc15a0f3d31397c35dcf24ced9244e6edab7daebd4dfe3b85ef6d38940c04b5`  
		Last Modified: Wed, 06 May 2026 17:08:04 GMT  
		Size: 51.9 MB (51871018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088be84364467e266433d89d8b4e46aa60bb697067c632fcf6b2dd12af0708a4`  
		Last Modified: Wed, 06 May 2026 17:08:03 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:84ff3559fa2be6f64fc78071ed93104a7d64b982fc9878253ab10ced10bb2ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6135621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b72604d02e655b28230a32b76b7258596c7d6b60e75252b5bdcbad3e42bb2b`

```dockerfile
```

-	Layers:
	-	`sha256:6b5f7f468727208152779228c8275266b035eb384588b9f274222d75ef9dbee0`  
		Last Modified: Wed, 06 May 2026 17:08:03 GMT  
		Size: 6.1 MB (6118176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68faecaf895d4b743e377ad878431a09ab74f77cbf3857c68dc8f13270eee6a0`  
		Last Modified: Wed, 06 May 2026 17:08:02 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
