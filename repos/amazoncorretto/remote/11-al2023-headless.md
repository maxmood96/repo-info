## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:37a5e39da470cefe4241eda07f5150bfe03ed055d4f1790d26e1d8295f0fa261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d292d3a3b8a83e8ab2bad4d6437d5a054bb541bd4958c9956a6c3bc84bfe1347
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128472662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89293ed71d0d891a8d3c781057f68fcb1db56b7908b35a09703f998ee02e081a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:32 GMT
COPY dir:7cf66bb9a4300419df5b669628ccf58a30d02fe56dd9811e6baaca920acf962f in / 
# Wed, 05 Jun 2024 00:26:32 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:38:21 GMT
ARG version=11.0.23.9-1
# Wed, 05 Jun 2024 02:39:07 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:39:07 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:39:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f6175f9c503b77e6cec852666a7133ed71ff16fd23342bcc58c01fa48948b06f`  
		Last Modified: Tue, 28 May 2024 21:59:02 GMT  
		Size: 52.3 MB (52320215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf83850824d09f99084465f63c28b706e549f09590a26e2c0c47598e61022e1`  
		Last Modified: Wed, 05 Jun 2024 02:53:00 GMT  
		Size: 76.2 MB (76152447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dff4e54a2433bf86b7ecab8a0605a29317ec2f861cd69eaf5938ee8e833d4666
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126705673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc82a28e2333c09f6bccfdb156d83cc7408009cb9b3470be13717d1ae95c33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:30:52 GMT
ARG version=11.0.23.9-1
# Wed, 05 Jun 2024 02:31:30 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:31:31 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:31:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5977f4615516a16a60c2960c6cde948b84a0ba17457850ef893e446c9e3ad58`  
		Last Modified: Wed, 05 Jun 2024 02:42:32 GMT  
		Size: 75.3 MB (75301795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
