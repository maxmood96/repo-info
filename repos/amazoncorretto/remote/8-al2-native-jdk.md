## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:15c54eec3c12695939df205ac1d4cbab1b1a46d9640ae0f152b393adec6466de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e41f0f595597130e2d9ac8b452212985489b10c96e807f70bd7ed87926c3fca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188317020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec69fee230f7037a9517cd840308207ddbe3b86bc9cc15f68bfc66fdf56062de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:16 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:11:16 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:11:16 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01fd9bdf5fa8571ff869ae5324f8461d1f31474140df337dc18b798223f5e3`  
		Last Modified: Tue, 09 Jun 2026 21:11:40 GMT  
		Size: 125.4 MB (125375070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e80b328018344891de30b2f884997749a4376d774dcde4af93eabe89603449de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fd438797f72b08acd793ac793610b4e7c0a60f330ff872ae17e8c6f2fabf41`

```dockerfile
```

-	Layers:
	-	`sha256:de948c1fec163c2e293aa8e329ed3a692c6ef59e8143b02c63299b31ab2ddf30`  
		Last Modified: Tue, 09 Jun 2026 21:11:38 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cdb13669f82b1eeaed1e1e4da35107d301ad8a458ddf6ee056e7a8285828e5`  
		Last Modified: Tue, 09 Jun 2026 21:11:38 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b8f4a4da79a550389f71bb399ae3a9d4a03d800e94c9ab5848adf8f242689cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132469683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708d7fcfebba48df7d1fc0f6d808019caf3e05ef848052e3d40c26e4d5eae5bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:00 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:11:00 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:11:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cfb789a7eceebcac06a5c786c5d53eac1a9c316c3201eea04fd968275aa6c6`  
		Last Modified: Tue, 09 Jun 2026 21:11:18 GMT  
		Size: 67.7 MB (67678974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72e47dcc4291697a31d368695756be93da85e3453e1f794ab7062cb374daac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fd2b52c63021ab75e5c9d273bb6354ccc0d66405eb8a67f02c2b66935d9f34`

```dockerfile
```

-	Layers:
	-	`sha256:247a418d2df1a5f038e1406c84da1132f7c9646842c6d12107f6c9a42a148e5a`  
		Last Modified: Tue, 09 Jun 2026 21:11:17 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaad062ac8528251262efb701de42fa345843430652a58053a244807ad2fb9b3`  
		Last Modified: Tue, 09 Jun 2026 21:11:16 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
