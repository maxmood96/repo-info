## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:bb6db2391e72dc7623da493f66771ae64e4731f613899bca4af8d3ef5049fa96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:10b94b11a42d82bb291a5ba9ce1ed96e3a5d0ce7acb366e3e26845ad443d2e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228726181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bed97b3892898aa58eefd1e723d75cbb9543b91444b0c6a9fc054f963d2107`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:02 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:34:02 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:34:02 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a713105e3ae4fc410f9e2c64e6f98e134a923bb19859fdf9d5cb57adb49a5f9`  
		Last Modified: Wed, 11 Mar 2026 18:34:24 GMT  
		Size: 165.8 MB (165769671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6c1d903e72310d153f6eaa558b6ac941ac1bab6b216899478adf4c18213f031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3084c519af7271d1183877ff2b898ceea5d9a8f68a3e490f73130e2c21af341`

```dockerfile
```

-	Layers:
	-	`sha256:782f3d3ca1dcf6eaf7e858a372e63ea0dc96b7b18f1a54f4af5ba6392ab1bf7f`  
		Last Modified: Wed, 11 Mar 2026 18:34:21 GMT  
		Size: 6.0 MB (5971814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377cae7e25e5505b961a3ae73cde7ebf9a20e7e2b767533d765e14999c172abb`  
		Last Modified: Wed, 11 Mar 2026 18:34:20 GMT  
		Size: 9.9 KB (9914 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9edc571d979fd5f57c9bc9bd4b66118ff50bd9f6b187aa6ec1ebabf0f251acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221067233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002928704e0cb3a9bbb489626f63cc776fede3fac7553747ce34b17bd720c110`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:23 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:23 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 11 Mar 2026 18:33:23 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b82a9047ce41a82fd11dd6a4d3187fd11aeebd081d1460df788986b03d9af`  
		Last Modified: Wed, 11 Mar 2026 18:33:45 GMT  
		Size: 156.3 MB (156264084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9130efd1a32b74fb0f238bc959db1c698768c56f38f0237eb3b335d581736e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2571d7559d17621af9da5b9b553b8a735af3df1c4f7317d999093ee3413394c4`

```dockerfile
```

-	Layers:
	-	`sha256:50892828225715b4f03872acb5a3176ccc3b5b745c3709e35fc808570c4a9b15`  
		Last Modified: Wed, 11 Mar 2026 18:33:41 GMT  
		Size: 5.8 MB (5763684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c6b1d53f6a11deb20a6b183151042cafc7f6f2e8b83ed42a06e207dd7d0d6e`  
		Last Modified: Wed, 11 Mar 2026 18:33:41 GMT  
		Size: 10.0 KB (9994 bytes)  
		MIME: application/vnd.in-toto+json
