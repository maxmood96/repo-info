## `jetty:12-jdk21-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:fc2c0ac316c2a5d972e6fa8f0440f96140d3e5cad2d3bbb47bb73a0b4d9be491
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:7043fbf32db3a720ee0d855ed262e8958556ef0b4780ec3faee1304704377250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290295591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3af169b69f7160faa70c34e373c95ced6a4f5a94ebddd59250298689f6ffea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_VERSION=12.0.17
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.17/jetty-home-12.0.17.tar.gz
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 07 Mar 2025 02:59:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
WORKDIR /var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
USER jetty
# Fri, 07 Mar 2025 02:59:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 02:59:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Mar 2025 02:59:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77bd86a83f2072a722dba722ab93530cf7d7a2343793ba4a64a866fe5f8edd`  
		Last Modified: Thu, 13 Mar 2025 22:53:13 GMT  
		Size: 169.8 MB (169767609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b287bbf9beca2c733a9b8f57f000010acf16b571ab2239a123d2ae75bf9cb208`  
		Last Modified: Thu, 13 Mar 2025 23:09:54 GMT  
		Size: 67.4 MB (67399414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26380a20f80b1e28094e8d436193650a3a8a5fcc5a53f26e19823294cb655f1`  
		Last Modified: Thu, 13 Mar 2025 23:09:52 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ac975d15aebadb783edc53377b7824dd16708eed05d9e3df7d9e65ae45848acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc214ea052955d49284b958fce62a6a4099ae6b3b7fa6881a5d69c8dfa37c6d`

```dockerfile
```

-	Layers:
	-	`sha256:fa4803dd187134e95995f7dd9454f6c2e69b53f70f897a2c5f91bff32dc7518d`  
		Last Modified: Thu, 13 Mar 2025 23:09:52 GMT  
		Size: 7.3 MB (7323075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274489ae21b70c75d17fb5bd813ee01734d685f6d8d417ce609b4b16e68fdba8`  
		Last Modified: Thu, 13 Mar 2025 23:09:52 GMT  
		Size: 17.5 KB (17482 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:32eab9060254344025d0951603d99d580c9cb4589446dfd6a63615dc4ac88241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287768147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d4ba9f241e2ce7b4f968a85c061dfc4617b7dceb901cd567386a32cb3ca52d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_VERSION=12.0.17
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.17/jetty-home-12.0.17.tar.gz
# Fri, 07 Mar 2025 02:59:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 07 Mar 2025 02:59:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
WORKDIR /var/lib/jetty
# Fri, 07 Mar 2025 02:59:45 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 07 Mar 2025 02:59:45 GMT
USER jetty
# Fri, 07 Mar 2025 02:59:45 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 07 Mar 2025 02:59:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Mar 2025 02:59:45 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d295914b7779ce95c689cad1e7e96b527a1e5e033a9ef7df7271bfc18128b223`  
		Last Modified: Fri, 14 Mar 2025 00:17:29 GMT  
		Size: 168.1 MB (168075877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68919b840da465e0f44d301a2bb8052236aa60bd57020215a7d32e307aafcaf`  
		Last Modified: Fri, 14 Mar 2025 05:48:43 GMT  
		Size: 67.4 MB (67444602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee69c06dd88e90f86b3903a5761adfa03e7bb5608f57fa1595beb5c8f6848798`  
		Last Modified: Fri, 14 Mar 2025 05:48:40 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e4cc877fcf0111cb59b0f6743003d10a1c50d2e0485b397acb69dbaa45682609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818898b73b72cd847fb07d128aea14575bf0bf64d585b77be08ad66d3615f19`

```dockerfile
```

-	Layers:
	-	`sha256:f28c16616de5cfd040676524efa5f3628ba304a886b2c2b5bfb6902b4c34288b`  
		Last Modified: Fri, 14 Mar 2025 05:48:41 GMT  
		Size: 7.3 MB (7322008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a2635cb628cfb6402c22f88d09b68251299a95130d11a439e0bb33ace199dc`  
		Last Modified: Fri, 14 Mar 2025 05:48:40 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.in-toto+json
