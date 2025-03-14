## `amazoncorretto:8u442-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:bff21318048cbce96ba80172d3b2475551c260c57ce4bd6cd7a18ca85735e5c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a006b389dc0a222c123eacc5717dd534f79a63258405caca6437d8337a277ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171889871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb29eddec50955cc5a481baa71c19271e67d46df79af311f81f1183a3ebe9fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e5536e8e67d3422da9b2ffc926497bb81c18146944064b8bf3df70aaff6c12`  
		Last Modified: Thu, 13 Mar 2025 22:53:16 GMT  
		Size: 109.1 MB (109117033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ec077498132668f3af4f3565c9e9a8e6ef09fe51f27f05bbff1a0517d897365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf80bbfa6b3ee453bc2352c985b46b53fb343c1072d43d504562c9456db5e06`

```dockerfile
```

-	Layers:
	-	`sha256:86cd8d076c8ccdf92371f275d9dae48e1b81b060d715f419b2619c872272dcac`  
		Last Modified: Thu, 13 Mar 2025 22:53:13 GMT  
		Size: 7.5 MB (7483409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2c5677a67a926176116d59ed3d8613082316064ad8b6898c9b172b30ccff43`  
		Last Modified: Thu, 13 Mar 2025 22:53:12 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:06ff0342edb9e15e0eccfd42fadbc67ca4807362362b031071b6a136c58bd3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117405644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d589ee943b3f72a88fd73a690453d60cf0d42138e29b81f1f06783b3803f13d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e20ffa04f8cbb4f38a73ee5dbe40cf317989d5670075521d406efc28b5e8b9c`  
		Last Modified: Thu, 27 Feb 2025 21:09:17 GMT  
		Size: 52.9 MB (52884436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b918f8b7c7995a856e2088953fdf38d7a6f1f043537adb9ab3bd6d8d8347330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e150a2f2c561d6900e4d0610c61ca07720bc8d25206541030e61f5f6e830229c`

```dockerfile
```

-	Layers:
	-	`sha256:d9b62184ae7117295b4a3107417293658ec36d24d2698653b2e50c8db3c0cc63`  
		Last Modified: Thu, 27 Feb 2025 21:09:15 GMT  
		Size: 5.6 MB (5602808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6415c0f24d79fe19d700ae74a11be10ee4ee41061f770a04b47aedd33f803e68`  
		Last Modified: Thu, 27 Feb 2025 21:09:15 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
