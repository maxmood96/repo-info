## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:acc3eb760ce927554c8f9b5703b0348dc24d3e5b2ae7a786149fcfd60c01d5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:e1666a5993f07b4801049c0fe6e4de085a4ecb1ac1c53a6a4fcbbe75691505c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235985995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea88fa7fea07c883851106469063b4799546d97540380afce1c5cf9397d78b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:31:57 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:31:57 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:31:57 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:31:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:12:30 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 29 Jan 2026 22:12:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 29 Jan 2026 22:12:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 29 Jan 2026 22:12:30 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 29 Jan 2026 22:12:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 22:12:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 29 Jan 2026 22:12:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 29 Jan 2026 22:12:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 29 Jan 2026 22:12:30 GMT
WORKDIR /var/lib/jetty
# Thu, 29 Jan 2026 22:12:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 29 Jan 2026 22:12:30 GMT
USER jetty
# Thu, 29 Jan 2026 22:12:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 29 Jan 2026 22:12:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 22:12:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8326e4bb78b88f1d188237c6144a0f1f66da758b1b6fc8d8639c42d704a4202`  
		Last Modified: Thu, 29 Jan 2026 21:32:18 GMT  
		Size: 152.5 MB (152461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee62bbb05e0b456dfe07b8d8be6e002d5c0d5aacc5223eca8451e3519dd3c4dc`  
		Last Modified: Thu, 29 Jan 2026 22:12:42 GMT  
		Size: 20.6 MB (20559185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810588a897c9cd71da79f59adbaf739f8bd17c8305d1ec3b1e2423685710cd16`  
		Last Modified: Thu, 29 Jan 2026 22:12:41 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:2acff050b9aff5a8b87d09944ce1ae52e70a5b2de21742c0b3215b07b6176422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04b072234d12bb3e8862f30bdb0b5eda01ba7f525f0b3f0b967576fc7f4fa55`

```dockerfile
```

-	Layers:
	-	`sha256:9f8349c0ca2bf803682ab414803b8b61ddbb8cffa68b3f5875d6832a6b3a3f7b`  
		Last Modified: Thu, 29 Jan 2026 22:12:42 GMT  
		Size: 5.9 MB (5928973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6460c3a8f1925d8e5f437e17e064f2e4ed4b3cc71ca44d4908b9e6cc14c44753`  
		Last Modified: Thu, 29 Jan 2026 22:12:42 GMT  
		Size: 17.4 KB (17357 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d0438b79b98416f7b9d03e4d11e83683f867cd6a1f4c47f633736f070751acc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236371201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43cf92b810f180601e9ccf58808d377287e1bf61da816b4e16aa7eba35020e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 21:33:05 GMT
ARG version=17.0.18.9-1
# Thu, 29 Jan 2026 21:33:05 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 29 Jan 2026 21:33:05 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:33:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 29 Jan 2026 22:11:46 GMT
ENV JETTY_VERSION=11.0.26
# Thu, 29 Jan 2026 22:11:46 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 29 Jan 2026 22:11:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 29 Jan 2026 22:11:46 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 29 Jan 2026 22:11:46 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 22:11:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Thu, 29 Jan 2026 22:11:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 29 Jan 2026 22:11:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 29 Jan 2026 22:11:47 GMT
WORKDIR /var/lib/jetty
# Thu, 29 Jan 2026 22:11:47 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 29 Jan 2026 22:11:47 GMT
USER jetty
# Thu, 29 Jan 2026 22:11:47 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 29 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 22:11:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ee4d8a45ac6dbdf61b0ee55fe6f15b35ac70940c33ec3b405fba90deb89a65`  
		Last Modified: Thu, 29 Jan 2026 21:33:27 GMT  
		Size: 151.0 MB (150980367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0376212816dff59d9040c2951e91bcaaa1d3c820b8ccb3d4f6607f49a5f21d5`  
		Last Modified: Thu, 29 Jan 2026 22:11:57 GMT  
		Size: 20.6 MB (20590069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b560d290b35f251e1da3883153b91afb2d3c1135e8175d10657fdb17c5937d`  
		Last Modified: Thu, 29 Jan 2026 22:11:57 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6f0fcdf3c67fdb2a88e6b1da41d37f0b353639f2ce362a1d8b888b3d1282f27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be190c4892f6aba0f87407f31f48e8a9226ee4e50fecf8b4cfea7b28063687bb`

```dockerfile
```

-	Layers:
	-	`sha256:05ea04a23339c4638eaa9254faeeafc56d22d16f61b2ad82343aedcb384f2f81`  
		Last Modified: Thu, 29 Jan 2026 22:11:57 GMT  
		Size: 5.9 MB (5927602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8a964471ca80c0a52bd8d7732ce0aa729af5db201af36fcf0656feaac683bf`  
		Last Modified: Thu, 29 Jan 2026 22:11:57 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
