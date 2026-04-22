## `sapmachine:26-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f830064f576ec2d5a7eb24ab9eb1ef9a8cc77c93b3f3308027ca24e3a2de535a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e162eacf647c6866d158bb8b81314be401fe2000a8b524a6ad107f912880464c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88729266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e477b6ff1751083d2ef7cc4ba63f9cd5540aa99e8f2dbe4f4f3c940c21045b`
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
# Tue, 21 Apr 2026 23:02:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c63ca39ba49604b2bdc613bcdd75d7bf5a98f18a9349c5bf672bfb244fe1b4`  
		Last Modified: Tue, 21 Apr 2026 23:02:22 GMT  
		Size: 59.0 MB (58996288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:85d88704fad6d78d2954b736fa35dea708081d387ef745eda4bccbf29ccc5c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc679d20cfdd8853754ca0784de5601f69f1295fb05634900a2a855dffb2c6bc`

```dockerfile
```

-	Layers:
	-	`sha256:0dab54844144c1a5388bcd50ff6a2b753a1e90fda69c831dee35a782189bc65b`  
		Last Modified: Tue, 21 Apr 2026 23:02:21 GMT  
		Size: 2.5 MB (2526186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed831dc2947b59db943b140cbe69c343d436bce509b5f07ca50e0618104828b`  
		Last Modified: Tue, 21 Apr 2026 23:02:21 GMT  
		Size: 11.3 KB (11301 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:06803169fb016c06110ec3cc667c53bce9127645f2f553440ac77ef106c6db93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86901476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acd0c35fab3f20d070ba4bfbacf42b5fe1dd11bd47e2c29bac2fc788039c6c0`
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
# Tue, 21 Apr 2026 23:04:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181c9e7d8e3e2a73882ade2deba5f232efe7d0e9d45a292b44647f26425d18c8`  
		Last Modified: Tue, 21 Apr 2026 23:05:03 GMT  
		Size: 58.0 MB (58025691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfe959c76a7df041b44acbf5f64fb19b815debeacd4bb5c3e27cb745eab5c27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f81aba1aa87aca11b3e0f9fdfd5cbf7e0cde9bccd620b7a2ec97eeb390df3a`

```dockerfile
```

-	Layers:
	-	`sha256:3a437f2301ccab4f77a0bb29acee97f53097f7b9283eba830ffea044bbfc83dc`  
		Last Modified: Tue, 21 Apr 2026 23:05:02 GMT  
		Size: 2.5 MB (2526747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cc131038c75a23f2d1d5c6fc7d02377dc9dabd3e7f8fb00229ea1af914cdae`  
		Last Modified: Tue, 21 Apr 2026 23:05:02 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:531e35dc930286277e7ae5a2cc09fbca7296d0942534cafd6516cb5e34a1c493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94490893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9efae4451b0e28af05259993eb4d7e6e326adeea8d67cc437e3251ddf3b638c`
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
# Tue, 21 Apr 2026 23:05:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:05:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f2ec0a936fa01603b3d294c4aba8917349da62f6ed3f57ee9cba062650b602`  
		Last Modified: Tue, 21 Apr 2026 23:05:58 GMT  
		Size: 60.2 MB (60176715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b452988a9c67e840621e163f7011e6b85bf6efc8a183a7e8899b8125a376d8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2114aae706617ee13767e58667fd626930d3f4bf28f24b25af2a3db526888e6`

```dockerfile
```

-	Layers:
	-	`sha256:f5983bfddb748ec4c028b45527e71437597fc50721da1f0699c3e1a5fb266b5e`  
		Last Modified: Tue, 21 Apr 2026 23:05:56 GMT  
		Size: 2.5 MB (2525078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fefd1dbbc08221fc0e78aadc1bdf001652346f2e0404e3620f2006637867795`  
		Last Modified: Tue, 21 Apr 2026 23:05:56 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.in-toto+json
