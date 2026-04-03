## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b4e52baaf64af429bc196dc6700c31dc9ba5fb3c77622ffeea412818d0ad846e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6704d5629e8532d34ccf80a7b595b2aa2bb1b27db2c234ee90daa53c6dd06a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130036263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c7ce5f3d0966b0acbc2578d0d0fe1c1b81749c930874a241fc7440be996061`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:06:53 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:06:53 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:06:53 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:06:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bac8c04b715a0a92140a451596dc31a9925019aeba51d0ef50c492d4e0e749f`  
		Last Modified: Fri, 03 Apr 2026 17:07:08 GMT  
		Size: 76.0 MB (76003173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1a5e12fb035f7a7e4853a0a125a4fd5e369e4d56b490bf5de9c31511266aa2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f6a79ee59cad8f41bfb2640b5bef7a136007721984c5cc09768e077d4efd5`

```dockerfile
```

-	Layers:
	-	`sha256:8b61a18880485691c7395b2e54525ff01760996bdfe64921aa65e18ad1be92a8`  
		Last Modified: Fri, 03 Apr 2026 17:07:07 GMT  
		Size: 5.2 MB (5196893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580989724203f80efa41c72e30bea32c4a571976cae293fd235c87ac85aa99e7`  
		Last Modified: Fri, 03 Apr 2026 17:07:06 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18141293ece4e06d65bf3dba93eb497bc860ece7b418604557b1cee3447252be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128179728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d67560f8c3c90c594944d837f92170dbc0c7430ec094bd4904ee3218c0d50ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:14:26 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:14:26 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:14:26 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:14:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19aecf3d4baaa063dc28e6df10580eb40d1f49d68a6b02d62fa4d16f98f770f`  
		Last Modified: Fri, 03 Apr 2026 17:14:43 GMT  
		Size: 75.2 MB (75238353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ffe6ed2d1df487cd993b4ff1a5675c82be09bba0494a12788cd322047efc41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a50bf620aef754f32cb301e26e1ac9517212452321f8e89a5afb38dd5c5603`

```dockerfile
```

-	Layers:
	-	`sha256:69a432a43218788cf5dde12c90e39a39a5ffa571a8704a301643c23f2b1c44c4`  
		Last Modified: Fri, 03 Apr 2026 17:14:41 GMT  
		Size: 5.2 MB (5196511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1786dce0f25552294b99a3e88cdc454a4715531ac9a299924245f5f2aa41c042`  
		Last Modified: Fri, 03 Apr 2026 17:14:41 GMT  
		Size: 8.9 KB (8858 bytes)  
		MIME: application/vnd.in-toto+json
