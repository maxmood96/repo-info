## `jetty:12-jdk25-amazoncorretto`

```console
$ docker pull jetty@sha256:513c8cf761c276f3b91d54ef55b240794afdf8092efa6627741eee4be3837863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk25-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:dca673068bb9ae467e401b8782f9a7f5e80af2f06ba047abb6c32af71543872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322315407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77748c0e459a81fc46cf4218ede958a5bdae7e0b5c940ad9f6a443d9d568a9f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:42 GMT
ARG version=25.0.2.10-1
# Mon, 02 Mar 2026 23:15:42 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:42 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:42 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Mar 2026 16:40:44 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:40:44 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:40:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:40:44 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:40:44 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 16:40:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:40:44 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:40:44 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:40:44 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:40:44 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:40:44 GMT
USER jetty
# Tue, 10 Mar 2026 16:40:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:40:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:40:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bde93536aea729dc60831121cc5de0581f15b1e2767f2b7a4b932e58ca2b0d`  
		Last Modified: Mon, 02 Mar 2026 23:16:07 GMT  
		Size: 189.2 MB (189186090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1542acb504708ffce1db246d495ef32d1408ed298f1fb6464a97fe4c0acba42d`  
		Last Modified: Tue, 10 Mar 2026 16:41:05 GMT  
		Size: 79.1 MB (79094601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160be331169a9db2adba833055cdabce4a5479dc0ca6e8d6fb557fc4210abc7d`  
		Last Modified: Tue, 10 Mar 2026 16:40:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:e401533510ca345d0534c4029f310e425efbe872fd2c3e7a98181761ebc7de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca97dc45c27a45652765098d7371341a488a473b72454e69d23293c74bfe2ed5`

```dockerfile
```

-	Layers:
	-	`sha256:49e917102a2f6de007e8a38694665dbdadfc847b65ed276907e065547d227cd6`  
		Last Modified: Tue, 10 Mar 2026 16:41:02 GMT  
		Size: 7.5 MB (7474571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9d3bc8921b3730ffd0606fecf573241f674c4b124b1e05f296808c24f56141`  
		Last Modified: Tue, 10 Mar 2026 16:41:01 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk25-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:ca15110b2b1718b6dce0942cda4a59d49649606013365b15f3b6361e9c1d7b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319068437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464eebca63351362e40917cd2ed21c2570b99713fe26ae5bccad223ff5742d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:32 GMT
ARG version=25.0.2.10-1
# Mon, 02 Mar 2026 23:15:32 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:32 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:32 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Mar 2026 16:40:24 GMT
ENV JETTY_VERSION=12.1.7
# Tue, 10 Mar 2026 16:40:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2026 16:40:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2026 16:40:24 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2026 16:40:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 16:40:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.7/jetty-home-12.1.7.tar.gz
# Tue, 10 Mar 2026 16:40:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 10 Mar 2026 16:40:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 10 Mar 2026 16:40:24 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2026 16:40:24 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 10 Mar 2026 16:40:24 GMT
USER jetty
# Tue, 10 Mar 2026 16:40:24 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Mar 2026 16:40:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 16:40:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67cff3cdc82a1cc3dfd577220fec650c7345cfda2ba30437cb1b29e26e1b2fe`  
		Last Modified: Mon, 02 Mar 2026 23:15:58 GMT  
		Size: 187.1 MB (187088252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a26905136bd0bae0c4cb7e658700fef630f3571b87543de2897d77f478bea52`  
		Last Modified: Tue, 10 Mar 2026 16:40:45 GMT  
		Size: 79.0 MB (79036990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26b8a5eedeacec94106e6519dcb15604ed92121c4b0b12fcd92caa3e682daaa`  
		Last Modified: Tue, 10 Mar 2026 16:40:43 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:1a1a2ce99d12df9f76770f46e076744911e014c38bd9f079838ba36c5074f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62b00f059c15d73aee5ca6702456e034135ec306541747451674f9d8fe568d7`

```dockerfile
```

-	Layers:
	-	`sha256:b9fc7a803b220a2d127c79abe6bdcf9937eebeee3a6f3b569d6cffa9b5c84828`  
		Last Modified: Tue, 10 Mar 2026 16:40:43 GMT  
		Size: 7.5 MB (7473551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40873483230aa9857acf10554ba43e31bab30d5d7156c2790dda88ab89042b24`  
		Last Modified: Tue, 10 Mar 2026 16:40:43 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
