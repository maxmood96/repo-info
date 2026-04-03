## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:999e271e8c99fa25d2b9ab24929b8997f7ca85a9d367cf5ba1db4acc615584c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5939caac5f5997c1284148a11af60484e933780f58638022ea67f871ead9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224576383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8baa441bde02f1e72373da9ee8dca402e1b9daf00bb163ff93fb601a9a9ad55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:07:39 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:07:39 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:07:39 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:07:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e841b2d362e572038817b7b9de1fcdaf4aa85c414f4b18034eef262c16e13`  
		Last Modified: Fri, 03 Apr 2026 17:07:59 GMT  
		Size: 161.6 MB (161619873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9cf10bc40e890d4282ab49267b22baed41bea9e934206c86dd5b2e4d1dbefffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd6f29bf04dc48c11aca41918a9e3a8f2107417d304471c44f89f9605377f45`

```dockerfile
```

-	Layers:
	-	`sha256:78da3be6b57c4540d483888b54705b0659e782734fe9fee3ac8239e2c15a96a1`  
		Last Modified: Fri, 03 Apr 2026 17:07:55 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001e098cde23a2b084a4d393b5ffcf908ed3022389d3db48201f813b9fb301e6`  
		Last Modified: Fri, 03 Apr 2026 17:07:55 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c8a9d372de369ece931767bd28e92bde208a1290a197dc69d6cf680a25c6c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b628e512304cfb949cb79dc510c7b0b083858fc38259467d034b298e3bd502`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:15:14 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:15:14 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:15:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:15:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70b80eaa344926469c6efb53dec060df0b0c8ae50c35975e369f491e2eed37e`  
		Last Modified: Fri, 03 Apr 2026 17:15:36 GMT  
		Size: 151.7 MB (151702018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:950bed3b8cf7b54d17b1b644380b3b949c33cb15b199f6112e7d44e2c9facd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7144fb72575e88a5883149ecc77a9ca5dfe5431175fdc4eaa3162401ab1304`

```dockerfile
```

-	Layers:
	-	`sha256:c0798de7a96f304fbdbe2d22afcb4aee1a539019a1068759c7cb8af51e1adcee`  
		Last Modified: Fri, 03 Apr 2026 17:15:33 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ada90ee63c9426e3a63e8698f58f6440375f36769b0413a904bf31c33079b4a`  
		Last Modified: Fri, 03 Apr 2026 17:15:32 GMT  
		Size: 9.6 KB (9634 bytes)  
		MIME: application/vnd.in-toto+json
