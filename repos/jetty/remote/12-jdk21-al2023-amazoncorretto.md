## `jetty:12-jdk21-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:1481eaa4d1bd45855ea39e7131578f8d8219a92f6ee9295628ea063bdcbe013e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:15f8974c0abb6049b5524d3b9e0793eb5490a807efd7fb54b6f4d62f35b18bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291317185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9787938a0c6635c90bf7148c20b252ef6b8223efb17fbf72d7d2310436fc14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_VERSION=12.0.20
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.20/jetty-home-12.0.20.tar.gz
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 13 May 2025 01:11:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 13 May 2025 01:11:22 GMT
WORKDIR /var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 13 May 2025 01:11:22 GMT
USER jetty
# Tue, 13 May 2025 01:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 01:11:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 May 2025 01:11:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6047cc71e3682d3f7343413908dd8ac01a3ba2f0dfb49200fc496a7bffcf4db`  
		Last Modified: Thu, 01 May 2025 21:08:28 GMT  
		Size: 169.8 MB (169841166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b155c0598a59683c5d3f3eabb5d285da01ae0d19ef5f44c53d1ca7dffff1243`  
		Last Modified: Tue, 13 May 2025 18:25:53 GMT  
		Size: 67.6 MB (67593408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754563828283b430ff7ece64eb69f133c2b8ef87054cd0ee95afcaf779b22d5c`  
		Last Modified: Tue, 13 May 2025 18:25:31 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:f667db306356b1460fc9620d9bde7554c9dd3981242aaaec43664e466a1eacc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e88bf81df159ead19de3b1e13fc781cca9e96f2c90c2d24f1e084b2c456818b`

```dockerfile
```

-	Layers:
	-	`sha256:57d0c9726028c6f3bdde2149daefbf7c6d55687a0b32e3b02972bec0ea98682e`  
		Last Modified: Tue, 13 May 2025 18:25:52 GMT  
		Size: 7.3 MB (7334294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f3cfca14a03f94d8d6557a5f3cc0547a497bfcc44160d8716fef72d522998a`  
		Last Modified: Tue, 13 May 2025 18:25:52 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2611d5dbe06a0281c3e5faac8138a6094fbfb340f512406f6513806c2521565a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288489702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11604bb9c182d3f0449cbf19d057b18dc78cb276c0a697c0f92e8032579124ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_VERSION=12.0.20
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 13 May 2025 01:11:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.20/jetty-home-12.0.20.tar.gz
# Tue, 13 May 2025 01:11:22 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 13 May 2025 01:11:22 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 13 May 2025 01:11:22 GMT
WORKDIR /var/lib/jetty
# Tue, 13 May 2025 01:11:22 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 13 May 2025 01:11:22 GMT
USER jetty
# Tue, 13 May 2025 01:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 01:11:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 May 2025 01:11:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98cb343d84820cd8501d4b93618c2baf868f03a040147c8f52d0cd84e493a65`  
		Last Modified: Thu, 01 May 2025 21:22:57 GMT  
		Size: 168.1 MB (168145956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa043a06479706ff05c3b690e85639175ff5790b57a573088252609e6e6c8dc`  
		Last Modified: Tue, 13 May 2025 18:30:31 GMT  
		Size: 67.5 MB (67531007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2c6d2c1c1f7d25a127542a8be588ca8b744e948de088921803e3b3693ba40a`  
		Last Modified: Tue, 13 May 2025 18:30:28 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:21b52cdd30ab917c7795464046b8f4e34ca321af868bc1cb41cc0222f1abc522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2928e9bb9c35ba53d6bfb45dc578e8254fadd35c25c5e90a0ecdf56ccb4f44d`

```dockerfile
```

-	Layers:
	-	`sha256:8e7b638399c37613f16aba6aad80ffe28ecab1db7f30ec0f0f61f66337c49b86`  
		Last Modified: Tue, 13 May 2025 18:30:29 GMT  
		Size: 7.3 MB (7333227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d053f05223eb237cf8bde7c47f8fc675b81674d5f1d57bd148e08927ffcb1690`  
		Last Modified: Tue, 13 May 2025 18:30:28 GMT  
		Size: 17.6 KB (17575 bytes)  
		MIME: application/vnd.in-toto+json
