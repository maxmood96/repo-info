## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:5b866d8214bf80677cef098521ba9fd6f046130311d647573e3ac7db0f78427d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:20ab12e7ab0376668751526a15fce3a15c78d6e5afdf92b1e7293b3fe58aad5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235991663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf14b44b0c7e2e6d30f866b50c3899edfddb496cf9b6652e63f696d547df14`
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
# Tue, 27 Jan 2026 23:14:10 GMT
ENV JETTY_VERSION=11.0.26
# Tue, 27 Jan 2026 23:14:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 27 Jan 2026 23:14:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 27 Jan 2026 23:14:10 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 27 Jan 2026 23:14:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 23:14:10 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Tue, 27 Jan 2026 23:14:10 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 27 Jan 2026 23:14:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 27 Jan 2026 23:14:11 GMT
WORKDIR /var/lib/jetty
# Tue, 27 Jan 2026 23:14:11 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 27 Jan 2026 23:14:11 GMT
USER jetty
# Tue, 27 Jan 2026 23:14:11 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 27 Jan 2026 23:14:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:11 GMT
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
	-	`sha256:eb5f4875a160de6cb5adc89b6e0d2003eb031c4547e7348f6c26361d72bef9e7`  
		Last Modified: Tue, 27 Jan 2026 23:14:22 GMT  
		Size: 20.6 MB (20559213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f0d2442f9593579bc8172789d5105a073fec41f8fee68fed8791bf3d21b187`  
		Last Modified: Tue, 27 Jan 2026 23:14:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:61102c7df42ce8bc95941f9eb600b65e753cdf56e8f02cf40e2c58e2174e672e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860e8979be8d3b1f26b044e7bb82bce5158fd8f5c43dd873fb227614ccdbc329`

```dockerfile
```

-	Layers:
	-	`sha256:1011feb67029e722cb06809cbe7d6319fd7311b3dbd1cdf06189c3173c4a7142`  
		Last Modified: Tue, 27 Jan 2026 23:14:22 GMT  
		Size: 5.9 MB (5928973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c5268798c57e97188b90a72722c0e86139ff89ff2ad1029922ae97c853594e`  
		Last Modified: Tue, 27 Jan 2026 23:14:21 GMT  
		Size: 17.4 KB (17357 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:84093b1d919db399ad69cff5762e14e9d664d32af9b18784e6ae1b80df9c112e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236378516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1547aca0c847dfaecb9bf0895e53e855edc78e66636dd18e88f380e174aed3`
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
# Wed, 28 Jan 2026 05:40:13 GMT
ENV JETTY_VERSION=11.0.26
# Wed, 28 Jan 2026 05:40:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 28 Jan 2026 05:40:13 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 28 Jan 2026 05:40:13 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 28 Jan 2026 05:40:13 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 05:40:13 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.26/jetty-home-11.0.26.tar.gz
# Wed, 28 Jan 2026 05:40:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 28 Jan 2026 05:40:13 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 28 Jan 2026 05:40:13 GMT
WORKDIR /var/lib/jetty
# Wed, 28 Jan 2026 05:40:13 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 28 Jan 2026 05:40:13 GMT
USER jetty
# Wed, 28 Jan 2026 05:40:13 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 28 Jan 2026 05:40:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 05:40:13 GMT
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
	-	`sha256:e8622e876762a3067a17b4e721b7e558e7416b7d8c2c8a93b72d2a3193a6eaa8`  
		Last Modified: Wed, 28 Jan 2026 05:40:25 GMT  
		Size: 20.6 MB (20600075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed75842fb4aa2d0eb3a4d92d7bc0ae6759fb143fbdf16353d19ead9e06cb2c3`  
		Last Modified: Wed, 28 Jan 2026 05:40:17 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:11-jdk17-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ec4ce9c677561479d220d2758f252a3eab6140078293f4e384063d356731e164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722f543d6f6e9cce4d511c09ee00eecde130a3dae150087196fbf82f9a978053`

```dockerfile
```

-	Layers:
	-	`sha256:ddd504ec3d7ba4e898ac6403c339c8d352e983870b0c32ab7cec4f88507258b8`  
		Last Modified: Wed, 28 Jan 2026 05:40:24 GMT  
		Size: 5.9 MB (5927602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4618e83bcb903dd9ce3d23311d42545a93f04c36083a5ec05bbcd504d47b05`  
		Last Modified: Wed, 28 Jan 2026 05:40:24 GMT  
		Size: 17.4 KB (17450 bytes)  
		MIME: application/vnd.in-toto+json
