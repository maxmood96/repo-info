## `sapmachine:21-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:d9e97ae4240b5ec1de1cfcca4ac49f438146523c170a1d13bbcd7442e027ec79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:95b3c96df4688a0774164917649310a0e989301994bc74a11ebb7dae7dc854dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff7dfa6de010f048e23701ea261972fe5d476c9c370c8f64b32ce523828d626`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9305a310f84f7c8e44f41e136854a546d3460a1267a200301bed3a171270033`  
		Last Modified: Wed, 13 Aug 2025 05:42:19 GMT  
		Size: 214.9 MB (214931472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d346833c7b3c77cf94ff09c86c561cbbe4e5e138700f83ffd4f5b9ba35aafb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa1805902086bdb398bc5b4acf880d415953c1511fb14de02d6337b4e499905`

```dockerfile
```

-	Layers:
	-	`sha256:b0e0ea25d48bbf0f5fcaf482f86df89d905ab9cb8d2b13b983586979d208cb89`  
		Last Modified: Tue, 12 Aug 2025 18:06:31 GMT  
		Size: 2.6 MB (2631026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f84d90e82ba412364e400ad6bf429451f5f767cd72d9e38c15da0a594bc658`  
		Last Modified: Tue, 12 Aug 2025 18:06:32 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:21-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

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
