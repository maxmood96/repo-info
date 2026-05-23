## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:7d33b3b5731460478abebf2e6eb6760ed3fe013dea2c09666ac907a1d3405763
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:df6d2fed37c2f6e5a4d27be9644d90f1b6c80692bfdd1b5cd6a3586dff1bedcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188317945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ee1752e7ecf26e95e97f2493b470f647f9eb8eded54c60067e860dc1599656`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:08 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:11:08 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:11:08 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3002d48776a0ccd49531a817733df159775e8aec29dad417f7eab14b8a1ea3a4`  
		Last Modified: Fri, 22 May 2026 21:11:30 GMT  
		Size: 125.4 MB (125365970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e8593a7289dfef3abd4e7827e7dfa6dc6e1486ed4eede786278d459f30d4cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c6fe7f6ad24763964f679f71fdaebf117a2734f6be3642dc760f1a6752fc73`

```dockerfile
```

-	Layers:
	-	`sha256:c8f1ee62d0d592a127deb6e5a63b93237482a4a5b97562600d2a96614cc07ae1`  
		Last Modified: Fri, 22 May 2026 21:11:28 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf2e55d54afb860e0e542563cf22b52aa57f3ceea222fd6fdb571b402101e61`  
		Last Modified: Fri, 22 May 2026 21:11:27 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b436e90fa24dc2bcd54f7062be4222a6e3ee0a850809047b8777304e8b73c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132468719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba17f9557f307b5d828d00936b0704ed8f71305c2ca7c3ffdcd0c63f657c3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:38 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:38 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:10:38 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b8d9b174c81f89cf2170671976c6c801fedd8756d36e540990c95544020807`  
		Last Modified: Fri, 22 May 2026 21:10:54 GMT  
		Size: 67.7 MB (67678702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4bf8a9e850d6e23e0821a04b2ddd58e1a1ae8b1f08f3a9335b6d9cf037cc628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c678b78342f47367e1c09ca2e9ef176dd4d6e895a07575834a50af2b585ab40a`

```dockerfile
```

-	Layers:
	-	`sha256:aa07857ffa0d9039e67023294b429ff089e5e1f3114680b87e02de8ad0d9767b`  
		Last Modified: Fri, 22 May 2026 21:10:53 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c36c3c366b6d7829cbedf8776cd3b3c352806bf1fc45582a3526ea40aeae72`  
		Last Modified: Fri, 22 May 2026 21:10:52 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
