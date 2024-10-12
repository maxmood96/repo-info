## `sapmachine:17-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7a9e8c5369eb26b7f369bd3d826af80f3168ea6d97bd1e9aa126f9f3d9cad56e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6c1cc09b0a439e13371def43e9d190a55e42e20dad09098e7a60dd5ea7a501fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230182442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740cc3b81e78d5207016d097e484a02d3131c7ea4b0e282b7035e6ee7e309a09`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4388343ff89e58cb79f36854e3f9013dfb86b97ad3f609f7c5fbe800c0720c`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 200.4 MB (200431985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be3098db77043780764484f7c98fbe8528b2f94209e3dc77c8c283172820f4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82830405dd42f72323649900ef6c989e604c20dc0dd2fb859ca0e4d6843f0c88`

```dockerfile
```

-	Layers:
	-	`sha256:e9ef0ff4a880458c46fe94f5ba52fd4758fc4020941de98a221a2a84fdf7f2dd`  
		Last Modified: Sat, 12 Oct 2024 00:01:30 GMT  
		Size: 2.4 MB (2448372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd57637b4e72db994244f98c6d4b0441739b1287387662e30228580e421c1309`  
		Last Modified: Sat, 12 Oct 2024 00:01:29 GMT  
		Size: 11.2 KB (11177 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e3c1ccc2978389b35cf87bc5611ec814e53054a823c48c546f3a6cbdc14d18b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227967272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c413c88282dbd3db3471454432194915b398f7c831e48ea25397c26490105`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d2137d8a8a6c773113479474daa3c1466ed5e77326439202225748304f7440`  
		Last Modified: Sat, 12 Oct 2024 02:27:11 GMT  
		Size: 199.1 MB (199081656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:60602d943342b02a996c4d4875541dfcdab70f8afdc82a07590494002e95c2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42cfe80e25b6557d52a632548a0221e9644981b8f175461589cf8a9a81b845f`

```dockerfile
```

-	Layers:
	-	`sha256:d2d8ee463d4e179883259f78eadf44883ffc7e153d4dc56a72f82a1b65efee2b`  
		Last Modified: Sat, 12 Oct 2024 02:27:07 GMT  
		Size: 2.4 MB (2448935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc9ec34d20d64a9081e9151373803dfaf1e45728eaccabc70b8ef64b8356f78`  
		Last Modified: Sat, 12 Oct 2024 02:27:06 GMT  
		Size: 11.4 KB (11372 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3a45f57c2b1649da18b3479f7f799f1badc67a275db1f80b4d7df1631f15649b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236027439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c65123bc4d718d4b65a61b78f45cb1f0dcd9060f9b95184468f9d72a10c8ed5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216876f01c4fa7233424f2e89db8a79179c8683d6bfc7aecf676bdaf457ab9c2`  
		Last Modified: Sat, 12 Oct 2024 00:35:23 GMT  
		Size: 201.6 MB (201638027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73e76d41759b14cf138fd6d0a1b30adc5434d5451b7b25c1cb4fa7c25c1ad13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b9fc8c89e90ce3348da7a23e17c5cffcdd4572ff189dd65fd7d4ecff18ce8`

```dockerfile
```

-	Layers:
	-	`sha256:f91d3a99d0db2a104cb9c425e0eedf4675cf28551115d4c54359755b85b7febd`  
		Last Modified: Sat, 12 Oct 2024 00:35:18 GMT  
		Size: 2.5 MB (2450408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2830e7f65c3fd495c0fa9bd07c55ac2a063cad4677a449e6f1c508f347bb8b9c`  
		Last Modified: Sat, 12 Oct 2024 00:35:17 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json
