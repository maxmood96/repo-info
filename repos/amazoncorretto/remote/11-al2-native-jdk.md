## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:830f5951fd8da0dfddaa84f00b610e3b349d7969e81e3992721a1bbefe9811e7
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
$ docker pull amazoncorretto@sha256:1aeae0e2ed99086aa33fefaf071aeb475b1b62376b9615c8a6e4bfb29b9a74c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216929797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b7e4039e5d9d14e2ceca1ee9f3990d22bfdb13db9b63905f081bf08df5fb47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcf79b812aff6f428224f67866465b2a45ede389a609890795b900925f61c4`  
		Last Modified: Thu, 23 Jan 2025 18:39:12 GMT  
		Size: 152.3 MB (152339492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dda9c6251dad6ab53f5cbb86daa4b9ef65bf516c38c41be3ddc63f49ee5f5d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf6849a7e5971a763a004449623e4f250b274059dac6de0df986dffa42c76bc`

```dockerfile
```

-	Layers:
	-	`sha256:df07dd88b931d0ffe1e8615d50eaf0960b7a98e866c554e15ab846221f5426e6`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 5.8 MB (5771530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b462d870e7fe51bbdab60118bd11a23c8176ecadfeaffb5e4d97589adcc6f`  
		Last Modified: Thu, 23 Jan 2025 18:39:07 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
