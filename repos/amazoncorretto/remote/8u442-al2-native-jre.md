## `amazoncorretto:8u442-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:37e1fa3a20c4386ffc56283535d0f8c07d6b038b3e0d2857a3894f948bc8eed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e747e12d3029c072fcf9c9c4187a734ea8142316834cf89f2582e7c244ff707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171765824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e901fd061bef97bdb5ddb683e6ddc2b850c91a144b279473f12d534a966b8a`
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
	-	`sha256:b6252bf1f0f9b41e2a8f6374a8a252f1ae25a67239bcc02d43af3b859d1b4c3d`  
		Last Modified: Sat, 25 Jan 2025 04:14:29 GMT  
		Size: 62.7 MB (62669455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44670524bdaa897f812a0a877a8bf32f52ab2972d90a1665f9f565d24005c34d`  
		Last Modified: Sat, 01 Feb 2025 01:08:59 GMT  
		Size: 109.1 MB (109096369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ff303e57c8e9aae5a83d214c00b0fc7f6246046d0e4977543fde56de4fcf0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d51d4ebee357ec004d729bdc0b48310762a30fed789fb9501adef69cec840cb`

```dockerfile
```

-	Layers:
	-	`sha256:b5304642894f206105eb64ed20705129b6172c30e4def849eedb54ce08fe72c4`  
		Last Modified: Sat, 01 Feb 2025 01:08:57 GMT  
		Size: 7.5 MB (7483483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3c45d63c1825329758468c2c24ad80165ff86b23a5eefb52695329a9ae1d01`  
		Last Modified: Sat, 01 Feb 2025 01:08:56 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:abcbb0c41cce56f6a38953404b741c79c658e47ddd7beef7ea4ee76b228d7b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117492299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c12296a8b9766c591872d9498d51b8f1abf4dc00720848d621ccbee3c6935f2`
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
	-	`sha256:e694aca9e8d5c223f3e2469e032276879ab4b403abc21549d4277f4463b2974b`  
		Last Modified: Mon, 27 Jan 2025 15:17:25 GMT  
		Size: 64.6 MB (64578423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e433e0c54645fae2e8e43b0e15e7aeb1a790050228c88507fb73d7930cca42a`  
		Last Modified: Sat, 01 Feb 2025 02:09:29 GMT  
		Size: 52.9 MB (52913876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9e040faa0524d717fffa41a24ca278260116afb78812f6ce83015041810f05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b30545d374fa457a45cefec396ce09247402c614221762b7070896c42a239b`

```dockerfile
```

-	Layers:
	-	`sha256:b6eef3e4a9fa4ae858ea39cca044567a0615745112719d87906f6e771eb6fe92`  
		Last Modified: Sat, 01 Feb 2025 02:09:28 GMT  
		Size: 5.6 MB (5602804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad54a807da9d3c262eba84f6cae011ff4ccfc5186a8932f0119bcf42092a6e03`  
		Last Modified: Sat, 01 Feb 2025 02:09:27 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
