## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:d8d9b48cef26092264d75b3d7746ff88438e6b51194888eff5cb7e55cff08efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e3479ea8bffc2928f9f784d6d625e7863bc314b513bc76ba3ea5242d0cc427f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225209828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53195aba187ba14d8c0bba40ba5690abfd76161ba390a80eaea4dc0e58b6b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34265b625e179f45ebca683eadab70a376ab4d7cb11e55f10d881fb73d3f1872`  
		Last Modified: Fri, 13 Jun 2025 21:00:32 GMT  
		Size: 162.2 MB (162246889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cb7cbeb207732a5d32b8e437f30bdc483625241cee43c06eb8471721609e30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79f071584a8970162f28b613bfd2d3a49ac98fbf0e7da1a38bed574e5f1bc56`

```dockerfile
```

-	Layers:
	-	`sha256:c7ee1166c1ce1725411f9d1b44507ba99f4d5256c9732b3107a9705640124062`  
		Last Modified: Fri, 13 Jun 2025 18:47:29 GMT  
		Size: 6.0 MB (5995078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3b3437f0d8325aec7fe44f02904176d96da60a8ad87f4dcacc1832e0808356`  
		Last Modified: Fri, 13 Jun 2025 18:47:30 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3d70b8bc5501184915fe8bcebcdbb019a3f4cc66b030160f0b475a68db60206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217143994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8581cf88c6773192b1fff5c96654c7a7558da4a4d184223a921f17c2ea17e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570dcc04c162533fd71f00dea139dc5f5c14da59b928540e9f28ec745b1efa4e`  
		Last Modified: Fri, 13 Jun 2025 19:57:09 GMT  
		Size: 152.4 MB (152353248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e81829230190e4a14652dd1c2b81fba36fc6dd96d4f835dc6f8862a221200d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fc6f6037bc76ab4aa71371e11739352dbff229a0bf5b4a66d243fa339d27ef`

```dockerfile
```

-	Layers:
	-	`sha256:eab635a3f72827db3ec0201791da4a3b3be86ab008e8e66f8e708946dfaf6bce`  
		Last Modified: Fri, 13 Jun 2025 21:47:38 GMT  
		Size: 5.8 MB (5787792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3741a6861840bc3992cd58323c0a573b4629c2866c4228042db79bafc9357755`  
		Last Modified: Fri, 13 Jun 2025 21:47:38 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
