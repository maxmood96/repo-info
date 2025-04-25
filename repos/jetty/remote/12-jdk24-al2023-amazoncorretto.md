## `jetty:12-jdk24-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:882447429ac4813893c5cde3859be6089dbb6176c886e827fe0d00cea2b848da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk24-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4999c09dda81601747c3134e9f299cfb8250881377c86db4d9dde1781f923b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308809800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a660906c1be2ff996a344af68619d8394a78b95067c89e116e467dd0994a56fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 08 Apr 2025 03:30:17 GMT
COPY /rootfs/ / # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 03:30:17 GMT
ARG version=24.0.1.9-1
# Tue, 08 Apr 2025 03:30:17 GMT
ARG package_version=1
# Tue, 08 Apr 2025 03:30:17 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
ENV LANG=C.UTF-8
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_VERSION=12.0.19
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 08 Apr 2025 03:30:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
WORKDIR /var/lib/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
USER jetty
# Tue, 08 Apr 2025 03:30:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 03:30:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 08 Apr 2025 03:30:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10cfa39485352291814b023e501abd9f0c906774a3fffe6a1b9140abb2d0441`  
		Last Modified: Thu, 24 Apr 2025 20:08:26 GMT  
		Size: 187.3 MB (187269381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268f0b33043e7b86e6c9fcd7d226b54b47496f14d684606b3c2921df829a5165`  
		Last Modified: Thu, 24 Apr 2025 21:08:47 GMT  
		Size: 65.6 MB (65632206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13853018f2d770e5c7dabb491cf9bd6835f6d4f08ea63a0eaff223bb67638198`  
		Last Modified: Thu, 24 Apr 2025 21:08:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk24-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:664bb20733bc009742764cffa16b0c2a22d0c7ce3133fda3422b456052f3a680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7361789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80416791571668f4c342064d2a120609314dca6cecc64e983e305872711f67ce`

```dockerfile
```

-	Layers:
	-	`sha256:586cda5f9df01d5db4fef37c32dbeb6801d55d69f57183bf664ab1ee1fe9d668`  
		Last Modified: Thu, 24 Apr 2025 21:08:46 GMT  
		Size: 7.3 MB (7344307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bae0c0c1ab4098b735040d94a693899e6c721a00a47d4d5a478ba040332fd2`  
		Last Modified: Thu, 24 Apr 2025 21:08:46 GMT  
		Size: 17.5 KB (17482 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk24-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c71fceedfd4310136ca5f6d3b303980d12b9fb5d4eafff91ac19a15e10564104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305717156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6871c224f9c7b95317011fc29ef9ab84dd7e870c413178d0a819c161c2f5d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 08 Apr 2025 03:30:17 GMT
COPY /rootfs/ / # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 03:30:17 GMT
ARG version=24.0.1.9-1
# Tue, 08 Apr 2025 03:30:17 GMT
ARG package_version=1
# Tue, 08 Apr 2025 03:30:17 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
ENV LANG=C.UTF-8
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_VERSION=12.0.19
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.19/jetty-home-12.0.19.tar.gz
# Tue, 08 Apr 2025 03:30:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 08 Apr 2025 03:30:17 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
WORKDIR /var/lib/jetty
# Tue, 08 Apr 2025 03:30:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 08 Apr 2025 03:30:17 GMT
USER jetty
# Tue, 08 Apr 2025 03:30:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 03:30:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 08 Apr 2025 03:30:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44626409abc16f9f3c646403ae11c6d99108d5707bcf4dcd379a9acfd3e6a53f`  
		Last Modified: Thu, 24 Apr 2025 21:24:50 GMT  
		Size: 185.3 MB (185313383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0604967835cb16a87b1cdc0acf4fb8aed02287114bf94987f26f5774851975`  
		Last Modified: Thu, 24 Apr 2025 23:46:41 GMT  
		Size: 65.4 MB (65440602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfaa5ad9eda126f9c4977b860b89992f3f5ae39b4618867631505a39adc1c3b`  
		Last Modified: Thu, 24 Apr 2025 23:46:39 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk24-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:7268869d7ff10c0a3ede2671f38a04d04fca4fdfc5a7b93bab5a5eb3c9a2d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195c555d47c7f65c94eac66dbba9f3438a31bccc68c47d2de865a079186df211`

```dockerfile
```

-	Layers:
	-	`sha256:16c4ac4825062b635bcc627acc8952518d1fed8d020bf78f31c156ea9efedd69`  
		Last Modified: Thu, 24 Apr 2025 23:46:40 GMT  
		Size: 7.3 MB (7343251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e25c93c9711b06bb058e9f58976669a8de4b05b6bfbd1c9a44f5f2218ed482`  
		Last Modified: Thu, 24 Apr 2025 23:46:39 GMT  
		Size: 17.6 KB (17574 bytes)  
		MIME: application/vnd.in-toto+json
