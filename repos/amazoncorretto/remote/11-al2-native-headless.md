## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:18511a269cb99c05136d77a5be731105f4334db38681b4708b149e6808a5f1d2
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
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724f1d489c8c73f2562027ddadc0483e40a1d00ffb7024db1f5e79723d05ac0`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
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
$ docker pull amazoncorretto@sha256:c0bd547f4dc446b12a27b227d2b7e67cce2b1f96a90ff51051e8ad31abc3f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211824228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be2866395d7fe368648560662af3d34901630572c1d3113792c07298c94c350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b4652ba9c2363a01ecbbf5bc7812fd1c7e13aa1ecd384bb642d31db153ae2`  
		Last Modified: Thu, 23 Jan 2025 18:38:09 GMT  
		Size: 147.2 MB (147233923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93a1c442f169ad8fbb9f37ae610dec9c8e0d4a8ffd311e119c65287d81f9f86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5495628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3d7ce14b5745e25996774182306653b9e60372ce325d4098d2b08890ae703`

```dockerfile
```

-	Layers:
	-	`sha256:7df009a5ec264c3104ad1835db7afab1aaa9c0d3640a4d5a295a6376e70e9bb6`  
		Last Modified: Thu, 23 Jan 2025 18:38:02 GMT  
		Size: 5.5 MB (5486217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25e51523b379bfc27c737ed37c9cfe75b52139ba233d58560f3ef48997c9d54`  
		Last Modified: Thu, 23 Jan 2025 18:38:02 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
