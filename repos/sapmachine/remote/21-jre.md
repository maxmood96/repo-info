## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:85b409b9d52551de7203d1f1835afcc408576d0b669b8c75d5fb36b42ec953d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:6908deafd38bea8054c17f8f6742988b261953d186ef02070c9a1a24c347d24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90569289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd5e84356307edba97340cc7331231ac31eacd03bc331b298f1b29036acba4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:04:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afacc0fd7a902f40b1ffe7c398da1c31e02be29308f1abdc0e6a88aa854dffe`  
		Last Modified: Tue, 21 Apr 2026 23:04:45 GMT  
		Size: 60.8 MB (60836311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd44e4e96fc67ce6fd6d97e94e8edcb4bb6cb5bea04fbddc194b619210b4197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5ee17b8c436ea9f68ab85afdbe2d1cead66470a68ae3c3bc3224fc2483fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:305b9ea791285db02c8e98750ee58053f68d9d6e49e0c22a8b6ecdfceb3d1a61`  
		Last Modified: Tue, 21 Apr 2026 23:04:43 GMT  
		Size: 2.5 MB (2521694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92765648456c0a64d8eb15595b89482aba502da0b74931f2f1b55dd16be4d19a`  
		Last Modified: Tue, 21 Apr 2026 23:04:43 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:808e654a1b704e1f7b0562cfe6f33f74fb534dd03c54cd618b6f25ea44fe0e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88916754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d04ccf0bdca024546b00c3f6ef71441548ea46bf7717f4baa11c99b845be9d0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:06:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:06:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01095af4a95e5ca1c6c6099f78764b56a0c7a71fd7ed9c26be4cddeaefad08`  
		Last Modified: Tue, 21 Apr 2026 23:06:22 GMT  
		Size: 60.0 MB (60040969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c095e1e13e75e8ca5f1880d5c5af9637f3a518f2e2cec9ca34048b66a923dfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2532408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6182751af4975bdf87b413a2de14e1aeb7b7e4bd0c2895e5420898c869d3d494`

```dockerfile
```

-	Layers:
	-	`sha256:ca11673e074439b71fb7f0ecfebda3bf193fe3a70d72b5f846ff7523a7c78fcf`  
		Last Modified: Tue, 21 Apr 2026 23:06:20 GMT  
		Size: 2.5 MB (2522210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1470e086a19db3729c782be6af15a4f236619fdaad92fd7ebceb2de0b898b5c`  
		Last Modified: Tue, 21 Apr 2026 23:06:20 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:86e470329e1ff8e1974b371c4e2d013a899046d6ccd0ed1ab3bbc8b58acb780d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96478146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3aeaed7c581a695cb58aec3c1f12b4ade3cf6d7840c8fe0f0fee1d0687461a8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:23:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:23:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:23:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ce89c926adf9af81c43d0f2533c097c15ca4140bcaf88a2ed3fc72d330a39a`  
		Last Modified: Tue, 21 Apr 2026 23:23:59 GMT  
		Size: 62.2 MB (62163968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c4f8805ae47046895bdfe8ac1aa97757fa81ebcc4711aef42e0493984c52a48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857605380846f075465d440d97ccc467aee2214020c75078ac1d0f69d9a86186`

```dockerfile
```

-	Layers:
	-	`sha256:69ef4579a23fdae509693fd654d3b9d5985e693cc85c0e75d61bebaeafbc63e8`  
		Last Modified: Tue, 21 Apr 2026 23:23:58 GMT  
		Size: 2.5 MB (2521192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb5ed9856eafc73432618cf4b478e3fc0242e34ffea75ad3017bbc91be2618f`  
		Last Modified: Tue, 21 Apr 2026 23:23:57 GMT  
		Size: 10.1 KB (10112 bytes)  
		MIME: application/vnd.in-toto+json
