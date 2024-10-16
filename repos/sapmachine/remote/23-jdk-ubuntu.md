## `sapmachine:23-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:7ca62ade898c23f362a7375bee74f77533b6d075e090a4d44fd6758d5ff8a0ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d159d33c931a22df22bb0e4c7c8382f5c752b7b2f24132f94706eff8b1d1fe1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251937097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4435ca777fc5aa941a975ab89d41d1f510f3178b8680e26252da4de9d9d721e5`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31639c870f46820772ebc8c0ccd6c949f0b140e3af523288ef40931e02a880`  
		Last Modified: Wed, 16 Oct 2024 16:17:45 GMT  
		Size: 222.2 MB (222186734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01ebba4b70ec88de61b387a5c63a2fbd6cf8c9818e7479394b8894d33e252eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1b44cf38e4509f364d5dd479d137244071f9d8d688be840da32bb9880e1519`

```dockerfile
```

-	Layers:
	-	`sha256:03820c57a9e7b162ee1452d28be3126461af746f1251fa6c8419fe809ee600fe`  
		Last Modified: Wed, 16 Oct 2024 16:17:42 GMT  
		Size: 2.5 MB (2452728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff9809a2b5ea960853542f71ca5307cf53b6eb36fd8f5b268901d640291a8ae`  
		Last Modified: Wed, 16 Oct 2024 16:17:42 GMT  
		Size: 11.1 KB (11082 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:497ee9a0e27308def8e544e8f04908881e4d98c39413439d0d151036416994b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249056602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3300dd76474c634c21c228cc4a85c759a64c9fbad7e1a4d65ea58a06af585abc`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31654d2ae80c44c09259296d50870b683720bfd2d6edca0f235b09d6afdf0ba8`  
		Last Modified: Wed, 16 Oct 2024 04:18:31 GMT  
		Size: 220.2 MB (220170757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82fd3be039530be5d71a469fccca494adcd9dac0324fd6781f0dbc95c8e0598b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6ec3169791c0c24b8969ab66308d0ad6aa316b33f26750fd19e5bde42e0f4e`

```dockerfile
```

-	Layers:
	-	`sha256:bc0beeaa0ce18bbab6dd583cac32989e84830c1924f937f90642800b5962b3a3`  
		Last Modified: Wed, 16 Oct 2024 04:18:26 GMT  
		Size: 2.5 MB (2452660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a49da80044f1786380cf159c3fb43f63bb2de5addb8521f305445dc26ac661d`  
		Last Modified: Wed, 16 Oct 2024 04:18:26 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:41711d11cd755d90a26d39215691c8c5d127c9a0e8e42054984aefaec4e3c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257676622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b39fe2c6df46c5b4f5258594b1fa069601fe27431e22a26f9e74aace8d5197`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b978b0803fa06100b7e4e20e42311cfd06abf25c0cfeddd89b728b389f7c75d8`  
		Last Modified: Wed, 16 Oct 2024 02:33:47 GMT  
		Size: 223.3 MB (223287653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6fb9c72a8e3535e3b60d19b024b004460857e7d77e6b096d35eab4127cd9c642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b70cd3dbf5825e251049f06f85cbed830f8175ca9002eaf94792b6a62db3415`

```dockerfile
```

-	Layers:
	-	`sha256:de365a8171cf9dac78784d9b00ff58d33e0468146a0c15677d85d97cd3c33e69`  
		Last Modified: Wed, 16 Oct 2024 02:33:41 GMT  
		Size: 2.5 MB (2454145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6806c8872177de8bc8fbff0c7a5617c53868aaad689f0e3cfbe523b7b1f7759c`  
		Last Modified: Wed, 16 Oct 2024 02:33:41 GMT  
		Size: 11.2 KB (11169 bytes)  
		MIME: application/vnd.in-toto+json
