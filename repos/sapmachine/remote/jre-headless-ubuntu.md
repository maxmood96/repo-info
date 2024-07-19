## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:0336635358c147b9f715eca9bd553f391a07edbfc348a36fbc0191519ca21e8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:f7dd9f2c9d2d4d8e942aea4ba28dab4124248e81e041db8925334c0965ec0a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88032542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e4106dab35a09743b2577e382fe61a79965f2328e27996156f4f0609d1d43f`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf31b85a51781b2cb15507a47bf83dae5a4c63dd24cae6293f445cbe028fc80b`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 58.3 MB (58327389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0fac1e087395ef2c9a9b82f5917b2609e05480c3da4f209e5b75d7d99744cfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441788a92ba06faf833dd91f9bd3d1e28bb6b92c098b374940d799e87ba4a7d2`

```dockerfile
```

-	Layers:
	-	`sha256:03fb54ee45818ef026abee19ea1ddbfb05f613005e9b14fa0ed52bafb459d199`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 2.1 MB (2127650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dada7925b60b08846353cf806d72b42fd1768c26c7ddafa9b32d90a06a02503`  
		Last Modified: Fri, 19 Jul 2024 17:58:54 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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
