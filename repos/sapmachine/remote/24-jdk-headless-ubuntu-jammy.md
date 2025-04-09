## `sapmachine:24-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:db692e051bcb21ad4b9f4d13a0cab44f9daf70e6079afe94fc2f61dbe84a85dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:40c6e93d43304af0fb9a0f19e9df38f63d015f2794d45fcbc8b4fbf4defc87a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260332438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5e88ecbcaba01bf390c7a274f9ee16dbe38b3a3b9f57253e1ab84ed9f2b9f2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bf57f997a52e2d1372be43b3137975a147920338f7a3efa5ae83c383d7ccd4`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 230.8 MB (230800073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40081a5e66cdbc2faeb2b194804faa72919e857c9376d01ba8db8edd5d0e6a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60054314650443526073733587b69f971a47556ddfb681681d1c8f65827d341`

```dockerfile
```

-	Layers:
	-	`sha256:405ba1367498acb6fbca6bf546372439760787db33597a561ee747824a9d4cfb`  
		Last Modified: Wed, 09 Apr 2025 01:20:42 GMT  
		Size: 2.2 MB (2240429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4858045cb1447c7a817932a9e363b97a58f139b9063b250a728ebe751f3c4ea6`  
		Last Modified: Wed, 09 Apr 2025 01:20:42 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:23d9d775e5b1719db435f1c3b7d1fd5e69b1ee075b72ca5ee7936eca4d941d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256037305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef25ba6d7feea15a07d65f724692be7980e521c67ac4706199e365657595896`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d4817cbba6e52ab1d79cfa753cc6db8c12c3e69a03f9df2cbd6c09348d3983`  
		Last Modified: Wed, 09 Apr 2025 09:22:38 GMT  
		Size: 228.7 MB (228683074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:924eaa0a93cb79781f9dd53300748ec317c27405980cc1cfda2c2f2ec0aaeb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a029138ed30a73f915996444824732c82f8a1ae711df0665a863419208bab1`

```dockerfile
```

-	Layers:
	-	`sha256:fca79994c1b382fe7d0317fea82a420a3eba26b8dccb8b8a01fbe7e6262fbd61`  
		Last Modified: Wed, 09 Apr 2025 09:22:32 GMT  
		Size: 2.2 MB (2240098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb550266025b513ef06b172e3fb63188eda4ca4f67349ef240693cc1591d07b`  
		Last Modified: Wed, 09 Apr 2025 09:22:32 GMT  
		Size: 9.0 KB (8991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3e191f8ef093f74c3c10bf0554f82b6ccfb625fc9ae96c0e0251071e179a7c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266273991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2ffc774ecda378a3c512688e34b03f54e271f2649f70d9e2ad0c311f4ccc45`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3c257e85891ddc4487953c51ebded4674ce14b341ff4a8af22dd2177389aec`  
		Last Modified: Wed, 09 Apr 2025 06:40:37 GMT  
		Size: 231.8 MB (231831295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0378ad707119c92b2b4e51751c99c9c729cca24a3dae1e688d689f119f52fc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6ea962907de0ed42ea17529529bfd1053af04009a44e90455a3b43630f957`

```dockerfile
```

-	Layers:
	-	`sha256:9e7a1254f6bd184cce7cb970b44628a6a929bc3abc3db161c6e29c5021889ccc`  
		Last Modified: Wed, 09 Apr 2025 06:40:31 GMT  
		Size: 2.2 MB (2241776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcefe513e54b7a8c1c95f8bc2b65e2c5bcdc70507cab57706dc5f1ce89f746bc`  
		Last Modified: Wed, 09 Apr 2025 06:40:31 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
