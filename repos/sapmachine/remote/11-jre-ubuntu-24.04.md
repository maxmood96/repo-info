## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d162b747df12c8d3e1b92485dcccd69c11f1612d6312eee83f1ab799c377ec26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8ea991b5c360305d64ea85eb5d8211a301f1c62105e079b7598249c6aa4b474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80090424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78d2b5a946bfc13bbda2c9df244a39385edc23140978c1c0dc7cc4c87ffb95a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f3d607c397acf2c53a57f9a18ae66c80c6e6700e84781f01613c3c90d0c175`  
		Last Modified: Wed, 02 Oct 2024 01:59:55 GMT  
		Size: 50.3 MB (50340564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:45dbeee86aa3b170dacabe6c0dbb5d10235bbd0a45fc2bddd30b530137fa7947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff8df96074efa71868f2f2a7de053b982f22acfa3f2f5c264ccd9ec1a4366e3`

```dockerfile
```

-	Layers:
	-	`sha256:e69a3028ea024cdc38994a0037564ad63ec22f8bad436d2b293345e93169e309`  
		Last Modified: Wed, 02 Oct 2024 01:59:51 GMT  
		Size: 2.4 MB (2374838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a1743cc45f9fe172bd335c3d6f08146101e450858fa7758dd82af49ff4d7e4`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:74bf7d2dbf8f4574a9d866be9327f88b8d248eb97ae2af774585ba602d0a04b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78567166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c487b304f7d0629aca7676ab6d8ef3912d588e295e17d82902b26d63fcf6c72`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43e429fbb4afea1d69420f23f8510f1f84f5f75bbbe36f5fd715f7617162a51`  
		Last Modified: Wed, 02 Oct 2024 04:06:21 GMT  
		Size: 49.7 MB (49681736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0f9e46cf6391046a6c1a24994cf415f3593b8fdddf710b882c6bf9d046ff1c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f1bc2129c2b129950c80aa17443d4ebbb39e6b8d501ac416e34c185bd6a90d`

```dockerfile
```

-	Layers:
	-	`sha256:82d53f8f99d7e7fb3ab1b8182e9a2e9f844dc656de90180fc368d1dbfd5aa334`  
		Last Modified: Wed, 02 Oct 2024 04:06:20 GMT  
		Size: 2.4 MB (2375957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36af99803669ce8a80ab3a8cfe3394f1009a6137b22a3d991c61bdca78cb5d56`  
		Last Modified: Wed, 02 Oct 2024 04:06:19 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9f6046f49c5dcfb7135c63d10c02976320176b1f9d3bbf02b38aa4c49cf16035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83484892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae06b529f2a2352ffd177d656d6de8d27998c9737211e48d084600dba33cf32`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a16f52fd4ee53003ffd803f8b9a392627f2c04c69f8474c6b8c11a60a6f66cc`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 49.1 MB (49092871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:395ee1008b9ca11c3e09af588dbc28187b26a5f69e3589fff1075e3aa9517cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d83efbfc2f5fcf54d48d0f00ad624259b80ede3fc885d9adce2e47159d34d`

```dockerfile
```

-	Layers:
	-	`sha256:43437d070211a49538f6f79db0033296a3675927c3a95c430bbfb857103503a7`  
		Last Modified: Wed, 02 Oct 2024 03:23:44 GMT  
		Size: 2.4 MB (2378793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d52ce74ddece1220d4e076872c089474dcde209e34ba352a025a8ac28b7f5c6`  
		Last Modified: Wed, 02 Oct 2024 03:23:44 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.in-toto+json
