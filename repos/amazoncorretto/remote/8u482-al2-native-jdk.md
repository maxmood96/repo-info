## `amazoncorretto:8u482-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:05a5ee15621a2a39d759762df0b4205e03b28474c8a311b5a0ad5c4d73605252
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:380d236e763018df16d898fc3a1a954cf480ab99562cd4e97897903d832e4512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188237680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5718039db35465de88df9c197f45fda421fd8c7aaac4adfc87bdb2d703a6b50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:22 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:22 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:59:22 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c23c3b9563854be49257cf21b781536c99c68c498b6632e9a2ca2403f04652`  
		Last Modified: Wed, 21 Jan 2026 18:59:45 GMT  
		Size: 125.3 MB (125297524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42e2930c7876f83b264a4eea677e027549f20a62d3af8a4e0174335551d7e64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90c53cb857f2feb95710106ce197e3d699eba7545d6a4f89962a501c4e4d0cd`

```dockerfile
```

-	Layers:
	-	`sha256:95b8ef22025c0d0b8df09b3bcd2d9b7cc76ce929c335d5784abf167d73f2b104`  
		Last Modified: Wed, 21 Jan 2026 18:59:42 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3c63fb23f415fb7a99cc95366e16159b4fe6c7307234fb301246fb5f4713c`  
		Last Modified: Wed, 21 Jan 2026 18:59:42 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a10ff51aa525effa0d75cac6dc58a85275129ace3c5ee7f213f77bf2ba9fdfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132365526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be942bb2d4ae28ab11f76c7c7bb5abea1dca9b5dc1f454865f6156d442ee2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:17 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:17 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ad3d8c6462812ef98f010ddcb458313e9e58f8a3809e6e34b31b016b0895f0`  
		Last Modified: Wed, 21 Jan 2026 18:59:59 GMT  
		Size: 67.6 MB (67595092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2c221306128d5962bbc048b067fc5f9f530e958c85dac5f912264c20c39f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044276fc09d4ff6408a919466269da817ad1c67650c8ee4993310dc8664f6f95`

```dockerfile
```

-	Layers:
	-	`sha256:24555b7df14a1246cc131e7f7293d05bb5cc6037d884928dfc0005f898244778`  
		Last Modified: Wed, 21 Jan 2026 18:59:32 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a93a64aec1e3233ad8f1ebd77f5477d24fe61b499e7a4a3849e1334390fe837`  
		Last Modified: Wed, 21 Jan 2026 18:59:31 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
