## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2167548294e5793c731f5b2e229a2209f161c41ea551631876174e2b209bedb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0cb5d8306741b80e9e37a9bf40932b59222b5ed73e9bdc611541d56b9e318df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137059688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44fd06d3810cb9acd30a50ae1a3c5028d86bd3ccfeefa3a963ab4447e8a4c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:23 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:23 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:15:23 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:23 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0180cc14fad3d225fea8639275bd98edaaddfc3e71b14f915d5fd7eb24665877`  
		Last Modified: Tue, 16 Jun 2026 01:15:40 GMT  
		Size: 82.5 MB (82488532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e18b162e71cafbfae24891c6c5572dd64d357133deab4aab6b3eaf255df087f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171832d3dfe4b66e5a1a535952c89d42d2ec39742025e160c52636e58b49d444`

```dockerfile
```

-	Layers:
	-	`sha256:9b756ca795f0d86612d130e5eaf39b9a5a6265104cb8e7c35a7c06d541e9ce42`  
		Last Modified: Tue, 16 Jun 2026 01:15:38 GMT  
		Size: 5.2 MB (5190163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb6610ef8f8dbf88041bc3dbe72c3497984bd47480945e0562051d9a0d0864c`  
		Last Modified: Tue, 16 Jun 2026 01:15:38 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7e732ecbbf0c93e4e50a57bf2d1b6375944ce2d5b04933a7031a81132cf04eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135356504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc250e32fa7cd35d99d1220fc434621902b54cb2b15f533909a5f2ea11cc517`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:36 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:36 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:36 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:36 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f78132a4de0b08181d1e641950770e0450d015465b62cb012e5d9d95768f1c4`  
		Last Modified: Tue, 16 Jun 2026 01:16:54 GMT  
		Size: 81.9 MB (81898677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:831c648050e65ec487a1b748d611ecf252873c5148bc5d3121d6076f0d6ba6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71454d899ff25c8e705a57e8439d0653a7d9fb5c4107f011eafab75c7380f79c`

```dockerfile
```

-	Layers:
	-	`sha256:005c660d1c78f238fc6d6f19d0d5a391ed5a81216861ab8b7deee8eb6f8b32c4`  
		Last Modified: Tue, 16 Jun 2026 01:16:53 GMT  
		Size: 5.2 MB (5188952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e320621b1ca704d4eecb7bb46712cf53e9eda20fc919640d81864bdee3c7f060`  
		Last Modified: Tue, 16 Jun 2026 01:16:52 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
