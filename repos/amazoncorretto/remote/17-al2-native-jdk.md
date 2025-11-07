## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:1769280147c4b89a1232f1b550ccd675332560c7f424c00bb534d797a83e60af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99fc16ee14c94e90417692aa53df8b8ced88638733a6c86d70115cb462922998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228677752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2c03100f864060ed54d872697c32ea044eadf42e942e4ffc363d1f8352269`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:23 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:15:23 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:15:23 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a099d39d84473db4a8e349ea46e620816b3e5a8450e70bbf02fbf6fdda9dd`  
		Last Modified: Fri, 07 Nov 2025 01:50:59 GMT  
		Size: 165.7 MB (165743618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:242d8fc915c690d2c034ca10174e637e8c1988fb7d670d94f76b6db1d7194ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e5cad14f40dde40c9d25687775541540a01244d622d3df1d34edd264dae40b`

```dockerfile
```

-	Layers:
	-	`sha256:453cef9352b8d178653d02d93d541ba73918c19eb1754fbedccec69dd8ca12e9`  
		Last Modified: Fri, 07 Nov 2025 01:49:07 GMT  
		Size: 6.0 MB (5971820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97aa678429b8bf936a1d82cd1ff35624aa18a48263f50a27f8a69fde3410e45d`  
		Last Modified: Fri, 07 Nov 2025 01:49:08 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c69bed642f30d52297427801981532c7538b3d778166d5d984ca250705a54f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221064211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62649f3b311f9dcad928e80bca5634f0e52238fc548be1af19f1f71160c52bde`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:14 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:14:14 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:14:14 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8312c9516736298003cb019cbdb63af7dc8a2de59a12b1b9a5f125e26c111941`  
		Last Modified: Fri, 07 Nov 2025 05:16:12 GMT  
		Size: 156.3 MB (156270915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd07b7853576f45e87655a027b8ef4d51173de6b0917b740aef0389a90e4e09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da6c8c477b374faeb4d4e88e6ad4d74d88c55a610d015893b3a5853b3385abe`

```dockerfile
```

-	Layers:
	-	`sha256:34bc8369342e5bb3c9be5cdb4635af79ac70c5f71d75b9632698c86e536d6059`  
		Last Modified: Fri, 07 Nov 2025 01:49:14 GMT  
		Size: 5.8 MB (5763690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b8d6fc9d92bac6a0ae568dd8f09c7c53f61fd7dcccc71f605aa4c7810692e5d`  
		Last Modified: Fri, 07 Nov 2025 01:49:15 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.in-toto+json
