## `sapmachine:22-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:dbc6442d860e713595ecb826dac2f143c05d02ca90a902e6a2ce099ca4b3722b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f768e720f53727728e4c4d25c2020823b30ae7f5ea5722cfe0bbc4702055a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88233820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba94581d1a0945e54c99a37f500e06fd69dc5de38982f776792f09abe07e3c0c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ccfc50ba1d3a0f30071a61f25ef9db4a9be528dad878b169f92aeedf6dade`  
		Last Modified: Tue, 25 Jun 2024 22:57:31 GMT  
		Size: 58.5 MB (58528667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b266803ddc7dd76847e78081aab49d3443a969c400508264ae5b71e59afd632f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2113598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d13c6220e41bf1cb9eca92be71130c42dc3a6c762c138fb5436d336e9579d22`

```dockerfile
```

-	Layers:
	-	`sha256:77de8784452c90c7c2e8dbed67b628224616a9c01871bc6df29a7fecce42605e`  
		Last Modified: Tue, 25 Jun 2024 22:57:30 GMT  
		Size: 2.1 MB (2103207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ffbb1dbe0dadd5f63def4fe534b5395b22576e59aaa4084321ef8a1b19d055`  
		Last Modified: Tue, 25 Jun 2024 22:57:30 GMT  
		Size: 10.4 KB (10391 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:712b5e5755655b80f21dc461a812d7b0dd2f36567a4f1556a671342d6ed6aabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86408802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269f53f6da47b808c3f33b63f513883ed7339833d890b07ffc02cbea017c234e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c3c44c37351e9db550fbeb9cccf92f145a8997a03f15329ec182afed412e4b`  
		Last Modified: Tue, 25 Jun 2024 23:53:04 GMT  
		Size: 57.6 MB (57565759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:641d4d92e00b1fe70155b539ed78c9a6379576bda4f63b1446d92e9c781ffd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2113846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4dfd532ac9f60ad32716e8b7a1094d31aa12603fcf030527b67b96f1a7f433`

```dockerfile
```

-	Layers:
	-	`sha256:917692ef6402845940070403a79d432cb84eca462a461676d7ebab74eece0c9b`  
		Last Modified: Tue, 25 Jun 2024 23:53:03 GMT  
		Size: 2.1 MB (2103094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f280ae2989aa86e26c910ac244ccefc6d65c536800144352b4e895d1bcb934c5`  
		Last Modified: Tue, 25 Jun 2024 23:53:03 GMT  
		Size: 10.8 KB (10752 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:531b4d0b693b92b251ad13ed91c98dfbd06743013610ebc008b4b49f07c0c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94414088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85904bdad4008903d7a7132950f2f995d747099132b64f1aadf671de03c903c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8ad9c07056a2c004dee168fe472920d0130c89993c3d5dec5a5ec1e0307dd4`  
		Last Modified: Wed, 26 Jun 2024 00:11:06 GMT  
		Size: 59.9 MB (59908059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fa11a5b4dd30d494d8b82f09c3df864925fcdf135dc1f7845da38001dbdd6a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2116937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ef41a025eaada01d076f9fab2633fcd38799357e9a809c369b2df8bfeadd84`

```dockerfile
```

-	Layers:
	-	`sha256:f408e28b77c4185d01f32bcbf7108533d0cfd6987b83eb00e5976347d9aaa1dc`  
		Last Modified: Wed, 26 Jun 2024 00:11:04 GMT  
		Size: 2.1 MB (2106480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77a93fe84fa61196b2e8f2377fac1ca475a18ef05c19f9ab93f1fc358947da7`  
		Last Modified: Wed, 26 Jun 2024 00:11:04 GMT  
		Size: 10.5 KB (10457 bytes)  
		MIME: application/vnd.in-toto+json
