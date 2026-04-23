## `jetty:12-jdk25-amazoncorretto`

```console
$ docker pull jetty@sha256:cca4c374d582ee493807bf603bf76703a892bb57e7425c9f84e9fae7f833fdf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:90c814a38119af427aa181e8d0246dba04e5fb182f5538f3dde18a3d1b725319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322843187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ee7f67ea9dd495cc17142e9980cb5b7f95f210b013d437c37c81c3835fc2bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:13 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:13 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:13 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 22:13:30 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 22 Apr 2026 22:13:30 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Apr 2026 22:13:30 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Apr 2026 22:13:30 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Apr 2026 22:13:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 22:13:30 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 22 Apr 2026 22:13:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Apr 2026 22:13:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Apr 2026 22:13:30 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Apr 2026 22:13:30 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Apr 2026 22:13:30 GMT
USER jetty
# Wed, 22 Apr 2026 22:13:30 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Apr 2026 22:13:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 22:13:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2591012b75e095c7dcd4fd8cb3a454594c85ade551fce59b2251c4c9be4390a2`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 189.4 MB (189416737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695fb8e290e434fb079e94dd38f6cb30c9ff3f60c5f87b7afff5b8fb0b784d9`  
		Last Modified: Wed, 22 Apr 2026 22:13:48 GMT  
		Size: 78.9 MB (78853319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7f6c7777561c6fc4e09af5f3e59692c3d356c5d00b7943414d663e82674f6`  
		Last Modified: Wed, 22 Apr 2026 22:13:46 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:893158698bfba5346fef4d4720cea336051fee9c028e5c7fa990b42fb0039b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cda029daf8a7a5b1043c06eae84b93ef0e0ba97693dd99b07f70be82f7cc6f`

```dockerfile
```

-	Layers:
	-	`sha256:b9f976fbe942ccd67d4f362fbd385709dac29b81953b8638d98d27b1df3a7954`  
		Last Modified: Wed, 22 Apr 2026 22:13:46 GMT  
		Size: 7.5 MB (7478852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155a43c448227ae19c10e8ccb70c19b35b7d3fd5d480521ebf9469b22636bc2a`  
		Last Modified: Wed, 22 Apr 2026 22:13:46 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:d147e905f20edb7db37017254f836d8bf2ea102c69b2a4bfcf1d5d5848391fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319571422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634d0ea8096ab62b2eb6d9234f8cb677e304417e701f4b4e6ec1e3913f68862f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:22 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:22 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:22 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 22:13:20 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 22 Apr 2026 22:13:20 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 22 Apr 2026 22:13:20 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 22 Apr 2026 22:13:20 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 22 Apr 2026 22:13:20 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 22:13:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 22 Apr 2026 22:13:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 22 Apr 2026 22:13:20 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 22 Apr 2026 22:13:20 GMT
WORKDIR /var/lib/jetty
# Wed, 22 Apr 2026 22:13:20 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 22 Apr 2026 22:13:20 GMT
USER jetty
# Wed, 22 Apr 2026 22:13:20 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 22 Apr 2026 22:13:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 22:13:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f14a6bed93dc6cc05213cc8b33990b3e8252952c2db40348f9406226b36d2`  
		Last Modified: Wed, 22 Apr 2026 21:35:50 GMT  
		Size: 187.3 MB (187333284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14af488f5ff439baeb74a60e8db36587636da0242c437fc7d7d5c4480d7a5466`  
		Last Modified: Wed, 22 Apr 2026 22:13:40 GMT  
		Size: 78.8 MB (78793522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fd9ce57eacd77fe3aca325d50d1cf4b35cf395dc6c8cb09ea0851f51e8eca9`  
		Last Modified: Wed, 22 Apr 2026 22:13:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:19009b8eacab9e2bd266e3af7aab20e705108375a5fc7e831d8549a6222e7352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5203952058d77fc92f0187f6ee026d5e367e446c53dc9566fd8077bdb6fd66`

```dockerfile
```

-	Layers:
	-	`sha256:79f424b64c0901b1d8f3f0a6c2910b832cd838ebdd5be34e1b1079c42986a7f7`  
		Last Modified: Wed, 22 Apr 2026 22:13:38 GMT  
		Size: 7.5 MB (7477833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da73a890facda6bc0ac7b425cb072e44688865076de65ae2e6a4671f1ef3b93`  
		Last Modified: Wed, 22 Apr 2026 22:13:37 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
