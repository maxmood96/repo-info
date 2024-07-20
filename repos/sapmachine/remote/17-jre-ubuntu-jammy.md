## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:35d4b096585097b8c0c47a6df111777fb54e5b9376f4057d587ed65cb583695c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:284051c51b81401ba7e319d2154d6e6158551e2db997b3810eaa2ef180e378ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83244776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c89f8390e1b0b649984dabc489e4b12b8188fc515f93c8eaac04eefd3e010f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4407f7096eaf9f0a2b7d2e81d8b9a7173f8060b1bbc420e615ec4364c034b704`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 53.7 MB (53710721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b73437d79ac806cff6b9471f9f834beb120282ee573eb53a6bf088edb520d9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3c9030c8829321b4f9a589f86435177b7896d8e2f7ffbb3870860cdb5cd1d4`

```dockerfile
```

-	Layers:
	-	`sha256:35cf6508907c895a3d2a9cdc3c00d6e4aaf43c8429871d7eb035c144fd6df5d6`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.4 MB (2386862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b10397699bd666640da454cb58f64bd6659ef06b5200a9939158ab6a91e1e9`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:963ead15da639450aa3c476a9ad66731546fe4cbf50f1779e36a7bc39ebccbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80405726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0d98f3005423aa7963e0e24fc767af8cde3604d3cc8b6f5ebd32e0a5b81289`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfe7fc16fed13a737867eb06d7e146fec2f0ff07544d3a396ed862b112498a`  
		Last Modified: Sat, 20 Jul 2024 00:28:05 GMT  
		Size: 53.0 MB (53045701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1781ae860129677ac58994b58a3df8eeaf4a8c5459c38e33899a0d872cff15e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae03736d9d32408084e4e64a934ca49cfccfdb2d835c00982a07fdf099b08d13`

```dockerfile
```

-	Layers:
	-	`sha256:33a7944ff6a928463728af864afd03deb8847031c6d7a1d36e2420b518e2167c`  
		Last Modified: Sat, 20 Jul 2024 00:28:04 GMT  
		Size: 2.4 MB (2386542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b1fc7773723dfd685103222cf1528ac6c7556b66fe1256fab218f273d7feeb`  
		Last Modified: Sat, 20 Jul 2024 00:28:04 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b778fa1f310b30abf99259055326a08fca0bb1baf1af15bbe70c1021166e3544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89656235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63ec1426758a00210c5ad3d3dce877c8ddb37614c2b652c0faccbc58c7fc0ce`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c61b69f7e49fce52be09b8dcb1777adc12938c90886cf5fcaea7cd8dec215`  
		Last Modified: Fri, 19 Jul 2024 23:40:47 GMT  
		Size: 55.2 MB (55195154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:abf9607877ebb2749886f0f62a88ec24d198ee35bdcc6320a0da2bd3327303e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074cce4bfc98ee15cc4d1c2eb9b85fd54211812b3b639dab483bd4f0df3ef205`

```dockerfile
```

-	Layers:
	-	`sha256:95f5fc232b0dadf630ffa119871da1db6a6bbf2a089e005798e23ef3ccd85127`  
		Last Modified: Fri, 19 Jul 2024 23:40:45 GMT  
		Size: 2.4 MB (2390841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9aecff8f7291ddecd338c546e10a386f3874f4aa5b2ca9a44cabadf8d8ad2b`  
		Last Modified: Fri, 19 Jul 2024 23:40:44 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
