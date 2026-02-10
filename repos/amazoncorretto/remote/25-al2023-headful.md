## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:02e3e53f4862775ae63b937dd4bdbc18ab7b93b2b46b8a9401dd14d022c9be32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5eff3f39a822927138e0944e51decf060571bc41c098f45ea24e1d214333561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158370378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd75c8a2648b7397724e72fbd9bebc39ec78751673fcf7f351b819d3cbf5920`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:22 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:22 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:22 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:22 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cf02850ea1deec7d720dc0d326dc96bbf11ce06b8490ab5b4bbe62d087a50f`  
		Last Modified: Tue, 10 Feb 2026 18:32:42 GMT  
		Size: 104.3 MB (104332150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fceab82eb9b3702c04a622255adbf23ff68eb8a5918a133fb4acc5cfb20dc497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a63659bee391986a54ee3fd5f2843b16f6a24e4d969110b6509c1553bdb78a1`

```dockerfile
```

-	Layers:
	-	`sha256:4a67db72cdceeb46aa8358324d8fafadbe447d87b5f1f3163a905e9d205c23e2`  
		Last Modified: Tue, 10 Feb 2026 18:32:40 GMT  
		Size: 5.2 MB (5220218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba5aebe3444dd60080fd40b0e81c3591373768da08ab54c95ff4385b334007c`  
		Last Modified: Tue, 10 Feb 2026 18:32:39 GMT  
		Size: 9.2 KB (9212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b2b6afc69a00e645bdcdcc752ea3bb03468977f3169943b711585988a0004113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156182414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715fef8337aac34110f4bbab5d303b2ae3be9b11e3ff258865d25a18294e8847`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:13 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:13 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:13 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01325da1d5b8d25b4493330720e6a4073449fabcfc6d5ca778274bd4f496fcec`  
		Last Modified: Tue, 10 Feb 2026 18:32:33 GMT  
		Size: 103.3 MB (103264203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f63f55d3437797445aa48b87111da627bf6550433827e639022f09f9fddbe157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc671f606d66a0b274e0b2324d66ce55750fa6098590e996b27f27f9d41dfe0`

```dockerfile
```

-	Layers:
	-	`sha256:71ffe53c33d73af0e751bcd929099ac348e8026420a81dbce2ee23255d003aad`  
		Last Modified: Tue, 10 Feb 2026 18:32:30 GMT  
		Size: 5.2 MB (5219032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187ba773ec1f6e66a335324574bd419087c12e5eabb7fa724dfc1cc9f6e2b719`  
		Last Modified: Tue, 10 Feb 2026 18:32:30 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json
