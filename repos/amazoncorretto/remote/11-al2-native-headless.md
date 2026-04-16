## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:75d3dc250b0debbaa7898e37e652de7c1ca9d941af42caf785e22c86395117de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d3d38d04bebfef5e5f1e7716439d3c84cb264bf586d9a5b23ee5b2260ae4c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217289352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2750e358957e6b4bda8d6403a5764a38d47b65628fbc65319918b85d4974de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:00 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:26:00 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:26:00 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b57c36703b74839496087c9ba9c0b6bce4cd777a1086f2221c396ae9568db4`  
		Last Modified: Wed, 15 Apr 2026 21:26:21 GMT  
		Size: 154.3 MB (154334086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a82d8555dd33bf73bfcda744b88c7c2d02bb19bfa33e5d94a9eba84dcffc3266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee8d147339a06698265b178eee625b7dd338c1d3cda04405e9affdf02834e4c`

```dockerfile
```

-	Layers:
	-	`sha256:749d902113d4234e72e3a98849805f98cbf74c6baab6328340db6a49264234db`  
		Last Modified: Wed, 15 Apr 2026 21:26:17 GMT  
		Size: 5.7 MB (5683402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa743f30cc67ce19f711a229efe73bda2a3f9eba9c14d07a80860543db63ea84`  
		Last Modified: Wed, 15 Apr 2026 21:26:17 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b565079eeff21d61657caf049ce3b89d9a7dad07c9fa49f674f2b434ad240e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211413537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18be3e06d7a4c10195ac25af1a73a42c4e0d9ece55986f0a0e759320d79d85f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:48 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:38:48 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:38:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ed70b931d8c7fcb833c0b7d8c4a61bb2dc7484451ceb32c47a16e37dfc30b2`  
		Last Modified: Wed, 15 Apr 2026 21:39:09 GMT  
		Size: 146.6 MB (146610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:51066103c5e7b906ea3d47d03050ebe9d243a830ba5eb6db5eb85b8c0ba19fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8553bf21a322f56026454eab639e4e01e5841aafb71269ea21f84b5c7df38e`

```dockerfile
```

-	Layers:
	-	`sha256:3799dc49c714b154b203a558ec0928e05791d0acebe8f84b3a072803cd1432b7`  
		Last Modified: Wed, 15 Apr 2026 21:39:06 GMT  
		Size: 5.5 MB (5501870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4cc6b0aee395d7562b017f53eef2104085265ce10f15e812c9f73865325dce`  
		Last Modified: Wed, 15 Apr 2026 21:39:05 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
