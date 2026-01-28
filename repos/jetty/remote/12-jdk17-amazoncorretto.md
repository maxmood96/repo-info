## `jetty:12-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:05c47f8b58a7cfd7e005cd3629751d462cd0fcfb7e97b000e77011b002f79b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6334607493037ccae7163f071dcea825d276a566d3f3a6bff1a57986346fe21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267481770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422e1a639e6b8e51579b83edca67aff436b04623e51ba9e975d4736f0e64ef90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:54 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:07:54 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:07:54 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 04:57:24 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 04:57:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 04:57:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 04:57:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 04:57:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:57:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 04:57:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 04:57:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 04:57:24 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 04:57:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 04:57:24 GMT
USER jetty
# Wed, 28 Jan 2026 04:57:24 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 04:57:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:57:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e97d73ce2dcd3ddf3ca49bd76b8633f971d0ff9f5086086e3467c49d62b5d`  
		Last Modified: Wed, 28 Jan 2026 04:08:15 GMT  
		Size: 152.5 MB (152466718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b8acf0c4e1261b8ff691ff29019ff9b320d7d2ab6e52bdf161e2d93de742d`  
		Last Modified: Wed, 28 Jan 2026 04:57:38 GMT  
		Size: 52.0 MB (52049467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3db5726ea4dca9b8c1df878c9febd1091b912770c6a0037513637f77f0d245`  
		Last Modified: Wed, 28 Jan 2026 04:57:31 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:40d2ee27b664fe92d4db5fdc9f7201f533f8ed0c5a8bd728a04d6e8103888266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6169295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0099fbc4b0df93414b441e6b0818faee0928d482d9e58324ab40a2af271463e4`

```dockerfile
```

-	Layers:
	-	`sha256:a841f17684be817d5176276fce8b76b7b7c05dc96e647f1fcec57042d9acfd1d`  
		Last Modified: Wed, 28 Jan 2026 04:57:37 GMT  
		Size: 6.2 MB (6151943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97db0e67c3d4aee40e3c001ffdb43d05c63e255ba75f6d7d23c6fa359b13f81`  
		Last Modified: Wed, 28 Jan 2026 04:57:36 GMT  
		Size: 17.4 KB (17352 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ad552c41cbaefd349e7700abd8fcbe1937464497d30e01f105b6445f3f56cb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267865207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037c0005a45ab4b2e6f3ca935ea85f3b0eace76c584b026ebd8720b6b391f375`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:09 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:09 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:28:09 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_VERSION=12.1.5
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 05:39:25 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.5/jetty-home-12.1.5.tar.gz
# Wed, 28 Jan 2026 05:39:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 05:39:25 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 05:39:26 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 05:39:26 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 05:39:26 GMT
USER jetty
# Wed, 28 Jan 2026 05:39:26 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 05:39:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 05:39:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4c2e85453456072839dee22d819df60d20ada601be7fd4fd0190527e11fcf`  
		Last Modified: Wed, 28 Jan 2026 04:28:30 GMT  
		Size: 151.0 MB (150977675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d65bd473e77d8f72bd2efa313675aa354a8c07b3da2d00d01820998083e63`  
		Last Modified: Wed, 28 Jan 2026 05:39:40 GMT  
		Size: 52.1 MB (52086766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f9f5f0c2f6e8ed15b1338dea12c6b954a202ee208a670304570753949d3467`  
		Last Modified: Wed, 28 Jan 2026 05:39:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6a404071b050f4d0562a945c8e996fbd7ca149234f2fce6775e34ea1b8246191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d286e4c34703e480af8d5f7e9f6d76efdf4bc637b12649b1967a3331cd520883`

```dockerfile
```

-	Layers:
	-	`sha256:46c715b28f10a1167906a3d819809685926e223207b34b4f8a236ad2744e773c`  
		Last Modified: Wed, 28 Jan 2026 05:39:39 GMT  
		Size: 6.2 MB (6150572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e10b33cad391fa0b8f4720a527c709a3b6b251f2f205a98855835ecb185615`  
		Last Modified: Wed, 28 Jan 2026 05:39:38 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json
