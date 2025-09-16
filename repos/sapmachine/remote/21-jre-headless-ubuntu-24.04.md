## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:a7f7e8a006b8a67ffd9ea34526775c300c7f7e4284c079d9fbbe46ccf6b65a87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b0cfa5aaa95affbc46f811f5534247e6c086b3849ea3128afca9b26d4c173190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88739017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588639e40cd96e5c5f33f6e61070c332ea06ea601e5bdb0c7847b426ac9b977c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80519fb9a08e907bdeb1ba6d171793a8136674c68255a8aa472afa85492d4287`  
		Last Modified: Mon, 15 Sep 2025 22:27:51 GMT  
		Size: 59.0 MB (59015567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1fce32f881d41e3e26b1c2ae9f07373cee6e3168f5878436627e3887de1a147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a605bc0cdc1d353196164e3dea25aa7b01428f923152f824521b88a18e0f3cc`

```dockerfile
```

-	Layers:
	-	`sha256:5e06848198493fdf25353584152d6829877cc9bc82e6fdbff221ba7c0279700b`  
		Last Modified: Tue, 16 Sep 2025 00:08:42 GMT  
		Size: 2.3 MB (2273854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89efdacb4adfffcf0ed0a202c7350406ca70fe2da67249e5a1a2de304135509`  
		Last Modified: Tue, 16 Sep 2025 00:08:43 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f65c355b73e702e39ecc1e527dc27f42fbe2210c5213d72b506191221abc3314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87048149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056805b0a5feeaae8be204080ac0947cf7553883d216fde420b30f456b53f4db`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34cd8a72062e6262cbe2b4b3f1119cc5324a9d16401fd68fce59124cd376aa4`  
		Last Modified: Mon, 15 Sep 2025 22:26:37 GMT  
		Size: 58.2 MB (58186832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0bc926d4b58561c9638ca1b96ec95887f5225b76a7ef09181aa705fb1426177c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066dc392362f62ec3f90c937c911f9cabc2380411cae0c702a2f948fa5dbaba2`

```dockerfile
```

-	Layers:
	-	`sha256:302ccd2c8f505a67219ad1eb0fa4c9e827dc6a19834ebb1797aebe5acc28fd97`  
		Last Modified: Tue, 16 Sep 2025 00:08:47 GMT  
		Size: 2.3 MB (2274397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d6746520335e5100c5b902b71233f1e683cc6dac2d0357877267baac8e686f`  
		Last Modified: Tue, 16 Sep 2025 00:08:48 GMT  
		Size: 11.5 KB (11495 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c2fd57703829ba967f2e7cf46104c801d30a76418243589dc217e2b83990e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94386328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6741fec84e8f9f54b2c7fcaffb969b0945b5dad9a8fb5404ccd9113d305b26dd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71c07353af9c39eae6b9600e6ad5978283abc4552869129aee812b5df3a4a99`  
		Last Modified: Tue, 02 Sep 2025 02:06:20 GMT  
		Size: 60.1 MB (60056795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5b635d983026463a3f447e465d9c457ebe8648549a1b9931254b402e4f8641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0218c1e4abe086173ef93c48918992bdbcab73f9a964a2d49abc7e9139c8f3a0`

```dockerfile
```

-	Layers:
	-	`sha256:d834951e6d4af092ebe710576c671964c7df1918aa193f922eb81d5092a75147`  
		Last Modified: Tue, 02 Sep 2025 03:07:56 GMT  
		Size: 2.3 MB (2271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a01626735a8c87f3d21bc1872226a190f649bd618ee130f2f498e33aecb236a`  
		Last Modified: Tue, 02 Sep 2025 03:07:56 GMT  
		Size: 11.4 KB (11392 bytes)  
		MIME: application/vnd.in-toto+json
