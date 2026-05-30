## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:146c058658c18c691e2a6b2694105b6d6ab63f2f2574043af7c81d22317ded75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:20dffd0dba8c60e14abea79fd2b5671fd2e7c4133b40aa59d3495db84d4210b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224604166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef89c600d580f58cf7dccaa81becf972e0fa4e59700734f981de5092b5f7a3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:47 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:47 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:47 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0d20a9f7145d5877c397a54a1b6e99ee1539297879c3af888e9fa5afd135b5`  
		Last Modified: Sat, 30 May 2026 01:12:10 GMT  
		Size: 161.7 MB (161662216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:804dff565fec0f20feedf32fd3e5ff9315732f356c1e1db2f54b404c8982b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240f37c39d80be619eb6804fbe9bf838b69a1f55628b73ca96b5c558a572b8b3`

```dockerfile
```

-	Layers:
	-	`sha256:224b55f7a4c487128a4f330bd27b447d070ed6ae79b3a5d73b6ea8c8f70a9d48`  
		Last Modified: Sat, 30 May 2026 01:12:06 GMT  
		Size: 6.0 MB (5995185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ff2e188a69247da133f5116b931799aec73e0671349b3118e8dbd7e531107a`  
		Last Modified: Sat, 30 May 2026 01:12:06 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0294acadc5b0130de43be8e4fb15158c633eb2a0c8243c0d20e750079525cf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216526387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36abc54f187df616738de0535ad7fdc1e9ccc266b39643a438c46e20ea8f6b9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:42 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:42 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:42 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12432125455dec8c5192f3cf46b47fdd6b31f09b379f47682af455c38d58529a`  
		Last Modified: Sat, 30 May 2026 01:12:04 GMT  
		Size: 151.7 MB (151735678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c71021389aeba7f9e0a930025db272d7945a2b3cee91a35502c4e182a9b41eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28a6effaef8f3521dcee0ea2811bec12aeacbf5c11068509a46042eaf85cdb`

```dockerfile
```

-	Layers:
	-	`sha256:e6f05f6ddd5f1653c38878eb7124ea5d088bde824be5ab55bbcf348ea7c96f4b`  
		Last Modified: Sat, 30 May 2026 01:12:00 GMT  
		Size: 5.8 MB (5787899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20552e7d30e23d8dc7f2e199be02b88eb1d41b8f4ac33cc2547755897700fc0f`  
		Last Modified: Sat, 30 May 2026 01:11:59 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
