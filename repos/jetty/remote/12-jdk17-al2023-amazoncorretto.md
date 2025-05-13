## `jetty:12-jdk17-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:91296d5b0d9c194d06292f565dedc53623a18c76c043faa9e701674c0e0b2920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:920e0c5dfdb27fb9e6a4a1159a45404f701113f1b3f6a4d023d2cd68d0b866be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278087906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc2bd398041a6a3f25ad4d7a105861fde177c4da1214dc99727d1bc8a78869e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:f2f5fb1975b49763bbde3c24b87a9619078dcce912cabb05d9a8f5f8b583828e`  
		Last Modified: Thu, 01 May 2025 21:08:28 GMT  
		Size: 156.6 MB (156612852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc006ecbb9be96c9d5a7947faafba94a94a72a4616dc263458fc2cb7269a8f6a`  
		Last Modified: Tue, 13 May 2025 18:25:56 GMT  
		Size: 67.6 MB (67592442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9a8869acf09fb86bddc46ecb2a3011977a19a4a0985174e389be719cbe43ea`  
		Last Modified: Tue, 13 May 2025 18:25:19 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:6fd60bb1659c043ab186de2def544a4b97a896aab8b78a35fe97fdb7d2a3b7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9b1b32d719a8568576055ba9a1c41cd92c9047b16a9153dfe8dc3707c2b3e3`

```dockerfile
```

-	Layers:
	-	`sha256:900c6f0248454e0fcf1df9c424981efe801ababf800efe8e22c14f93ade350b7`  
		Last Modified: Tue, 13 May 2025 18:25:54 GMT  
		Size: 7.3 MB (7331880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f54c57ed3be5cf1286456993edbd952914eb1e46e9214dd880a44b00c6aa7f3`  
		Last Modified: Tue, 13 May 2025 18:25:54 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk17-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c5d4c0d800ab3c4c556ab137f91393a1c2028b6e20bc1384bd23affef074b9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275821638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49dde72865ce5cdff27cf663f14c7b1d684ea746f494ff2ee54c69f24e90214`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:3e65ba1f1abe9ffe6e6a8f95a6824c99278a8d2021bbd4cb4bfd9efe18e2fd94`  
		Last Modified: Thu, 01 May 2025 21:16:55 GMT  
		Size: 155.5 MB (155475961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928c18b54caf6dcf5f97538da8a7a04b3b55679802439dc99537eea311d262f0`  
		Last Modified: Tue, 13 May 2025 18:33:01 GMT  
		Size: 67.5 MB (67532938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d5c4f9ace1b54f0ba1f5301a08905589402e565f4922a61f33b5de0f9314`  
		Last Modified: Tue, 13 May 2025 18:32:58 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:22f0136bf1b4f82eed9161f6a0e43bd5fcafeb4def3e8dd019acc4947b19c99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2c0d30dc8561853147b2f3fef312d50527c13cd77c7ffe11da36fcd4f65015`

```dockerfile
```

-	Layers:
	-	`sha256:fd5db539ed2d8a59c81fd0352ec29955ea7ea8e50420a7812d3bfe2c120373b7`  
		Last Modified: Tue, 13 May 2025 18:32:59 GMT  
		Size: 7.3 MB (7330810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1caa72ef6458a0333dced234e422694d7d16aa245207873972e3752837ca3ab`  
		Last Modified: Tue, 13 May 2025 18:32:58 GMT  
		Size: 17.6 KB (17575 bytes)  
		MIME: application/vnd.in-toto+json
