## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:826499c6502ca2e1d20e34ec25387218d8cc6be39e860172bb2a1b4b2bd2cd1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba79a9ba750bf32792573f32fc1f8c766d78d3cb7b1f622ca1d953bdb76888b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88907045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365ca10c0c4936ea7b826f8fcde1c7ea37c49d1001dbdb4c5f148e91b7844ca4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b5180503f804baa9bd448c3cd30ad546912a49e4fa02cc0938d61770df8c41`  
		Last Modified: Fri, 20 Sep 2024 16:57:40 GMT  
		Size: 59.4 MB (59371357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4ab7d9dd76ea89e3da8688c9ef8f474ddb5a102fdcf9c3872dae8f311ab1d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 KB (10880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1882eef5be438a9791d0e7a49992c0b05acbc7a87d8edcf5dc8c939cdc5283be`

```dockerfile
```

-	Layers:
	-	`sha256:22658fa5f2d05cc0a67bb78e6cbc7caff9c3f0bdff94284e10b98c9bae3a4189`  
		Last Modified: Fri, 20 Sep 2024 16:57:39 GMT  
		Size: 2.4 KB (2359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8c04107e9f4ce4885c842e50432c314e8e63d810289d3371c7d4ac54e8bd6e`  
		Last Modified: Fri, 20 Sep 2024 16:57:39 GMT  
		Size: 8.5 KB (8521 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:340800fcadb0cdab89b41eb6355ce2c0e619b484a7f520b445cd1757001f176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85728810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f678040daba445d2f14898b2b9e900f8bd120ca1f614888051a4604dd29b288`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dc526693dcdbb1589e97465a1ce6d414d294d00f5bc4a64240deb36944856b`  
		Last Modified: Fri, 20 Sep 2024 17:08:30 GMT  
		Size: 58.4 MB (58370481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1415de999c37ea0e3d4dd01e2d87af14efe20c255eec2b498b604424bcb0ed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aa0505cff3d5c7e53d39f62c5995aacd13ea5f546b35d374baa6f245eb73ba`

```dockerfile
```

-	Layers:
	-	`sha256:5d873863368674a5423d4be3da591336b011158852f89cbd05e3e728450a9e2d`  
		Last Modified: Fri, 20 Sep 2024 17:08:29 GMT  
		Size: 2.4 MB (2389042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3037acf1ce9f182da300948a2ab41de6d1ce80357ddacd96554334666461bbb3`  
		Last Modified: Fri, 20 Sep 2024 17:08:28 GMT  
		Size: 8.8 KB (8823 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9e846f541815bf8eaa1745ad6850c14329f343d98645d2cf6a2c219736406549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95215934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f36c7921856bf5c3e614c7abfb8e1b7584c8e910e56997c99045e1390eb9506`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430002ead9782f6ba253fb799c658761eace5a8aedb0cf1d0f45ddd805b604d`  
		Last Modified: Fri, 20 Sep 2024 17:11:05 GMT  
		Size: 60.8 MB (60767692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6b046bd5e5733e479e3f065286c695cc03964c516c0b014dd528f24d84f9c631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103f09f01e8a1f32e5df7cad17378323c893917f851408d7e5709de8108e4b27`

```dockerfile
```

-	Layers:
	-	`sha256:8b79800b55f413c80344ca0b2c0f028f3786dfcce62ceb8a96112ecc3e966171`  
		Last Modified: Fri, 20 Sep 2024 17:11:03 GMT  
		Size: 2.4 MB (2393341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4893a4b541025654b4b6c509c545a97017432fdf42223397253bb3a123b6d626`  
		Last Modified: Fri, 20 Sep 2024 17:11:03 GMT  
		Size: 8.6 KB (8560 bytes)  
		MIME: application/vnd.in-toto+json
