## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:91ff838c096c044cf7194aa80c3123620d09d4f23be8021db75d4464dee5d0b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:af600fd742e54f5d13bfaf30c80916d013d398cfcc5dfcafe59db6ce37a29659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172097676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b893af689f93229751c7cf463e3ed7d48a1cdf33da2c853a350d66c8fb73a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:36 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:36 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 02 Mar 2026 23:09:36 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d0b493767715f8da1b4326b2b42538a547266eea01540158895d3376b32595`  
		Last Modified: Mon, 02 Mar 2026 23:09:56 GMT  
		Size: 109.1 MB (109137447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7f4da671003413a019a14f06c40575fbfc55be82725d3db36f80a875e5c16a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ada3efcbfe1a7de33acefd6f2773d4735200c0ff46b79caca136d7ad9b28b9`

```dockerfile
```

-	Layers:
	-	`sha256:d207917df98a010cc918180d9cbd03a5ac10fb3e0f1132cb540e2580d6dd4175`  
		Last Modified: Mon, 02 Mar 2026 23:09:54 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2227976b683d6094633bbc16ba84607145bcb8af70f6801d75c6532d12249259`  
		Last Modified: Mon, 02 Mar 2026 23:09:53 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4ad025fc1d657810dc4e6d80ed9e17c42f5cfacc03a611b9d866bfc85c7ed202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117778572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b1410260dc9677716b4426058945db50f0de4888ab54553df3b303b461679`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:10:33 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:10:33 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 02 Mar 2026 23:10:33 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:10:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd04074b865b86ff3ad8d4d6e2afbc540725c69fc16725b036798016054146b`  
		Last Modified: Mon, 02 Mar 2026 23:10:47 GMT  
		Size: 53.0 MB (52967161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b90c5ec72508c6a74d490f433b163dbc7474a3e9cf2a363346e7c325a2d8866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c404c2dbf32a0ee8ca45e20fefabcb19f06a4179a6a294d91b3a9f700e9fb182`

```dockerfile
```

-	Layers:
	-	`sha256:234f43ade9c0f4e6922f034d0b154f7a60704997e446ecc2dce3f90f63bfcf1e`  
		Last Modified: Mon, 02 Mar 2026 23:10:45 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35bd4b086cf8ea96ff84bb25b361941cb82cf8e4563574a2fec3505e788fcfe6`  
		Last Modified: Mon, 02 Mar 2026 23:10:45 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
