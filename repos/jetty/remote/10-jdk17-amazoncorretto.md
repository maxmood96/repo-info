## `jetty:10-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:379efc23cb33fb648a15122586432f60427584d71b42944b18c3f7f9bb5d43fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:10-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:7532b21316f7b66d3125425f86f6660c3853881701f9f998c976d8d27ef250fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232549013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e1b9cdee3b04a3086af233ca9166d3e45e1863cf425b3b1abf6333d33a8876`
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
# Thu, 29 Jan 2026 22:12:43 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 29 Jan 2026 22:12:43 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 29 Jan 2026 22:12:43 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 29 Jan 2026 22:12:43 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 29 Jan 2026 22:12:43 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 22:12:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 29 Jan 2026 22:12:43 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 29 Jan 2026 22:12:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 29 Jan 2026 22:12:43 GMT
WORKDIR /var/lib/jetty
# Thu, 29 Jan 2026 22:12:43 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 29 Jan 2026 22:12:43 GMT
USER jetty
# Thu, 29 Jan 2026 22:12:43 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 29 Jan 2026 22:12:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 22:12:43 GMT
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
	-	`sha256:fa28452732089a211dc2cc391d4855a6bb470a30645e9fffae70edd579466a86`  
		Last Modified: Thu, 29 Jan 2026 22:12:55 GMT  
		Size: 17.1 MB (17122203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb1232bab11e50f375f94c89c398e6771e028a631ce4f0dea2a6eb6f42f6e9`  
		Last Modified: Thu, 29 Jan 2026 22:12:55 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:56086051c1b8f89e95460ac1ad9af2a91441a1f943b2644674d1b7d379bf8e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f49f51a05d27e6994f3737e2b5c6b713e2eea2236cd290a253db7ffc7b6f98a`

```dockerfile
```

-	Layers:
	-	`sha256:1595cdaf78c2a2ecc3e1f15f38d21ffff4e00a750a62fb73f127385996808238`  
		Last Modified: Thu, 29 Jan 2026 22:12:55 GMT  
		Size: 5.9 MB (5928923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8381fbab114a5f0c54a4f3e88d1d8224607b52220e3c4d8aa0f276fecf12ed`  
		Last Modified: Thu, 29 Jan 2026 22:12:55 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:10-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e73888c6610bb2246891780c2d681cfecf1f11ca612459826fae01911a07b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232931193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f94c3151cc4c7f063450b468eeab44cfa7797dfbc75ffbcf770c3f852976399`
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
# Thu, 29 Jan 2026 22:10:40 GMT
ENV JETTY_VERSION=10.0.26
# Thu, 29 Jan 2026 22:10:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 29 Jan 2026 22:10:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 29 Jan 2026 22:10:40 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 29 Jan 2026 22:10:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 22:10:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.26/jetty-home-10.0.26.tar.gz
# Thu, 29 Jan 2026 22:10:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 29 Jan 2026 22:10:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 29 Jan 2026 22:10:40 GMT
WORKDIR /var/lib/jetty
# Thu, 29 Jan 2026 22:10:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 29 Jan 2026 22:10:40 GMT
USER jetty
# Thu, 29 Jan 2026 22:10:40 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 29 Jan 2026 22:10:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 29 Jan 2026 22:10:40 GMT
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
	-	`sha256:fc9bc5ecc29e7f554e23d4cdcf29ff859ad1299ffef2c5559f46ba8d0f836bef`  
		Last Modified: Thu, 29 Jan 2026 22:10:53 GMT  
		Size: 17.2 MB (17150061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656bd16e5efbd178a2ae70e294b1a5cb91a1346733ed6d020f2c918c42f1c85f`  
		Last Modified: Thu, 29 Jan 2026 22:10:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:10-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:31c97878a061ca980af3b2e6d9e7912ccb61c84c02d6ba824c7d40ae3ad2439d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350ea6a9e5df5d125c957fe4128de241966b1b3d18aa3cd99f3942745b31f23c`

```dockerfile
```

-	Layers:
	-	`sha256:29f51ccc9dd6a6f3b75cac496e43d10720dbad513c351d62e789f5f843e1981c`  
		Last Modified: Thu, 29 Jan 2026 22:10:53 GMT  
		Size: 5.9 MB (5927552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc05ad67be79e76f2876722cc56015d22b0f2df5a41a9ebe4999db644da2c4e2`  
		Last Modified: Thu, 29 Jan 2026 22:10:52 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json
