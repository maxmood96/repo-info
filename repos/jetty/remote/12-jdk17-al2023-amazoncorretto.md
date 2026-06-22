## `jetty:12-jdk17-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:8e990f1e68e98ecce9b9493e297ca1168593b309a52ca831231e55890f2b18c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b8aadb3b27960f2efb221fbb29537cd2701a5aea6ecf937226eda911619c016d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290947746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d508963d38dabeca3cfd5a767d68797c09d6a55801e521683d73fe7c72bc7ce9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:06 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:05:06 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:06 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 22 Jun 2026 18:16:52 GMT
ENV JETTY_VERSION=12.1.10
# Mon, 22 Jun 2026 18:16:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 22 Jun 2026 18:16:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 22 Jun 2026 18:16:52 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 22 Jun 2026 18:16:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 18:16:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Mon, 22 Jun 2026 18:16:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 22 Jun 2026 18:16:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 22 Jun 2026 18:16:52 GMT
WORKDIR /var/lib/jetty
# Mon, 22 Jun 2026 18:16:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 22 Jun 2026 18:16:52 GMT
USER jetty
# Mon, 22 Jun 2026 18:16:52 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 18:16:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 18:16:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c983efb3d9caab78dd5f7e804d4131aca7970c4f8c80cdc377a8fc76a1809`  
		Last Modified: Mon, 22 Jun 2026 18:05:28 GMT  
		Size: 157.2 MB (157157640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7bcc68084c517df169ed9d2d6619d56a0c4aca8976aa7b2187c08817db399e`  
		Last Modified: Mon, 22 Jun 2026 18:17:11 GMT  
		Size: 79.2 MB (79214047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90f33ce4c605144d3642598ba44bed238a1a83bb1d655b1c8b35b732abf58a9`  
		Last Modified: Mon, 22 Jun 2026 18:17:09 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:00746e39be09c2a4c09c4ce43ca6a6f8b699a41459d50ffa8537e9bb337aacdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d80a84e3062310678a7eeae35a394c2b68bb31be8abb23288ff6284793f18`

```dockerfile
```

-	Layers:
	-	`sha256:33e4559b458a784649aa9084e1abd22eef4d8b1520a58eca6b8842007f53bcbd`  
		Last Modified: Mon, 22 Jun 2026 18:17:09 GMT  
		Size: 7.4 MB (7439185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8f246f5731a78ff85050932c12e2dbf6b41dedc334fbfbcb487d4bbbf826e2`  
		Last Modified: Mon, 22 Jun 2026 18:17:09 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:92a1a90b70aece5a4f5fba487149a7648013e2c7a3be0bb3c1ead59fb094ada1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288539043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bd177b753e25139da9bc4f0fc64bf2e8f6d669dd253277866fdd0170fbf7f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:43 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:43 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:14:43 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:43 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 22 Jun 2026 18:32:37 GMT
ENV JETTY_VERSION=12.1.10
# Mon, 22 Jun 2026 18:32:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 22 Jun 2026 18:32:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 22 Jun 2026 18:32:37 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 22 Jun 2026 18:32:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 18:32:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Mon, 22 Jun 2026 18:32:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 22 Jun 2026 18:32:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Mon, 22 Jun 2026 18:32:37 GMT
WORKDIR /var/lib/jetty
# Mon, 22 Jun 2026 18:32:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Mon, 22 Jun 2026 18:32:37 GMT
USER jetty
# Mon, 22 Jun 2026 18:32:37 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 18:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 18:32:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e6827a1bd934536bbaca8ee73b82a907a6f504f2a8c7bf2da0903d11d72d4b`  
		Last Modified: Mon, 22 Jun 2026 18:15:06 GMT  
		Size: 156.0 MB (155988813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7026ab447809c565877d2580366b2e3959a315b35d1e4d179143a051833f7c52`  
		Last Modified: Mon, 22 Jun 2026 18:32:58 GMT  
		Size: 79.1 MB (79097668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784e15d983ef168d5b09cba86c7ab5dd93c04629534cdc0b2d8909cb25351b65`  
		Last Modified: Mon, 22 Jun 2026 18:32:55 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:90d7b2422fc79fce4dc8b0fec102cbb636fe4376c87ab5b4fb38e5aec5e77cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb808f28c0620c4390e669a605802414a21d41368998582a94fc95b00783810c`

```dockerfile
```

-	Layers:
	-	`sha256:24d83320bdfc1507357e1843a5d478e5de0c80667dfa07835a194fd2601334c7`  
		Last Modified: Mon, 22 Jun 2026 18:32:56 GMT  
		Size: 7.4 MB (7438116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98920fca7f5194b99d106a67125c51cfe780a12ec03ad4711b5634a26cbca7cf`  
		Last Modified: Mon, 22 Jun 2026 18:32:55 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json
