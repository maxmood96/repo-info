## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:899dac91c97a8f89ee550cf69b5da6ffe43ff7d3b07af1e3847c0738d7e9cb2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6efe0334eb0d4644657085f848ab5747d0c88b9a7497fb2fddf84fceaf6b0d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217294644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b321a0d18d0b59d84c658765b670db6adfdc711899575bf3c60e795a107a11a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:55 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:55 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:55 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf49703b7269baa488648d0cd92d735ddfc1e0813d28b1403b6c7cc7b0f2ccc`  
		Last Modified: Fri, 03 Apr 2026 22:14:17 GMT  
		Size: 154.3 MB (154339343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:458f2648082c934a27ba4928fe598d2e2cfa59d689e8d2f19f4dad23be962d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd54cd4cc6e9230bd0bc085c830ba7ff112041b6ecd20c53ae2bdc62583771a`

```dockerfile
```

-	Layers:
	-	`sha256:5b7a64968c07e342924f67c06f1b202a23712502ea0980175166b49510fc044e`  
		Last Modified: Fri, 03 Apr 2026 22:14:14 GMT  
		Size: 5.7 MB (5683402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb49508b4dc2677e62698a073f53dd55b6d7fd49d590d7ee2d0913c514accfe`  
		Last Modified: Fri, 03 Apr 2026 22:14:13 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e74b3ce5cf6fe19d426a528d1136ae536996cebe9b8dd5f525623ffe7cf8d70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211406424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a2d2b8979ba211d32f4458298e4b393d1dfceed22236b1301539850779e037`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:47 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:47 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:47 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f30031f808fee8295843cdb6f66d789789d94cc1d8695eb8b428926bb98d62`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 146.6 MB (146603585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d65c5c1ccf0849d8a09679cd30361569cb73427425b9c906dddc4f6c2f44ae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1355deded90ce007c1247f3986f37f84c2aa4944160591af79e30efa395a0b`

```dockerfile
```

-	Layers:
	-	`sha256:426de9b4266f64d8f3ea0ef359b3384f97a7534a03e3c7bff5bfca95f51397f1`  
		Last Modified: Fri, 03 Apr 2026 22:14:06 GMT  
		Size: 5.5 MB (5501870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a05c699c912f2482b37a4d01daebbc253457707f9a47377ba6ca2aa67fd71d3`  
		Last Modified: Fri, 03 Apr 2026 22:14:05 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.in-toto+json
