## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:86ae910da573745a16c1bd924aab5fcf85357250f1ba3092436840c4dc306d8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1f67800903677f4c1a36c84145c071b7359a44e46de20408cf7f3488449881dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757dc36e49c0754ac7503c0b2468754bf849bf9d5f5738962fd76dbeb3ae65c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bef725ca9ed816905536ea9d06a30e37d6ed0bd0030260bf8f04780ac1e7212`  
		Last Modified: Sat, 11 Jan 2025 02:29:35 GMT  
		Size: 162.1 MB (162147669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fa89bf4bb01f5bbce38542a72f5f27ad3e366098292b76a627102a847fe29162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0cf111b910d9b37b3e529828f36e58ee3138f3c682a474084f5618fe32e360`

```dockerfile
```

-	Layers:
	-	`sha256:5ad60c05772f487f5fe185a0b0d987c42bf3e17be1da928f2bfd826eed7312c5`  
		Last Modified: Sat, 11 Jan 2025 02:29:33 GMT  
		Size: 6.0 MB (5978816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b323ceeb3c9cb45aa99c97b9b2e1e5a6668253a051388701b7b307cf6afa80b`  
		Last Modified: Sat, 11 Jan 2025 02:29:33 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:58dba734ad6937a4e575c24fc1528c3710a1a5fa8f8edaf405de59be1fb80867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216926521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc2b1a10c2b78ef9d218e4efc4e0db1d76207e20fa9bfa3b429133c281e2b19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce53fbd606c8734def4dc24e28e9e6eddd854ee3a2d63627350beaa58fe874e`  
		Last Modified: Sat, 11 Jan 2025 03:02:56 GMT  
		Size: 152.3 MB (152336216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef9e932f296ec346afd6b39217a3535240ae949f80f2195e135300daf8a0901e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19b5d9cbe5473605f08e1bead5cd24814ed4d9e81b55344549d5b1833a059a0`

```dockerfile
```

-	Layers:
	-	`sha256:1703cf6170349460707a3a5c9af2c24c8784960aa33b433e6928188c4b06c11f`  
		Last Modified: Sat, 11 Jan 2025 03:02:53 GMT  
		Size: 5.8 MB (5771530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae981e68d614a0a16a7975eb9d3cd37d3c1727daabd27dded91a842ecf42d89d`  
		Last Modified: Sat, 11 Jan 2025 03:02:53 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
