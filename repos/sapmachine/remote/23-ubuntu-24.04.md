## `sapmachine:23-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e66dda7129027518a343035c35a2960a3ab8ce8ed15150bf6e45ddbe19bbbaad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:958aa26449912ebf7d0ba891f0e8fb1c28a6206be2449cb9213b1690ca1f036d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252396528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c288d88c0dc6613ffa42bdb539267fe91dbb8fa6f913b09ff6d2aae838dd61a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3933b03d67a826e6417b196664882d4dfaaf76c889baf24831b320313794f3e6`  
		Last Modified: Tue, 28 Jan 2025 01:29:55 GMT  
		Size: 222.6 MB (222644560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8286963cb34046058d6c08693770b7d9fb7180d3e2790f5d5bf3625a820b96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4328d0ebb1d83e6ee1eaedb75cb116626acefbba3c35060992b69691c13d48`

```dockerfile
```

-	Layers:
	-	`sha256:3e140ee24193aa83f968e1269b2a771c5e3c7d482bdc7d58ff1ac6c9c06e17cf`  
		Last Modified: Tue, 28 Jan 2025 01:29:51 GMT  
		Size: 2.5 MB (2474334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:408679a885c1c1c02e52af361f15a0bd07c504f5bfb0ea0b207cdb64b6e88422`  
		Last Modified: Tue, 28 Jan 2025 01:29:51 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:363b887a2bf3a176ab92f98e30e731e8cdbd1905a700eef8cc404775cb668b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249552342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20acb818822d7a8d9d0ccbb0e3840119fbf068c7a34089d5e70f72412eef4184`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85bc133a635d647c395d95f23f52af61c928dbb448063f69ef1214c4787ad9`  
		Last Modified: Tue, 28 Jan 2025 02:20:01 GMT  
		Size: 220.7 MB (220659671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1f1bd3be31ebc75ec18f0fe84e26159b2c40e4229bed575a9b8d9ab2a4e49100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b75efe29f3f8cee30c66e376cc2ec4e61f77e6849548a542639fa3a4ffed88e`

```dockerfile
```

-	Layers:
	-	`sha256:d4711b1eb29e7cd1922e783782fad8e43ddf0228c208cb4bae041e32b7f5d399`  
		Last Modified: Tue, 28 Jan 2025 02:19:56 GMT  
		Size: 2.5 MB (2474340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1de1088a7a3a7dda88bd8408d3a2409b1902b7ec3d8d6b738d290689511ee4`  
		Last Modified: Tue, 28 Jan 2025 02:19:56 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:22dc7f44255795da230e8fdc05c3889d82023eec2141a78de0e5d59d98c75998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258194706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a56d17e2fca0f8dd83a0776ddb52068839b2aca89592b11b9dcbbfecc4353d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cb504b0f0b39eba54f37a5a1b7530fe147dc417b465dd929f2900968e88702`  
		Last Modified: Tue, 28 Jan 2025 02:17:22 GMT  
		Size: 223.8 MB (223805886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6491657c7187e90c43ed9f16d41f5af736c6f8541434a9b354e8e2e91938220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5cc499605eda870d5e0cba1a47fc7bb8bf906dcec799c3ca3e8754192bc74e`

```dockerfile
```

-	Layers:
	-	`sha256:1789c6ffcf33f384b350c60af4ada14a43fad0cf996e54c28aac73f92c332799`  
		Last Modified: Tue, 28 Jan 2025 02:17:16 GMT  
		Size: 2.5 MB (2475793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ba5c44c203a21fd5539ca931fc9de3e74c2035cf28b403149918ef2341a72a`  
		Last Modified: Tue, 28 Jan 2025 02:17:16 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
