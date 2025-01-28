## `sapmachine:23-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f0a8e58785aa6f38b3a227f9f544bfe1444e4d5c82c968117b23b4ff23c97146
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:78feb3c219dd283a0062316686e7b71f6d6790f4b76d537f7031346b2847d76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88727393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6207c7328293b2e7487fc58d9676b0913225a4f2ca5d8579aa5d69e2afa65d88`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d46cc52909b8271d900fab038338c195bd94b79f1590eed675250978f2729c6f`  
		Last Modified: Tue, 28 Jan 2025 01:29:35 GMT  
		Size: 59.0 MB (58975425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd0ec4fdf80a9e419bc7616a15971cc4bf5d86f714c05f55220ee0a90ee665eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b85f9142cee3596279e1e7336d1347b66799c7f363effbf35b35bbbe695f3c`

```dockerfile
```

-	Layers:
	-	`sha256:4e04bf76059f0aa52e38b8e29545f922f70517d077b9afb92915d50256eeeca3`  
		Last Modified: Tue, 28 Jan 2025 01:29:34 GMT  
		Size: 2.2 MB (2150495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21db19fff28294408a051a14f146eb7158975461830bd580dcf16255d0d536b`  
		Last Modified: Tue, 28 Jan 2025 01:29:34 GMT  
		Size: 10.6 KB (10627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b23e7aa677123859bdb9100bfca0a499d08d9820e54c35fec40fe7ea5de2cc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86935847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581533851fa6aba532bfac6c36ad80bedc2ccf9d5f4e5921f9f963d759f22b51`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a6a220086de508995fd04738ac96534401de13054a4c95fd47cf54c67d2f0868`  
		Last Modified: Tue, 28 Jan 2025 02:23:08 GMT  
		Size: 58.0 MB (58043176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5052b203a4aabf4f7a8db8ffc0f8e7912a2450290f0a61b8e24c0e03224b0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66222a04152baba0240ac094a46678320c83a64177599a22fa69a45c93c0469b`

```dockerfile
```

-	Layers:
	-	`sha256:294c09e82faaf81680c0c340832804314d40306c3a0bc7e3d8ec784507cd250b`  
		Last Modified: Tue, 28 Jan 2025 02:23:06 GMT  
		Size: 2.2 MB (2150384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8479b37aa7d9ec3b40d1eca65c7025d564cd7117a214f2969c0d92e68ad55378`  
		Last Modified: Tue, 28 Jan 2025 02:23:06 GMT  
		Size: 10.8 KB (10790 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e500d4e46a8ea8743d6b42f159955f6c0de88f96e840a31ed420e1027afa9d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94742260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb5ca27c29b4443229cffe646bfbf20c5264a50ec62775b308b8cfbc33a6a08`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9872ef85daa452717cb3cba7c32cecc04d4acd5928fa4ea623f80feb40631cdb`  
		Last Modified: Tue, 28 Jan 2025 02:23:45 GMT  
		Size: 60.4 MB (60353440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e164940acc755f39170018c0c92b0ca0a006e0d577ba9010dd5715138c5a70be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a6a4658411ff5e17432ffd5d43c8b7ef955a425fb56d6f5525aa1f63d9492d`

```dockerfile
```

-	Layers:
	-	`sha256:47d7470482bdc6a4ec434a8a4a65ca3c708d5de84f438e5228c11af377d28360`  
		Last Modified: Tue, 28 Jan 2025 02:23:43 GMT  
		Size: 2.2 MB (2153771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4069df1b850b659fc40c5a4183f806eff4e9ad405243c13b930d0c90f73497d8`  
		Last Modified: Tue, 28 Jan 2025 02:23:42 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
