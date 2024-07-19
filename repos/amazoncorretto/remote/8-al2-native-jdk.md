## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:5f8cc698dc9d0b5b83bfc70e976dc4d18ecb4239e1fb41bd070db7ba431ff43c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62c83219e02d687e4f9553c782ca6866e86adc790b416a92debd2e15e523436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187907360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b44f7b6e922f74bdd17851bdf4965bfbf3276662a2ecd189fb5e3d7c7380c5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dd8f9d3c2a4623770e73ecbf80dc15c89c8d2441cd5bfade5ab36ee74947cb`  
		Last Modified: Thu, 18 Jul 2024 21:49:40 GMT  
		Size: 125.3 MB (125259434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:456086c85a80e2c9d4f3245a8111134bd31cf833bc9c61e9f97f4f63b97bdfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8873c36ba70f331e84d43d5a9687996f048e78a078d659903c8ad5b7d1d2747`

```dockerfile
```

-	Layers:
	-	`sha256:281da8fe87ac6dd43cb0e9d8680d41a69f32d2aff2708494d7a5cc441f8d795e`  
		Last Modified: Thu, 18 Jul 2024 21:49:38 GMT  
		Size: 8.0 MB (7971152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18de7812c4075df202b8af72cbda771de98eb6230e3144ef2759ec916ca9e12d`  
		Last Modified: Thu, 18 Jul 2024 21:49:38 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:709481d1836a51d1376aa188fac8ecccbec2060d1d43519901c19bbcdbfae6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132128669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbacd96d591953efca717dc14cc3c9c22f7faf14f6c731c8de7656528b9ab830`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d51d5d88ccd10b6665e6926d0faed7ad5c42d274e1c66595863143b37da11`  
		Last Modified: Thu, 18 Jul 2024 22:51:21 GMT  
		Size: 67.6 MB (67553358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8bb51c19a8866713576c1a1ecd39c587b56ecc4feea774061bb18897304720cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d04adb9f71c4b70bb752b37f212ec1979d2b56c86f3456fc5c5b8f0b263ef7`

```dockerfile
```

-	Layers:
	-	`sha256:09dcc6cd9bae4c49e645576939cf85622b81598add41c94f83012f985483d55c`  
		Last Modified: Thu, 18 Jul 2024 22:51:19 GMT  
		Size: 6.1 MB (6077693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be4d50f4f36afa7f34931ea6317a9f9c082264ac5abf46662f07f5177b87ec1`  
		Last Modified: Thu, 18 Jul 2024 22:51:19 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.in-toto+json
