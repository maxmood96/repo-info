## `sapmachine:24-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:8cee6fff34404f0cc209e9e84684e4bb0d3c15572053b5073956d3e61fa3d194
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2e296b13c7d7e2b8781e025168019242ded2e0dde92d632c095857eeb51b7be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97238454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670bde39003b9451e9d511d4baa94b01ee63e67005fa7c521fd44b48aba63d4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15260fb2b638defc26640dbeacf26e2a88064b855989107d3e4b435be069b7c9`  
		Last Modified: Tue, 12 Aug 2025 18:06:13 GMT  
		Size: 67.7 MB (67701461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ec2c22fcbe6821872ed82b3f9b10556b0c6f6e5b3273b0c5362ce93d8bec080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fff20a0c42bc796453a4e7cf7356022f1bead190addc4c9d235fad23f274c61`

```dockerfile
```

-	Layers:
	-	`sha256:c46568d5bb617e9407f14fdcb06addb46cb88b717771cfa9757e67f022ecf1f0`  
		Last Modified: Tue, 12 Aug 2025 18:08:41 GMT  
		Size: 2.6 MB (2552577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a0070100eb1236b1f04bd4dd78f5ae8b8a3262f9351154a0c81df1c5166a15`  
		Last Modified: Tue, 12 Aug 2025 18:08:42 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:920eb7a78df1844e93cefee4d02c56b4120a7d32203d52c7049d8dddc6ef37a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94053309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae6e3d8059bc2b79b6d0e64aa9164b498260a1e456333b60c424a34bf0702c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e08eae9fe7343cf8cf94271ee2c9250832731824b2eaf2ed38633f5f89ca60`  
		Last Modified: Mon, 18 Aug 2025 15:22:38 GMT  
		Size: 66.7 MB (66694062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7aba24d9e115e7925cd2280d7100e71f77cf8919adeea8fe77d23841b3a17265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ff48616f691f56d9cdc26a120f12821476e1a08b602cbb0f484f52b6d92667`

```dockerfile
```

-	Layers:
	-	`sha256:d6570b0c5495bf48f54476358046e0706d49276ac1ee075ace76cfdba5d45c46`  
		Last Modified: Wed, 13 Aug 2025 00:09:53 GMT  
		Size: 2.6 MB (2552280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d5386cb0600f9dfb5ceb32c0a9db677042ac2da32e01a535172ba07c47806e`  
		Last Modified: Wed, 13 Aug 2025 00:09:54 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cb4a130b6ed2038f664cd6381b5cdc1908c2d6295194da203f89b31a4a79a5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102955072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1fe8a41df6f788e49529e17944a30db362d3afe736f20ada3690501d7adfdd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f304d2e0d48964fbf4ccc6c17af1c88790e17441684d1002673165a6099412a7`  
		Last Modified: Tue, 12 Aug 2025 22:33:39 GMT  
		Size: 68.5 MB (68511927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:69ad28b914f7cf7e8f3c6c545b3291c0a5d53d1b264768e26b6c5fcf5b620e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a88d0c3c45b25d37e83d97d3641625735cc1006179731a39d476dc52c42d74`

```dockerfile
```

-	Layers:
	-	`sha256:43aeb443d3000560e6f26c2e3a0526502e17476a58ef372aa8e71abba6446d21`  
		Last Modified: Wed, 13 Aug 2025 00:09:58 GMT  
		Size: 2.6 MB (2550074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267a66fede760f30eb2f2daba643fcebbf5ff89e6d7076263dc1e27bd971e2d3`  
		Last Modified: Wed, 13 Aug 2025 00:09:58 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
