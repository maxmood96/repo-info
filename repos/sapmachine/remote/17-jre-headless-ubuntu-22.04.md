## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b8b733d5e9244218a55fd357768972939c730dd73243e29434042c782fd45660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:55979b970cf5439090a9b341c1b2cbbff99cc9a8d9d09edae9fa432a55e91dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82695800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af2971803da7070ea1114932593fa258d5fdc779f2eb22858ba676f0c65087`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07674c8183fda0f206972f0df5845c98fdd3255b400b6c5f3a187770f23fadb6`  
		Last Modified: Tue, 17 Feb 2026 20:35:52 GMT  
		Size: 53.2 MB (53158434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:85c34f4b04dfbc77fb8a0e0e4905b0cc88bda0db046a1f333eebf9f50e50a638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796f31979d2ca0c4e0a9ad509ae1b0e5e3ac4557343ef41b58b3d0b4ed48e49e`

```dockerfile
```

-	Layers:
	-	`sha256:f8af090368ee689ede5084bdca409eb5d6b5502d4ff9581eb7bc8cdbcfe333ab`  
		Last Modified: Tue, 17 Feb 2026 20:35:51 GMT  
		Size: 2.3 MB (2295247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8739f38a8d08707189a45bdfa2fc045fd32fc0ce4fc7cda18b757f884812efaa`  
		Last Modified: Tue, 17 Feb 2026 20:35:51 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3bdec4feca1612a35540d09b1d51a252e8b763a4dd3e5889c3476d61e3ea676c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79930068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a55c30ed9574614a9f9ac2c99c7e080ad9ca67682f2b6a3b5ee5bf35550dc45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c82291e339f6aad020632b8c94b3b80a28f6e12f94918fa067f9bf21702634e`  
		Last Modified: Tue, 17 Feb 2026 20:34:55 GMT  
		Size: 52.5 MB (52545124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08d9bfc59b86191a5921b50412316228eea63fd1bb4b82e20fb741cd098051bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b43f431330067bf88a9220c32ce86d56138375f5787054fe699a353794a196`

```dockerfile
```

-	Layers:
	-	`sha256:5443f0357108ff0b3503b16e43e9c1e10214ad0ed7e6b852d727391886b074f3`  
		Last Modified: Tue, 17 Feb 2026 20:34:53 GMT  
		Size: 2.3 MB (2294919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02406a3cd45e9e727e52f4107cdde8c5cb93ed217b6064fd1aa5bca65d44296e`  
		Last Modified: Tue, 17 Feb 2026 20:34:53 GMT  
		Size: 9.0 KB (8989 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

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
