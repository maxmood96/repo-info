## `sapmachine:21-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:d7ef72dec1307350ea1b181f10884bea0d16dc9462c9ca07aab2dc821141a471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:b47b0bd7b84c477c9dae3ddcf5264ce790982cf886f8b9083d0c2309a1b89691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245160959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6940ff9674b38b969d039151445b54b9a9b495dab013287ef9cfe7d15e78d0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde96ed1f059e28dcf91573757466b291c6bbfa831eb6b9283dc9f81ea369ba`  
		Last Modified: Tue, 25 Jun 2024 22:58:57 GMT  
		Size: 215.5 MB (215455806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0476baffc8ef13923d8d02610ebdd803fb0822339f297854181b0c02ba0eec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57acef09f67ec199755858809f9d5634f44bd7616cdcb66db43d814d986df067`

```dockerfile
```

-	Layers:
	-	`sha256:1a6effb36fd8e469f74495c7443dc18508bf15eb366106ae6fccb70348af893d`  
		Last Modified: Tue, 25 Jun 2024 22:58:54 GMT  
		Size: 2.4 MB (2421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc690dd694cbf4565946632d15472080ffb353f691e0e97b89de6a6e9b3b3ae`  
		Last Modified: Tue, 25 Jun 2024 22:58:54 GMT  
		Size: 13.1 KB (13083 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:335cda01da2cb2ab0746cb36f491eab38e9e32effe0b13168da8c4e96765df1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242401958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1892dc2e4cd834a34d467e791748b6f7132169f18d8d49d52671d2fa38f4ef62`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2677f3515230e572a08622f5a0bea8ef48085540a56a214c4fb1e0b52b2a63ef`  
		Last Modified: Wed, 26 Jun 2024 00:03:00 GMT  
		Size: 213.6 MB (213558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb0bea40aa4377e63cf7f9c2ad6c633a168076bb0cb911c07d4a3e602693e1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eb3117f273252acda9c3af3f58969697399ecf8f5d4ac3f531578db228cebc`

```dockerfile
```

-	Layers:
	-	`sha256:83edd8352c924ab26eb2b508e530a9041876b6d787d3c9797010eb8de660ff64`  
		Last Modified: Wed, 26 Jun 2024 00:02:55 GMT  
		Size: 2.4 MB (2422160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ce311a4f65eccd8d6976d5fa6e14e98067ddb7ca8905590910720e98caea6c`  
		Last Modified: Wed, 26 Jun 2024 00:02:55 GMT  
		Size: 13.6 KB (13552 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:286e946cace12a89bef7a1e9a5334e661c92b0c1cd15fa7147a391e078f2e1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251420580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6813cc724818e53082754631d42f27470611269e208142ba11990b97af586e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7412a1960288eb7288f1a43f168ed6eba52de00d601789ca3300c977a21d191`  
		Last Modified: Wed, 26 Jun 2024 00:26:56 GMT  
		Size: 216.9 MB (216914551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2d73cb95c1ddd98c8d1588a71e6ebb8c2a6b422f17a089be739fc037a1674a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c640b0da069867d57020bd71adb57c15d51d3638d9af2a462f2d3699a51432`

```dockerfile
```

-	Layers:
	-	`sha256:3e99d7b08f208ca8c462a0f0df93279ce0f1acc356eb183b7d5a16b934ce263f`  
		Last Modified: Wed, 26 Jun 2024 00:26:51 GMT  
		Size: 2.4 MB (2423597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc42c42e2a2d671dbdf2076860387c730de3aa5c85504f816d06a5fc11e415b`  
		Last Modified: Wed, 26 Jun 2024 00:26:50 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.in-toto+json
