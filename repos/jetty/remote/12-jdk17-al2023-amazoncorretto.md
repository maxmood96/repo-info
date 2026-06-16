## `jetty:12-jdk17-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:4a82afceaeeefdff63a0862de48e081ecf0d5edc42ed8f48e5bb1817f7a9893f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:6d5a35eadb65c5ab69a777a3a419f842ebe21618ce5d28537c435292bde463fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290577958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174af78ffc0db67289f78b7417eeed8b2e6ac82597bdd5f722520d227a4fb63f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:28 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:28 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:15:28 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:28 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:21:18 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 16 Jun 2026 02:21:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Jun 2026 02:21:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Jun 2026 02:21:18 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Jun 2026 02:21:18 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 02:21:18 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 16 Jun 2026 02:21:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Jun 2026 02:21:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 16 Jun 2026 02:21:18 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Jun 2026 02:21:18 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 16 Jun 2026 02:21:18 GMT
USER jetty
# Tue, 16 Jun 2026 02:21:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Jun 2026 02:21:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 02:21:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbe16b91281bbab0f677616f852468a1efb463957ba2554f568b2f9ac583b3`  
		Last Modified: Tue, 16 Jun 2026 01:15:51 GMT  
		Size: 157.2 MB (157156724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c7a7731306282f7b07c499bab86ada89d88726256a26a9319c44bde9a1607`  
		Last Modified: Tue, 16 Jun 2026 02:21:37 GMT  
		Size: 78.8 MB (78848202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421d165ffd996ad7da03508a6df929ee599869cd5529cd17a85d15a000ebfdc0`  
		Last Modified: Tue, 16 Jun 2026 02:21:34 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:473acb4c5877b117f71429868b9e8162538a2206379e9a3ffde5f1e06ab770de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c1db4888ffe7559d2c77cc7f0050fda3d90134274b82f7dcce32dbd6ec3e5`

```dockerfile
```

-	Layers:
	-	`sha256:965580248fc67e4048c674f9c65e0d7f8517218dd2da48b8e65ab2fd5fa2b65c`  
		Last Modified: Tue, 16 Jun 2026 02:21:35 GMT  
		Size: 7.4 MB (7434042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d061a26e474b9751d47d9e783c04847b970f4f8ec0b2e48f2a8e553c418aee1`  
		Last Modified: Tue, 16 Jun 2026 02:21:34 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:f28f3f38b7ff3a0edf05f1b8a57ee127d19150da4686f935b09d141efaf04eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288227629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7949b2ae326f91e46efbd7e0f1b510c0de5e933d3227b037cf8f78116c663e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:35 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:35 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:35 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:22:06 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 16 Jun 2026 02:22:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 16 Jun 2026 02:22:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 16 Jun 2026 02:22:06 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 16 Jun 2026 02:22:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 02:22:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 16 Jun 2026 02:22:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 16 Jun 2026 02:22:06 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 16 Jun 2026 02:22:06 GMT
WORKDIR /var/lib/jetty
# Tue, 16 Jun 2026 02:22:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 16 Jun 2026 02:22:06 GMT
USER jetty
# Tue, 16 Jun 2026 02:22:06 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 16 Jun 2026 02:22:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Jun 2026 02:22:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25f04afa63e84df40811c8b1eb43c711fcfea0a157148dfba69328e8dc1769f`  
		Last Modified: Tue, 16 Jun 2026 01:16:57 GMT  
		Size: 156.0 MB (155987128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579d89d234031e4d66e3f1e86553ecbccbfdffe3b0ee7ce9f35149e784daca31`  
		Last Modified: Tue, 16 Jun 2026 02:22:26 GMT  
		Size: 78.8 MB (78780798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04974365a35f126bc76624088a4ecdce129c20aff63aaa38f398e15d9150c197`  
		Last Modified: Tue, 16 Jun 2026 02:22:23 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:ef5c94bcc09665f22da5dbb8fa48ab4cfd93f607207a646b8996330182a8366e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f895b9ef3198754c3ce5a42be65a0bf7daaee969ea60fdcaf3dac35633e5c7`

```dockerfile
```

-	Layers:
	-	`sha256:e0539224a981a8f7271ca40c5d5284cf6827d35fd83026775937ddf11395934c`  
		Last Modified: Tue, 16 Jun 2026 02:22:24 GMT  
		Size: 7.4 MB (7432973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d894a638715ade2e75b25fbc5742b05a8d1e3e6c4c2ed054a307cd6a2418d452`  
		Last Modified: Tue, 16 Jun 2026 02:22:23 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json
