## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:91f85313dc566cfa85a4cb67ae6839062e66ed615b2ccb43c73d2bfeb7db3279
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:455040a570bac4d19cae2ac810bd1ecbb4259a788f47a6564c4ea144ec532d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267481856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b73b272ae33fbae58315c81e077667414c1d0816f93e276703bdcac9818964`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:01 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:13:01 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:13:01 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:13:51 GMT
ENV JETTY_VERSION=12.1.5
# Tue, 27 Jan 2026 23:13:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:13:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:13:51 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:13:51 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:13:51 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Tue, 27 Jan 2026 23:13:51 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:13:51 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:13:51 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:13:51 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:13:51 GMT
USER jetty
# Tue, 27 Jan 2026 23:13:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:13:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:13:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7714698ec291fac5fff300229442feb97cb1eeeb2bb977f35f7e11cef7892537`  
		Last Modified: Tue, 27 Jan 2026 22:13:21 GMT  
		Size: 152.5 MB (152466864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133d285134587f3b139183dd0fe42a5c06dbe7928b82f838d16aa182688437c`  
		Last Modified: Tue, 27 Jan 2026 23:14:04 GMT  
		Size: 52.0 MB (52049406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17c135b86b8ba32f29ad3619d03715873b6509063c99e680f8b5cc046dd56f4`  
		Last Modified: Tue, 27 Jan 2026 23:14:01 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:180d9b6b33c03cd9132f50b4f2166cc9a7a91a3e8eda0c693a9befb162ffdb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf64c2316df5ca8a014af590b477bcc97adc01f2920210758339b6b4c00ae09`

```dockerfile
```

-	Layers:
	-	`sha256:10810d1bfa606f93a61da3ca411e58d9abef449aa919d3487b0e54de926cf06d`  
		Last Modified: Tue, 27 Jan 2026 23:14:03 GMT  
		Size: 6.2 MB (6151943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0ece26dceca163fcac00cbdec25857e9bd96131794c28da80d6e5fad08480b`  
		Last Modified: Tue, 27 Jan 2026 23:14:03 GMT  
		Size: 17.4 KB (17353 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5696cedb0849e326332edd099f606825666ca2ea93c82ac0380dac6c26d6c650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267865080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1058ea05990dd7b6f01b44a5f1af4458f53e6e6258223bc855a70c81d4ba7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:13 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:13 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:13 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:13:17 GMT
ENV JETTY_VERSION=12.1.5
# Tue, 27 Jan 2026 23:13:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:13:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:13:17 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:13:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:13:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Tue, 27 Jan 2026 23:13:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:13:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:13:17 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:13:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:13:17 GMT
USER jetty
# Tue, 27 Jan 2026 23:13:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:13:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:13:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefcca91c46c186fe23ce434b50d9455a9fcceed3632768e2013f9ac8703212e`  
		Last Modified: Tue, 27 Jan 2026 22:12:33 GMT  
		Size: 151.0 MB (150977605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11efdead83a389d626375273271847edc4d8d56994366b2e827639698a9500c`  
		Last Modified: Tue, 27 Jan 2026 23:13:31 GMT  
		Size: 52.1 MB (52086709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e54ef10b2392211c061134634e4dc312a02f94147d69593aedc1b14c147ea41`  
		Last Modified: Tue, 27 Jan 2026 23:13:29 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:55821f97dd0273dba03ef0068018b7f8945fe337e9850db95eea5e46a6a86c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7acc2c5cc4795d36a7d38baa1215bc4ddb577f4e577e59f9e78a24cc40e81e`

```dockerfile
```

-	Layers:
	-	`sha256:3c7f96980c7821b856f9c0de3a35ad0c7d919d8d63ea0eca231aed9d86c85ac1`  
		Last Modified: Tue, 27 Jan 2026 23:13:30 GMT  
		Size: 6.2 MB (6150572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba3a521944d06663de7e22c3aeb82d024606373d14ce6ec9d4825bd4ceb47dc`  
		Last Modified: Tue, 27 Jan 2026 23:13:29 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
