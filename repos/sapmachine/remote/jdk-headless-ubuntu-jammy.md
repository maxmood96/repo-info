## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:63987c1ed877437e347059a0ee4d1d5c3ab4ae146798f7a394e8be3eb57bf420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ed441827c7b9576d3e9dcca6d18aa1ee23fbaa0f80ceca43965ab49d1594962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254293802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3db065998b97900d3abee74b873eb12826d992c6de6fcb7318b39c8ceb76ee4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:52:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:52:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5897f2d13ba75ed025002bbccea208043415bd2e975ddd9025731a104a2ab48`  
		Last Modified: Wed, 18 Mar 2026 17:52:46 GMT  
		Size: 224.8 MB (224755282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ac5dd7848d90808df884cf2c51bd9a33b3bf829ecb056cd54570040ca4f8685a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da73b3704554ad96a375ac190560722689c08f71ae6e2f46b32963694f05e003`

```dockerfile
```

-	Layers:
	-	`sha256:09dc012b33a67261f4937802dfdcd8a851315dfb3c492cc7e0de2ac2a5fc1d85`  
		Last Modified: Wed, 18 Mar 2026 17:52:36 GMT  
		Size: 2.4 MB (2367547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62d18c371cad7e76e2853d18251127339fca39d8b1cad8abb1b601479a6f2e4`  
		Last Modified: Wed, 18 Mar 2026 17:52:35 GMT  
		Size: 8.8 KB (8845 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6337d3158fbeb638620f25bb5602b84d4275e0a17a2ee6e689b51770f036d487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249957271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c118dc4086a9de58c5949a8917e63c2650a17a131517def6a4c71735d7f4d302`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:51:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:51:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:51:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e648f95f870d9a36ab73f51dc3764445ca26464400a0b71d9f3bcad7cc7a180`  
		Last Modified: Wed, 18 Mar 2026 17:52:14 GMT  
		Size: 222.6 MB (222568246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3342fda8fb35724cf2773227f976a942d64529fa82bdec195bb352cb4a83bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb347031ebe04dcc6d50cc6e662ca346f4db37a6c38a7e24738f5de32d7b75d`

```dockerfile
```

-	Layers:
	-	`sha256:7534d9e303189bcd1466bd89f836a5bf11f93061efedb3be6f2d129bfc182c61`  
		Last Modified: Wed, 18 Mar 2026 17:52:09 GMT  
		Size: 2.4 MB (2367216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8338c74cd00b546438613b2f41a0c3f61f3fdfc0340711c66b5ee720e105dd13`  
		Last Modified: Wed, 18 Mar 2026 17:52:09 GMT  
		Size: 8.9 KB (8949 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c1ccab27a4e931a4d1f4498fd8be3994e8f3375ee95d501f3175082244fd36a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260194969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c25a143aaf120823d9463b0b77583971644acf79acee5c301017ffe6873a22`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:50:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:50:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:50:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f9f199d57d275c99e982354d41d5acaa10e6d9fd38f3102a50d29e209ce706`  
		Last Modified: Wed, 18 Mar 2026 17:51:36 GMT  
		Size: 225.7 MB (225741521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9e4ba1437b1241e285c24d9c6a9801ff1ec763d8adeaee80101c70b2dbc9656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18de306a039046a010cbf088e13b46dc325710cbe47e40467140f10e7acfd2d8`

```dockerfile
```

-	Layers:
	-	`sha256:555216c940f6cfa0a791ea2d7c3130d0b63e93c6be33e7a630cdc0f08e64805b`  
		Last Modified: Wed, 18 Mar 2026 17:51:30 GMT  
		Size: 2.4 MB (2364425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7bc421cb7fe75e7504dc1c0d29776e4af09a9c6a90267187799d521893c700d`  
		Last Modified: Wed, 18 Mar 2026 17:51:30 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json
