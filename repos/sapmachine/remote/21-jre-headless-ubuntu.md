## `sapmachine:21-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:75fb261c61f6af4d34b0ead90371ac81cb9e56f7fe4694257ff139a3528a143e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d8fd7db96652922e72db91f96bac93a6aa38ab54947ebe5fd1425e11ae5fc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88846741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f896581cd1f660379d9852010237ad10f45aa3f14fcd89599d6791c82731b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f33c9db92523acaa27ac6562e59c86087858df90084e8a9cd970e24e617d95`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 59.1 MB (59141588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e537c21fabf635fbd58e6d75b0e5cafde53ebca51646c4987b5754e85822096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e67d0d6b39c827efe13c54e8dc4e66f81397f8098555569d090385811e617a`

```dockerfile
```

-	Layers:
	-	`sha256:232437f512984513abe65b1c23321c1854e8a71a3c574dced9c3e875433b95c2`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 2.1 MB (2127043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686b51044d30b4356c201f59a682c6975cfd1ee45f19d4d77c4d9556c3d025cc`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9472d937b31ad9787ab179970d2094760d1872a5f63cfdd99cdb37a442bf64d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87014743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcca1facce061f0c59c286a3ad610b7ffbfd9e1559d0b187fe5080d9dd01df95`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b2cfe6a634e7608013a4c1180fb5607215621f164dd7c2e68febf28d8751552b`  
		Last Modified: Wed, 26 Jun 2024 00:05:39 GMT  
		Size: 58.2 MB (58171700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d303cb8ae965c775277868cc11be6031fcc4b9c5a97b4fdab90be38cbd7f4db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2113894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93502e0cacd96737ba61bac00f8eb5b30b55726757c9b34401f81bbfed2a1e9`

```dockerfile
```

-	Layers:
	-	`sha256:c84d39b137260ccf62335e10ebde563365b928889509e44b13218927c5dd71a3`  
		Last Modified: Wed, 26 Jun 2024 00:05:38 GMT  
		Size: 2.1 MB (2103118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17464874b2ef345fc5c185dde23f56ba5b8776958368040445509dce58849ab5`  
		Last Modified: Wed, 26 Jun 2024 00:05:37 GMT  
		Size: 10.8 KB (10776 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:774b80ab777608fc01c3aa775ca56c24623a71c961a773ab5cfd9036dd9176d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95075082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85147d8acd97b1ce36a3b9ef9de33d392def9953a292c9432887b4e3b2252d5e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b20f0aa7ec9aa797a07834e5ac6998f9e42a3d1b828db0edd137b5deffba07a6`  
		Last Modified: Wed, 26 Jun 2024 00:31:35 GMT  
		Size: 60.6 MB (60569053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78cfc01624199ec0973903da86f9f28e899e9f4849a2110748c426b0fe056a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2116987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7bc1c11773f1ac1fb406c411f3d79d5231a12248bd4664f5da3e7d8016836c`

```dockerfile
```

-	Layers:
	-	`sha256:ca34a7a9fef748a88100155f8df052a16f634497412a945587e6ac9c5ce0ddd4`  
		Last Modified: Wed, 26 Jun 2024 00:31:33 GMT  
		Size: 2.1 MB (2106504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8f4f442629a419d43d9bc99b4d53d05e23b39102f44867f278253ef74688db`  
		Last Modified: Wed, 26 Jun 2024 00:31:32 GMT  
		Size: 10.5 KB (10483 bytes)  
		MIME: application/vnd.in-toto+json
