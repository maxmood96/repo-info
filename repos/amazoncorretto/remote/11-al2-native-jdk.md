## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:3093ea38542aa5d7b64cfaee70eb52ed3eb054f719549d93e3acd81cf54fe025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5768e4442541a992dd522d712a0bb399b47a7b5f49933368c940a7f626c773d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224603450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197998290cb0122d437594e9f14020a7cb70836c97296c167bf668a142c8ee30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:29 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:29 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6523c7fa20a45d6cda3713225132842b3f5ba61e2e16aef3f7881a71ed40747`  
		Last Modified: Mon, 22 Jun 2026 18:14:52 GMT  
		Size: 161.7 MB (161661431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3f97e8a7f82444cfcb18b0909b132c7b9406fb2db8d2ea54fe6b48422113c369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93399d50d3fd9e84ea02f5b5767d07f45735f2ba86e72089bb4e6c060b54a05`

```dockerfile
```

-	Layers:
	-	`sha256:ba71dc6a7cd496ca60b2c701348fe4c8cf68214841bd0265689d62025652859f`  
		Last Modified: Mon, 22 Jun 2026 18:14:47 GMT  
		Size: 6.0 MB (5995185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037d082fa2c5ac409aa758f9175897717e81c6621288f577dfb0fbe2335c0430`  
		Last Modified: Mon, 22 Jun 2026 18:14:47 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:471b1b4605135cf3cb21ae23cfb57301026f0e3cc459952a2f3b640911f86cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216472386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709546aab09f3ac80677e55cdfe12a6b579823b92f9f68f6b7d8d09afd3addfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:30 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:30 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:30 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19816f639ac744c81d13f843389829da7b8b464413cee25c9a2fb8f9f782532`  
		Last Modified: Mon, 22 Jun 2026 18:15:03 GMT  
		Size: 151.7 MB (151677650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b498ffe6cbe57df3a167b3a0e5a16d019df36d2b1e65c2d4af3cd477909d8a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35656a24714b44e9b25de5b66935513e48f9994e7e78709a883be1b942ee903`

```dockerfile
```

-	Layers:
	-	`sha256:4f716bf0167e83147c15d1ad3da942926e41812e981c104e1c3a63ffca8d839b`  
		Last Modified: Mon, 22 Jun 2026 18:14:59 GMT  
		Size: 5.8 MB (5787899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d9a2f462fd40ed9906da5916995a4a77e2448992846fd061969d436a26b65d`  
		Last Modified: Mon, 22 Jun 2026 18:14:58 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
