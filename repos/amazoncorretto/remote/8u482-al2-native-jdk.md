## `amazoncorretto:8u482-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:e202385cc16d8e68395505e2217aa89642835e47fc258f1c15f0370e6b9bd445
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d323b217db7279822658664637ebdf87a5c3ff66fb5da8d263381601d92f8c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188259909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaaca81f4e98359d4a2ed46cd82bb983c53c4b53fa6f3243b690af64f8c2c51`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:42 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:12:42 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:12:42 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdb1ca422f08cc5701ca071fe20f04e4b162ba19dd9a485120c10bfde2e7414`  
		Last Modified: Tue, 27 Jan 2026 22:13:04 GMT  
		Size: 125.3 MB (125296200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:049bf7d147824eabec11e065d731307d31041d428ffbad40def9d85babaca17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ebd2253ad40d78c0a422707191254d610c8945842099093b81d6e68dc52701`

```dockerfile
```

-	Layers:
	-	`sha256:9896d3f19d92c6cb03cccec2ecfda52fa1ad4e49bc8b704450da1c2a3bc47c9b`  
		Last Modified: Tue, 27 Jan 2026 22:13:02 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e03e64d170d7318f8d082e0a68c349c077a636736c6bfc1059ca5a5abe3ca5`  
		Last Modified: Tue, 27 Jan 2026 22:13:01 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f686160cfe3d8e4ac5639a4dd30f182a94b63c132d2083a8297df1800bf17306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132408385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d868024db96629abe53aced98e231ecb3d36c7794cda17f9eac9dbfca8b9e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:34 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:11:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:11:34 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d6233b986eb774d293ca98ef8ce465a7b01ccf9448edb8cc7bb75a95cd218`  
		Last Modified: Tue, 27 Jan 2026 22:11:51 GMT  
		Size: 67.6 MB (67609496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:340e05d93e69dfad1341fc8462dbd24114fca3087848c9db5c7f175535214efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979d1a96220f892e9acf50e946a9257a4e2007899e57dd744964b006c8069447`

```dockerfile
```

-	Layers:
	-	`sha256:3af1a2c427e7c5b0dac43bc45a5e5de06e2520c7dfd540699cae7e8d4a903ef6`  
		Last Modified: Tue, 27 Jan 2026 22:11:49 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061a19f6376e47353235d3caeac9d192f96e6f9ff9fc615825749edff1ef233b`  
		Last Modified: Tue, 27 Jan 2026 22:11:49 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
