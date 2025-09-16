## `sapmachine:lts-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:53a27bbacc06105ab6625327ee429ccc23ef911ce8e30dcf8c38aac642727766
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:900e02961485516dba7219dd63e070e31a24fcbfcf0aa9b69f3756beb159982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245033508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe13dc867c901c486f902f6720f04247c82d508f752f6d4d770cc8dc1e226767`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799639fa354b664aecbb07809bc430f5056b1c0fff0e692ee257009b4a23d88`  
		Last Modified: Tue, 16 Sep 2025 00:09:46 GMT  
		Size: 215.3 MB (215310058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3682fedeb0153affde2251bd83a81c66650ee38c61a4007bb0fb3a0d47887c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c168870bcfe582e95e26c2b40ca563c9cb7e7b1c06f69b5a8fcfd6a570df91`

```dockerfile
```

-	Layers:
	-	`sha256:99375e0b76fe63b63627bce055e8d139885c3970d8ea3c5b03d3807e86b6dd16`  
		Last Modified: Tue, 16 Sep 2025 00:07:53 GMT  
		Size: 2.6 MB (2606957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4481445e609afec74a8af253fd4025dee72f99a495dffaf97a4dbff48bb1e455`  
		Last Modified: Tue, 16 Sep 2025 00:07:54 GMT  
		Size: 14.9 KB (14885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:36d1d058aba4bd97b0f3bdc7379299d440130ad9c1b36f794cef526fa69b61ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242407790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0761b8731f557723f2b4b384debcc270d9fb42fde5940f86ef847de7abf0e4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fe52aef1b20b37b3c8be5f276ca686a29fafb64a47884d9c3862fdd9e7e26`  
		Last Modified: Tue, 16 Sep 2025 00:08:44 GMT  
		Size: 213.5 MB (213546473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:42e39fa19bbb1fa779fe4875c8cdaee15b12c4f567464f99e8b72016ef20e49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e172887a675f6311004c8f53264d4cb6843dc7df70e95c7d9b165d557cde91`

```dockerfile
```

-	Layers:
	-	`sha256:82f062a62f037bc075954fb985859d0c7e284df0a4be0c5550739785213b5ef1`  
		Last Modified: Tue, 16 Sep 2025 00:07:58 GMT  
		Size: 2.6 MB (2607653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8fac9bb15a03455b08cff226234270c5a201f074c38ec131de9396dffbd9c8`  
		Last Modified: Tue, 16 Sep 2025 00:07:59 GMT  
		Size: 15.2 KB (15217 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:63751a4b216dff6d5d9f93c005479a63f09989ff70f283deb22796943afb1f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250593532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559297c530dcd2156afd7c9095edcb6bd830d74a5829a4c398b5d4066234d36c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110505d30f9d2a804b70954ece15e95c10049c25bdf4a800289377442f481ca8`  
		Last Modified: Tue, 02 Sep 2025 14:50:56 GMT  
		Size: 216.3 MB (216263999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cfb88ba3abc50c15c0d31840d5081b68413414228c2e15b8cf74652ad61f09a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7a8cf2ba847106788e866a890b07e3443781a969c1039c248fa77d0501aaaf`

```dockerfile
```

-	Layers:
	-	`sha256:afa7fc63a46d72d028db9ab60907eefa804e3e85fe236c1b8191df9fbd7f6f39`  
		Last Modified: Tue, 02 Sep 2025 03:07:16 GMT  
		Size: 2.6 MB (2603178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6180fbfb9a565ed0fd43b47cb9a9226d6093eb9934b9307571e178d695de8e`  
		Last Modified: Tue, 02 Sep 2025 03:07:17 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json
