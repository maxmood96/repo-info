## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:23ee6188ec59b29a34b0947ee75df7519e444361e7ddebb07ebd36ab924aa91b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d8adca86994d7ba621feb3ffc952f702a20a4ac4b5baa36bb663508129046236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146281146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82963f7ca937e59a6d4a5b369c644b502c4360327e503f5616a855214b1b5696`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fc28191fc77de6bd2f6b076f8240d520398480018f2a3466cef7f8e7702a6`  
		Last Modified: Mon, 10 Feb 2025 20:08:51 GMT  
		Size: 93.1 MB (93130563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20d2b0612c5d02fbc6061c2876084850eca15508f8b7bff70ae9c030301841b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eff615ac24f2aecd8c4aa5ce88f28703b2527f5cb247b685b0c419624e81f52`

```dockerfile
```

-	Layers:
	-	`sha256:7336e94892266e99883e3e3f4a9f0f0a79494973357ba2bb72520e12deee2892`  
		Last Modified: Mon, 10 Feb 2025 20:08:49 GMT  
		Size: 5.2 MB (5164154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f605364427fab96789556c4b3ddca7a75b8ae3f6e5b82dd1382ee19244b8f9`  
		Last Modified: Mon, 10 Feb 2025 20:08:48 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:690f85037ae179a004b70140187dda1fadeae2bdc35136f8959681e7eda3f278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144408480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e990f933613f7380fc77cbb7c753c60d6fd7036dfdf75f1fd4ad59716b6f97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6a5b8bb929cb2e230733e1ffd40f96a926f60841519bb84c519d2e8c0421c9`  
		Last Modified: Mon, 10 Feb 2025 20:30:29 GMT  
		Size: 92.1 MB (92137529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:260ab53e67af41b42b3998f9454a5b918e5efd9c74a2bbfa1a62096760c87371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ff2644f935741241645ee524568ca8b738d4ba5735cd8be28c99bbdf45003`

```dockerfile
```

-	Layers:
	-	`sha256:494d559b98e35cba0c614c2bfce47861d65c929c7bcc84f87cee7fc93b46f06d`  
		Last Modified: Mon, 10 Feb 2025 20:30:27 GMT  
		Size: 5.2 MB (5162143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b61f5802a6844e45f6550be25ec274447ab4f0282aeb0de689faa6341d131f3`  
		Last Modified: Mon, 10 Feb 2025 20:30:26 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
