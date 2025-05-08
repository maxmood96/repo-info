## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:940b81a0a0a1e0bd89b5e3c98b6dc7aeb766096a4876ca40c235308f61f4b17c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ffdbef4c2d77e26e55e00d28f8740ffa1ab28c90fa7c33519245e1d013fdce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224994331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff9386b1aaa4bad33343b55806bdfa96afd60551cf643fa744c222fcf9d6418`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6959a9489c362f28710ac3f300a6cf9395856bdeecf8f5076ff553c9125ca`  
		Last Modified: Thu, 01 May 2025 21:08:30 GMT  
		Size: 162.2 MB (162235001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:59a5c79d9a3a5fd887c264764aec2820dc9f3618add7b670818a321df23ee3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5991386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e82a0d61098c2a738321cdeced6dd1928d102325fac6d19882bafe7ca7ade07`

```dockerfile
```

-	Layers:
	-	`sha256:8bc3d3776fc29b64c3f8e83d49d382c4a5d699907fe3b2aa419efc51288ec780`  
		Last Modified: Thu, 01 May 2025 21:08:27 GMT  
		Size: 6.0 MB (5981946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fade79edc3528ee3142f7baeee6c1b34d41c739d1d83e085a39431572a63c5f1`  
		Last Modified: Thu, 01 May 2025 21:08:27 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:974c01c0b82f5bd0a74d4f98290475deb80b9fd01e424b10a0c6379217761909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216972551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3328cae8c5d027032dbe583b74074787440be930fc539f76f832988382b962`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84b926fff48818fba320c848183e69a65722b329e5bb63999eaaa72d870a87e`  
		Last Modified: Thu, 01 May 2025 21:15:08 GMT  
		Size: 152.4 MB (152377824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:964b18b1f7e96a12dc295896a82f779d2095e2f8184dee523f419d33c737a005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5784180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b74c0fa7cb7a709de0ece22280ca885cad74f4012c79c4f1dc6ae2382e94e`

```dockerfile
```

-	Layers:
	-	`sha256:83db2d48ea9e72cbd78cff714750e886f2ea8bdad6004447b3c83e1c3f2700a0`  
		Last Modified: Thu, 01 May 2025 21:15:04 GMT  
		Size: 5.8 MB (5774660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:064783cd534bff3a5064b40b0a20b6eefdf4521778cdb9d4a0600d99cb82b02f`  
		Last Modified: Thu, 01 May 2025 21:15:04 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
