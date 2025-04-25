## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3888fe8a55fbf3c52790805d5d5cef05b340aabc4431b401d0f2a65e8652e8cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b308e8a8c89feb12604159a3deb102364a345a88937c55fc4cfb12c19dc9963b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138874872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df182ccb3f0482602f41f30a561f07e3022f869faec98f8a1038133cfe1c8b25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1ea93e25ba07317935a967085c788b07bbf863c193190eb1e54a2cd9f0605b`  
		Last Modified: Thu, 24 Apr 2025 20:08:25 GMT  
		Size: 83.0 MB (82968351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:10fa5defd7f129fb3278698035fed3ef08baf47db87822010dee4c947b3034d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f81b5dc651be4e1df502a1f1ca8ebd53ebfd3c9afe13a4d246a98fda114a14f`

```dockerfile
```

-	Layers:
	-	`sha256:5fdc824e29dd71558a97506440f1995bf6b013a15e16123984585c58cf20806f`  
		Last Modified: Thu, 24 Apr 2025 20:08:18 GMT  
		Size: 5.5 MB (5451028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0f45cc899ac146f9a4b6d69e7750d85426c312c5e2a296802dbc140be3508a`  
		Last Modified: Thu, 24 Apr 2025 20:08:18 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a56b04a45aae25fe201b1461666a6b850aa2f390f38a3698e25b42f8bfbf06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137386064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97049b5885ebb990888e87fa7b304b288294639a30ec524a00c98d32647bee73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de600d7298a31b514a3066644ceb9a091b297399c1b10263359d670910478bc`  
		Last Modified: Thu, 24 Apr 2025 21:18:04 GMT  
		Size: 82.4 MB (82424585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2a3e613d78edbfb820ec05edd2ccbc1f3e0485db53ab65aab6b7324384ca95e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17faeea2b3627165d6d2a827a2be4400ae415766886a47898fa7ad706f2f4634`

```dockerfile
```

-	Layers:
	-	`sha256:2423bcab21cb44abf1a7090ae82579a7fb51b880070d9eb8edb9ab75abd59e07`  
		Last Modified: Thu, 24 Apr 2025 21:18:02 GMT  
		Size: 5.4 MB (5449819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00df92be04076917a696ff643bc5d95c1828ad9e6955f9bb0e55cd98b6dcf7ac`  
		Last Modified: Thu, 24 Apr 2025 21:18:01 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
