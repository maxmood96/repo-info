## `amazoncorretto:8u462-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:2d97c7b628ba17bbfd54fd4a61725dcdd196da632c8d18783f80622a3d1a3bfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ddf5f623a05fc353f98cde77a39a7f48e243d0493f78ec5f8779cd8b76a0072f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172128417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c882090a4ff3318aa1059c2f2a9280776c813410f4142e2e16ce5a1f381c86d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcb937bdd46f5f1da62614f54c17b9f9d765df777ef4ec3db94ab05421e6aa9`  
		Last Modified: Mon, 25 Aug 2025 20:19:10 GMT  
		Size: 109.2 MB (109150292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c494b9fcfaf2922b6ef48af34d0a1a1f5daeff2d84867bc4e4b32c6397e2762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abb7bd3c3283c1c30ada2332032f06b90cae59ac19917e5ba4692272b7dda79`

```dockerfile
```

-	Layers:
	-	`sha256:1637f1004d0c96aea324a73b3ac1dfa3c1d4dcd8901a090f06aadc643abd7a92`  
		Last Modified: Mon, 25 Aug 2025 21:50:21 GMT  
		Size: 7.5 MB (7504120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e531e5b58416a3b48af1e210e0435b4eceaad029f306e2f2d5b3e38f0efe9b5`  
		Last Modified: Mon, 25 Aug 2025 21:50:22 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:19d5a9d7ea68f519c408c99fbc358f8646283eb84cab15bff3ea62d96015980d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117729002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cee29d3afc7cdc8345082df46e6d39f138d0fbc36db9c0cec140f4c1e59c7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14735472dfe7e8cf1e1ab59ea8a64198e740ce33a3be8e61fef5afc74552d5ce`  
		Last Modified: Sat, 16 Aug 2025 05:10:48 GMT  
		Size: 52.9 MB (52934638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:016dc5042e925f575b102072a44416b9aae58dba73cdfd33925fb4a89d2d938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391cf4b60dc3bb16632052b89cad1b8c1b0c3dfd79e0d8710ee3eed79774537e`

```dockerfile
```

-	Layers:
	-	`sha256:218358102bf27da68a2d838ede6a58998a72802e495b0bf94f3450b859f64555`  
		Last Modified: Thu, 14 Aug 2025 09:49:53 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61dc418bf9dc7f12dbe116b2f53b2fb3d7022c1b5f989644472051e7aa8b247`  
		Last Modified: Thu, 14 Aug 2025 09:49:54 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
