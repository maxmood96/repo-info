## `sapmachine:23-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5dce7df043049a10d12efb3309c3f8e44f8c7de0441b8d28fe9b7f64d572faae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5c852de22c571c3c6b188c3cad87344508c4789d46165afb1dc463103e82cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88332927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc2414ffca868bd8c2b351de6e499a40b440e475923a2c8857aee1f3dcbb244`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c6796433a16479bf926828537f603149f515986c68cb2b2446eb925e660c0cfd`  
		Last Modified: Sat, 12 Oct 2024 00:01:14 GMT  
		Size: 58.6 MB (58582470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:949039407535b1677d4bbad538a036b890e668f9699404ceceb388be885d0483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0862c678ce68b23ed9e5ed234c8f134aed594d7b1a8d7601116394551561c6`

```dockerfile
```

-	Layers:
	-	`sha256:84c55ad98859e03856f297e22e3ed2ca8b8a59c7597bb4a4be62ebc03edf20d3`  
		Last Modified: Sat, 12 Oct 2024 00:01:12 GMT  
		Size: 2.1 MB (2130431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a63e04da8622d42b9ce745c9b335a1e925cd6eefbf991e374885cb7a8d2c600`  
		Last Modified: Sat, 12 Oct 2024 00:01:12 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3b8fa85759e3905d1aaa91e694128c94c4c0c4718641777bce446d5dddf0f696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86497664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a734b684f08cbea4aebed801c45945fd6fd53363f62875810fe15d3839c654`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b87dcd1f68e888611129acbc7220f6fc0c43898a56ee41108484865fd1b58e`  
		Last Modified: Wed, 02 Oct 2024 03:44:34 GMT  
		Size: 57.6 MB (57612234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e66c2630076dc9acc9e46b60f84c84397805dfe084515051d3dbc49e4acfe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141c1b3ac79a9a3d7dacba1307eb4aa462f1f77bc7a374d5baf7370fca4970a1`

```dockerfile
```

-	Layers:
	-	`sha256:e447facfec23191be1bbdb4383d513ddba433fc109686b0bc1c4fa97b655796d`  
		Last Modified: Wed, 02 Oct 2024 03:44:32 GMT  
		Size: 2.1 MB (2129643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cac0ecd1675da195a73a8e9280499635b40c42ed5dc5d393d3df25df4a2d7fe`  
		Last Modified: Wed, 02 Oct 2024 03:44:32 GMT  
		Size: 9.4 KB (9430 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:82aadb83b893ef6119386ebf9c39773acb5deca14937baad7324c1f1404f01ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94280955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c012af9c4312bbc5096e6a98cd79f42fb1e8ac7a71899d91efa1df908b8a442`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:888813e271cc35ed01306aa8ceb1c61d55dc4c81995633b3ef2962dc814e18bd`  
		Last Modified: Sat, 12 Oct 2024 00:28:11 GMT  
		Size: 59.9 MB (59891543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be8b3780ffa8e03d5b97033efc521055fef3769fc67d38f7ac8fe4f01e7fdbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aca703d69347c9a864fe82c814d4648a9e27032a26fc65ae76ed34dd73dd3c`

```dockerfile
```

-	Layers:
	-	`sha256:1471eb3eea6bef2007d855ac30503952e049b46ccc7af76f40082cc6d188a6bf`  
		Last Modified: Sat, 12 Oct 2024 00:28:09 GMT  
		Size: 2.1 MB (2133686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4c927d79b8a09745a1ac33800cd5092276e1089caa4011bc55e1aa9c3b9659`  
		Last Modified: Sat, 12 Oct 2024 00:28:08 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json
