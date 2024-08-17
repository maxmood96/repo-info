## `sapmachine:lts-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:4802d2b5b2d24fec3511e5ff027b9310ccfe45934177cb6f87b737cffe659d92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c56651831027abf4bc32593372977cf829a67fe5adc34e8c60c5611b34c8d494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244106588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef45a95a34e03dd49c5a873b090472c656a4ae65f12141bda2bb6d59ee3dede`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccac6d8f0fef1cf32b90b83d83bdf25223e53e880d7c4294e6f7070d3cf579fc`  
		Last Modified: Fri, 19 Jul 2024 17:59:15 GMT  
		Size: 214.4 MB (214401435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:625fd079c78c700cbb0c87e044392bf30bc29cb2b1e2e43e106e0176d7aed519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2c47df56cc1fe94f3184b983ee895b289cf76b0361db4aacbcc2833485f381`

```dockerfile
```

-	Layers:
	-	`sha256:c7095a770cec64e06ad5d923336a91877a8bfce6806566c7a316acc0fe8740db`  
		Last Modified: Fri, 19 Jul 2024 17:59:12 GMT  
		Size: 2.2 MB (2210696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d406e3a9f5ad7d434ade2a691780e4fc705230616e53d1d5befc9be4b948a7`  
		Last Modified: Fri, 19 Jul 2024 17:59:12 GMT  
		Size: 10.4 KB (10398 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d83578f5d5f9fdc1fba2a1b4e1e2e097526a4f953ea8a4df889dbf732a3ae92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241345186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9e911598e9e3acbb36447bb53742bc4eabb2d28e2736b265576c9dc7fe4e12`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b5bfe892cea0688775af50881da8305be40d8ed58037d5696f5a741c77962`  
		Last Modified: Sat, 17 Aug 2024 04:17:23 GMT  
		Size: 212.5 MB (212501500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:551405bee301ea9758b1ce7af81b95c57d572f81039c5d5a663fa091cb74aeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8241cae52ab25f61461e67236c29ed8b966d0af15b7c0240dd5c15199a3e27a`

```dockerfile
```

-	Layers:
	-	`sha256:0630c761da97cab931c3b56487cc3f8d256936630836ebded9c4cf103c870b58`  
		Last Modified: Sat, 17 Aug 2024 04:17:19 GMT  
		Size: 2.2 MB (2211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca4fa66d9041f9fd159c4ffd8509ebeac9fad04c62cc0665de44f97f816ff0f`  
		Last Modified: Sat, 17 Aug 2024 04:17:18 GMT  
		Size: 10.8 KB (10759 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:624c8a1f7d72d54b16e6666aa098271b51562cdd4024ed0dc4ef42374d29071e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250184565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb0d089d7ea07290adceb89996ddb3ca78f88e2f43a39fddb5cc62d92c5a8cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df2444d98a77da1302aea9dd3e59a875ab3d9432cea65ea3e20661d084826d8`  
		Last Modified: Sat, 17 Aug 2024 02:48:28 GMT  
		Size: 215.7 MB (215676993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1adfc19f7f3c48914321df9c61a5be8cfe699d1104cc317e194be852cb56d933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf7cb49208b4517bf2bb953465b29644d9ff3d7c7112ea9c1a70f67562900fe`

```dockerfile
```

-	Layers:
	-	`sha256:419e6d13f20ba16ef34acebf8247327379279a1b8f10e15fe943ffea002930c3`  
		Last Modified: Sat, 17 Aug 2024 02:48:23 GMT  
		Size: 2.2 MB (2212651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f423a1385abfab12dc485441b4fc5b0c7755877d547d4185e41bc3401f1b138e`  
		Last Modified: Sat, 17 Aug 2024 02:48:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json
