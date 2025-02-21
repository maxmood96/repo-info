## `sapmachine:23-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ee3460f8f67491e64a9122d889403938cba6cf9b4821685ee6a5b75d5c72e4ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:576043a16d4675fdb0c788368c80fe013a1dc413dbbf324724f32291e00ed6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250577982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424167bebd85bd7d9551e3da52698da29c3deb5345c3ebf66ca496f1f54bafd1`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47654bd29af7fb2ca650b1a3b554abe8244e73c238adfa833c58c5e225a55c`  
		Last Modified: Tue, 04 Feb 2025 04:48:50 GMT  
		Size: 221.0 MB (221042041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e9513fd30e429775826ef428f6dec32730bee3a7d75d9841f67017af38089c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1869d3ab8d977f9a4b990a7f32866ae12063290c745b76e09ced4ea6457705`

```dockerfile
```

-	Layers:
	-	`sha256:e921b27c632afdbc28e5125eada2c4cba3cdbdcbc454d454ba89944b408cdf4f`  
		Last Modified: Tue, 04 Feb 2025 04:48:46 GMT  
		Size: 2.3 MB (2252285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6c0baf8a5ddb4c65c6b4545d3da57c8c97931de9dc005e8506a68c1d4534ac`  
		Last Modified: Tue, 04 Feb 2025 04:48:46 GMT  
		Size: 9.6 KB (9611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bf45445d1cf397ca76446313b1263fd815632d8799ddacb7f4b574d6c36424e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246375841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cfbac61a4e6752979e927fa0baf7b91def86c4b32c2c6b5da128a4ef95b24`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f3ec48bc3c8e8c68d81caf39296232e6e567f46899bceddbcafc4d8eabd12d`  
		Last Modified: Tue, 04 Feb 2025 15:22:57 GMT  
		Size: 219.0 MB (219017659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a8f20794d738bd01425c11165bdd109cfd10a1209fe34421b503b9bc9f8df62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568c3b9f15fb5c797e413ab286110d414854c56b6df0ee72408612c35ce02a3b`

```dockerfile
```

-	Layers:
	-	`sha256:d3dcef5ec078e35fde95c6115fa93d2e6857163682f135557f0731dc6bed125b`  
		Last Modified: Tue, 04 Feb 2025 15:22:52 GMT  
		Size: 2.3 MB (2251351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a1082d0124dc13e5c853504435f2407cdaaed146d6d4308425256022f46648`  
		Last Modified: Tue, 04 Feb 2025 15:22:52 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:26ba23b453747eab688c13fdf740418a2af5c81060981ae2f5872d1b782b8642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256353291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3a37f51714326f7ed19c202bd33654a824ca0455f2d312b5fb0e4a17a381d`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a94841e7e611c5a58ef5f05551c1f81d612096f72d35551d187f31ca92f2eb8`  
		Last Modified: Tue, 04 Feb 2025 14:29:36 GMT  
		Size: 221.9 MB (221905356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3051bfd3292c3b416c80032f35a7ff12eeb78b46b56870bcdd87bb3fc2e3ce86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2263311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7fc8c0b9e59cb4b231fa7bac362aa8a1ca1976599b20c3656a8fb7396b9f54`

```dockerfile
```

-	Layers:
	-	`sha256:b5013a50a9be4129e02dcfe74f96e28cddc3e0c3dbfc2c1e12d9b5337ef4e63c`  
		Last Modified: Tue, 04 Feb 2025 14:29:31 GMT  
		Size: 2.3 MB (2253644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e2ba41a1dd88d1df0e0964a5bb46384ecc43cbae43195e3f85c58a62a673d1`  
		Last Modified: Tue, 04 Feb 2025 14:29:30 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
