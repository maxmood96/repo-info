## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:ace2eb6ee5934b3453760909c6880e8cd5f0942048991e41f1fe1ed0f9a0a374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:a5d6d6047ab90b65e74621ff7fead695e79e058989cadda878bf33a55f428514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273416963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cf18dc0a497e230753ec7dfc8e2bdf3643a6fee44613f8ee190da0ab2804fb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:52:39 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 00:52:39 GMT
ARG package_version=1
# Sat, 23 Sep 2023 00:53:01 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:53:01 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:53:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 27 Sep 2023 20:52:22 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 27 Sep 2023 20:52:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 27 Sep 2023 20:52:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 27 Sep 2023 20:52:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 27 Sep 2023 20:52:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 27 Sep 2023 20:52:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 27 Sep 2023 20:52:22 GMT
ARG MAVEN_VERSION=3.9.4
# Wed, 27 Sep 2023 20:52:22 GMT
ARG USER_HOME_DIR=/root
# Wed, 27 Sep 2023 20:52:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 27 Sep 2023 20:52:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 27 Sep 2023 20:52:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a770b2366df61a5ec8acef9d3568998b51764afbcfccc3a75611e3301d684ee`  
		Last Modified: Sat, 23 Sep 2023 01:04:50 GMT  
		Size: 170.3 MB (170342216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df08d52c91b1a712403c2d29db7b5c65c185a080d60e14024b1a63d60767d142`  
		Last Modified: Thu, 28 Sep 2023 20:33:56 GMT  
		Size: 41.3 MB (41290871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db70381512a6fe46d6f4f61f23f62f8dadd6c28f0a484fa5d55dab26c0a0b509`  
		Last Modified: Thu, 28 Sep 2023 20:34:37 GMT  
		Size: 9.4 MB (9406408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6257306fd23da3cba0603b51be17ab82d76c43f2db098ad41abd98aad6d8994`  
		Last Modified: Thu, 28 Sep 2023 20:33:50 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf8847144370e99997e98ba1bc22be4fa05a3255ec0da971015178dbb83d090`  
		Last Modified: Thu, 28 Sep 2023 20:33:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8b5c5255c21008bf0fbe8a4937abf855323ce9d9c2d50a2d4900be7f107a00`  
		Last Modified: Thu, 28 Sep 2023 20:33:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
