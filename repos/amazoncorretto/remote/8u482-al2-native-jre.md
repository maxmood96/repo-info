## `amazoncorretto:8u482-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:3f1d89c8677d96a50e4b2aaabe968e5d2ea78889ad3e7a3765562dd715d5296c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a1432acb684682fd883b9d894b9725ab65daf6e9e32083f305fbfa7a48bc65de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172087368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c2c1143bc7c1e8eda41de97a622cf901b65b8ea1c4bf98cf4ff23626b1724`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:55 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:13:55 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:55 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be6a24514775dafe31132c16c072ee73ce9ff1bb7542efb5c612b55f6d850cf`  
		Last Modified: Fri, 03 Apr 2026 22:14:16 GMT  
		Size: 109.1 MB (109132067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98f12d905aed9b699a520a5fdf5521f52f7482e985c0ecc5f36707d39ae076ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9449c142a4ba89a448ca5e2669f2774a6a6127577ebca1ba23a9fb41711029`

```dockerfile
```

-	Layers:
	-	`sha256:c52342ec0a0519f84f9b627cd1ed9ed681be50699d28a048946708c223fe60cd`  
		Last Modified: Fri, 03 Apr 2026 22:14:14 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5613b9ec8d422de8c698910f71f9683690c415372edd1c6de8028c24d2ffe38`  
		Last Modified: Fri, 03 Apr 2026 22:14:13 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9775998bfcfbd8cb6ab98a3f8a82c88c2ac6057bbcdc11de37a42ebae551bef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117771788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddda5d47b76c0e9940a46dd2c4d27cc159fd61f4c7a398a7f29e58ac25ec8b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:11:24 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:11:24 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:11:24 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:11:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c03747e2a1ee229fa783d5327a70626f629f936c23ba140f63a84d8774b3991`  
		Last Modified: Fri, 03 Apr 2026 22:11:39 GMT  
		Size: 53.0 MB (52968949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d1f9934e4afd05527b4d20d14852d406df1aba1db39d8708361b1dfd831b10b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432079b3c7b14051f4803b42c8a208c11a43533005b5b563ff56d805d551d557`

```dockerfile
```

-	Layers:
	-	`sha256:99596b0ea617440576e441a3ac300f5e917a44bcd1a2b1d9760e455e9e5155c4`  
		Last Modified: Fri, 03 Apr 2026 22:11:37 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cef643085b0f4408c56491bb54ccf2cc7d292d3882e0af77b0f3927db022f57`  
		Last Modified: Fri, 03 Apr 2026 22:11:37 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
