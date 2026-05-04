## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:ab69fc832dcf4306d4ffe8af898b5eb9581dcc6e2bd4893ab16e4e78b7a5fc4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e459cdc037ba14ad89b64c71fd7dda33a0097c16d9e91993d363606c1af0b251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224464954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49265becc75d82a81d438f28699f23f6a7715b707eba20685ac6e127da624dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:09 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:12:09 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:09 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5ccb5f44f32644fc4d28353f9a4cd22c3b12d32070f59e11e388845c931fef`  
		Last Modified: Mon, 04 May 2026 20:12:33 GMT  
		Size: 161.6 MB (161604945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:21c3b1beb9c5e0b8ac6dc58c605f1b02e214cf8231682c828abe8d149bb52cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b362223fb2562848be438b8e0f3d254027ee913fbaa4896afb4df0a722540b`

```dockerfile
```

-	Layers:
	-	`sha256:df2ccba249bc0e36f1059a7348f8ee47a458615394972933efef7f82792378a2`  
		Last Modified: Mon, 04 May 2026 20:12:29 GMT  
		Size: 6.0 MB (5995185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77885c4792f36bda393f054acbb3afb61da45dee825b29e32a169649221c924c`  
		Last Modified: Mon, 04 May 2026 20:12:29 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:968f0960a094fac0ddc8001faac243444a2057adce7e07fbc0b0d58dced479ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216545369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f366521a8ba0d5cd2b8a80f178bc709fc17e03997916eb9133681418049536d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:16 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:16 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:11:16 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6606233ee5d6a5dd3f51c7e91fa515b618316e932923e8f0600c60c2c6d900`  
		Last Modified: Mon, 04 May 2026 20:11:38 GMT  
		Size: 151.7 MB (151749838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:70db84ead39209e9f5a682f2b9db2ec4feda301393e57c48ba8c01b8c00fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8f1b44885b1ea1edca315086229db081231ae01752567000b086ec8713732e`

```dockerfile
```

-	Layers:
	-	`sha256:efef17a13d9e784cf96194b100d0ca4a36581e23324c78fe7dfe88ca1b8706e5`  
		Last Modified: Mon, 04 May 2026 20:11:34 GMT  
		Size: 5.8 MB (5787899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8daa5cbce4e8b10b4e108c462ea5a6e4b3f0936c327616445a7b6bcccc7d20`  
		Last Modified: Mon, 04 May 2026 20:11:34 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
