## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:c64faf3e48435cdbdb79a55df4d9b71b6df62ce91126ca5890f7d372a6029a03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a1b0e1fba08b7d4c1673dd46590da5a48ac7fb336d034d159d8f7e44c9234620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89927464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea1a74841284c2c9720b7d44b2aaa03bc21cf858d7d701f74693c0de62ad7e8`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:097ffd649f53d4dfe0cac028219849da8362decafdd79aa3c8166ebd7fdc4a92`  
		Last Modified: Mon, 15 Sep 2025 22:27:50 GMT  
		Size: 60.2 MB (60204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dfebff703750c727cc31cbe71271255bd4abff2afb20ecaac193c1bd3f9c4ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8cebafa46caf037d8a3686ad9d9c8351d4e7fc0c6b363525d01141087ecef`

```dockerfile
```

-	Layers:
	-	`sha256:5df30bc3e4be57295bf0e84b52a5ce1adb7538555b520578253a72f6398b1b10`  
		Last Modified: Tue, 16 Sep 2025 00:08:32 GMT  
		Size: 2.5 MB (2519622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6bda9c016f95cad55ae206cdf039ab3350dcb1b0839c17a3a549a73fbd4f89`  
		Last Modified: Tue, 16 Sep 2025 00:08:33 GMT  
		Size: 11.1 KB (11070 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:26769d2c747096a1474165568c05199b1050df4a568b501b2816dee31120074d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88246631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba51c706f1b9639cc8acbdec74687688d6d9e1947226c5915f21489563f489e9`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0064029974fca3d531b079ad95eecc13cd48e434563c7df747c7ffceb7a60235`  
		Last Modified: Mon, 15 Sep 2025 22:26:11 GMT  
		Size: 59.4 MB (59385314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52339aadbf05afd473cd4bfeaaa45bdcd7163b20065b81af08752021c5822f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62edba170364b3bc66aa6da532303976b4d012ddd19b844fe227fc8fda5a4d8e`

```dockerfile
```

-	Layers:
	-	`sha256:4f4a504a00e3168f042046fd109c5411a387570db7b171d5644be3da6ec9675b`  
		Last Modified: Tue, 16 Sep 2025 00:08:37 GMT  
		Size: 2.5 MB (2520174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a391cc393d4a1cf17204efba1d060fa21bb0f5a7b4a0c9785098930843da629`  
		Last Modified: Tue, 16 Sep 2025 00:08:38 GMT  
		Size: 11.3 KB (11258 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:faf5140c72f3ccfe492557d9635585911f648440148a1defff132a523d01e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95765697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d5e7056b8e38e93cd02a6fc83870a49ad85520a6e9a874bc464861b53b3a63`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e0b78ae4eb2380cbb956456b2fcb96f5830621a15160d5dd226c664a502eef51`  
		Last Modified: Tue, 02 Sep 2025 02:04:58 GMT  
		Size: 61.4 MB (61436164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:300f1b642cd8797b30e4c3500e84359f28aa38f014dbb6ea452630e6e21623ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6b4fed1d483454fcca1b7f130151b30df2e6735befdfdb473b3a6f2fa126e0`

```dockerfile
```

-	Layers:
	-	`sha256:f59060ff1d0cf44375e757b62f35665c60ae0e4d627bbcb0adde345d9ee20ecb`  
		Last Modified: Tue, 02 Sep 2025 03:07:49 GMT  
		Size: 2.5 MB (2517717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a2762bd91b3ef3688d3b9cb3e82e3609a94804789590aedd5afed4e5235a25a`  
		Last Modified: Tue, 02 Sep 2025 03:07:50 GMT  
		Size: 11.2 KB (11154 bytes)  
		MIME: application/vnd.in-toto+json
