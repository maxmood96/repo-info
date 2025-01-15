## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:14a2586cafd13fc343bd20590f1b210ef31af094b914d5e4ede10dcf17dbb139
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b709cade036d8315bd1d1d51ab510cd4c3a60164a3d9491928304772eeed8928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217518079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5573451aef39d0d6e9834dd9dc3e98058dae2cca4923d1a497933df27292a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724f1d489c8c73f2562027ddadc0483e40a1d00ffb7024db1f5e79723d05ac0`  
		Last Modified: Tue, 14 Jan 2025 21:45:05 GMT  
		Size: 154.9 MB (154882249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c12116047204b9b02232aa1058e10f1fcae771cc9944e854b73bb81df46608e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5677080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6f21c8a94081767f797e0f213de9c49b6d9d71883811695ac950aa0f6106e2`

```dockerfile
```

-	Layers:
	-	`sha256:cb76ec7638879fd57d5ab903cfd6ab939b93cc8500b775bd63ebc1b6e8ddae8d`  
		Last Modified: Sat, 11 Jan 2025 02:29:38 GMT  
		Size: 5.7 MB (5667749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46921a229f3974f1613c1f1c5b27c2f9406e634e4d582263d25edf3344200ac8`  
		Last Modified: Sat, 11 Jan 2025 02:29:38 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:38c44dc0dca75ec0de9eb6678a8132793b2d95123d7e05b40413f745aca0cc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211827017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6d806cd1b9def9418c74ab7de129880efadf5d7b12c63fa6a8bc454a3d71c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab71d323be8174450580cb69417d36537b6c2486db8b0bfaed27042fac0d1c`  
		Last Modified: Sat, 11 Jan 2025 03:01:57 GMT  
		Size: 147.2 MB (147236712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6990494b934489ab63f86947a840827a03f9f675d97ffd7020bb2da9b8853805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5495628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19667c57fe330c6ff84cbb9cd1bc28eb481ba42177d830c85429a8c62ee7a371`

```dockerfile
```

-	Layers:
	-	`sha256:7f76e2fcd2ddea21dbbf8d8cef1007c528843f5408abe5954bc3dd96399e526b`  
		Last Modified: Sat, 11 Jan 2025 03:01:53 GMT  
		Size: 5.5 MB (5486217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9accc3ec433eacaddae708c5091e02f48e785986f24f8357179115bf3bf2ff61`  
		Last Modified: Sat, 11 Jan 2025 03:01:53 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
