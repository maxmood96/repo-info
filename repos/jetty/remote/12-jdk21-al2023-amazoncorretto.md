## `jetty:12-jdk21-al2023-amazoncorretto`

```console
$ docker pull jetty@sha256:c8757a58b22b13cd68f3a123a3f5f169fc6eb6f9db8ff4fbfe7b5bbd2bf5a312
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1e4e80856d8dff956dba2561298a2c79f9dd842a1cfd3e3061ff2c3bef39e316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303865266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb7bcad04e2a4a4bf120adb58800f29e84b074a5f2c7f6a7f05ddec1aa44c1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:31 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:31 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:31 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:31 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Jun 2026 22:06:52 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 09 Jun 2026 22:06:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Jun 2026 22:06:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Jun 2026 22:06:52 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Jun 2026 22:06:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 22:06:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 09 Jun 2026 22:06:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Jun 2026 22:06:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Jun 2026 22:06:52 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Jun 2026 22:06:52 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Jun 2026 22:06:52 GMT
USER jetty
# Tue, 09 Jun 2026 22:06:52 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jun 2026 22:06:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Jun 2026 22:06:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655da4f67bbe8b448c113c5608d6d6a794180419e8ce9d70d44ad817230d8f55`  
		Last Modified: Tue, 09 Jun 2026 21:12:55 GMT  
		Size: 170.4 MB (170445528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad04e736b39c4af34fbae8bde5074c1769889a49903b95598cca0f034ee4ce0`  
		Last Modified: Tue, 09 Jun 2026 22:07:10 GMT  
		Size: 78.8 MB (78846706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d0c27893b263f47f8227b873c3f32e851af583fe3052c604eb1966fdeb8103`  
		Last Modified: Tue, 09 Jun 2026 22:07:08 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:43c53bdd10c750df2cab5a4a6e2d9e1225e5ac2b4b2e5f55eafda8f071b3fc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a448aee94700c68bd0dc19ff14a2b036c2bc2909e7033740e9ab956bf5468`

```dockerfile
```

-	Layers:
	-	`sha256:2e3c9b5be4aa23252f0ae4db7ea4ef67789ff6b362f5ab47ed9c042ca857419f`  
		Last Modified: Tue, 09 Jun 2026 22:07:08 GMT  
		Size: 7.4 MB (7436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab479642310b87406f6086310e6d7119ac4203fb3faf8ba3bb9901a709729e6f`  
		Last Modified: Tue, 09 Jun 2026 22:07:07 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-al2023-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:01ca40d86d73ced6e28aa9ef5cec31ade93d2b4f42b430d112f1f19b22cee91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8f9d6390a8ca796f2547bb357ee767ad582470396f6d0ff56d9893a4e37533`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:22 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:22 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:22 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Jun 2026 22:08:23 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 09 Jun 2026 22:08:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 09 Jun 2026 22:08:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 09 Jun 2026 22:08:23 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 09 Jun 2026 22:08:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 22:08:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 09 Jun 2026 22:08:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 09 Jun 2026 22:08:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 09 Jun 2026 22:08:23 GMT
WORKDIR /var/lib/jetty
# Tue, 09 Jun 2026 22:08:23 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 09 Jun 2026 22:08:23 GMT
USER jetty
# Tue, 09 Jun 2026 22:08:23 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 09 Jun 2026 22:08:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Jun 2026 22:08:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f96f7a22616d3711218ad3f27f42e8bca5f4556f0d0043e7d5d0391c69e25a`  
		Last Modified: Tue, 09 Jun 2026 21:12:45 GMT  
		Size: 168.7 MB (168720857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425e2cf223c744042009aa5ab6abd7d397bb23bb1d49802a978b9bad4244cafe`  
		Last Modified: Tue, 09 Jun 2026 22:08:43 GMT  
		Size: 78.8 MB (78780768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43cc5e007ba66f695c43ae38014424653fde80aff964348c7fa16316c8d2fa3`  
		Last Modified: Tue, 09 Jun 2026 22:08:41 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-al2023-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:3e8ee56cab568d5050b4076f1b811101d195754c49948918e400b8ce403207c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b0fff34e67ce14238983a26b7527a4cfb16202905a049da0230c4a0e12c3f4`

```dockerfile
```

-	Layers:
	-	`sha256:5f40ce7d0309a9bdca05be72dd86738165447cd1137cd814e28178ff960ec7a7`  
		Last Modified: Tue, 09 Jun 2026 22:08:41 GMT  
		Size: 7.4 MB (7435402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b66bfd3f832168ac26fb1a517a6bf0c4d028eae7bfd7fafe09a573ea8919b1`  
		Last Modified: Tue, 09 Jun 2026 22:08:41 GMT  
		Size: 17.5 KB (17532 bytes)  
		MIME: application/vnd.in-toto+json
