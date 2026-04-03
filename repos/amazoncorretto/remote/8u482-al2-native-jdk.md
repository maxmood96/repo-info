## `amazoncorretto:8u482-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:e986c184ecb75d39a47f2e3c74a6173912658c1ac1c1577b7dfbafe06db66333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ef6f30b73223521f4bbae3bdfe80e332a0d7644d6f4547db5a78e3523ae1e6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188248794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721f15a5c213a3c324c2a47fe519c9d336ae9bd22de829ee843f839c64107e10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:06:06 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:06:06 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:06:06 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:06:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da372e554c0e914fa28ddb44bf35102a4c97e0d0fb2550df2c7733f9f6b111d7`  
		Last Modified: Fri, 03 Apr 2026 17:06:28 GMT  
		Size: 125.3 MB (125292284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57293cfb77cba627f689b5adea3fcd25d3373b82fc73e090b51e1757f2ac266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19c992bf6d46482a39572b16d09f1651b847e48b38d771c0e2ae8d4e71410bd`

```dockerfile
```

-	Layers:
	-	`sha256:0a638c64d53923ed006bdd71a15584115452478d836a1d6626bb0e80436233d4`  
		Last Modified: Fri, 03 Apr 2026 17:06:25 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0f01d03cbbc75575c90b52de4fa5e0bff8e7f60e08649953307b660102de3e`  
		Last Modified: Fri, 03 Apr 2026 17:06:25 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:648c80a47f7abf2c48c32f2560a7eb42fefc7ab734fac34f9760c8728a8b31cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6d7fbf1d72394cfac79df5e13c33e4c162aa2f943b9f5fe2caa4d1fac4f15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:13:52 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:13:52 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:13:52 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:13:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36906dfcc58c904c22820711b8fe505d1d826b040e6a93f6c6720a39729167d`  
		Last Modified: Fri, 03 Apr 2026 17:14:08 GMT  
		Size: 67.6 MB (67596797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d6c147d8b50789bbdea4fb91a6c7049a227283ec275dc6c1c0d791faa0d5d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53482e9370f33d5e249a7a81f28fbb08cd66296013e4078f3459d2bd6fa8968`

```dockerfile
```

-	Layers:
	-	`sha256:d0f191a993e9c7e2b5f1b3b575c07d31bb70de2f1a405c9efc1fbabd0d47b24d`  
		Last Modified: Fri, 03 Apr 2026 17:14:07 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4be91185d8e16d58a353d6374d6b857b79e725b397163d4022ff82e5f823dd8`  
		Last Modified: Fri, 03 Apr 2026 17:14:06 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
