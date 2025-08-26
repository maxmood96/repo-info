## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:8f1255a80b6859fba0ec7aab898cbc0b6845e39a5ce26fecfc0c423987872a91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:66ac92afcc48623672d4745c1ea1673631711e1ed6b0e9e1904d5eb695398a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228648445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ec222c1e6966ad17c1c8e3ed88ab93bfa9c2f353ae513b1b1c05e8fde6a760`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7618deed62b53d71b65a15a1030e35f312d2bef8cb2c404b04ab1675daf21f`  
		Last Modified: Mon, 25 Aug 2025 21:58:49 GMT  
		Size: 165.7 MB (165670320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:474f115717ac096c2b3d17c3ae36ca944ba2d77e6ddba49917e3f4b00f700a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4435a10bfa11b527db0a099fe4a4cc4123fd11b2a96815600cb38eea290e0e6c`

```dockerfile
```

-	Layers:
	-	`sha256:f9d88556552ecbaf6133fffa924174686d091ffe6e7bfdef1aa5263aad9d4a86`  
		Last Modified: Mon, 25 Aug 2025 21:48:17 GMT  
		Size: 6.0 MB (5971810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e875104a817c093e2edd896714263f09247f5d454cafc6b06eab94e025ae76aa`  
		Last Modified: Mon, 25 Aug 2025 21:48:18 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d380d5796e753099e7435fb961539488b09f507c7338a6b0c681901d3dff9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220920506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5683816b3d2fbfc84a3fad94a47440bc96a9561c86cc268a0be478fa97803c49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb0aa64c94952d4ca6e2513c9501d5d3e9b9ed390fac475c949c19bf4fa23b`  
		Last Modified: Tue, 26 Aug 2025 04:48:18 GMT  
		Size: 156.1 MB (156119156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3a81de333452f8bd9ca287f07f351a3af8aa1e60bc28953459f03299642477fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98abbc8cfb7e936a464f3bbcd9b2b626660fc6f94cd5be902f09f3256b7d852`

```dockerfile
```

-	Layers:
	-	`sha256:2af92184bb83a46cb7c8b8146a583cd15ac0e5b63bf5a8d673f24eb1467eefa2`  
		Last Modified: Tue, 26 Aug 2025 00:48:20 GMT  
		Size: 5.8 MB (5763680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819edcd0f0956d1d85afc0d36f83db61a04e35982b2ba407e2b40025d174e537`  
		Last Modified: Tue, 26 Aug 2025 00:48:21 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json
