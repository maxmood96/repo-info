## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:03e8dbd0d8b79431baa164a7593b0eb0c38ab33a1411cda0911a856cb025ef52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:41d208bf05b65e621cdaa00c304fa436f25a27aef07b4b34873413d4721caa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83978505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8984bee325327631f98d51a35fdc31f59358ea6dd0f0fa3e5d2d96af8532eba1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b88a19ad4ba18ae6fe465d7ca6534beeb780e011433462342d3cc8dd302b68`  
		Last Modified: Tue, 02 Sep 2025 00:25:13 GMT  
		Size: 54.3 MB (54255441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37d68f9dd0630aba1c21439077a5aee9fb28508642a82bde306e5c11c69b3f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a51df322eaeaa88fa35fbfb6b7710a77b9b14574aaa22c4ddc924f56395294`

```dockerfile
```

-	Layers:
	-	`sha256:74a79387526fd7bf3161d9cd821945210ec1f83b88389aafcdcbd49ca96f451b`  
		Last Modified: Tue, 02 Sep 2025 03:05:51 GMT  
		Size: 2.5 MB (2517382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475d175661643d7d89cf6c0a9e37ce9b65cb5fd989bcf313554535703dbcd745`  
		Last Modified: Tue, 02 Sep 2025 03:05:51 GMT  
		Size: 10.1 KB (10093 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e5c4933e612bb5114daf9334a0bf0cc6536842c4baf56ba038c9f25559e55d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82546163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e93c0e6bbd652586504593c19bdb04afd0c95c24b4489f849a304cd4294cc25`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df819de86f01e32f0e9e0e289ae27bed473a085ed415daa4aaaf340c4dff6547`  
		Last Modified: Tue, 02 Sep 2025 07:28:13 GMT  
		Size: 53.7 MB (53685923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c8bf95356823d79f889cd31d8902f8e8a6fab36b35563669335941e0dcbd2ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba32e77594cb90bd9026f9d92f3367b81eb2656f12d47655135a8ba39db7a62`

```dockerfile
```

-	Layers:
	-	`sha256:c13ceb52777a00501daa794d30852b855c5d178325356f41fdee742b17e66331`  
		Last Modified: Tue, 02 Sep 2025 06:05:07 GMT  
		Size: 2.5 MB (2517898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6eac9c97ba05393c620e102f24afa5864fff1baeda0d0a0576a27dc5f915d7`  
		Last Modified: Tue, 02 Sep 2025 06:05:08 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7f382e8694fc062a2736073d41bc2f5d07cfaab85fbd894bc49044a54878c043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89776746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36645f9f2b7df2c5701bfb02703fa5c2556fa3766853cde97326a3e05b87f3d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb710c3718b6335021d182eb2bb01df567dd263713b68330f369b00dc381da2`  
		Last Modified: Tue, 12 Aug 2025 22:55:10 GMT  
		Size: 55.4 MB (55447096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14938fc47992b725ff0613a7468ce0ae225a194ad39e7f4f555967e48d90f78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240fbc57b3a9a112ab759e4823f12a6f377f788d158ce07da0ae941cbbf7276f`

```dockerfile
```

-	Layers:
	-	`sha256:5bcb60dafbf58f91da31fec8f5f748d07e195f73f93c4f7a0f3defc39963b058`  
		Last Modified: Wed, 13 Aug 2025 00:05:24 GMT  
		Size: 2.5 MB (2515463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ce2c84b1c29ae765724ff30953ccc5b1fb10cb4cb3dd7d1915c1373f4e536`  
		Last Modified: Wed, 13 Aug 2025 00:05:25 GMT  
		Size: 10.2 KB (10161 bytes)  
		MIME: application/vnd.in-toto+json
