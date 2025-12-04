## `jetty:9-amazoncorretto`

```console
$ docker pull jetty@sha256:2f9606a31109b85449167f6b4eae6f3b03ca4f47ce27d52489d1d092301d5d00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:bec74c1144e14e7a71fdf9c08fa2a3657602104083527e59a69447170f4256ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244645531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a7673e732b945201e5c7bf746fc654c291aa6a5f9568cffe932a5922da050e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:21 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:23:21 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:11:59 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 03 Dec 2025 21:11:59 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:11:59 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:11:59 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:11:59 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:11:59 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 03 Dec 2025 21:11:59 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:11:59 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:11:59 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:11:59 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:11:59 GMT
USER jetty
# Wed, 03 Dec 2025 21:11:59 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:11:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:11:59 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb2013f839dc1b3c014b823b3aac80d0e6d67fac06ba1b5ce16eef96069369`  
		Last Modified: Wed, 03 Dec 2025 21:11:38 GMT  
		Size: 165.5 MB (165496684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56369d5889d0c77300a41cf25122a916139f8251222e68d4c0d85a02706312`  
		Last Modified: Wed, 03 Dec 2025 21:12:18 GMT  
		Size: 16.2 MB (16216401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32ade5478c62f7c83278f7e2d48625b8f194fa21f5c4a1c3b3aa88984a555c2`  
		Last Modified: Wed, 03 Dec 2025 21:12:12 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e7c4fce2ce38e6af76af5ffd9d9b2f1d4d69520f4cfcc9ef3e75b03ed8bcd0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5933896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956071e994b64bd0ac92dd20a9fe32315f19d9a496ba078f2033ef3883ec5a0`

```dockerfile
```

-	Layers:
	-	`sha256:5a46803f7621da4e823e722bffb99c6f94a4c3e0888e6945e0c7c83b5e751e6e`  
		Last Modified: Thu, 04 Dec 2025 00:19:36 GMT  
		Size: 5.9 MB (5915547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f697b54167da7248e7439482e9a1a5bf3dff3af3c8b0d243e5d8912665e18e24`  
		Last Modified: Thu, 04 Dec 2025 00:19:37 GMT  
		Size: 18.3 KB (18349 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5056caa11f9ac3a0cc27749f628299ba39a9b1c56dac305f1213bc17d419f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244646150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b023ab477f8ea0f35d8f4c10748624f71063b50c9d4b5b2d622b68aa697e471`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:26 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:26 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:26 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:12:28 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 03 Dec 2025 21:12:28 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 03 Dec 2025 21:12:28 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 03 Dec 2025 21:12:28 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 03 Dec 2025 21:12:28 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 21:12:28 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 03 Dec 2025 21:12:28 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 03 Dec 2025 21:12:28 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 03 Dec 2025 21:12:28 GMT
WORKDIR /var/lib/jetty
# Wed, 03 Dec 2025 21:12:28 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 03 Dec 2025 21:12:28 GMT
USER jetty
# Wed, 03 Dec 2025 21:12:28 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 03 Dec 2025 21:12:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Dec 2025 21:12:28 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba2b3f44053754feffb2ec7cfa45b66127e117d0d28e5607dbc6e1b6044b97`  
		Last Modified: Wed, 03 Dec 2025 21:41:24 GMT  
		Size: 163.6 MB (163582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a6f3f5e86737cd02b746333c3284b15cb24590f99e6136d8d66bc36ef8ad29`  
		Last Modified: Wed, 03 Dec 2025 21:13:01 GMT  
		Size: 16.3 MB (16268592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4f1f7dee0f6071d43d9c40af4995d53adbde2f7c31f3455dc7cbdb35b8a2b`  
		Last Modified: Wed, 03 Dec 2025 21:12:20 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:698369b7e946790f8df627ebd06c0c80df1dc319f29038ecdec41c062da869ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7270824d1e88ad66c1ac8274f9563d76cabdcd83a8cfbd55e5aea5430ddab283`

```dockerfile
```

-	Layers:
	-	`sha256:7c718ccd3171babc7666728e6ab82a574cbed8a29e217e9caca4889b4b328d2c`  
		Last Modified: Thu, 04 Dec 2025 00:19:42 GMT  
		Size: 5.9 MB (5914212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb32185b409625763e29d2d49678c9661221999cfa32a24842fba7da7fd43a7d`  
		Last Modified: Thu, 04 Dec 2025 00:19:43 GMT  
		Size: 18.5 KB (18478 bytes)  
		MIME: application/vnd.in-toto+json
