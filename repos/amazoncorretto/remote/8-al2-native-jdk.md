## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:bb6cd087fffa6d718aa4062089ae413c093258cf1ed1e796b0c5318eea43c7d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8849ddeda805fd284b502d163c194ddbf0320bf19c9802a786ef275541336ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188196065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b89f2d419e2ed8f66fa16919224acf146b40d3a84925ff1e48ac382e03117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:48 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:48 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:08:48 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e81b4d81335d0b8130ab192306571f31b802f7ce18fe519cd1cb5088a56f1b`  
		Last Modified: Thu, 15 Jan 2026 22:09:31 GMT  
		Size: 125.3 MB (125255909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0d50ebb7cd41f5b5936ef1399a67d25b9b1dda75f67fd3dd8aa304cc73ee2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9442b6f0438b88ddc61e88bc9e897d60b69984575d33c81e44bb47f5526dbd`

```dockerfile
```

-	Layers:
	-	`sha256:9d861674ce93fc73d67c5eb1a65595e4381e66ca27072892827bfaa2dc6110af`  
		Last Modified: Thu, 15 Jan 2026 22:52:33 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1e55ade1f33867ca3a843ff666ee820159064b9e9f5dac3a73b4f59b96c758`  
		Last Modified: Thu, 15 Jan 2026 22:52:34 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6292bf5882ffb4c2dd56f46fc61b4f314f2ab2edea7e64112237ee53418ac550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132316344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae92c19481d946f7000c6343c7a280c87b279ae015192a520df269a19f538a10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:23 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:23 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:08:23 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528454a0d692bda06f9ef21ac04162e3159a516c03ceac0a6f4a8c8896b3bf0f`  
		Last Modified: Thu, 15 Jan 2026 22:09:02 GMT  
		Size: 67.5 MB (67545910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e66bfd52ded719b2b42b17b268c9d94306599ed8a02e171e14d4fbab3e8189e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9220b11d565f06d1962e5cbc6e7ea0585e3e05ca7ff2af8686dc238160e6b9a2`

```dockerfile
```

-	Layers:
	-	`sha256:ffa77e964b6ce3e7e0c8efe2dca0635996809fd708b548301cd2ad6a914710b4`  
		Last Modified: Thu, 15 Jan 2026 22:52:41 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5debb8c2c51b05b664ee25f0aaca4bcd5aec873132b8bc8bcbe693cbdc1e6c6`  
		Last Modified: Thu, 15 Jan 2026 22:52:42 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json
