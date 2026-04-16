## `jetty:12-amazoncorretto`

```console
$ docker pull jetty@sha256:fc2a0655088ee3a5ba1224459438500d57f7bb4373fcdc4d611179ceda7b7d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:fb9daed3304b1077294db53c83116e79dc1fb84964566dcf91affcdc6a59346d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322613267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ef5b0d1ce47d366a621718b0e4975a9a0400ca1644d1931d03c0645f72d8eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:44 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:44 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:44 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:44 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:19:07 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 22:19:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 22:19:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 22:19:07 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 22:19:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:07 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 22:19:07 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 22:19:07 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 22:19:07 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 22:19:07 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 22:19:07 GMT
USER jetty
# Wed, 15 Apr 2026 22:19:07 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:19:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:07 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ea217645c100a6a722630601c1c84cdadb45351d90b7a9d6e48270865321b`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 189.2 MB (189188253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5ba679c673aee89c0457d4b1a4989fc53d905beecdc902dbf65f274c5e3eed`  
		Last Modified: Wed, 15 Apr 2026 22:19:27 GMT  
		Size: 78.9 MB (78851886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a47291c9fc109f3f8b6e72a82d0e002b59f55f75fd633403de54af94c314054`  
		Last Modified: Wed, 15 Apr 2026 22:19:24 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:0e6794aa520d632cd9fb140f44403f48bcf2f39be13d9ec94387b2562590d58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72c6e00a9b6be958121970be661af4911f6ee9d1ad17d291b103999f2b3805`

```dockerfile
```

-	Layers:
	-	`sha256:3068cabcede6c88cb98d784482186c77c00851ec42fd11fcf781614813bcb726`  
		Last Modified: Wed, 15 Apr 2026 22:19:25 GMT  
		Size: 7.5 MB (7478043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa811488040b50dd4fc6237cc31fe87938c764d4ebb8d0859b22c4d550705ee`  
		Last Modified: Wed, 15 Apr 2026 22:19:24 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:439848f5e457c0243ba673bb11c4a629385ed394598072abdeb3ebacc841d0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319327167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88384f762b244a9d9207555fa5cfd23733fd868ef7215d400d161ebd3f13bf68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:50 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:50 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:50 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:50 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:31:40 GMT
ENV JETTY_VERSION=12.1.8
# Wed, 15 Apr 2026 22:31:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Apr 2026 22:31:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Apr 2026 22:31:40 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Apr 2026 22:31:40 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:31:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.8/jetty-home-12.1.8.tar.gz
# Wed, 15 Apr 2026 22:31:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 15 Apr 2026 22:31:40 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	yum install -y shadow-utils tar xz gzip which && yum clean all ; 	command -v dnf && dnf swap -y gnupg2-minimal gnupg2-full && dnf clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 15 Apr 2026 22:31:40 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Apr 2026 22:31:40 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 15 Apr 2026 22:31:40 GMT
USER jetty
# Wed, 15 Apr 2026 22:31:40 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:31:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:31:40 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e5eaff5c173c2d572c7ece0a4ad5d4ba6d11aa38fa3b123836e74ff874e0f`  
		Last Modified: Wed, 15 Apr 2026 21:40:18 GMT  
		Size: 187.1 MB (187089832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdc45e309e26a4b7bd53996cd1191981753deb723e03839d73814eea58f3461`  
		Last Modified: Wed, 15 Apr 2026 22:32:01 GMT  
		Size: 78.8 MB (78792720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f890ecec7a2a7a18b6e0a57d9c6da3a9bd377b8b1c077e525a129dd99204244`  
		Last Modified: Wed, 15 Apr 2026 22:31:58 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c2095ba5bfb38ae558be97352f98fbde73ca9cfc319d916a8266d66983fee12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509fb0e639b06fba9dbfaa7538771c1dfb7fe7518f2b279a026a172f372445f6`

```dockerfile
```

-	Layers:
	-	`sha256:47cf98dc36df49b3fc6478edd578f534b23b05ecf5eaf063ffa8ab5e71951eac`  
		Last Modified: Wed, 15 Apr 2026 22:31:59 GMT  
		Size: 7.5 MB (7477023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e52e398566d7bf2b856555e74756d9dfd59fcf78fee77a9bcfd68428a7d1435`  
		Last Modified: Wed, 15 Apr 2026 22:31:58 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json
