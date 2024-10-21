## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:1c19ef00459f518aefc6ff6a4f24c001b526506a72c3e884fcae8bfa03f1ea92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3eab71f0015275f46faa38684f75f416763a83baa1dec3b05bccf7873af8d0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187919677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66472030301a38802baeb8c9a641d186f435fd1c8098266cc3b0f75d5f0c34f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca0d18b41a7e60c6e41b0771999a6f1564d302ee6159f1bd2bdf3c920ebacd`  
		Last Modified: Mon, 21 Oct 2024 18:57:18 GMT  
		Size: 125.2 MB (125240138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:345b44877852cacc8acee277e32d1ef58d317049b9bea22e609aab2d4e179fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25deaf34011e8c10c83548ade7f3996e97097f446b9791aca0bf20c3908173c`

```dockerfile
```

-	Layers:
	-	`sha256:08b37c38cdb86dd5112c87b926a00251fc9538ace0890bc183b33670f4e1c4bc`  
		Last Modified: Mon, 21 Oct 2024 18:57:17 GMT  
		Size: 8.0 MB (7971252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a885fc91f84a41f4aabee8710b51c2ea1940a62656dd359d96c7945fabc018`  
		Last Modified: Mon, 21 Oct 2024 18:57:17 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3a3f20ac7e54072ba852675637a439cf40fc18781ed7f6f24b11dd8f7f47c9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132120566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6903a79f23c38126e25a0125f8de01b060b1ded8874c2b43f647f930804b697`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc245bc10c0e45234a0020718c5e72b1b18800afa73e19916adcb5aa57f0854`  
		Last Modified: Mon, 21 Oct 2024 19:15:58 GMT  
		Size: 67.5 MB (67533477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7f0313f4fea65e4859ecf24b1bd48234a6b2bcba9ed7cfbc0e2b08154d3f068c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae0e94226dba4d6e49e89090ad2673671eccb38e18cceeb370a56eaeaaf5fc`

```dockerfile
```

-	Layers:
	-	`sha256:60eb448c32a71e5f8a4c596d606d63d446b0694832fefabfea6eec4c61be4d51`  
		Last Modified: Mon, 21 Oct 2024 19:15:56 GMT  
		Size: 6.1 MB (6077757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361eb1b4baf4abd309db6904038fab6e331394f42f166e49b02c551269ce6dd4`  
		Last Modified: Mon, 21 Oct 2024 19:15:55 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
