## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:f22240ee4be895cb3fabb90e9d4f1b3219ec2c8ef969470af41b69ade22bec15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d2b658832c62e20526d10320127117c1da06a79891871d7ec6dd697cbfb9dab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248026047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f0fef43a1940a22a5f433cd2786d62f8df43371b8558875988af4837c74f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:34 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:19:34 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:34 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b7a72c98e682d1076395e72f4c530a217dc9630b3d728f95711cc26484bec0`  
		Last Modified: Sat, 09 May 2026 00:19:59 GMT  
		Size: 193.4 MB (193449243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:953f7ae774400725b490def080d4bc44d191a4db4ddc7cf388fd68bb150186ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68782e37228ef469513d057466c3825319a96036512b17403881b8aff07892ec`

```dockerfile
```

-	Layers:
	-	`sha256:8f1f8cb505a5e52398d226c09170192678eb17cb3e3ba566d9e387d117803a7d`  
		Last Modified: Sat, 09 May 2026 00:19:55 GMT  
		Size: 5.3 MB (5332742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cec2459bf6ed047d6493a9b4b627d5b3736215cb7e711a09a09c71022e7049d`  
		Last Modified: Sat, 09 May 2026 00:19:55 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9132697d75172edd3b10ab4c4bef730437be95d9f6adf83761a241796c39a00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244730789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0633af6f2768b09b8ea61a29091089255cc3457d17ae17b13120a3959dda2ffa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:53 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:16:53 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:53 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:53 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb374f78b6fea07d5aa41abdb8393d250b82aa0fe84ab4cbca9d0fa9c26c6c6`  
		Last Modified: Sat, 09 May 2026 00:17:20 GMT  
		Size: 191.3 MB (191273814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d36c38429af1a1b00771b077372bc5d0d5e1ab3f90639bf8df530496be248268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf03ce7d1e549a08ec68cf04cffb84028b95c26fade2e190bff432beb48684f`

```dockerfile
```

-	Layers:
	-	`sha256:e0e146ea40b087965395b568412b0f85c6a1fc80edbfb7e1d33882334296a62d`  
		Last Modified: Sat, 09 May 2026 00:17:16 GMT  
		Size: 5.3 MB (5331718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f0c2eee5b342b7e390a2d1bee283ed098969f043ddfc6f4994ccaa56888b85`  
		Last Modified: Sat, 09 May 2026 00:17:15 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.in-toto+json
