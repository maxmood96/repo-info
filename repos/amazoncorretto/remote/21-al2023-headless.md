## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c598a183637711c044e1e06ba7392c97837fc99660f2074c3226d6c3b2c8620e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e3962f0cffb2b8e94bf93fc1a45aaf2a6c5d6d9ab001dae240b029525e576051
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141883147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b58fd0ded57343f01237cd3646ab02679ed49e6422b846b2082924852012cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:32 GMT
COPY dir:7cf66bb9a4300419df5b669628ccf58a30d02fe56dd9811e6baaca920acf962f in / 
# Wed, 05 Jun 2024 00:26:32 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:45:42 GMT
ARG version=21.0.3.9-1
# Wed, 05 Jun 2024 02:45:42 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:46:28 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:46:29 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:46:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f6175f9c503b77e6cec852666a7133ed71ff16fd23342bcc58c01fa48948b06f`  
		Last Modified: Tue, 28 May 2024 21:59:02 GMT  
		Size: 52.3 MB (52320215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f897c209f60338b27020c7fd4c557ab4a8523b8cc84a3c72cd4b5c43b9cecee`  
		Last Modified: Wed, 05 Jun 2024 02:57:50 GMT  
		Size: 89.6 MB (89562932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:05a3c35a658698f0236d0390294ab6eb2bfc5523388973f1c368ae9d2819fdcd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139987225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34cb07b8688a20c85d9c5ed8891a348a7707f47ef29fd12ef4e4f1d324d5e7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:36:26 GMT
ARG version=21.0.3.9-1
# Wed, 05 Jun 2024 02:36:26 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:37:04 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:37:06 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:37:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49b37818490cac1a22a4da804cac63f272d97172fce9b84926129043ffad244`  
		Last Modified: Wed, 05 Jun 2024 02:46:44 GMT  
		Size: 88.6 MB (88583347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
