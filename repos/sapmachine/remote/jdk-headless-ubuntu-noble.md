## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:75648092ace72b8b7f1e7e21e66caeb20e56e40333bafc5ad0f7c35f03c71c8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:a314ed928574338df6d3a1971b7f826b3d9244fe28b65a8600e200ee699524cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250750704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7703bd616e0bb5df4d8a7faa128ca35f7efed2d365d1a6c1109ac5073394283`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c95017bd0d70cba0a24dbab87a037ec84a2bf24c99da596cdf98a427b8e3199`  
		Last Modified: Sat, 12 Oct 2024 00:01:24 GMT  
		Size: 221.0 MB (221000247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e042b57a53d4b3617f21799ca20cb2adc461e3d71f183985919b03046e254dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32599cd2b7bc8c96e2b712e9dd774732ff00f413e34cf0237958842153547d1b`

```dockerfile
```

-	Layers:
	-	`sha256:6e9d3cab2726aad190b0ffa4df411dc7cdbd3e7cf0c89c87330b548bfd713293`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 2.2 MB (2214745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc3c0135b52bd1e5b40fd3c8e17ac9b67ca2b921d793cd4edaa3d6a120ddf7d5`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0b4af8776e00203871b72af5314e1a243885eaf068d15dbae0b47fadfd704418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247859772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac8928dec1f64b5cd2c1b7ec3bda27dfec608185e01ac71af3c5136354b381c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757956311b08fea26c7c4bd759001035daed71467b57b351426e41f99898113e`  
		Last Modified: Sat, 12 Oct 2024 02:20:11 GMT  
		Size: 219.0 MB (218974156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3f4760c25db63e536ceeeee2b822206d75c924924c66705cadde1c12e3cd1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b5866364b3df89b62c1d7014c55bd6a7cd28a52670567773592e7264b3e45f`

```dockerfile
```

-	Layers:
	-	`sha256:86120999fa1023ea685f68b0d8df8bc4676499e0dd4f1d82cfbfd3ab37ad1045`  
		Last Modified: Sat, 12 Oct 2024 02:20:07 GMT  
		Size: 2.2 MB (2214596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5849a8c67e81c8831254e0806f634a204479c9c0ea4cae87001944e1459491ec`  
		Last Modified: Sat, 12 Oct 2024 02:20:06 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:63bd211a8a875ce08bf5c33d53cc7625f09b97fc5e6a632a4ebb8dc2e6e952eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256296340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0e1bce3f956bfb6ea4a3768778a5334f014513b41fd41cafe6ac1dc44da6a4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a306f0415a651ee9c9a0b1ed0a2a4e97a3bff4ddb74a0563be705973d817eb9`  
		Last Modified: Sat, 12 Oct 2024 00:25:55 GMT  
		Size: 221.9 MB (221906928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3586fb507ddd5787c1cc982cf5d9eed35ebf238e0a8cdafac1bda3500ff7680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86204eae07a33956168942e99b2d84f75e48dd5179bcdc7c110128ec01a4483a`

```dockerfile
```

-	Layers:
	-	`sha256:deb5246f4db1c76676e9acef21bbda9f614aa56ca3c80aa570574a364326a5a8`  
		Last Modified: Sat, 12 Oct 2024 00:25:49 GMT  
		Size: 2.2 MB (2216063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c1f9bb53af02a09c13cb3f1322ba37602a4d68f006ce5554f5df8e5be5ae96`  
		Last Modified: Sat, 12 Oct 2024 00:25:49 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json
