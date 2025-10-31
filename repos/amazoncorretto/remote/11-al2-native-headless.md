## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a2c3ed9137f95426455253a99cf20c99314a3685843187c05a6c65c1d2699632
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6bc23324dab23f22fd46d35396d50268a9b8763d70a6f65896997436e7d661d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217239417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09533f26901838d7417b1fca6afb65fe7ec5af2fc964211493e136dd02062442`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:15 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:15 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:15 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc5eace825a068ac19d7ebb5afa9942aaf23f87b2a1840773935fdfe6d0853`  
		Last Modified: Fri, 31 Oct 2025 04:18:25 GMT  
		Size: 154.3 MB (154305349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da219b8e06b61b3a521231113283c24088ebed9f902c4d7dc293f60fec0e3656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6042d767748d754b3d8879b21b6c1ce45b00ecaa28155daa09fc1b0d7146c1b`

```dockerfile
```

-	Layers:
	-	`sha256:4c8246fc2571937031efc5b84a8dec128bbeb306db7444f952bc48f3a5c55615`  
		Last Modified: Fri, 31 Oct 2025 03:47:33 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f84bed7e7acee59c45e06a5f9ad856ddc7330ce145a2140be0b955ece93da75`  
		Last Modified: Fri, 31 Oct 2025 03:47:34 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4a34fd58e397264ce4484f3cafe2340c5c7246169226dbd92e514d8f8d570af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211381487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2018acb7b5b97b973f8c89f818669a47161099f0ca3399fb061c534fee64645e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:38 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:38 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:38 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665b424e141d241604ce98b2358b2a647dac2a148d9f4ea9298e90aaaa9d145a`  
		Last Modified: Fri, 31 Oct 2025 00:11:59 GMT  
		Size: 146.6 MB (146588029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:381a16d84ab7ed0c28dc763f8b71c5fd64f721f9bea13baa4cff430f7386aec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc425403457a0290f20651faacc232823d8535bec431225cf9925e0691e02b64`

```dockerfile
```

-	Layers:
	-	`sha256:c4392e8091274a83ff8d82f9edc0c89dc97773219eb6e34eb96ed92cabe8ad58`  
		Last Modified: Fri, 31 Oct 2025 03:47:39 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24b6e013206eb052391dcda65de2feca1cd5d5530ae79e587b472def29a3c6f`  
		Last Modified: Fri, 31 Oct 2025 03:47:40 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
