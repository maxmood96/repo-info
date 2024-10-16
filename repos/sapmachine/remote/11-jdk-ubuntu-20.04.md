## `sapmachine:11-jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:b1528b1fa673c3b0727cd4c110ae78910aab875452c717f09a38d76dfc16145d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e917cccc01ef6b1bf4910266a7b78d59446e38a587decb831f999e65be37e80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227794350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9f6fc552ff19e326ceab933dc6c255a8fb2fd5c2a4fdb729ff8644ed57c4f4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9c3b9b07dc76ac0d24a1f87dac8e956141073301fd25d4eeac25913530a101`  
		Last Modified: Wed, 02 Oct 2024 02:00:23 GMT  
		Size: 200.3 MB (200283298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8bf72f3282c0fc15e5fcf02e9d58f4a3fe88d80a3d4289a79b4db22f8c184fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfedef0702fdb41a57204b9e0847aa6cae0adda6cc227afe5d4103205b41d5c`

```dockerfile
```

-	Layers:
	-	`sha256:b37c1d9af874292b9b805f387b9d61a37d0f98bbc4e16541f113b6ebc8d888a2`  
		Last Modified: Wed, 02 Oct 2024 02:00:20 GMT  
		Size: 2.4 MB (2381944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac740fe99dd390ddc0273489eca91faea36c59cb3e834a578a053520e6d9497c`  
		Last Modified: Wed, 02 Oct 2024 02:00:20 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a95bdec16f15d940eae1897782611719fcbacc661fa1f8280c474cd1c1fbe49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224743394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b8d1f470590d3c22323af8c146cb9ed5b5be18a6c1106a0b372c1689ae2f85`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931baf8417d3d63713b54464338147da5e5420de7f5f5b429f076a2706d7d7d3`  
		Last Modified: Wed, 16 Oct 2024 04:51:29 GMT  
		Size: 198.8 MB (198769566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b227c0bc10deb44f8a61a8616bd180e9d5a26fcf06e296ff3488e5828b9d8ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2435b20ae68882f67162e8d97686fd52ea6df919e0c7cd47102feee58cb5a3dd`

```dockerfile
```

-	Layers:
	-	`sha256:6adbc2ea7efa482f63b9853c60321b71c8688fbdb829c20edbc04392ef230e5c`  
		Last Modified: Wed, 16 Oct 2024 04:51:24 GMT  
		Size: 2.4 MB (2382256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393935f5fab32790046929d18231de2a0a75377c2a747873a9788ee6cf693b71`  
		Last Modified: Wed, 16 Oct 2024 04:51:24 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ad534e97695b8d4980a57b021f6244ee17482176a7d0d604c6b58db66c0a24a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218625459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e907ada374a059425065e3ba5dec02013f683f8989ca023cdb66b84ee58a4ef7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c3c7be274eb116e0063b788e139f3c398cf2d296512b9fc66b288d8c8aa6dd`  
		Last Modified: Wed, 16 Oct 2024 06:16:03 GMT  
		Size: 186.5 MB (186548953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27e98764f6ffb6831e561451787111e24f9d3148e45ca23123b2edefa63911a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d7c48f1d6cdf6157f42cc4dd29eaa01e11552b613ba6ffaecde087619c9662`

```dockerfile
```

-	Layers:
	-	`sha256:8dd6dada5bf20fc70e66260b43e8d264830fd9a19c0804218bda8ac1780820d3`  
		Last Modified: Wed, 16 Oct 2024 06:15:58 GMT  
		Size: 2.4 MB (2383159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d95a9c8d9251fb69d625b08056988af704d4d52283f3d522426b72d18e59ca`  
		Last Modified: Wed, 16 Oct 2024 06:15:57 GMT  
		Size: 10.0 KB (9983 bytes)  
		MIME: application/vnd.in-toto+json
