## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:941cb6f656257ea902bca9cbec1259484144ec289446c45156fb4ac8509d6026
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3f4e2c0257ad498ced77e6ce36ee39adcf3cd1618fc6a2ec92d50009fcca1038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217336393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cb262e5b42afbda740a2e80c5c0801d7458ae7300e005aff92a932888a9135`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:22 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:22 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5654f1d26d71c1d28f27e3ab60c8dcc789649b71bad4c18f87a8e7a80f6a67`  
		Last Modified: Mon, 22 Jun 2026 18:14:45 GMT  
		Size: 154.4 MB (154394374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75e0eae353d2456c80dca3df7520094db7b5a5ec7d7cd292eba317ab1933a77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67c627db9ae7c3cedcf29743111c7dba2a8a2a95a3dafb23768d3336478e032`

```dockerfile
```

-	Layers:
	-	`sha256:cc39b0c1d1e12294d71af4ffe4831280cf5a989f99d05a9068a91f6a0a90d9d5`  
		Last Modified: Mon, 22 Jun 2026 18:14:40 GMT  
		Size: 5.7 MB (5683406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3399d07ae9139ebc7556ef8fef3819a078265df1457ba63b1ee2d4119562bb`  
		Last Modified: Mon, 22 Jun 2026 18:14:40 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6350e96e96e1eb84b73a7b93c765914f0f6d9a790d6dcb42740956da35ea89c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211366452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b7663109ce9527bd90da942de33760ca064d7b94bd5194396a3dd7db443328`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:14 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:14 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ff840f0ded350569388eb56d7b1bb6e7e5cafa5096415b453f5466a33b9f14`  
		Last Modified: Mon, 22 Jun 2026 18:14:35 GMT  
		Size: 146.6 MB (146571716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a11e3125ea8710f4193f9dc8a42526be80f3a323fc9cabb5cc08819dd7cc188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7860b89127c863cdd2597df195445d1e4c70452645c3c7f2584db44f64a905`

```dockerfile
```

-	Layers:
	-	`sha256:36275dafe52925bf58397c9bf700ff531c76f80a40a085d530d687d1300bd8eb`  
		Last Modified: Mon, 22 Jun 2026 18:14:32 GMT  
		Size: 5.5 MB (5501874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2353f118a707b2d1d6d62ae221f5e515a3a95cb06cae7ceb39bbb6605b9cb63d`  
		Last Modified: Mon, 22 Jun 2026 18:14:31 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
