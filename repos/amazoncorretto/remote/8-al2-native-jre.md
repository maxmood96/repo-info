## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:aae3c542bd54b39c810f36fce547b7cc00633106960c62214133e7fe84e22563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:158b4dcd98aa8b74c1648faa1202ec1de97a09c40beb6b7771608e91c49d48d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171928201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e892e226096741c8ce86a05b47df1ef476c01f408d024590e2b5f1135dd068a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13739331eb757a54f200d1054d0cb97f45d08488beaced96436f10dc95a23f1`  
		Last Modified: Thu, 27 Feb 2025 21:08:22 GMT  
		Size: 109.1 MB (109126159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a478d77272a851e16311f20984d24e801a0ea25eda1cc1d69a920f92fb9aad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a697e5bccce44b489a3ec65439a2732417eca59b3007a4d70658cebdc80f55`

```dockerfile
```

-	Layers:
	-	`sha256:38e6dd8f29b2304bae586b475e7e104a328f20dc7d3f49abdafa7dfd61c7aa7c`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 7.5 MB (7483487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df006d26b2d4de652fecae22ad5e0174345b6326a43f7e49aafcd830b2e9fec9`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:294e37a9008aaa7a20f90be7ad13eabb46d25bb77e440602788404fa0d7ee657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117492795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d1d17a43123dcae397297ef278f9f3d2fef13fafb1c5570787ec5adfd037a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037805eca9cc3326934b48ab309757d449bf2956a9a2f5489f7e0d8c97b1416f`  
		Last Modified: Mon, 10 Feb 2025 20:13:32 GMT  
		Size: 52.9 MB (52914573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5058e1101150a262e0402aaabd242024aecaf2b21ce7d86a77eeed704f8e0bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077268381d9968af8b6ee54ab1280679980002e830afb357b930fee4a93ed90c`

```dockerfile
```

-	Layers:
	-	`sha256:64c8c853065e6547100ccb357dc06103027ad1244d7946a0f5ba9e65b672c9ef`  
		Last Modified: Mon, 10 Feb 2025 20:13:31 GMT  
		Size: 5.6 MB (5602808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d248be187a63a73937db93e361934f74209ea4f092e3f717c467646c0b345322`  
		Last Modified: Mon, 10 Feb 2025 20:13:30 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
