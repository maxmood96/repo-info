## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3af9fad854c31376ce77f79942883149687f0256367cb39b5a0f52e99a881159
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9fb05363c625e476442d23f983373044d0df884b27b67ffc93ade8fda29c0207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228416763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344791aed26c7492cbf9990804ad2ab1c2d419bd6f67fe1bcfd3c6f389b87376`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c61eda9da03db371c36b0e47c9b798ce753212642382ca2fa480d3034d36c6`  
		Last Modified: Wed, 13 Aug 2025 21:22:16 GMT  
		Size: 198.9 MB (198879770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ab1db30b245713a866e870d367f07e0c783004daa053285de105ece7d4a1f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b372bc2a4b1d44edc44cfbc57c17770eaf9a77810e0a40580de86c16676d13`

```dockerfile
```

-	Layers:
	-	`sha256:bdb5ac0f65f250c6c4edfc78727b3863ec15ffaad18d613e37ecc6d85f2005cc`  
		Last Modified: Tue, 12 Aug 2025 21:05:38 GMT  
		Size: 2.4 MB (2375751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5264b9c6dcfe33e02552cd214db2edc5f29fee5f50a8f6288f4f289bdc513a1`  
		Last Modified: Tue, 12 Aug 2025 21:05:39 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a5aeda79c07fa6f138e03972a11845dde10d7d6c9612a9c49388479f1deff2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224910002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9036e69bb3bc4def641b0fd777a1d8786134c211a10255e999ec526acc919`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a0762abb70624a814b740c47bc78e9f9cb3454c2f63b7e0204bcfdcfadad9`  
		Last Modified: Mon, 18 Aug 2025 20:55:35 GMT  
		Size: 197.6 MB (197550755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3de96eed857b50ebbf0a451f1ada8c4d3a9dc6f87127d0e926f4d13fc5952386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573df8aecebf5da69f29f7d793f7aaf4dad310b3e81b670534b2b8aed1f9bbb2`

```dockerfile
```

-	Layers:
	-	`sha256:86413c8bd40189b657f411bc6f92bad9d705d301448d39a00fc3933b0efdc42e`  
		Last Modified: Wed, 13 Aug 2025 00:04:58 GMT  
		Size: 2.4 MB (2375423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9d26f93246eef2a035591188c749ee86059eabb4b7e5b4e215d3065f9629f0`  
		Last Modified: Wed, 13 Aug 2025 00:04:58 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:37f8d863010f61931492e533e90129aebf68339c137685f917137581bbccc035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233818343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51761c7061c19f00d9c2844b56570311f712d4a44b50948251222710e0450a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e268db40202083cc16a89e074b1be9d1b7d9218312be86a0b0a4c3f86538c41`  
		Last Modified: Wed, 13 Aug 2025 01:08:34 GMT  
		Size: 199.4 MB (199375198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9218f5e821ca08ee19c4cad9b4d9967a46a2bac8506bc1b7df3b42e520248639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184988c98c674735711b5d11454b3adcfa33fe98961c8ad025c17b3dc065f6c8`

```dockerfile
```

-	Layers:
	-	`sha256:89741400507075d7b4ad7273d3db56b8304f55a4a728e972b78486c2d12f1df5`  
		Last Modified: Wed, 13 Aug 2025 00:05:03 GMT  
		Size: 2.4 MB (2371830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21405fe52967bdd4532d428fd1e025544a47938f5821d1a605de6665d909e7f8`  
		Last Modified: Wed, 13 Aug 2025 00:05:04 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
