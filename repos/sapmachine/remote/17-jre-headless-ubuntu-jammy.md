## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1bd967210ebceed1d0cee3d0a1803eea231c9eb5144ed8a298f820d2b755b1cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5d773c4c1db9c60a801f1ff706158a3debf1cb6f5093973d15c1aa85a6d0888b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82696774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4e57c991c086d6171839316e85c26cc30d2f494bb9d742432ee305afb7b9d`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:25:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfa47575905a29d44253844da24b1212616fb217d9e5db6c95e38c7e619056c`  
		Last Modified: Tue, 17 Mar 2026 02:25:52 GMT  
		Size: 53.2 MB (53158254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:57762c5ad4e83d6b48843b519eabb375672d103ef97f3d793816e86467663562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c46116dbad1b23ee8db3e00a452db614153be1fe5ec423c22bbda9d3e3c4e14`

```dockerfile
```

-	Layers:
	-	`sha256:446389fdac9e43224ee78541d88b2fe1435fae48dc42e8a34093bce843ee54ef`  
		Last Modified: Tue, 17 Mar 2026 02:25:51 GMT  
		Size: 2.3 MB (2295247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afacda298ac21cbd3711bba3a750bdeec331cfa3019662b070ac793f64209627`  
		Last Modified: Tue, 17 Mar 2026 02:25:51 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1a6a9f52ba36c2a1af955242def9f40537485e23876a97ff471b8ef0cd43cf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79949107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247fa609a429a72511896cd2b68cf290770aab73ce03f3e16a3d91fca8e75e00`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:31:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aaeee2107197d46235130a0f24c41ba216d31b5ecb9afb6fa78ca320837b37`  
		Last Modified: Tue, 17 Mar 2026 02:32:09 GMT  
		Size: 52.6 MB (52560082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:79a97b9acc19c07f17dfa424ac530bc09462709bf233c3e529f887ed71c71a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdad1276cb4fcc902143edf6c9462f0277fb8bd922b106275b9dc0d5cc8895`

```dockerfile
```

-	Layers:
	-	`sha256:2843e7d94c5fa85a7df8c572264290b06f5005f82eca919ac7cd9859369b5776`  
		Last Modified: Tue, 17 Mar 2026 02:32:07 GMT  
		Size: 2.3 MB (2294919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae02d2c2ed5906fef913f30770761b14254cb5eb6681631c5661cef9ba63e72`  
		Last Modified: Tue, 17 Mar 2026 02:32:07 GMT  
		Size: 9.0 KB (8989 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eeff87656f5b15a0082c1a40b51b4fb3ef2ac26f4702091132676602e49bc9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88612255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386f991576b4f07b568e29532bb7bd0a9cdcd6b7a4cf52ec19377e2e1846d866`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:41:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:41:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:41:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b6a97d3ed705216f4d4ba724eb8b5b25c4e93024e0f242b04c83e3f2f0e2`  
		Last Modified: Tue, 17 Feb 2026 21:41:48 GMT  
		Size: 54.2 MB (54166153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:16274365930c447250f867095f5125067ace450a3aa466258012e37254519c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2bddf76e6cf5846d7dfd63680a1944c7d165f67c7d82808c8134b3b726f12e`

```dockerfile
```

-	Layers:
	-	`sha256:5ded797244c8b2b876ca1c0a31471b0b26870ce677d79717e8feb53b5406a82c`  
		Last Modified: Tue, 17 Feb 2026 21:41:47 GMT  
		Size: 2.3 MB (2294689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926087b2570d762fac1237c0a47e9c0fdc5afee0e9ebc7287584f696ef0b6926`  
		Last Modified: Tue, 17 Feb 2026 21:41:46 GMT  
		Size: 8.9 KB (8928 bytes)  
		MIME: application/vnd.in-toto+json
