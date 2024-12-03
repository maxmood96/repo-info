## `sapmachine:lts-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:0a4db23755f22959da929e54f5e0ab8eb03ef7ffb896f434287f79176bc4ec56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:26c853b86d91fbc242d6a1eb531f31e45a85ea666192fd4b455c9830173d7337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243515423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e7de54432d48f8fa084df34c500718749fdf99533c369dc44f3238f13efece`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054204f8d1352a767c7a3c198ca89a77e8f10974907614994b63fbc3ae9618cb`  
		Last Modified: Tue, 03 Dec 2024 02:36:23 GMT  
		Size: 213.8 MB (213763455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6adc29275e7f7f0b20a35c862bd0319becead69f0f552605f8353ee25d4a3e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3a0e1a16c8ab5da421034f2c524ec61f1ca731312fcc47bfa24ecbfecbac8`

```dockerfile
```

-	Layers:
	-	`sha256:1a68f2f6bee7dda93838cca2e23e3ad2ae59222a3ecdc83ffbc12ae28f808879`  
		Last Modified: Tue, 03 Dec 2024 02:36:18 GMT  
		Size: 2.2 MB (2233704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b32ba70e726b69a53bc66a412691c6dcf278dc99e6aa9e698dd01fcc29138fba`  
		Last Modified: Tue, 03 Dec 2024 02:36:18 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ccae8eb221b2eb110ce9528b590ea474891a20b6fbdee7ef6fb95eea11d8cbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240838808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39788949161b21a489ef327f15cbaac8867218d5fc1bf501e29d02c1c5aa25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545f0bb3bc824c32028f68e13b9ab32079661c0b4673d1827c77a3e4745803ae`  
		Last Modified: Sat, 16 Nov 2024 03:48:18 GMT  
		Size: 211.9 MB (211946383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a320d70ca0e8a66433c1c3fb09d73d54be16c6af03ecdc0e49f39835074e686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd64fc15638b4c9a7cdb52f327586683ee468dd5c52048eccf7f0d6129d7f64`

```dockerfile
```

-	Layers:
	-	`sha256:65757bc1167c47853c0ed41a24846dff4030393e4faec2646e0d47276218f790`  
		Last Modified: Sat, 16 Nov 2024 03:48:13 GMT  
		Size: 2.2 MB (2234202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2ca4e23060012f6a7b909db804f5a045b08181e801db2e91885a454b9ff9ab`  
		Last Modified: Sat, 16 Nov 2024 03:48:13 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8973ba54642777ba9adb4f1dafdd6bc69a2fdd4bb77c9fe7c4924877f32f703f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249396847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addd0acb1cec35b664be8181c0c558df47541a084b7cab3353e01aa593b7e59e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315cb31f7b1f9d60fd20e661ba6df2aea90d89b290900c9f5f67f7ebe76fa1cb`  
		Last Modified: Tue, 03 Dec 2024 08:34:03 GMT  
		Size: 215.0 MB (215008027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d03ac8251c9596a7432c766b4eff77d08e4cc6c131c308f111d4a8a93766bbe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ca9c35d7f1a0f9168ad1414c54ebfc25e028cbe9bf17ff9c58894b61c831ad`

```dockerfile
```

-	Layers:
	-	`sha256:3de0044f61bb66dcb24e6b4de58f3f5c2ef8665a218b2966ffe43420db238a04`  
		Last Modified: Tue, 03 Dec 2024 08:33:58 GMT  
		Size: 2.2 MB (2235659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9313e4844d7b53719162fdec45a0706ed3f8f1069ac98f771a71d4227c94362a`  
		Last Modified: Tue, 03 Dec 2024 08:33:57 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
