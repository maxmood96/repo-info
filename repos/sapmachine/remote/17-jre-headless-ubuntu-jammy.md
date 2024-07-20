## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0f6decaf2e9d2a6e0560a3edb5f7ea2dfafb1bc150d31475e1d47a85b809a6ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9d4f07c99872dbf496c40423a4dec23834d33e728784b59707dd139a54be81a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82019305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a31a033908c40028d422862972732cdd0611409e0395869a543afdcc4096952`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbc101c45c86f185f82a0d36fd9f35ab934822b252a2668d707f506ff939e80`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 52.5 MB (52485250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c60394af52410773cb0ee189552c55a255e11a74594dcb80a0c9adabd0c6d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734edbfb79c8d6b1db848f03280d68fa815eef0e315296c2ea83b8734af68865`

```dockerfile
```

-	Layers:
	-	`sha256:5ca240ca62e0b027ca63ffb11c00a3e6617785f6ad2102c8a65a01b6d8cfd39e`  
		Last Modified: Fri, 19 Jul 2024 18:00:08 GMT  
		Size: 2.1 MB (2144916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d8107ae941fce3fe7ad13b2d1dabc4ec48066f669792cc3e001cc2111075e9`  
		Last Modified: Fri, 19 Jul 2024 18:00:08 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:805152ef6a5e9dd9644893234e2bbc302c09e3d6f5831f9f3168179422b08a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79178752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f50de75e078cd45ac489a169edee7dfcff9c6e7f064445f345d7ee53b315a5b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3387aaf9bea465bf6791a5b9400ec73cc948c27b66035e36606d8153cb5162`  
		Last Modified: Sat, 20 Jul 2024 00:28:54 GMT  
		Size: 51.8 MB (51818727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebce3bbd0395fd7afd239b39e13c279214f75058052ce154fee0b8dbe0555009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c86cb3aa706ac6206ee3a2787ce05ea4ce393c5ffa38cc434c8822f30ecb49e`

```dockerfile
```

-	Layers:
	-	`sha256:cf58e70ed897e4a1906c8ac0ab529ba05f659361f586c425bbfb4c4c8d6528bc`  
		Last Modified: Sat, 20 Jul 2024 00:28:53 GMT  
		Size: 2.1 MB (2144586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eba80dd72f1e3120028828e27a84a0a2e5dcf8389215ee68ef342aebfc6a0029`  
		Last Modified: Sat, 20 Jul 2024 00:28:53 GMT  
		Size: 9.0 KB (8978 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cced8de79bfbc80bbf87abb8d327cffcfe4d94a5a59b162858ee20570af5f284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88262336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348c866bce0840ee1db89c1aff2ee9867b853e87e42d525a0b126ac8e00aac02`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b4f3b257baddb2f628a53b5a39f9515d3cb693d6651d56e3a1af9588b4fb1`  
		Last Modified: Fri, 19 Jul 2024 23:42:07 GMT  
		Size: 53.8 MB (53801255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f739603f7bee0e98147e1b69727bb95f2b9d3827f568d1657decad209f3105aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f410060f92290db1bc291aa4d62113c4f5ce5c6b4b6f23d2acb33acac6114291`

```dockerfile
```

-	Layers:
	-	`sha256:5bb6d8a2c7c4acacebbcc631201f58720c3d30922eaa8daef33450847bb8ebd2`  
		Last Modified: Fri, 19 Jul 2024 23:42:05 GMT  
		Size: 2.1 MB (2148825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5cd1b305c5acf388834e82f64e9692fe638001a66a6ffd7beabbbec5922baa`  
		Last Modified: Fri, 19 Jul 2024 23:42:05 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
