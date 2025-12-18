## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6cf6de52f1c44fbe9c949bb442844bf3b43cc74063dca0277bb10995fde7b45e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8b37478e4fdf4f0935ce01700a755bbede619314ed414379b78e72b0d3e4aebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143235199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b846eb455e8d426bfdac6cd949430a435be479f38794cee88af0fa9b53a612`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:44 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:18:44 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:44 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:44 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a8f79a921b094fbf654eb084ef862cc456685c4ddd64672f4830f3cade1ee`  
		Last Modified: Thu, 18 Dec 2025 01:19:17 GMT  
		Size: 89.2 MB (89246739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c6d6143dbb20de2fd88bf01a3da3094d5b890dfc3d296a0f75d73660895f2bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115d9a4fc528db8dd0ef040a0118dc641f790e24e9ae4b82419283a5fe7aaecd`

```dockerfile
```

-	Layers:
	-	`sha256:f7d8a1b49460ebdb9339b464ed40faaef04d2300af1af039acf3cca658368387`  
		Last Modified: Thu, 18 Dec 2025 04:50:23 GMT  
		Size: 5.2 MB (5184514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4617dcc1629ed0a5f08aee7d0735a2172dd91b28352398201478ddf730ff55`  
		Last Modified: Thu, 18 Dec 2025 04:50:24 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56c3142cce163254ecb80cd3b683aff2b3c14e99949b9bbb4214e911809bf7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141234425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ee8dde9bcc9378f5504d14c982780e329cc6118d28fd3a302237e9f8a5d2de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:27:25 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:27:25 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:27:25 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:27:25 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:27:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd5913b63802f69b9e0359ab1a1ba7e653202945aff75833f32cd0e93f6dfe7`  
		Last Modified: Thu, 18 Dec 2025 01:27:58 GMT  
		Size: 88.4 MB (88360975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:822824fa1e7e58887edc8cccceb87894350b89a324d3ccfc3f40accb9273e1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0cf5e6062daaffd0b2be3bd59bbd53451779ad9a3e6f0e8dd0873aa8c78e69`

```dockerfile
```

-	Layers:
	-	`sha256:0ae85c45aa4280986f4325dc729e68ea2468b7bd777a485bafb99276c983ce26`  
		Last Modified: Thu, 18 Dec 2025 04:50:29 GMT  
		Size: 5.2 MB (5183304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4ca2114d2e04a5aafca6785cad878bf5642309606acb5d357c06464c787260`  
		Last Modified: Thu, 18 Dec 2025 04:50:30 GMT  
		Size: 8.8 KB (8786 bytes)  
		MIME: application/vnd.in-toto+json
