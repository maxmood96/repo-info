## `sapmachine:jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:cc256f7246ec94677e5364400454b2478377dd1b93901ecd4741e89b78a9de7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:063f1276feda6f430020c85d1b6f6f3c6120367d0e4dfffe3c399260dea0b3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86190038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69adaaf2fe9eafca10435ff2d6c7bf5780a8146058429dfb8599207bc253450`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a13caae626c3227a751a5190227c112eaa90ae29e4e543757e21a7c7c007800`  
		Last Modified: Fri, 19 Jul 2024 17:59:07 GMT  
		Size: 58.7 MB (58678269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:00b82c1aab4788b28da70095f9d1031e4363bd83449ad0183841433c0b17911a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82eab9f282b74c863b80344ea66a882ea858a01b54a65c74e22d7dc9836c9c7`

```dockerfile
```

-	Layers:
	-	`sha256:4da1581b1fc2d93037b63bcc47c35a24630bd72c28b08e585e3bd594e70ecb49`  
		Last Modified: Fri, 19 Jul 2024 17:59:06 GMT  
		Size: 2.3 MB (2282819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7702a91eb300b4aadb95068aa1ce05548dddc70fd515148ba9e9abfaf4b76a65`  
		Last Modified: Fri, 19 Jul 2024 17:59:06 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:61d313fce51b400d4b3fecfe998bb32fd32c524466f9f1f8f0c0a96d2d43aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83878619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70ad9efdf2510f6dd783cc992fe7dd0ad0a8ad129d1763975b4279c3daf29e8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e370f6f1b35b247f480b4c83d58d1a867d29fe5c2b32d326792d305a7d0962`  
		Last Modified: Wed, 26 Jun 2024 00:01:01 GMT  
		Size: 57.9 MB (57904402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:931f7e79d1f386603d95267f816c9c822597c9d3cb4817fb8bf3123f3495d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60221e89af1113fef21cc771b221cbdb826dfb042d729d30d2dfbc986ccc46f`

```dockerfile
```

-	Layers:
	-	`sha256:6eb680e09d7d1b5de7eec2cbe4b1b93fe03d4bf5b4c0caac8bc2a1ff7cff1a0e`  
		Last Modified: Wed, 26 Jun 2024 00:01:00 GMT  
		Size: 2.3 MB (2255260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cbb0fec5fe49dcbb562edb94dc0f8cdc1c17b1f6a153ab2c7057ba922dbafcd`  
		Last Modified: Wed, 26 Jun 2024 00:00:59 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8596ad26896288dbe79de467d30cc900c759eee604723d5464d7e195c651d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92007777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2841cb508fc66f4e20b14d6f52b7ff302bb31899347989bd978336201ccf2b19`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6b1fe164b1499d1ddf38ea7a433b0fc77e130696a759f273373efae4023950`  
		Last Modified: Wed, 26 Jun 2024 00:23:40 GMT  
		Size: 59.9 MB (59930637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0face31eefddbf0d08402658ec57ab6dc9adbd7202ff7d9127bad854164656b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fcd6c582cbc3aac04344d74777cccc982e150e79f33c6c5a5dcbd02eaa822`

```dockerfile
```

-	Layers:
	-	`sha256:9d511e78ac5635b301cdc0828ea8c37b337b4139bf344632bcc9b67062c069b1`  
		Last Modified: Wed, 26 Jun 2024 00:23:38 GMT  
		Size: 2.3 MB (2259377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58d0a9de2f8eb15547ec6bbc7d0f0faa1d689a1f1435a509d03b1aa927b2543`  
		Last Modified: Wed, 26 Jun 2024 00:23:38 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.in-toto+json
