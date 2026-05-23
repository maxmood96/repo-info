## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:8e828e8141e9afd3fbc49b780136527de694f2c54b7ce2665d221a711d66c110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:331fad4ed9659b3094e3256db0235022c1b07396b42ea45e99764ec740aad4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172098653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24437d37fd022e7d70d53cbd9a081959784df6de9302004446e2ddada17a734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:42 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:42 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:10:42 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2fbdf89cea0200d7bd9519e4faaa5a36d2e4c1d6a5dfbe062b77c1cd6b6b45`  
		Last Modified: Fri, 22 May 2026 21:11:03 GMT  
		Size: 109.1 MB (109146678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9365b7dd2de6d293a61134c0f11c213afe2e083c0e4fc0a4d544c49f95c2e5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e00d9a09bf2300543b33a98e295f2e33253a6b753beb34b8fab06c6cc3340`

```dockerfile
```

-	Layers:
	-	`sha256:ebf46d44e46156f6dc115cc05e2f44696760d5092cc86d2b75cab59214526f49`  
		Last Modified: Fri, 22 May 2026 21:11:01 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0607d25395748de26bdd9b4fd304de14d3f9398c439e2c87f4106f62858a22`  
		Last Modified: Fri, 22 May 2026 21:11:01 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f26228058f1b0343ad7250214ce25da40cea63d04eff32527a45302dd50226a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117739912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f976e3780052a5789283fd0e6e8f8e85e4c1a0a335ff965b2dc15a27ded877e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:35 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:35 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:10:35 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8b2f3cfe1bce7b6d3fa8af89137a03325a619ac1d920eedb2680f0fa924e1e`  
		Last Modified: Fri, 22 May 2026 21:10:51 GMT  
		Size: 52.9 MB (52949895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0d0ca84fc65a15126a6473c537cf2b0b1ec88a248d194ff7ad9483325b1da019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d1bec71efb0f6d7eead367ef400bdc97476bfa92ce09767b9119628c529d4`

```dockerfile
```

-	Layers:
	-	`sha256:ba9642bdb82c25bc0c47b2ac1fa446838e89b0deb1cf2fa0e953d9deefe270ee`  
		Last Modified: Fri, 22 May 2026 21:10:48 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed6954408bea66b49f45a1c4c902604bb28693d499123014a7d4617b6d1fd68`  
		Last Modified: Fri, 22 May 2026 21:10:48 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
