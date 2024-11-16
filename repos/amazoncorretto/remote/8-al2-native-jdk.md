## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:03615fe56149190bb30bd8b6bf6e1691e847c4531e96d5f3bee7f0e7028d45c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:23595ba701d0e4ab9a9cc6501a74b630620295272bf75ccb31fb4f35f7e91c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187920638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f31b844abbf972e9799d5681ef124d74efe6ecb5324595353fc5a0c170327`
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
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461665e29c7897b934f238c802162c4feadeb4ef62869e289bf7c30cc708223`  
		Last Modified: Sat, 16 Nov 2024 00:48:37 GMT  
		Size: 125.2 MB (125243199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:992f9a7b945795c1e4a13f1601ebf4d95a749a5862b50a645e903e05921ade1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e613f118c07e9a928690852aa00d6274a861fac783f6c9a6a7dc6a420152794`

```dockerfile
```

-	Layers:
	-	`sha256:b7f304c4182d6218e5a5b5a8df431f0195483b75b3636351b8456907e23563a5`  
		Last Modified: Sat, 16 Nov 2024 00:48:35 GMT  
		Size: 8.0 MB (7971252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9582c96398618802658537d4eb4acb75bbefe4bf14d3b856854bfe1febafbda9`  
		Last Modified: Sat, 16 Nov 2024 00:48:35 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3e7fe6446de158475b089f2377ce662b9a9db77f0615e9a266e1e237c0b662e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132118760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43edb1f7db741e2d88a1406ec03216bb76bb688013cc16424c7ed40abbae28e2`
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
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd65e55563c37d306d4606e4e9a8f923db13bfc4435504fe31ede59f69e64e`  
		Last Modified: Sat, 16 Nov 2024 00:51:01 GMT  
		Size: 67.5 MB (67536873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b882bb1d628491a6fbfa84a55dc63c2052d12b6ed3de4ad8626300c0e043c209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e7003a1793b031962dc53321058401b7d0a6bb3d0a5e1588bd445de8ee2e19`

```dockerfile
```

-	Layers:
	-	`sha256:9dcd7dacff7d2639c86e29dc438726e933354d04c9f81b32e022901c1116bf69`  
		Last Modified: Sat, 16 Nov 2024 00:50:59 GMT  
		Size: 6.1 MB (6077757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0fd5e2afdaabecf7196df0b67ad541349d872af34ffe84ee1c69be81b71594`  
		Last Modified: Sat, 16 Nov 2024 00:50:58 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
