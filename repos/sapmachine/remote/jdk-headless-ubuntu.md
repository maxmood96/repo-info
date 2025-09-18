## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:0398910c0f6f8e1ff9b1882c19e246d51d030f779d1c82f5ee727a4adc7f04a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:155ff07dec5724241df277c15739d421866dbf844994db38531d4475e5b9d4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262161825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b1de6c10e22cfaf8b12eed8f26afb5f669222891ddfe287c151cbd3eb5e23d`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:3be6268a09a3e04539f34859f5fa1b8960eff14145bcbb1fbe78a99b1c36b393`  
		Last Modified: Wed, 17 Sep 2025 22:09:04 GMT  
		Size: 232.4 MB (232438375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d943245213e4dbc155b69c4ad1a259bc2fd7f701e981cbaa3bb9cd12142d5e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10aef3a7852bae1b4e624ddcbc7739b9bf95d09bc8b0038ae4a3ebd9ce3d65`

```dockerfile
```

-	Layers:
	-	`sha256:47c36f244a9c4da887386e04912ac204b52b60e56f295b13f4092fe1007573ae`  
		Last Modified: Wed, 17 Sep 2025 21:10:40 GMT  
		Size: 2.3 MB (2348697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48a2faa2817d347d62d0ede938007437fb1ed0fea9f678ce96a3e49849f3c29`  
		Last Modified: Wed, 17 Sep 2025 21:10:41 GMT  
		Size: 11.2 KB (11243 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:141f58afa4523f7dd7f79cee1ee1fe285651acd4b58b560bd7034eeabdd4c21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259098464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4183c201d4efd4b65eda131b38ec76e9d29c595df3e30a7123a57eb56aa2ff`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:42a3075df63d4cbaa5d32e34dc713aeec4c0ba7bb7cc24595650c4808038ac00`  
		Last Modified: Wed, 17 Sep 2025 22:40:56 GMT  
		Size: 230.2 MB (230237147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b7b0f359c35f229175ba4349f8669de3bf6dd7df8fe6b3e75d8070911231a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a98eb81e3fa6dd53502d5b48d98befbe29944cbe972f3370d9ec0412824358`

```dockerfile
```

-	Layers:
	-	`sha256:609a93b972d01b30cf77310442ad17fed9228cb5b1a12ecb12aa18d94f7792cd`  
		Last Modified: Wed, 17 Sep 2025 21:10:46 GMT  
		Size: 2.3 MB (2349237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e549890d27a39d81097b758e32415f3c91959c7e89d3fffcbb5a6858fe6881`  
		Last Modified: Wed, 17 Sep 2025 21:10:47 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3a42091668ed0143162edffc6feb62edb07eee2c422a210891d781ca9ba7e7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267415883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101222c91d48210994abc07c8c63650d5bff6a00f6ee2671fe2f069f97c00410`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ce456ddf55d46713b3d0143f186e59970c83d3eb76283978ebd33d4148b71c2b`  
		Last Modified: Thu, 18 Sep 2025 19:42:02 GMT  
		Size: 233.1 MB (233112756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73d6c19e668356652cafa6e33c6c31f57a165e85812c834a2de60105ba39d33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64c2b18b4995adf2e3a3d03d08d8e4d2cb50e4ba4dd449242e992f59760ff99`

```dockerfile
```

-	Layers:
	-	`sha256:4b8343cc71fa70cd57c47c1baff421f58dd5117a2bbb5e2e11f478aea46f9759`  
		Last Modified: Wed, 17 Sep 2025 21:10:50 GMT  
		Size: 2.3 MB (2344151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f938ee8dedd5a8a9829c87626a45db1602fd14960e93645053b1a79dfdbd55a6`  
		Last Modified: Wed, 17 Sep 2025 21:10:51 GMT  
		Size: 11.3 KB (11330 bytes)  
		MIME: application/vnd.in-toto+json
