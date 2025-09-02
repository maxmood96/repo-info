## `sapmachine:lts-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:61aa35b24a2881ce55bcb380150b28e2e318d23f5386a39e55e0dcce9dc905e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6523a40678f5f6b75617d228ebd294e2edd6c8513d36211a48158e57dddfb590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf8f0bd667074b79796bfe85af433a16aad2b7f73b7ddbed4aa6f7413cf00ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3915ff5494fc50134ad6ef219f4ac08ac6654f733763d21c9dc5a1a454572e1`  
		Last Modified: Mon, 01 Sep 2025 23:12:08 GMT  
		Size: 214.9 MB (214931514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a846e813ab19d2c69d2affeb9b433d200255e885323096682977eb5e620c1105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdda9f6799092e21980d9c10edfb40411082fece0404f05081db8aaef1fdf2e`

```dockerfile
```

-	Layers:
	-	`sha256:97191018b6e3ccd21f9bda92f7c44401bfe78f3b995f2d3c2b9d00ca416aab18`  
		Last Modified: Tue, 02 Sep 2025 03:07:32 GMT  
		Size: 2.6 MB (2631042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7190cf3b85b404b5f1e1afdbc6440c82736b2c17bb089ecf0ae9496da5c78a3`  
		Last Modified: Tue, 02 Sep 2025 03:07:33 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a654d70b246bde8aafe5fc85db20f5596da05a57496271abd311ae17dd3ba6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240466439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3883ac810f8c7482949ee4faf85ee8cda95c7fd1120534e8a1170938809f3847`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6bf6b18316ad81ee83c5315630455828210c5b8a9536fd1d534f5c9a604e36`  
		Last Modified: Mon, 18 Aug 2025 14:58:32 GMT  
		Size: 213.1 MB (213107192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1d30289af8f12e2ab08cf56da1eed12bc75dc816a629ccbb7eae6bced454365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d18d9092f39f2e70bad2b5afbdd5f2596e5622c3686de92fe08826fb72299b3`

```dockerfile
```

-	Layers:
	-	`sha256:10e63dca306dfbc1a752097c5366ad279689e6819e732f895b5a969b30c1a330`  
		Last Modified: Wed, 13 Aug 2025 00:07:13 GMT  
		Size: 2.6 MB (2630804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ac9f40831d09d91514350b0a42054ef071fb77053344930dc0275d14da2aa5`  
		Last Modified: Wed, 13 Aug 2025 00:07:14 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c396ff239b631ad7fa24d44c08cdad71543d819d81a0d8bda89f6454cc8987e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250207975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d442b897f5bee6be3db11baf63ea056401002afc7f78a4cd39e7e422cebcf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
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
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fac4e66c39dc45614a0ad61667c648101d08a6cb4233226c9810cfda825bc`  
		Last Modified: Wed, 13 Aug 2025 17:30:33 GMT  
		Size: 215.8 MB (215764830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f16bb3fa312ff242b68c3ab163c061b9df0f8bbb32dc83735030c7a57eb5aaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3230171704479e79582e04d1db7713630ecccafe8428a67815d5e9857f49bb79`

```dockerfile
```

-	Layers:
	-	`sha256:c89da740b6e9179e89dce9cb7b17d8692616a7d09b75c8753bda9da3ce3cb37a`  
		Last Modified: Wed, 13 Aug 2025 00:07:20 GMT  
		Size: 2.6 MB (2627243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca04e94852bedbc1abb72761e828adceadc02619fb3773f032bf1e1952bc6ce`  
		Last Modified: Wed, 13 Aug 2025 00:07:21 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
