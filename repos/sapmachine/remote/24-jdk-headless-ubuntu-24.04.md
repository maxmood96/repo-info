## `sapmachine:24-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:0df56abcf3d497988c4c01926cc586123f064667ab5001038d68240f8c81ccd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7ae2d1fc8717b4ec72103d4ab1d27ccab412add9a39d3a5661f86fc277e2a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260973844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3e63d71c4a7835f0b82ee730d9c59fbc56f1083d31160bbfc9274aa766454f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0071928ec8174c0675155b2d764cb90d4851c96cd327b9922877d7f8d281251`  
		Last Modified: Tue, 03 Jun 2025 18:02:14 GMT  
		Size: 231.3 MB (231258507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:379821affc2a5b76deadd77b8330fbc48488eae9c18d5ab3ec0944d329a36547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c94c931020c207787887d45716504511d329bfdc42584f9bcf73f1ff5700a92`

```dockerfile
```

-	Layers:
	-	`sha256:7cea45ea1ad2e1b88dccdb78bb9c298a2f95dcd2c38d65470dee2d55972b21ca`  
		Last Modified: Tue, 03 Jun 2025 04:17:56 GMT  
		Size: 2.2 MB (2246455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f3979320d434add9956888ee429cf6d255bcae35651a7f26690d8e7007436e`  
		Last Modified: Tue, 03 Jun 2025 04:17:56 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed883763b1c0916969353b729eeca442b69292dcc3528f13e5bd8e0822abcf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258017790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2539f0368b5736beda24acb7610c2dd6e09763639c5df6f840048ff617be08`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f841730254c0144a4d324cb687d900a3137e4f6e06cee3ed80253ce07368d97`  
		Last Modified: Tue, 03 Jun 2025 05:52:10 GMT  
		Size: 229.2 MB (229165891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:db302eea61323276b0fd26c699e96c9ed0976993c34d6ea3d4b343868ecda54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d46be0f24785c1df093c87071841f9b97ed36b9d8db33ecb58629a26ca07426`

```dockerfile
```

-	Layers:
	-	`sha256:5308a683700426c1bafd4bca16b9bf0d3e19686896a92b1dd018a9856e1a17ce`  
		Last Modified: Tue, 03 Jun 2025 05:52:05 GMT  
		Size: 2.2 MB (2246971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bb83e00e81489ad1ef82b521d74dcc4c5af98b344143ed4380aa1ff69b4769`  
		Last Modified: Tue, 03 Jun 2025 05:52:04 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7e3f93e36405131c470fbff6971b2c68da9a293d811a90f652b0f574a2f20ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266702572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0c4d64d944bacf997219add8de0082bf045df6d2e8adec4c0a24ca05d59d3c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a7b89c0546ce32bc2657e230fc61faac464f53b0c11cff4d1b8c7f0d7663fe`  
		Last Modified: Tue, 03 Jun 2025 05:44:34 GMT  
		Size: 232.4 MB (232377362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:384851feee3cf8d51c4098797b48b550228546054fb8aa5ed7f80481590db40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9d8d4593cba88a2e8eda06a4b39956911f7f61d5f0a343e03b6e0b63e21274`

```dockerfile
```

-	Layers:
	-	`sha256:737650c5196a27864f4dec157cf77a5c3bd945f857ab39d151fbc1445cace0ed`  
		Last Modified: Tue, 03 Jun 2025 05:44:25 GMT  
		Size: 2.2 MB (2247913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc74bd74c275e6a5cd7abec01bd4292e2cd4832b3c88ae5af9841fe4e903e2f7`  
		Last Modified: Tue, 03 Jun 2025 05:44:24 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
