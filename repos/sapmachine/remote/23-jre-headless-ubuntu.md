## `sapmachine:23-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:8541187453affab90f734ad74fe245d38e221ef8674a8b4c13bb4202733ebac6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d6fb17b7f262a333d0c466cadda608e1016c6196923a068e0b6536e9c82dce3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88729656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6210b465bdb02e7e507acacddacf81baedac036a16794a34191345808032b2d0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d515e61cce0af8ce59b8c5abfadb27fa41794f7650b676fb9e717bf9e880a5`  
		Last Modified: Tue, 04 Feb 2025 04:48:01 GMT  
		Size: 59.0 MB (58975366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb850de939c8aa053c855853a0c08805399d896a59e9873899fd330b00907e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d963516ad70f5b8d71f189f1e39ea85f4074b303ced06b6492d6c88f4b583e5b`

```dockerfile
```

-	Layers:
	-	`sha256:09dd827de280b26098aca17a25a1a1fe194e98287d3020789cb67431884e1f85`  
		Last Modified: Tue, 04 Feb 2025 04:48:01 GMT  
		Size: 2.2 MB (2154457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e737596fde1ef860fb68b83fb7cc1ab219b8471824c04f89ab8b60d99504f5c2`  
		Last Modified: Tue, 04 Feb 2025 04:48:00 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:23-jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:23-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:453dce80e3c14a771569f7c4a6f202a57d0ed0d2374bf650e2b207401badb365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94726832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f146ac73364357d9c6229e31c900f7f6bc98102102893cacab029fb503ccf3b8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9e448f8091aafe9a2899581500beb3c390937a192aebac0ad02756d7f10286`  
		Last Modified: Tue, 04 Feb 2025 14:25:02 GMT  
		Size: 60.3 MB (60337008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23cc5b0a7518338a938798952d060edde35f264115fc1362355086151ce94e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829df587760818fac1caab0d5b474a504654fc1f6cc4853c437f6f9b3983c6dc`

```dockerfile
```

-	Layers:
	-	`sha256:8935b75e8e372d20ef6a7cc2cccd6ef2862feffe657b1f3ff9c8b0a5dcab0554`  
		Last Modified: Tue, 04 Feb 2025 14:25:00 GMT  
		Size: 2.2 MB (2157733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69dea93f53edd94f51ffaa0dde3708e730711f8f8d5bc130f13233ff12b1812`  
		Last Modified: Tue, 04 Feb 2025 14:25:00 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
