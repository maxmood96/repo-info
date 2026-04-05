## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:09d60512d3cb5647ed23e53c4d4d305a57adbbb2a7b10f68bd26fdc7c9477e7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d76e98e7aca942ca22155ad6df47239ad8f7b36ff95c378940f1780ea61191fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224579336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb96109e9e2e8a39bcfa9ec557489e6a5e3557c436cc1ed245ffaf1f8f09c8de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:59 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:59 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:59 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0753827b962eb4a9718cfdf9d078c9750b20a9eec08727aecc5b10256088465`  
		Last Modified: Fri, 03 Apr 2026 22:14:22 GMT  
		Size: 161.6 MB (161624035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be0b494a840faff6f1d1a38cd79d771bc85318680dbd1de9ac13f6f1292f02e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a57eda2b4d14a137172267e97f7894c514b8fac759d99266022e6704792a445`

```dockerfile
```

-	Layers:
	-	`sha256:6b845ef168f1b2f342b894407c488c5f0405a8e1ad688eb0f67691480a79aea5`  
		Last Modified: Fri, 03 Apr 2026 22:14:19 GMT  
		Size: 6.0 MB (5995179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b383853cdcb05f182887ea6ad06cd842e62f19bd0ec81878aa5b4d04cb3e66f`  
		Last Modified: Fri, 03 Apr 2026 22:14:18 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6ee9cec82295d8628e8ac76967779854948d2dbed869b217927af17256ba77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa200eeba272a7aaa48b2299bae7e55c9afb466b4de2a846540b7c16b4ee5870`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:51 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effdb2f538696eab9fab37e47aa9ab9b206b06ad1a434f67b78fc1fcb3788c19`  
		Last Modified: Fri, 03 Apr 2026 22:14:13 GMT  
		Size: 151.7 MB (151702278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:961e68a17ad7892c28993d6626dc505a63f384dc7979be4f8bb58fb081e502c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ededc6d14d62d48f89e55d80e977d774a43c7709bcca4b77d27071781b9f850a`

```dockerfile
```

-	Layers:
	-	`sha256:c3537900104f08c7588c787e13b81cb0cfe6f462cac21329f66f513dbd465f23`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 5.8 MB (5787893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c603fa3e5fe5696b7f6ea498ae3d9ccbb13abe4eb1597779ec941a841fef098`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 9.6 KB (9634 bytes)  
		MIME: application/vnd.in-toto+json
