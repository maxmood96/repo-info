## `sapmachine:jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:4148ae98e85f55ebf23a92c43154371fbd968be45337ab0f416d2bb72c689540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2fd17b158cc26f99584ff3c523392a81387e60adc91c9ca8665a42c369f64154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90730802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829229bb17a8d6fdd0f9a4e19a136b56836ad260ad98d4715b52c16c398c783`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47063881a81f2ad255c26f86878f114e28cd9811c71286efd70f65d445d0b5c1`  
		Last Modified: Fri, 20 Sep 2024 16:57:40 GMT  
		Size: 61.0 MB (60980974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e7009d3627e7b0195c87c61a0352bc96aa7d27b1b39b5c6a178c0a62b0d4e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86df5dd441fa088c54ce644167642ce175f6c1a0eda251933826de41f9d4ab26`

```dockerfile
```

-	Layers:
	-	`sha256:bf74892356ba430a02b9eb7cc7361e90953f57e35da9806702c28c24a56d3504`  
		Last Modified: Fri, 20 Sep 2024 16:57:39 GMT  
		Size: 3.1 KB (3101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880f7a7a7cc739803ae0bf30a369a86ebec9edb85986efd45fbbc7505708a41a`  
		Last Modified: Fri, 20 Sep 2024 16:57:39 GMT  
		Size: 9.3 KB (9303 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ca2a086565e59ea213d78f77aabd65197e6caa3ec0deecde5a3a2f4b4899d095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88722104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaa5ea59d3389aeb4bda4921e4c0c4a078df8ee870c9cd5aa1c44e912f3b6e4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb86b4c17f90904002adf8fcf0920015615462f15a43693805ebff49e9defd0`  
		Last Modified: Fri, 20 Sep 2024 17:04:19 GMT  
		Size: 59.8 MB (59836505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd6bf4561d366b617793986d8c948fbc7bd13c7ababd3355b64baffe3545fbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7f777a19c22595955bd18b59e1d6411194fc288ed634381fbc6ebee70aded`

```dockerfile
```

-	Layers:
	-	`sha256:d6037847b878753eb8cf99dc56ffa65103c4b3f6dd56b481711472a9cc80ac3f`  
		Last Modified: Fri, 20 Sep 2024 17:04:17 GMT  
		Size: 2.1 MB (2129630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9902ccd0beba8ed2686b77d236053c762536dbba6d9bdb3c9bfef6f11fe2b3`  
		Last Modified: Fri, 20 Sep 2024 17:04:17 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0058dadf0310f7932a2b392a5d070b14b76a8ad97d8cd871f9bff0c3652d8d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96909571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebdfa9dd3232705e6f39cb9db807ba644e6b6b12a259b7812cc51eb99619a76`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5b04bcc5b0048ea2b7526b7362cb57916d199bad7af163bd351886766ce966`  
		Last Modified: Fri, 20 Sep 2024 17:04:31 GMT  
		Size: 62.5 MB (62517226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7a68952a44c0b18d3c8489749c1e1f29bc93cbd3ea33501b991d81fe2a134599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34bdc0d342ba372e3b1314a2d6335ea9600c571b6737379ed448f073001a5f8`

```dockerfile
```

-	Layers:
	-	`sha256:513450b8e01add6af37cff7248bec4d27187916cd52eeb5ad000434ca5a4ea4e`  
		Last Modified: Fri, 20 Sep 2024 17:04:29 GMT  
		Size: 2.1 MB (2133034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f092bae52ccd44e34148f159c2b48a83ec90c350ebd7141bc236f844329bcbf`  
		Last Modified: Fri, 20 Sep 2024 17:04:29 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json
