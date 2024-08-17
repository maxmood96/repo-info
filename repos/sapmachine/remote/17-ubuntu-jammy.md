## `sapmachine:17-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9cd551553fd84647cfe3521175b17b2e186dc38945151726fd383de281f62fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:777fee954d5195f1a897738f930727576483f0950f623d4e48057deb3cf01d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229587740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf5bea496b374ec4c4bea959430a6c9ff09dae3ca661edf4869f297e738f408`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55570a97954719328ca7f12b52995030bd47a2e1a1ba20316f8a7ae960e9db63`  
		Last Modified: Sat, 17 Aug 2024 02:06:30 GMT  
		Size: 200.1 MB (200051715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:03cdcc34962a8f88879babdbdb1c35f6e5ab6c2de9743eb2bef9b763b05e91dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef4e739c64def29f6ab2b63e6a2d4aa1dd7bc8ae4da8eb5dee84f6a3a3aa71c`

```dockerfile
```

-	Layers:
	-	`sha256:34ebae39056092c8fad3225524761e80710692ab2b6cf119e7a5b6449eec8946`  
		Last Modified: Sat, 17 Aug 2024 02:06:26 GMT  
		Size: 2.5 MB (2471217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603b0a7ccfa546b8d8e5009f5413a5bf14f1783ffc02d920467cfc63810d5e5c`  
		Last Modified: Sat, 17 Aug 2024 02:06:25 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:56f554c1640f1faf16426f6d46738cacdf91b2356acf2bbc180ed8a104bfbb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1493209208a21216134535bf15061dfa750e98c3818f2401b6375ce20ccf13c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bc73cbf6d1597a3ac502ff1f4ba2350c93950661a1d3dccf8308f6976c2a9`  
		Last Modified: Sat, 17 Aug 2024 04:34:01 GMT  
		Size: 198.6 MB (198640917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dab482ea2984b76caca7a29616c18759f818e24cd2ee3144f4d01d802568f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ae4a4f6e805da78a7cc0a95c1f1fff7f311b9cd747a78afc0bb28290f8db7f`

```dockerfile
```

-	Layers:
	-	`sha256:b8dbb678048230dd5ac0e94d5ad903effd0952f07ab5eee5ecb486a2670adbe6`  
		Last Modified: Sat, 17 Aug 2024 04:33:57 GMT  
		Size: 2.5 MB (2470945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f55a6bb9e30eaae90fdb714f0541aac8900eea9609c24ddbd0feace725b481`  
		Last Modified: Sat, 17 Aug 2024 04:33:57 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b19f69ac00e0a918ac975dcdc0aa6de8ebae695bd59de615a8bd427be7722b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235588860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb981c602a994ef49e417fa07753103340b8be406a194d3d2e619281036c31f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea8be783bf6b329c06ef1ae934c2aab67be18617de1c81af48832c098c37aa`  
		Last Modified: Sat, 17 Aug 2024 03:14:49 GMT  
		Size: 201.1 MB (201124682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a30f3d75b7713cc6d77a41555d3b461334242233190c09ed0c2c45501503fce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2979fde55c63419a4515550a9bd5a2c736464090ffde754d4cf79d1dbbb72`

```dockerfile
```

-	Layers:
	-	`sha256:7ee2a575c0571384bac63e1b95939eadb701ab92b881a01d8d666c10a2a89bd8`  
		Last Modified: Sat, 17 Aug 2024 03:14:44 GMT  
		Size: 2.5 MB (2473271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8c659929af7b4cfb4f9ac793a297663e1109ef9dc6f0c3415ee87a3e00b151`  
		Last Modified: Sat, 17 Aug 2024 03:14:44 GMT  
		Size: 9.9 KB (9945 bytes)  
		MIME: application/vnd.in-toto+json
