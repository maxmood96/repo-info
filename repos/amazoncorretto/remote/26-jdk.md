## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:4c445efde5dc4feaf37706cc941efe01d715543d49e274ee36aca204c5c8552a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a38ca48f6f71ea36bee8baf58e323b3a30d77872a68228c5197fb669601866e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248023991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f2b1c99874773bccbe07ae87a83a8d248f422c632ea538bbade3af5b3e8e97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:05:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89540e7f1948b9cdfd916831c36aadc51bc055ba3210b16a29c727cca6e3c68`  
		Last Modified: Mon, 22 Jun 2026 18:06:04 GMT  
		Size: 193.4 MB (193449808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97680c0969059b623ae1f9f093c3c9049f4dd65bfffe5413162da35346f082c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ea99423f586444756affab9c086d915fbda941ad5afca2dae202dfa2b60dcd`

```dockerfile
```

-	Layers:
	-	`sha256:fe005c2317bc9ecbdc91c19cb77e4c959492850387e78e3af72a61b8422c62b6`  
		Last Modified: Mon, 22 Jun 2026 18:05:59 GMT  
		Size: 5.3 MB (5338500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8722423ba5bf136f8392aca820f9a1ad863e301fef29a7a4cd1788a23590e73`  
		Last Modified: Mon, 22 Jun 2026 18:05:59 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8f7c75c601fdc03c99bc75588d1271438e06435e5bcf1e9b061bc94d3229a131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244724085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13947b0e1e4c39e726ccbaa1ac43acbbf13045e4b40de8dea4377cb4e6ced09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:15:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d96dfa1bda3810217adf300288ddcf0930ea9cdb2f132ac9d7c70180a735c41`  
		Last Modified: Mon, 22 Jun 2026 18:16:07 GMT  
		Size: 191.3 MB (191273399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9f7e79debebf98625fdc189528f7df18e624fe85aa5985249cfb8dbd8678259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2509ed87478473ca545ebb9ca45697ca6e52d93b82e499c44838ec7a44fd34f9`

```dockerfile
```

-	Layers:
	-	`sha256:f2996842cb264e94a24cc75976a023fcfa907fcfa52d90d17b876a4e3ae70197`  
		Last Modified: Mon, 22 Jun 2026 18:16:03 GMT  
		Size: 5.3 MB (5337476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421906244dcc98d201977694fa6c8f4c5b125702253e557dcfafc4461b7a515c`  
		Last Modified: Mon, 22 Jun 2026 18:16:02 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.in-toto+json
