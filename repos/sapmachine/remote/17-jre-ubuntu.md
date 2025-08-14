## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:148a77f215243ace6a8a7152c31485551a9d884f819839149ebbeee4a6a46461
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e6f9e31422f6e1639341fa0434f5a2214ba13a350a400fb8f74e75da2b5faeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83978589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e0b87509d48ea4ac843b64c983661c3510496e56420ae1fc2e3af91a871d10`
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
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16429229da515509378ec59eec0cac582c3432707206c8192338c3638ac6dcd9`  
		Last Modified: Tue, 12 Aug 2025 18:02:50 GMT  
		Size: 54.3 MB (54255374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea3bbdb6d9ae35cce4006bc1d8087f51f26b276b0957da7fbb6cf3fc4970e94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca75b982d526cf12cc28143fc42b03eba94b5868d32f5dbbcf68e445761ac015`

```dockerfile
```

-	Layers:
	-	`sha256:236018d61f2ff041e9be081df4a1b0bc421334cd9fdb7bf79d9a2db711749a89`  
		Last Modified: Tue, 12 Aug 2025 18:05:00 GMT  
		Size: 2.5 MB (2517382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5a978ad39ee6941470267b15c39f68da36ecdd8b35965b2ac97e0dffcdf6d6`  
		Last Modified: Tue, 12 Aug 2025 18:05:01 GMT  
		Size: 10.1 KB (10093 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:658cdc21f3efefa9b5ffc2486d21404a38ff026691f52a870f462f7a2221756a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82546398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8db3f288cf3dab6bbfb46f6408ceee523f313ea212f016bf6765b36cf62d203`
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
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
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
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82ced03484273889584295eb1a934019a65d8889a3cb7e1e7f200bab9bf2ff`  
		Last Modified: Tue, 12 Aug 2025 21:32:13 GMT  
		Size: 53.7 MB (53686021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:96e41efefcbfac94ed9c3bf8117767f34970dbf281b448b4101ec96eee94593b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da23317090fbd0923d6c92794ac808079e794dbc4c6292b5e017f8544783d0e0`

```dockerfile
```

-	Layers:
	-	`sha256:028b2acec422f9692b723a1ee8ad05124f727e8b229bfd331ea3430d23583f8c`  
		Last Modified: Wed, 13 Aug 2025 00:05:19 GMT  
		Size: 2.5 MB (2517898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52220fdd242746b0f723f5dcbf79b3703daba205b0ca583cbe80938926c6b9cb`  
		Last Modified: Wed, 13 Aug 2025 00:05:20 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

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

### `sapmachine:17-jre-ubuntu` - unknown; unknown

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
