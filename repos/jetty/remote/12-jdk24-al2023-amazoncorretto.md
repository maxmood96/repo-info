## `jetty:12-jdk24-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:f6f6d65841ec72ab798648c4e7707e9972023215b2a4d0047bbc2ebfa1191a13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk24-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:8890ae24876d057039ccf8dca28fd634b20f1965c30c56a725518a9719662fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308388596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b46d26aa5395ad8d65a2520c4b611cb765609134bd1b0ff511810c08e83756`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62dbbf3c08e9d1517a47b48f3a2d5a2957390e20d36f17ce3f450b6179adbac`  
		Last Modified: Mon, 19 May 2025 23:46:03 GMT  
		Size: 187.2 MB (187184906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68220bc45aca6fc7f5b0c9f06b47e9e912fd7d80517d75390c3007a20630918`  
		Last Modified: Mon, 19 May 2025 23:47:53 GMT  
		Size: 67.6 MB (67587296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7226936b382e1ca4b5e2e9f8c3c604ecb3c404d31f9b2fdcb932c7734b6d2c50`  
		Last Modified: Mon, 19 May 2025 23:47:31 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk24-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1b245aff8519c93cc36ef6575b1c27ac6adc082ab232ff4423106f4cdc9dc378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7379246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9069da32769f78781313541ad64300e1ecdbf813a2cdf5f53d60d1c3c5686a`

```dockerfile
```

-	Layers:
	-	`sha256:25fe610c4b4c29c2a7b318ce1bdae79ac31c4351bab964016890c3424cea603a`  
		Last Modified: Tue, 20 May 2025 02:17:56 GMT  
		Size: 7.4 MB (7361763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5e2328ddcce7545b48fb17a8a9e3837c01435f6fdc2ae3af0dc224aee0d9f5`  
		Last Modified: Tue, 20 May 2025 02:17:57 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk24-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e246ca2b0331c5805c764b3439c5fdba7453556e025f1bbd2de8ed8c836fd50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305329237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c51f1d307e04963d85448abd87d5df8246546b0a6a0cac45058ad6538c115f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_VERSION=12.0.21
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 14 May 2025 08:21:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.21/jetty-home-12.0.21.tar.gz
# Wed, 14 May 2025 08:21:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 14 May 2025 08:21:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 14 May 2025 08:21:42 GMT
WORKDIR /var/lib/jetty
# Wed, 14 May 2025 08:21:42 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 14 May 2025 08:21:42 GMT
USER jetty
# Wed, 14 May 2025 08:21:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 08:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 May 2025 08:21:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 00:04:05 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81e792802cd42987066116cd3eb580445622bf1742925d5cd8b76e877d674c`  
		Last Modified: Tue, 20 May 2025 00:40:59 GMT  
		Size: 67.5 MB (67528916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e130f2dbb6237cff0f09a0dc56fa62807591c4b624d915805fe4af110507bce`  
		Last Modified: Tue, 20 May 2025 00:40:37 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk24-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:85b47e32a33621410eb4a7e17b865d78d7a025b658a4a7d3e665aaf56c063267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7378282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92097a81bad2063ab5730d986fc28a114fb2f834f4986f65f314df3460c13f3d`

```dockerfile
```

-	Layers:
	-	`sha256:7c9889fa9b6d0274454bc58e378b255b62a1e5da9c9703102255cd9b938eeb41`  
		Last Modified: Tue, 20 May 2025 02:18:01 GMT  
		Size: 7.4 MB (7360707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6531be2ceaf71a611ae894eba92f3831c70b30c90f9c742ae138d758d540d16c`  
		Last Modified: Tue, 20 May 2025 02:18:02 GMT  
		Size: 17.6 KB (17575 bytes)  
		MIME: application/vnd.in-toto+json
