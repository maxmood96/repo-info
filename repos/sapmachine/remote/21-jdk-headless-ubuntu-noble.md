## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:81281deee50906a4719f6a28ab5c80257629ee5867ae3718efcabe3d057028cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:66a5437e21f9719a22878dce6c7dba3b7e1c5943c73dc4e0a858bbae247403da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246552255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa966306b099527c3dd911f9006d7d015ec6d2a442607718c2faf87970a405`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213428cc52167e382231c404da36c43a8a41e5f7b04d42facdade35baef66440`  
		Last Modified: Tue, 17 Sep 2024 01:00:55 GMT  
		Size: 216.8 MB (216802427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6160dfb0c8a22bcb762abb5bf16852717207ba7bb761785fb64da452a567dabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa9e49f8e74ed6246b6ae431db995badfbe48a3bbf27d91cf1fe88b2e280acf`

```dockerfile
```

-	Layers:
	-	`sha256:e8e76c1630a75cb8155e3829ae881736b86e21ab3519d0fbe76cb68a35028fec`  
		Last Modified: Tue, 17 Sep 2024 01:00:52 GMT  
		Size: 2.2 MB (2213254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87adb721823b4e258786ba35534a34a221187398c618c5cf6353b1266ea2bb4b`  
		Last Modified: Tue, 17 Sep 2024 01:00:52 GMT  
		Size: 10.4 KB (10398 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9a5a35f3673aa97b673f3e9ab5d6f9e1efb50f8060482662cd7617881bf26f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243605605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73beca5d72de573b5c529b341c25583f49f19fbcff286be66f931924dc81c5a5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6f1b8554cae96686c2809a7bc1a4e33258e6bc8c89578bcf6451d3e09544d0`  
		Last Modified: Tue, 17 Sep 2024 03:18:33 GMT  
		Size: 214.7 MB (214720006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:accbda5d48ac3349afca5b19004e6f6169c7014c9d6ad581ce093284b6372eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0219abaca2942495167962082a9664dbb2cdec92ab2ffe5b0b9e3995cc5ca`

```dockerfile
```

-	Layers:
	-	`sha256:77e0928c9a63c2fc5b8f9dea8eaf6df413ba1759b9d5a146899c8264f0ec797e`  
		Last Modified: Tue, 17 Sep 2024 03:18:27 GMT  
		Size: 2.2 MB (2213772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f39588a63caaba8e9fb5b3cacc9c9d0fc5766a56c7ae5b67c42d755268ff20`  
		Last Modified: Tue, 17 Sep 2024 03:18:27 GMT  
		Size: 10.8 KB (10759 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5d9590fd93cb9c59864491f2e7857842dc802d7a68b248796f47b2e460999f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252687104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c5b4b6dbce1fe826c9e266957d1443eec139fb7bd2d6d391fa3407ba7da976`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1d930af0caa9427173432aea53f41265f61ad11c0b3d57f63ded92216f202c`  
		Last Modified: Tue, 17 Sep 2024 02:32:30 GMT  
		Size: 218.3 MB (218294759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbb78dffe9d7db16b89f552eaf4623f013db18137d9c67f2dfbdbde7768ab292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5340827076d5f5b9fa623404db8a793c267ddc4385fca4a555ed3221ce11ad7b`

```dockerfile
```

-	Layers:
	-	`sha256:a3fc43317a67ac9d79218af53f92bf5847024c75f1bb1409dae2fa451c070412`  
		Last Modified: Tue, 17 Sep 2024 02:32:25 GMT  
		Size: 2.2 MB (2215209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9e42f703395c512b5219679deb66285edde43099ef3068d04af424fd0504bf`  
		Last Modified: Tue, 17 Sep 2024 02:32:24 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json
