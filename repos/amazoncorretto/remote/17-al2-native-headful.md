## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:2cc2428ff021fc8998f537d6b4710524ec553274232f8dd0e5014b4bf4843260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4d04bd09a6c5f8b8a77ff9b6616dfe4e748b1374250a6bd3336a69d87cc731db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154115238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c6cef866bd8ba8b0232cdec4bc1479627324b061dc6b39e694ae59960fd61a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a02a034fddba4f2107a2270ae6754cb76784c4088a06a1a620495582e14cd6`  
		Last Modified: Tue, 24 Sep 2024 01:57:52 GMT  
		Size: 91.4 MB (91436704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:237598dd83fa73093d4eeced0d398fa9d5c96efcc46a27316bdee603c4fa76f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fcd153a1ac851970349c25644be16b241d6cdcceb00202db8e1ba8fdaa2673`

```dockerfile
```

-	Layers:
	-	`sha256:a9e0436555b4d7d2b766e48b3ce134a311dbf055e7766f0d8e3609282d168fe0`  
		Last Modified: Tue, 24 Sep 2024 01:57:51 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dea889701c3d2219baa6251daed9b4f2dd53d35a4ce6c829ecfd45692301e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146778753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560fd89378cc5a8d41bb44310d1179559da87330ebebc3169136008bac4b9d9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbaf728ad418333b47d1abccc8e51ff10a5136d6f9a63532f87594a411d7cea`  
		Last Modified: Tue, 24 Sep 2024 02:40:38 GMT  
		Size: 82.2 MB (82192206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a35b150bccbc0523aa3f26e2b9c0dacd6ca1712d8a238fd0d16fe7da4e35c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fba60f79dee0a47385e58882daf2d1e78315e97e5c16d31328231a32ee0dff`

```dockerfile
```

-	Layers:
	-	`sha256:93898e0da5c8b2dc141dc5ba75cd53dc5b6e0bc811d41e8397e12b051910f0b9`  
		Last Modified: Tue, 24 Sep 2024 02:40:36 GMT  
		Size: 5.7 MB (5651477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99da78e3270ad40ad103d9dddbf7edd1dc8e312b38b9bb2a851c5cf999b4cd2f`  
		Last Modified: Tue, 24 Sep 2024 02:40:35 GMT  
		Size: 9.8 KB (9798 bytes)  
		MIME: application/vnd.in-toto+json
