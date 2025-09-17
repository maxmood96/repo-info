## `sapmachine:25-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5db5dc4a50f46821c2187f092352cd0aace53791ce3820795ff3bbd8ea171445
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c54b4d4a5b2de9d467ef0927a23024d22301bf59d46ff98c6ad10b8ab6f5dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263348064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6521943d3c5317530d904ce6bc63a6c82034b91ef731abea313d2ccf12beb764`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e0d94b1583917327229d8b4b4a26396c18ef7e17839dbf460e61d90c4f4b5c`  
		Last Modified: Wed, 17 Sep 2025 21:25:09 GMT  
		Size: 233.6 MB (233624614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:daa5a81cd6411d5cb6f26a6f9aaac4a7930304aeba3964e56defa5f46f4b62f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dd9b4699a0aa93c528e4898d48a981371f379404d0ddc87b783e1c8b8c9db8`

```dockerfile
```

-	Layers:
	-	`sha256:bc71c67a851aa1edcc590703bc01c231b841f03d178ce796d5d12fa8547c85f9`  
		Last Modified: Wed, 17 Sep 2025 21:10:13 GMT  
		Size: 2.6 MB (2598219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e8fea722c47389c705d4a88ec0648992b71b22f11c652263321dde93dcb412`  
		Last Modified: Wed, 17 Sep 2025 21:10:15 GMT  
		Size: 14.8 KB (14779 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3f68ea64a38ad29bfc0d9da405a7b55f64913736114acec52e494802d064850b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260297448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1a490ba97f9aca5d89e5574831bb1fc72d477f7bfcd371863dd2e6e97af81b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba25b8960d63aa2c367d9d67db7a5b21dc33b8157ff6c405c47662ee2727c0bb`  
		Last Modified: Wed, 17 Sep 2025 18:10:51 GMT  
		Size: 231.4 MB (231436131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9fedf874241d5e9391ee7c0f924354723c62f164d81311f6d4efbae1960153c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b703573581dd4fbc344426d1f2d7a98b1efb9bead04928bd1f2ac8f4f98a7bee`

```dockerfile
```

-	Layers:
	-	`sha256:bbcb249278a5c01b4f9cfa6a46e1a2d2c21f52e6c2773e92783cfce0f82b46ce`  
		Last Modified: Wed, 17 Sep 2025 21:10:20 GMT  
		Size: 2.6 MB (2598912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efe4fbf3eb0881be50cf43254757505697c4853d5a3cde33770037954ff1d43`  
		Last Modified: Wed, 17 Sep 2025 21:10:21 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6bb86f11ed56b657e110238b8c471cd4932b6d2cacdc101a972150c35824a0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268799582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9f87483cf40703c515a29940ff46218003c7326bb17393c9be7fad8ca67ba`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af7e0dcc16d048eb7780a560deb0e700e5bef5dd9d664618c27b53acfa0d586`  
		Last Modified: Wed, 17 Sep 2025 17:36:21 GMT  
		Size: 234.5 MB (234496455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3fd8f7beb9a57284aec9b8014cdd051837bf0542a4dca29f2ec014dd9d1e8eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff88a7a6d5778692e9e6e466d120342044f23f14e1f0850bf9d425800d2fbcb`

```dockerfile
```

-	Layers:
	-	`sha256:555fc032bcec35a67108ae51c873474c531931f8791034ba718c80d084e823a8`  
		Last Modified: Wed, 17 Sep 2025 21:10:25 GMT  
		Size: 2.6 MB (2593826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2a88c2ecde85ccea72384e897fd4dbf539586c9e1143bacf4a42ea6aacc63b`  
		Last Modified: Wed, 17 Sep 2025 21:10:26 GMT  
		Size: 14.9 KB (14936 bytes)  
		MIME: application/vnd.in-toto+json
