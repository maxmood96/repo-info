## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ed1e531b4d368d39f6c792e082b804f4b959970285932063e9329aa936a73045
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd0a122bf3cdc56b9103934c104df8583ad72379224e4c89c225c20f5e25736c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144543095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be3f3b3ded3a15de8a8a53cde39d560c37ef75bfd7959e63f547d25e3e5c747`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:52 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:52 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:52 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:52 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ba1b5780f977493686e4898a2aa1c8ac85e95497ba06de72eb0d7fe697b75`  
		Last Modified: Fri, 03 Apr 2026 22:15:09 GMT  
		Size: 90.0 MB (89971792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c063a560ca7d195c47537b049cc76ff688221ff322986342acfb730b01e4d090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adad2b2e2246fb32fa43f8a094ca4397115fa51b7d354eefa4fdfb82cd682ede`

```dockerfile
```

-	Layers:
	-	`sha256:62d2d6cafc5478ff3f51c2b32d716d481f03ad7999dc98c88c43a1166c4a2a4f`  
		Last Modified: Fri, 03 Apr 2026 22:15:07 GMT  
		Size: 5.2 MB (5216395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df1787c0956d9b38bd63815f09dd22b4471340517de1bd206028f883bdbedb7d`  
		Last Modified: Fri, 03 Apr 2026 22:15:07 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:52534511e5b269136d5d43fb7d59e4e6c575d01d1c72671289a69487e5bd16a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142555949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac589f73e20b00e0ab0e02b9b7584f8e7742b88ef488514ca44caa5330bbd87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:36 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:36 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:36 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550f66a69b6d7f9ca8bfb33454ad9bbdf9dd940f8c3d6f46010ff3338aeffae1`  
		Last Modified: Fri, 03 Apr 2026 22:14:55 GMT  
		Size: 89.1 MB (89113124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e736420b173fc37eed03c1acccd9dd398f50ff127276c7a96e28a8a0e8531fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896d116980a3ac1ef50f66973c6dc8262c19800228e9241c2f7da86d8014076`

```dockerfile
```

-	Layers:
	-	`sha256:d892b247f637308e9e59e768adb782534572ea90791a6f342d5dcf7ac2ecbdb3`  
		Last Modified: Fri, 03 Apr 2026 22:14:53 GMT  
		Size: 5.2 MB (5215188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88dae18be11a1d22e64364b654b7139a491acef955eb529a2d91b94117e87fc5`  
		Last Modified: Fri, 03 Apr 2026 22:14:52 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json
