## `jetty:12-jdk23-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:643f20ce6849c7e16d8ddb5f016acce7daa927a3b687b0a7a922f33c52049d6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk23-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:74e9c53e7194569d6c1a3957c43a2166e17ef134ca6507d88cb2264e3ea0bcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298056896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1341cd08ee3048241bfe040ab615e67c76c09ee4cf1dbaa88c6fe85b6a4299b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Tue, 14 Jan 2025 20:33:09 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07f8d795ab2586d4cfc2c4556601ad2202c502add5cf1d931a02506ce41c99`  
		Last Modified: Tue, 14 Jan 2025 21:09:25 GMT  
		Size: 177.6 MB (177562039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa66a7fc3e70f8ddcc8095b6d874826af065e7017c5797ee47fd1b9dff9872f`  
		Last Modified: Sat, 11 Jan 2025 03:09:06 GMT  
		Size: 67.3 MB (67342715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb2d267f8290e038deb33e30483a8a33f7957cb8c2f97ba8b46b1f898f8b92`  
		Last Modified: Wed, 15 Jan 2025 09:31:34 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk23-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:5d9ef95463c40e7322eadfca7efaa7eaa09d16dfa2122f6110a1b0cfb367ad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7359435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc48aaf70a7a58e749e3f9052fa8fc1db7e8ebeb727341354d9103b07b5abd2`

```dockerfile
```

-	Layers:
	-	`sha256:349d2fbf2f29798e0329a4ffeebc992c3c68e5b358d75eb27cd7f3873a1741f0`  
		Last Modified: Sat, 11 Jan 2025 03:09:05 GMT  
		Size: 7.3 MB (7341952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95696a0894f2c055ad6df76ac2fdf3cbf1008f361a87b7786b7ddff1a8a901ad`  
		Last Modified: Sat, 11 Jan 2025 03:09:05 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk23-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:394d560ccd957c879b1e8409008e1f5676ced0cdb1d712fe0209e3eaa2b2d0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295196610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191fafc949d1826e08bccc97c6bd0c526ab9c4ff4ed2d03928108729444bd713`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_VERSION=12.0.16
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.16/jetty-home-12.0.16.tar.gz
# Thu, 02 Jan 2025 02:56:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 02 Jan 2025 02:56:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
WORKDIR /var/lib/jetty
# Thu, 02 Jan 2025 02:56:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 02 Jan 2025 02:56:23 GMT
USER jetty
# Thu, 02 Jan 2025 02:56:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 02 Jan 2025 02:56:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Jan 2025 02:56:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Tue, 14 Jan 2025 20:39:04 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd30df951d52363ba9c4e788796c51aafd05b6df3a3ce4b89fe59669e7eb09f8`  
		Last Modified: Sat, 11 Jan 2025 03:12:41 GMT  
		Size: 175.5 MB (175538098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3f5f7b0a94b87e8bce6959ee0083f2a4e173a761002853e1f1e28b90ab2815`  
		Last Modified: Sat, 11 Jan 2025 04:12:55 GMT  
		Size: 67.4 MB (67388652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031ec7de8cb67d4ce9f8dac7eb85b8223619e5c966939f855f400dd16d0cbf5f`  
		Last Modified: Sat, 11 Jan 2025 04:12:53 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk23-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:eaf05fb7c6da5c3611ff26ab51c683586925911f5b5fc6b80ebd1d6571cfddc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7357647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4b2803febe6b0d03097865541a5c295c5f7ae977be6ea2e8aba5809606019a`

```dockerfile
```

-	Layers:
	-	`sha256:a7910ec8b08586d43d85870491ee1b68a8c66c95b772ccd406402ccd1e48e2b0`  
		Last Modified: Sat, 11 Jan 2025 04:12:53 GMT  
		Size: 7.3 MB (7340072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33d05cb355d3c6b4d73f281c838048ee2e574ac3eff9d165d26eb34a5793439f`  
		Last Modified: Sat, 11 Jan 2025 04:12:53 GMT  
		Size: 17.6 KB (17575 bytes)  
		MIME: application/vnd.in-toto+json
