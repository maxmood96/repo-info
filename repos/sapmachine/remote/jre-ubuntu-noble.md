## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:1cd692d96b4182632c0301e43166f2d40dfd5ed37627b8db1551d27953be588a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:61f5f4f10368a0e3e04bfa321c7bde735fdb2171d636c7ed04af0108b1afde39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89497580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a4bdcfdb5a5f514dfecc431cd7ae862c9e1c344522471a80399b51b493786`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6533af0a9e96bc7ab0167ab039cf4d7e96e9f70d7d96cafe434dcdc9da6c581`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 59.7 MB (59747720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f905a9d83179ef1ccb7d48bad49674f832489dfc3a4e551b911b742446559b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccb3ce3b1453eff0398bc4b745c9fe10a68efcf201974ac90703747e8507af4`

```dockerfile
```

-	Layers:
	-	`sha256:856564bf94ce0e58443532f0cc7d13a2d3d116f67bd4bb4dbcfa959a0fc1cd5f`  
		Last Modified: Wed, 02 Oct 2024 01:59:56 GMT  
		Size: 2.4 MB (2365887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8826fa3ae1bf37e338e1bac168b10a98a032dce57ce36ef82f14419e86170b4`  
		Last Modified: Wed, 02 Oct 2024 01:59:56 GMT  
		Size: 9.2 KB (9161 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0593eea706b84b06649741799e7532c9268141278c77397a94129f2eea868eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87695259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61b8acb9e5654f5905cfffb0164eca0558929e7cf21a6400201eb714e276a4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df2b3aaccd38a25269ff56c65b97c7c1c651a2fd094c992a6bbe5f173346df7`  
		Last Modified: Wed, 02 Oct 2024 03:43:43 GMT  
		Size: 58.8 MB (58809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f74e7d4a48482e65305d6bf6b43b77117cd2cbd515c5ed50fd7d12535bc671d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a20f769644efd44a46c6e98f837502e6723807801a657fb475c52a3865303bb`

```dockerfile
```

-	Layers:
	-	`sha256:08be3a64ade88af4713d1259ea8a45f23dc6df31912093ce83cb9af50a372776`  
		Last Modified: Wed, 02 Oct 2024 03:43:42 GMT  
		Size: 2.4 MB (2365747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4cd3332a68aa685e8e4609f23d0eb3b36740080c4138e5dac142327f7fc3f8`  
		Last Modified: Wed, 02 Oct 2024 03:43:41 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8cf803a2ac2000f799e645961bccbc5e386c52332f86b2865f3b8ac041b0f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95678066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a201248330a37f9a4ea093b68d141750d9bf3568bfb67ce3558f9dbadf0e7738`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdf8a8e6ff35c8ea018242e2d4c30950d430153d0c4c8ccf332dd7368310c6a`  
		Last Modified: Wed, 02 Oct 2024 02:48:26 GMT  
		Size: 61.3 MB (61286045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0696df683cac476da31c88a75707ca1029965f84112ac778bd63fb8877ff3257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc17732f8797baa8e0494820d149cb274f1611cd12cd3001b59d4e62d09b45`

```dockerfile
```

-	Layers:
	-	`sha256:46665268bcb618004da54d47c47367202105a0ff5620a98f8e54880302999f85`  
		Last Modified: Wed, 02 Oct 2024 02:48:25 GMT  
		Size: 2.4 MB (2369205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c05a79c7e808f86441073619addfc7fe251f8ebc15fdb77f1e366dd97e240b23`  
		Last Modified: Wed, 02 Oct 2024 02:48:24 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.in-toto+json
