## `sapmachine:21-jdk-headless`

```console
$ docker pull sapmachine@sha256:63fa42d8b22083d5d067bb74626282f3d9933fd25fd8cb6bde2282518ef563c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:593d88135bacef4499e90d2e86129ccf38b244819219daa29004c3cdfdcf03a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243843577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f5b625f98dc71089d605d85cfa1241bc461eb779ee891dee2f7a3f1aaa4121`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d618dee019b272ef7e10cfdbb03aba9eb95c0b7c01390c282005391191e3b`  
		Last Modified: Tue, 02 Sep 2025 04:48:30 GMT  
		Size: 214.1 MB (214120513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:391bbe78a4d4fccb49535770a0b513ca10511c0c8a82004ab92a3215442189e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca400f9971d7456e6dc7b8a15881b35287f0bd2f47749deac8948ccc9223df8`

```dockerfile
```

-	Layers:
	-	`sha256:7cebfbad414f708c41a48ce5d2c1562646ebb56a4f7a8ff0b2e1a89efd2c799c`  
		Last Modified: Tue, 02 Sep 2025 03:07:19 GMT  
		Size: 2.4 MB (2357371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067970b98ee41a5309bea445d515acd2697e6c00e8a58933b7ac92662088bfa3`  
		Last Modified: Tue, 02 Sep 2025 03:07:19 GMT  
		Size: 11.3 KB (11308 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:37b88ec7702a72e985290514d60e77b973502aa01c4008a051b26bff1eb53c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241208958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d831b21d08126ae8f5a05440280634c703f150a40484e04d5c8d1915a872fe5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02b8e22e94f8f4a379d80d3f11ab9ed31d9ef0e4a00e7a14fcee498b95bff14`  
		Last Modified: Tue, 02 Sep 2025 03:06:42 GMT  
		Size: 212.3 MB (212348718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34eea8f032b449e4b64a0d2df62acc7c429f3505fa162d84f473cb9f6f41615b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f9a3b6d6b56ec128f44ef103fbf282d2c2ae3c9731e27713e7aa9d9b5be63a`

```dockerfile
```

-	Layers:
	-	`sha256:1e8cce49dd15e39fb7b74e266fe192528602ef410dc5ebc86c6f265dbd8df19f`  
		Last Modified: Tue, 02 Sep 2025 06:06:32 GMT  
		Size: 2.4 MB (2357914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57279721fd413db54dde84fe011fa785411b575426c45d61a6db945c0dcbce4`  
		Last Modified: Tue, 02 Sep 2025 06:06:33 GMT  
		Size: 11.5 KB (11496 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2016ac42f1b8c343f0c3024d022de5af06b3307e320826d4cc6e9c3d2296f99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249209500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f90741fef4167bfaf4d4ebe5000dcbe91acb89afdd27636619113f438aca446`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae02ac5881e1b3cf16c7bee2fd17f35f39bb7cf535132429319624f3c06e29`  
		Last Modified: Tue, 02 Sep 2025 02:03:26 GMT  
		Size: 214.9 MB (214879967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6e465dd66ea6035bf4a0dd4c58e49b0dccc2ff94ddf021da04550df05d41cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58bc4f5d50e88de4be62bc9e8e07c5154f15db76e5981a9db813c08254460d`

```dockerfile
```

-	Layers:
	-	`sha256:3d144e4969b50d43fb2b4b0381d898ee0b238ddd988ae7cef05f44ebc6b336fd`  
		Last Modified: Tue, 02 Sep 2025 03:07:27 GMT  
		Size: 2.4 MB (2353443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bf5e743734c256901b34f1cb08073b23abc17057e6a59a49c458842b24e7f4`  
		Last Modified: Tue, 02 Sep 2025 03:07:28 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json
