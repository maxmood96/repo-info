## `sapmachine:24-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:82ca521143f658ce961b0a0e7ee7444880c330c7fe878b52eb8136aef0f77864
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:12745f0e299e80a80fbf3619a9b774d8e94f5d6c61ec6524fe8b56d8ced97b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260369906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e27d5a8bfd59fa1a74a7aa73920ec89363c326fae6ea4715bbbeccba5ca4906`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd1f995a95f41a28b9163b098dfcfe40a2879d05e46d85f5db73559de0287f`  
		Last Modified: Tue, 03 Jun 2025 04:18:03 GMT  
		Size: 230.8 MB (230836903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89953372c208846201ddb4cbd7f022af63d7477c2560965f15de571cecf8122b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2273853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3151964f2d53f9e8bdd1d3da41053dcf0f0fb826e770089a4446c3985da7cec0`

```dockerfile
```

-	Layers:
	-	`sha256:4d32d99f3f851a494f0bebb3ee39f2321d6d9102962b353522a0122f17cd6348`  
		Last Modified: Tue, 03 Jun 2025 04:17:59 GMT  
		Size: 2.3 MB (2264241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10aec8d5e7f7243a2dfb89b30e9b9bb26bc529b66173715510b7d1c6415240f1`  
		Last Modified: Tue, 03 Jun 2025 04:17:59 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:75a2496fab427b30084844d1ceb8b86ec816cf2a2dc6e41f181ff89d5d4edac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256063257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc3825c38b2450f0aa08c5ae7dbd58035eed84d6bd8d00cd61e3eebc14ef162`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2457fd2fdc9bde3d20fdcba8005bf99b5c2f4510149ed459b0485b06d19bf99b`  
		Last Modified: Mon, 05 May 2025 18:28:22 GMT  
		Size: 228.7 MB (228709046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:328c7867d80495da7109775a55ae7892d9b1ad4ca3522b4b395fa781751df0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b92101bb0e6a0709ad36d677302c78e52e4e21a7c7a6bca5653416f2acf7c1`

```dockerfile
```

-	Layers:
	-	`sha256:f672d5a2e148fc4e56b117546605d67d11ad3d6dd69a01f5010025aebf9c5848`  
		Last Modified: Mon, 05 May 2025 18:28:17 GMT  
		Size: 2.2 MB (2240854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9f790503dccaca79a3650dbfd2ed77ac53233882289659b497897174d9732b`  
		Last Modified: Mon, 05 May 2025 18:28:16 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:97ba664cd649727f7c29b80d1abf641de48f25262714c45242fb1096d5e58a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266306202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cf70720d245a7dd4cf9944fcd8ae9af2653dd1a4460c6655096968af4d7c9e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb88ea5fd46cfa5ff591f2bb1bd8ea69aee62c3e944fa8242b7e08c7b328c96`  
		Last Modified: Mon, 05 May 2025 18:18:55 GMT  
		Size: 231.9 MB (231862987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef4746669dfa807528fa2c49b3c8af87f2676f4ddb5cd3278bb272c05ebd1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2252188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878725c598713fb73f8e6f2ab0d91d0995eb8773831392fcb8bf4235af285e7b`

```dockerfile
```

-	Layers:
	-	`sha256:538bb0942a895f4d8279e3163fca261e7be99f8ac8e0f7ad06cb0931a9a94b1c`  
		Last Modified: Mon, 05 May 2025 18:18:49 GMT  
		Size: 2.2 MB (2242520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0811362de4dff029e80b4f38d3a265ea67dc28dfb660acbdd597c6f221bf2a2c`  
		Last Modified: Mon, 05 May 2025 18:18:48 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.in-toto+json
