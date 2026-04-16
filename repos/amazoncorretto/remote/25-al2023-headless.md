## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:9f4e1661853abd8662581cbae94cfef120f4bebaec23c62c0cff1db2514783af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1799f4f3881493590702d1b64e873b61a09fc1de1c4fa962253348f3bae65a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158180843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57f392851521d2b0fa8a60e49c3a52414f889a5581f979924dc45c2f57ffbf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:41 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:41 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:41 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853aa346d50e04c5bfe5404c3a979f5427d71af7d8c1b01ea9214641b46d34b`  
		Last Modified: Wed, 15 Apr 2026 21:27:00 GMT  
		Size: 103.6 MB (103609589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6d7bd0be72dc9d24d6cfd10bedff5a7d5d216e1ded19a95a246cea6e3a169ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4239b61921a0b12c0d85519b8fffc6aa88f9dfb6d6815b3a0f01168dc196af1`

```dockerfile
```

-	Layers:
	-	`sha256:98552fea11c05f000b6a59af947fa987bbc7c1d7a1378c5ac1846a05eedd9a73`  
		Last Modified: Wed, 15 Apr 2026 21:26:57 GMT  
		Size: 5.2 MB (5201235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc79cc4e718a2fe635b6fdb1d75b112575c5d4dc5099e78a3769c47d5f0cc508`  
		Last Modified: Wed, 15 Apr 2026 21:26:57 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0a8d4af02fa9c9bd22005013010c3424f5a9e8a8dca33871ec35ec1a9dc15f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155972746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e9cb647773cb7e2969289edbaebef910dba0f48362e7c20b5bbed6b4cbbb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:55 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:55 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:55 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:55 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5fe1e4408860d39c99166166fda2d3e79b6468aaf8ea32fac47eb22046d1c`  
		Last Modified: Wed, 15 Apr 2026 21:40:19 GMT  
		Size: 102.5 MB (102530007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0731b5f533f0ec8a69dc51b76aec47dac825426c16a981a4bd3c5e6b4ce3581f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fd6b1269b71554302427716f1f238ebec56e322942619eec5a70fadba87d7b`

```dockerfile
```

-	Layers:
	-	`sha256:dcbbebf504d016759007b135ab7db098777cd097ed79f3221e1520b83690ad40`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 5.2 MB (5200046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f298325a213357a226e11b908df809e8b585e0e2d9e6e26aad36aece44caaa99`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
