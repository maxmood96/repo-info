## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:407f0e2e7096d9ce9bf92111c3b27bae06310ee51b0c19f53af1650c96ac44b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf87df7b766e606fdcb0de4e9561d228ae760514caccbd902af5c88d1a3ebf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256036710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdd64af589dd2d60e414e2f96d9f85e576b72b8b87429c098a006637c474c77`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f60f7710c860ec3ecea7705756064b4866acfd9057bb3f4589bc8a1356db21`  
		Last Modified: Wed, 19 Mar 2025 20:37:49 GMT  
		Size: 228.7 MB (228678528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c5c5df726852635edfafd561bb18ad368dfed926237f8ff2760304ef233f8fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71db45b224f38a5a322ec65aa98432e7050e60951a31763cc926c1b6e087db04`

```dockerfile
```

-	Layers:
	-	`sha256:db06d61c4879211893aa487cf1c99cb31c5f8b282012f9d3723ac8890e63eadc`  
		Last Modified: Wed, 19 Mar 2025 20:37:43 GMT  
		Size: 2.2 MB (2240010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b164ff159cc601d74b18fb06b8befc26a5a22538ba2648860b9339eed929434f`  
		Last Modified: Wed, 19 Mar 2025 20:37:43 GMT  
		Size: 9.0 KB (8992 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

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
