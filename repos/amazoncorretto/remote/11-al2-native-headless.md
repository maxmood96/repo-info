## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:37d915d1f13571f1f334128afd3fb4e3942041723940535735696df0e40c7504
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:156c942d59d413eb77e1fed9087956b5cdcd18c14bcaaddce0907df31c980ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217336224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2c2606ea83ed60395bec3745c909ddc90cd0510adf6c6863b935211fd791e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:05 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:11:05 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:11:05 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525683bc2233a896de5fb54bb78f9f1ca0ac92876c794828fb60f1eaa58bc9d3`  
		Last Modified: Tue, 09 Jun 2026 21:11:25 GMT  
		Size: 154.4 MB (154394274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:01ac573716b0200149abb7c617a46a3ece806f22908e2f46da5d32f3eb48fd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcf78880926d305bd94282c7a6908252ad82b6ddac8723307cc02cf7d700618`

```dockerfile
```

-	Layers:
	-	`sha256:41dbc6fd140962aadf5f0ea45e47b835865e3c6924f0deb3273c472fa2c6ea28`  
		Last Modified: Tue, 09 Jun 2026 21:11:22 GMT  
		Size: 5.7 MB (5683406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdcb03c0f41f54015758a0cb3a5f5d9a7886ee3439ee59f0a557069abd9e771`  
		Last Modified: Tue, 09 Jun 2026 21:11:21 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e8a6b17e54cb26efdda184b08998aa103d262110caed5dcdfd2e52bb17d39aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211414591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b6bbe31553e84829148d5d922d591b6cde7a1ecf4cf5459d8215b1b124fa03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:22 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:12:22 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:12:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b97c71be006f4b9745957ffccea320425eb414767bbd9f3053228a9929159c9`  
		Last Modified: Tue, 09 Jun 2026 21:12:43 GMT  
		Size: 146.6 MB (146623882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f683ee75c69a81855a57fb882b83d7e6d9521d63f34fde58dc02082f21b7997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c825ce8708ef585ef2dfca62464396aae8824fb7b6d6bfc7190661b69542f57`

```dockerfile
```

-	Layers:
	-	`sha256:65957861b6572eaed5de42d87e55f842ac5029fad67876676ce6ec89957c2229`  
		Last Modified: Tue, 09 Jun 2026 21:12:40 GMT  
		Size: 5.5 MB (5501874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1307c17a62e7eb0e0243b6eb98fca4a3f56da2f60fd09f432b2a6fff85b28a`  
		Last Modified: Tue, 09 Jun 2026 21:12:39 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
