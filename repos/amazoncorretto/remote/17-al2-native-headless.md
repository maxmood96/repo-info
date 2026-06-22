## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:5d0f44969399a2dd8235412940389734ba358b12afddf300842659285dd6a7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f25e95364c742e2521eb195c64fd07e3ae4f2ec876dd48ac094c662fc298e8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150645457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9264b50c82aef027bfa557081b2fce3efe6acd26c8657cdf00655844627e7055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:28 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:28 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:28 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2051805659a2825299f9ed53d05677d50db63dc9aae3c577af1a836046bfd1`  
		Last Modified: Mon, 22 Jun 2026 18:14:46 GMT  
		Size: 87.7 MB (87703438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:535b0820514c68700ba469b89364a98209d7187f8e9e7399b4e36be51d50cff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f904e6a88c50680ebca271478bbf7768b79bb254cb8b627138b77d079d58deb`

```dockerfile
```

-	Layers:
	-	`sha256:d517c5bc0412585b8f07d2bfa2045452a55b836e917b6da18225b6f09604f57f`  
		Last Modified: Mon, 22 Jun 2026 18:14:44 GMT  
		Size: 5.6 MB (5632679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f069c8a897bdb7f214ffdd148dd57fb74e6ca6db01b8e13beaf3acd1fd5753c4`  
		Last Modified: Mon, 22 Jun 2026 18:14:43 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:abd03e49d96c65af710ef299b3fc2464c907f77df535abe4a11e87cca63cf7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144682322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961fecf33a80cb4130daa78c4cf968692553f9a5cb6f793f423965faf97896d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:38 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:38 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:38 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df2c8c60f156f548e10665bfb1c68c088b7fc1d0094e9a8f83b017aa4b73495`  
		Last Modified: Mon, 22 Jun 2026 18:14:57 GMT  
		Size: 79.9 MB (79887586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52ae35ac6cdd1cd0b4848d2eb7c015535b88265f70107ac5fe9dc77092a90b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03536002274917b0416631ef2100754fd51c417774a50005e3cd026b2f220c2`

```dockerfile
```

-	Layers:
	-	`sha256:d6bdf700de188af70384d7aec369de6f8c9132c10d1ff064ed82c8bbfdb54861`  
		Last Modified: Mon, 22 Jun 2026 18:14:55 GMT  
		Size: 5.4 MB (5448956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2529a89dcc5cf38d4125cb6135e225a5ba3924ff1073361809eeb0934ad6316`  
		Last Modified: Mon, 22 Jun 2026 18:14:54 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
