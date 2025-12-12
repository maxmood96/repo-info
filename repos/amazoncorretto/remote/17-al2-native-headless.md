## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:06eeaed3e601f42bf3ade2b80e187e67026ac55a4cfb2e8972722c9263a9f847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d8c6f859e9058a2bb5b324a34171f0f096afe177ffd788497cbf6f8053b7215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150543471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f34968a12a3ac197990ec39ee40f8079f8967351667f77fd82f150a221f31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:47 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:11:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:11:47 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2876b282060baacaefaa33e1ec9e01e1651eaf484b86ccfd7b429e823c286a`  
		Last Modified: Thu, 11 Dec 2025 22:12:27 GMT  
		Size: 87.6 MB (87602496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:332caf204ea39061826b16e1720af2fe283dc4a26705abe1b1ee7fbb33685d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91680da267144691633bdf4075cce7189b094d0188303476d7a1403c5fc10e87`

```dockerfile
```

-	Layers:
	-	`sha256:edd917e8f55bbbe52f4d71a75bc60f164996db7e5d64f9d7e52a830cbe7e72ae`  
		Last Modified: Thu, 11 Dec 2025 22:48:50 GMT  
		Size: 5.6 MB (5631763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a19c2c5f3345bb216049b048f7f3770682c48e0932bfb0a7f596b755ea1b266`  
		Last Modified: Thu, 11 Dec 2025 22:48:51 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:be6daad2888b53f027668e95fa2cd6998fb39b0ab37d489d58d570446feb0e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144623729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624af8813da7e661d18e323a799a7a986e532deec9e4352c6ff43b381d8665c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:16 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:16 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:12:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee95f1028a6b7847b32226b0d7d5d580db0d024acaf73f13441ffb8aaac80d0`  
		Last Modified: Thu, 11 Dec 2025 22:12:49 GMT  
		Size: 79.8 MB (79827974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8030b5674c611985d27253029824ca0e75410a917f790ff805b2404ecc9e8efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0201513dbb40600b82d9fc43954f9422e4b9577522f28c5d451963a55e659`

```dockerfile
```

-	Layers:
	-	`sha256:ee352ff2017651cade3519e7b221d12fa8b21b4d9b6125e83346af1bb8f6abbc`  
		Last Modified: Thu, 11 Dec 2025 22:48:57 GMT  
		Size: 5.4 MB (5448039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36eb4a1657ff0fe8b82adff01da63547183a36175787244d50b7a2f4b1dfbd3d`  
		Last Modified: Thu, 11 Dec 2025 22:48:58 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json
